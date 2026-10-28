# 05 — SSM, separação protetiva e parada

## Ideia central

SSM permite movimento simultâneo mantendo distância protetiva entre pessoas e partes perigosas do sistema. A distância precisa acomodar aproximação humana, reação, frenagem, intrusão e incertezas.

## Fontes e precisão

S03, 5.5.4, pp. PDF 16–21, especialmente 17–20; S01, pp. PDF 22–24; S08, 5.10 e 5.11, pp. PDF 38–50. Fórmulas e o valor humano de referência abaixo pertencem à edição de 2016. Confirme a edição e as normas de posicionamento de dispositivos aplicáveis ao projeto.

## Estrutura de cálculo

Na S03, a equação (1) é:

`Sp(t0) = Sh + Sr + Ss + C + Zd + Zr`

| Parcela | Significado | Origem necessária |
|---|---|---|
| Sp(t0) | Separação protetiva no instante considerado | Soma coerente com a implementação |
| Sh | Aproximação humana até o robô parar | Velocidade/direção e tempos considerados |
| Sr | Movimento do robô durante a reação | Velocidade, aceleração e latência da cadeia |
| Ss | Movimento durante a frenagem | Dados/ensaio da configuração e condição relevante |
| C | Intrusão antes da detecção | Geometria, resolução e posicionamento do dispositivo |
| Zd | Incerteza na posição humana detectada | Especificação e condições do sensor/sistema |
| Zr | Incerteza da posição do robô | Sistema de medição e ponto perigoso considerado |

Para hipóteses constantes coerentes com a fonte:

`Sh = vh × (Tr + Ts)`

`Sr = vr × Tr`

`Ss = integral da velocidade de frenagem durante Ts`

**Tr** inclui detecção, processamento, comunicação e ativação do comando de parada, excluindo a frenagem. **Ts** vai da ativação da parada até a imobilização. Não confunda ambos com o tempo total. As unidades de distância devem ser as mesmas em todas as parcelas.

S03 usa 1,6 m/s para a aproximação humana quando não monitorada, com ressalvas e referências na própria cláusula. Isso não é uma velocidade universal suficiente para todas as tarefas, direções, partes do corpo e edições. Justifique o valor conforme a aplicação e a norma pertinente.

## Método de projeto

1. Defina quais pessoas, acessos e partes perigosas devem ser monitorados.
2. Mapeie regiões não observadas, ocultações, reflexões relevantes, interferências e capacidade de detectar mais de uma pessoa.
3. Determine o encadeamento sensor–lógica–comunicação–robô e as latências máximas justificadas.
4. Obtenha dados de parada para velocidades, cargas, posturas, direções e condições pertinentes.
5. Calcule a separação ou a velocidade permitida. Em limite constante, use as condições desfavoráveis justificadas; em limite variável, valide também a lógica dinâmica.
6. Posicione campos de detecção considerando todas as direções de aproximação, intrusão e alcance de partes do corpo.
7. Verifique desaceleração/limitação e parada ao perder a condição de separação; controle também ferramentas perigosas associadas.
8. Teste cobertura, falhas e transições, e registre a configuração de campo e os resultados.

**Por que funciona:** a pessoa continua se aproximando enquanto o sistema reage e freia. **Falha típica:** posicionar o scanner usando apenas a distância de parada do braço, omitindo o movimento humano durante o mesmo período.

## O ponto perigoso não é apenas o TCP

O cotovelo pode se aproximar enquanto o TCP se afasta. A peça pode projetar-se além do flange. Uma segunda pessoa pode estar mais próxima que a pessoa acompanhada pelo algoritmo. A S03 exige aplicar a proteção às pessoas presentes e às partes relevantes do sistema.

Se houver limite da quantidade de pessoas detectáveis, essa restrição precisa ser documentada e a ultrapassagem deve levar à resposta protetiva prevista. Não dependa de uma regra administrativa para resolver uma incapacidade de detecção sem analisar o acesso real.

## Exemplo trabalhado — soma das parcelas

**Exemplo criado para ensino; não é dimensionamento de instalação.** Hipóteses constantes: `vh=1,6 m/s`, `Tr=0,12 s`, `Ts=0,28 s`, `vr=0,50 m/s`, `Ss=0,09 m`, `C=0,12 m`, `Zd=0,03 m`, `Zr=0,02 m`.

| Etapa | Cálculo | Resultado |
|---|---|---|
| Aproximação humana | 1,6 × (0,12 + 0,28) | 0,64 m |
| Robô durante reação | 0,50 × 0,12 | 0,06 m |
| Frenagem | Dado hipotético fornecido | 0,09 m |
| Intrusão + incertezas | 0,12 + 0,03 + 0,02 | 0,17 m |
| Soma Sp | 0,64 + 0,06 + 0,09 + 0,17 | **0,96 m** |

Os 0,96 m são resultado das hipóteses; não autorizam uma distância de scanner de 960 mm. É preciso definir de onde a distância é medida, a geometria do campo e o ponto perigoso, verificar todas as aproximações e demonstrar cada parcela.

**Sensibilidade:** se Tr subir para 0,20 s, mantendo apenas para a demonstração as demais hipóteses, `Sh=0,768 m`, `Sr=0,10 m` e `Sp=1,128 m`. Em um projeto real, a frenagem e outras parcelas também podem mudar. O efeito da latência mostra por que usar tempos nominais otimistas é inadequado.

## Comparação de estratégias

| Estratégia | Vantagem | Custo/limitação |
|---|---|---|
| Separação e velocidade constantes | Mais simples de descrever e verificar | Pode exigir maior espaço ou menor produtividade |
| Limites variáveis | Pode aproveitar a distância disponível | Requer medição e lógica de segurança mais complexas |
| Combinação SSM/PFL | Pode permitir diferentes fases de aproximação | Cada fase e transição precisa de justificativa e validação |

## Ampliação do curso — evitar um afastamento fixo por analogia

S30 descreve uma estação que para a cerca de um metro. Use-a apenas para entender a sequência aproximação → redução → parada. O valor depende do arranjo demonstrado e não substitui as parcelas de Sp. A aula não fornece sensor, dados de parada, incertezas e geometria suficientes para dimensionar outra célula.

## Antipadrões

- Supor que a saída de uma câmera comum tenha desempenho de segurança.
- Usar velocidade do TCP como velocidade máxima de toda a cadeia cinemática.
- Usar distância mínima de um único ensaio como pior caso.
- Ignorar atrasos de rede ou usar médias quando o requisito exige limite superior.
- Aplicar a fórmula sem definir intrusão, incertezas e referência geométrica.

## Decisões a reter

1. Modele reação e frenagem separadamente.
2. Confirme todas as pessoas e partes perigosas, em todas as aproximações.
3. Obtenha dados de parada na configuração pertinente.
4. Recalcule e revalide após alterações relevantes.

## Conexões

Ch03 para escolha de método; ch06 para cadeia de segurança; ch07 para campos/layout; ch08 para testes. A memória de cálculo é um dos [modelos práticos](../references/modelos-praticos.md).
