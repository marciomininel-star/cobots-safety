# 02 — Apreciação e redução de riscos por tarefa

## Ideia central

Transforme cada combinação de tarefa, pessoa e perigo em uma decisão de redução de risco verificável. A apreciação é iterativa: uma medida só encerra uma linha quando sua eficácia e os perigos que ela introduz foram avaliados.

## Fontes e precisão

S04, seções 4–7, pp. PDF 20–37 e 76–77: **projeto ABNT de agosto de 2013, sem valor normativo**, usado para estudo metodológico. S08, 4.3–4.5, pp. PDF 16–19; S03, 4.3, pp. PDF 10–11; S01, pp. PDF 11–15. Para requisitos de um projeto real, consulte a norma publicada aplicável.

## Estruturas introduzidas

### Ciclo de apreciação

1. **Determine limites:** uso, modos, pessoas, espaço, tempo, ambiente, materiais, vida útil e intervenções.
2. **Identifique perigos:** considere operação normal, falhas e uso indevido previsível. Uma lista de acidentes anteriores não esgota os perigos.
3. **Estime risco:** avalie gravidade e probabilidade de dano, considerando exposição, evento perigoso e possibilidade de evitar/limitar o dano.
4. **Avalie:** decida se a redução é adequada e quais riscos precisam de medidas.
5. **Reduza:** aplique a hierarquia de três passos.
6. **Reavalie:** verifique redução, novos perigos e tarefas que incentivam burla; repita até a redução adequada.
7. **Documente:** mantenha evidência, hipóteses, responsáveis, pendências e risco residual.

**Por que funciona:** o ciclo obriga a ligar a medida ao dano que ela deve impedir. **Falha típica:** preencher uma pontuação depois de já escolher uma proteção, apenas para justificar a compra.

### Redução em três passos

| Prioridade | Tipo de medida | Exemplo específico de aplicação |
|---|---|---|
| 1 | Projeto inerentemente seguro | Eliminar pinçamento pelo layout; reduzir massa; arredondar ferramenta |
| 2 | Proteções e medidas complementares | Intertravamento, detecção de presença, limites seguros, meios de escape |
| 3 | Informação para uso | Procedimento, sinalização, capacitação e instruções sobre riscos residuais |

A sequência é de projeto, não uma ordem para desligar medidas existentes. Uma solução pode precisar de várias camadas. EPI não torna aceitável uma geometria de corte ou aprisionamento que pode ser eliminada.

## Identificação por tarefas

Divida o ciclo de vida em transporte/montagem, comissionamento, preparação, ensino, produção, abastecimento, inspeção, troca de ferramenta, limpeza, desobstrução, diagnóstico, manutenção e desativação. Para cada tarefa, pergunte:

- Quem entra e por quê? Pode haver uma segunda pessoa?
- Quais movimentos e energias permanecem ativos?
- Que falha ou comportamento previsível muda a exposição?
- Há risco em uma máquina adjacente ou na perda da peça?
- Qual parte do corpo pode ser atingida, aprisionada ou exposta ao processo?
- Como a pessoa sai ou é retirada de uma situação perigosa?

Permanência curta não implica risco baixo quando o dano é grave ou a fuga é inviável. Ausência de histórico de acidente não é evidência de ausência de perigo.

## Conceitos que mudam decisões

- **Perigo:** fonte potencial de dano, como movimento de esmagamento.
- **Situação perigosa:** circunstância em que uma pessoa fica exposta ao perigo.
- **Evento perigoso:** ocorrência que pode levar ao dano, como fechamento inesperado.
- **Risco:** combinação da gravidade e da probabilidade de dano.
- **Risco residual:** risco que permanece após medidas, a comunicar e gerenciar.
- **Apreciação:** análise mais avaliação; não é sinônimo apenas de identificar perigos.
- **Redução adequada:** conclusão sustentada por medidas e evidências, não por um número isolado.

## Exemplo trabalhado — retirada de peça presa

**Exemplo didático construído a partir do método:** o operador retira uma peça presa entre garra e gabarito durante uma falha de alimentação.

| Campo | Registro inicial |
|---|---|
| Tarefa/pessoa | Recuperação de falha; operador e possível apoio de manutenção |
| Perigo | Movimento do braço, fechamento de garra e energia armazenada |
| Situação | Mãos dentro do ponto de aprisionamento, alcance limitado para saída |
| Evento | Reinício por sinal externo ou liberação da peça com movimento inesperado |
| Dano plausível | Esmagamento dos dedos/mão; queda da peça |
| Incerteza | Não existe confirmação da lógica de rearme e de retenção da garra |

**Passo 1:** modificar alimentação e gabarito para diminuir enroscos e permitir retirada fora da zona perigosa. **Passo 2:** estabelecer estado seguro apropriado à intervenção; controlar movimento, fechamento e energia armazenada; impedir reinício inesperado e prever acesso/escape. **Passo 3:** procedimento e capacitação específicos, com ferramentas de retirada adequadas quando aplicáveis.

**Verificação:** analisar circuito e sequência, testar recuperação controlada, confirmar efeito de perda/retorno de energia e de comandos de outras máquinas. Não testar prensando uma mão. **Conclusão possível:** “pendente” até demonstrar as funções e acesso, mesmo se a produção automática já passou nos testes.

O registro final distingue risco inicial, medidas implementadas, evidência e risco residual. Pontuações podem ser adicionadas conforme o método escolhido, mas esta skill não inventa uma matriz universal nem apresenta S×F×P como exigência da ISO 12100.

## Ampliação do curso — equipe, 3E e matriz de risco

S25 propõe uma equipe com integrador, instalação, engenharia, operadores e outros interessados. Use o conhecimento das intervenções reais para revisar tarefas e falhas, inclusive após mudança de aplicação. Registre divergências; consenso não comprova segurança.

S23/S24/S28 usam a pirâmide **3E: Elimination, Engineering controls, Enterprise controls**. Ela ajuda a comparar medidas físicas e organizacionais; veja o ch14. É uma formulação didática, não a redação literal da hierarquia normativa de S04/S08.

S26 descreve escalas S1–S3, E1/E2 e A1–A3 e menciona E0 para verificação posterior. A matriz/tabela original não acompanha a transcrição. Não reconstrua os cruzamentos por adivinhação, nem misture essas letras com métodos de outras normas. Há erro textual “E3” e extrapolações indevidas entre classe de risco e PL/categoria. Se usar esse método, obtenha a referência original e aplique as definições completas. A aceitação empresarial de risco não substitui obrigações aplicáveis.

## Antipadrões

- **Lista genérica de perigos sem tarefas:** não mostra quando a proteção deve atuar.
- **Mesmo critério antes/depois sem justificar redução:** produz aparência de melhoria sem evidência.
- **Reduzir gravidade porque há um sensor:** o sensor geralmente altera probabilidade/exposição, não a gravidade intrínseca do dano.
- **Copiar a matriz de um slide para qualquer célula:** mistura métodos e pressupostos diferentes.
- **“Operador não deve entrar” diante de acesso necessário:** induz burla e ignora uso real.

## Decisões a reter

1. Registre tarefas previsíveis fora da produção normal.
2. Explique como cada medida altera o cenário de dano.
3. Reavalie riscos introduzidos por proteções e mudanças.
4. Use estados “pendente”, “implementado” e “validado” com significados distintos.

## Conexões

Ch01 define limites; ch04 aprofunda contatos; ch06 especifica funções; ch08 define evidências. Modelo de registro: [modelos práticos](../references/modelos-praticos.md).
