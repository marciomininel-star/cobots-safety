# 07 — Integração, layout, ferramentas e interfaces

## Ideia central

Projete fluxo de peças, acesso humano e interfaces de segurança ao mesmo tempo. A ferramenta e o gabarito podem mudar radicalmente os perigos de um braço com capacidades colaborativas.

## Fontes e precisão

S08, 4.2, 5.3–5.10, pp. PDF 14–16 e 21–46; S03, 4.2–4.3 e 5.3, pp. PDF 9–12; S16, pp. PDF 4–12; S13, seção de ferramentas/acessórios, pp. PDF 28–35; S18, p. PDF 2. A lista de decisões é síntese operacional das fontes.

## Método de integração

### 1. Layout a partir das intervenções

Desenhe em escala a base, envelopes do braço/EOAT/peça, dispositivos e zonas de circulação. Inclua alcance por cima/baixo de proteções, passagem de materiais, acesso a gabinete, limpeza e retirada de componentes. Use planta e elevação: uma planta sozinha esconde colisões com cabeça e acesso sobre obstáculos.

Projete intervenções fora da zona perigosa quando possível. Se a tarefa exige movimento energizado durante acesso, defina modo e medidas apropriados, em vez de tornar a proteção fácil de contornar. Evite criar aprisionamento entre braço/peça e colunas, paredes, bancadas ou máquinas.

### 2. Ferramenta e peça como componentes de segurança da aplicação

Avalie massa, centro de gravidade, orientação, alcance, arestas, temperatura, fechamento, pressão, retenção e falha de alimentação. Uma peça lisa pode tornar-se perigosa por sua borda; uma garra pode perder a peça ao faltar ar; a ferramenta pode exceder a velocidade ou envelope considerado pelo sistema de monitoramento.

| Pergunta | Evidência procurada |
|---|---|
| A carga pode cair ao perder energia? | Estratégia de retenção, comportamento declarado e ensaios pertinentes |
| Há fechamento com mão acessível? | Eliminação de pinçamento ou proteção adequada |
| A troca pode soltar ferramenta? | Travamento, confirmação e sequência segura |
| O robô conhece massa/centro de gravidade reais? | Dados e configuração coerentes com o conjunto montado |
| A peça cria perigo mesmo com braço parado? | Bordas, estabilidade, calor, resíduos, energia armazenada |
| O limite de espaço cobre a peça? | Desenho, offsets e função adequada à condição real |

### 3. Interface máquina–robô

Separe sinais de produção, como pronto/ciclo concluído, dos sinais que cumprem funções de segurança. Para cada máquina, especifique: estados permitidos, quem comanda, quem confirma, comportamento em perda de comunicação, falha e retorno de energia. Um aperto de mão comum de I/O pode coordenar o ciclo sem proteger o acesso humano.

**Por que funciona:** torna explícito o comportamento da célula quando uma máquina para e outra permanece ativa. **Falha típica:** presumir que o comando operacional “porta aberta” basta para impedir o movimento perigoso na máquina servida.

## Complexidade da aplicação

S16 propõe examinar consistência das peças, apresentação, máquinas, ferramentas, montagem, ambiente, programação e necessidades futuras. Use essas dimensões para antecipar esforço, não para concluir risco baixo. Menos sensores de processo podem simplificar programação; não dispense detecção ou funções de proteção necessárias.

| Dimensão | Situação mais previsível | Situação que exige desenvolvimento |
|---|---|---|
| Peças | Posição/orientação repetíveis | Variação, emaranhamento, deformação |
| Alimentação | Ninhos/gabaritos definidos | Seleção aleatória e realimentação complexa |
| EOAT | Ferramenta adequada e estável | Projeto especial, troca frequente, várias massas |
| Interface | Estados bem definidos | Máquinas legadas, dados incompletos |
| Base | Referência e fixação estáveis | Movimentação entre postos e reancoragem |
| Ambiente | Condições dentro de especificação | Respingo, corrosão, temperatura, higiene, poeira |

Uma capa pode proteger o equipamento de um ambiente, mas também mudar calor, movimento e contato. Verifique sua compatibilidade e impacto. Não transforme a frase “ambiente adequado a humanos” em especificação de IP, atmosfera explosiva ou resistência química.

## Exemplo trabalhado — atendimento de máquina

**Cenário didático:** cobot carrega peças em uma máquina de usinagem. A solução inicial abre a porta por comando comum e move o braço para dentro.

**Questões:** a máquina realmente atingiu estado seguro? O comando de ciclo pode vir de outra estação? O robô pode esmagar uma mão no dispositivo? A peça pode cair? Cavacos quentes ou bordas permanecem perigosos?

**Desenvolvimento:** documentar a sequência; especificar interface de segurança com a máquina; projetar a garra e dispositivo; definir espaço e estados permitidos; tratar recuperação de falhas e limpeza. A retirada de cavacos entra como tarefa própria, com controle de energias apropriado.

**Critérios de ensaio:** falha da confirmação de posição/porta, perda de comunicação, falta de energia/ar, permanência de pessoa, intervenção durante falha e partida externa. A função precisa proteger a pessoa mesmo que a receita de produção seja interrompida fora do ponto esperado.

**Entrega revisável:** desenho com acessos, lista de interfaces funcionais e de segurança, dados de EOAT/carga, sequência de estados e matriz de testes. Não é necessário finalizar software de produção para descobrir essas lacunas.

## Ampliação do curso — inserção, máquinas atendidas e automação parcial

S29–S31 propõem ajustar trajetória e velocidade ao se aproximar de superfícies rígidas. Em vez de copiar um ponto a 50/100 mm, determine onde o aprisionamento se torna possível, a peça/corpo envolvido e a distância necessária para a transição. Verifique outras partes do braço e acessos; redução do TCP não cobre automaticamente todos os perigos.

S35 descreve troca de racks por fora, entrega de bandejas entre robôs, testadores de placas com tampas e robôs sobre transportadores. Avalie cada transferência, tampa, fixador, eixo externo e pessoa no escopo de risco. Prevenir colisão robô–robô no sequenciamento comum não comprova a proteção humana.

S36 usa atendimento de máquina como candidato de implantação. Remover cercamento para caber num corredor estreito pode criar aprisionamento ou bloquear escape. Avalie a máquina servida e o processo: químicos, ferramenta pontiaguda, calor e meio abrasivo não se tornam seguros por estarem num braço colaborativo.

## Antipadrões

- Posicionar o braço e deixar o fluxo de materiais para depois.
- Usar o fim de curso comum como prova de estado seguro.
- Supor que a detecção de colisão resolve a ponta afiada de uma peça.
- Mover uma célula sobre rodas e reutilizar parâmetros sem nova referência e avaliação.
- Proteger o braço e esquecer a máquina atendida.

## Decisões a reter

1. Inclua EOAT/peça no envelope e nos contatos.
2. Projete manutenção e recuperação no layout.
3. Documente comportamento de interfaces em falha.
4. Reavalie mudanças de ferramenta, carga e localização.

## Conexões

Ch01 para espaços; ch04 para contatos; ch06 para interfaces; ch08 para aceitação; ch10 para especificação de compra.
