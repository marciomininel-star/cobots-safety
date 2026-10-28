# 13 — Dinâmica de colisão, inércia refletida e controle

## Ideia central

A massa da peça é apenas uma parcela da dinâmica do contato. A energia do sistema, o torque que o controle continua aplicando e a distância/complacência disponível para desacelerar influenciam o resultado.

## Fontes e precisão

S32/S33, transcrições de *Force-Limited Robots*, partes 1 e 2; S34, parte 3; S37/S38, *Testing*. Brian Carlisle/Precise Automation apresenta mecanismos e práticas do fabricante; há outros participantes no curso. As tabelas, gráficos e vídeos mencionados não foram fornecidos com estes TXT. Para localização, use ID/arquivo e as expressões de busca indicadas no catálogo. As equações abaixo são reconstruções didáticas do mecanismo descrito, com hipóteses explícitas; não são fórmulas universais de validação PFL.

## Estruturas de julgamento

### Três contribuições a investigar

| Contribuição destacada no curso | Pergunta útil | Evidência necessária |
|---|---|---|
| Energia cinética | Quais massas/inércias e velocidades participam do contato? | Modelo, postura, ponto e direção de impacto |
| Torque dos motores durante o contato | O servo continua empurrando antes/durante a parada? | Comportamento declarado, limites e resposta do controle |
| Distância de desaceleração/complacência | Há recuo, deformação ou uma superfície rígida atrás do corpo? | Geometria, contato e aparato representativo |

S32 usa analogias com amortecimento para explicar por que aumentar o percurso de desaceleração pode reduzir força. Isso não permite aprovar espuma sem avaliar compressão, envelhecimento, distribuição de pressão e condições da aplicação. Também não permite transformar contato quase estático em transiente apenas pelo revestimento.

### Energia cresce com o quadrado da velocidade

Para uma massa equivalente e uma direção simplificadas, `E = 1/2 × m_eq × v²`. Dobrar v, mantendo m_eq, quadruplica E. Essa relação explica tendências; não determina sozinha o pico de força nem a pressão local. A força também depende da dinâmica de contato, do controle e da deformação.

Em uma aproximação didática de desaceleração, o trabalho `F_média × d` pode ser comparado à energia dissipada, sob hipóteses restritas. **Força média não é força de pico**, e torque ativo ou aprisionamento podem acrescentar trabalho. Não calcule uma “velocidade segura” apenas invertendo essa expressão.

### Inércia refletida

O curso explica que motor e partes rápidas da transmissão podem contribuir para a inércia vista no lado de saída. Para um único eixo idealizado, com relação de redução `N = velocidade_motor / velocidade_saída`:

`J_ref = J_motor × N²`

Para converter apenas essa parcela a uma massa equivalente num raio r:

`m_eq,ref = J_ref / r²`

Use unidades coerentes: J em kg·m², r em m e m em kg. A expressão simplificada não soma automaticamente os efeitos de todos os eixos de um manipulador; a massa efetiva real depende de postura, direção, acoplamentos e ponto de contato. Não iguale essa massa equivalente à carga útil nominal nem a um parâmetro denominado “payload” no controlador.

**Por que funciona:** mostra que transmissões de robôs com a mesma carga nominal podem participar diferentemente do impacto. **Modo de falha:** comparar apenas a massa da peça ou usar uma tabela de outro robô para definir limites.

O curso compara reduções por correia e harmonic drive, mas sua transcrição tem inconsistências entre razões, massas e multiplicadores. Preserve a tendência física sob hipóteses declaradas; não use os números da comparação como caracterização de produtos ou regra de compra.

## Exemplo trabalhado — efeito de N²

**Exemplo próprio, não dados de um fabricante:** considere `J_motor = 0,00002 kg·m²` e `r = 0,40 m`.

| Hipótese | N | J_ref | m_eq,ref |
|---|---|---|---|
| Transmissão A | 5 | 0,0005 kg·m² | 0,003125 kg |
| Transmissão B | 100 | 0,20 kg·m² | 1,25 kg |

O aumento de N por um fator 20 aumenta a parcela refletida por 400, neste modelo idealizado. Ainda faltam ferramenta, peça, elos, demais eixos, direção e resposta do controle. Os resultados não são massas efetivas completas de um robô real.

**Decisão:** ao selecionar equipamento, peça ao fabricante dados pertinentes de colisão e dinâmica da configuração, e confirme a aplicação. Não conclua que a transmissão A torna qualquer contato aceitável nem que toda transmissão B impede aplicação colaborativa.

## Feedforward e feedback no argumento do curso

S33 descreve um controle que calcula torque esperado por um modelo dinâmico (**feedforward**) e acrescenta uma correção de erro (**feedback**). Um contato pode elevar a parcela de correção; o fabricante pode limitar essa parcela e reagir ao contato.

O valor percentual citado na aula é um exemplo de implementação, não uma configuração recomendada para outros controladores. O modelo tem erro de atrito, carga, acoplamentos e dinâmica; a função precisa ter comportamento e integridade adequados à finalidade de proteção. Não implemente um limitador de torque em software comum e o declare função de segurança.

O curso afirma que o controle pode ter papel importante em colisões de menor velocidade, enquanto a inércia pode dominar impactos mais rápidos. Use isso como pista para investigar, não como uma fronteira numérica universal. Solicite resposta temporal e medições, não apenas o valor de torque configurado.

## Projeto de aproximação ao dispositivo

Distinga transferência em espaço aberto de inserção perto de uma superfície rígida. Defina um ponto de aproximação e uma fase final com limites compatíveis com os contatos previsíveis. A solução deve considerar dedos, braço, peça e outras pessoas em toda a trajetória.

Pontos de 50/100 mm, velocidades de 0,1/1/1,5 m/s e percentuais de receita narrados nas aulas são específicos dos exemplos. Uma redução comum no programa não se torna um limite monitorado de segurança. Determine a função necessária e valide a fase e sua transição; veja ch06–ch08.

## Antipadrões

- “Peça leve implica impacto leve”: ignora elos, transmissão e torque ativo.
- “Baixa relação de redução comprova segurança”: ignora o sistema e o processo.
- “Energia calculada substitui ensaio”: ignora o modelo de contato e sua representatividade.
- Reproduzir demonstrações com mãos/criança para testar o braço.
- Aplicar 150 N, 75 N/mm ou um percentual do servo como valores universais.

## Decisões a reter

1. Investigue energia, torque ativo e desaceleração conjuntamente.
2. Separe carga nominal, massas físicas e massa efetiva na direção de contato.
3. Use equações simplificadas para entender tendências e conferir unidades.
4. Exija dados da configuração e validação para definir parâmetros reais.

## Conexões

Ch04 para critérios PFL; ch06 para integridade das funções; ch07 para geometria; ch08 para aparato e evidência. Veja as [ressalvas das transcrições](../references/curso-transcricoes.md).
