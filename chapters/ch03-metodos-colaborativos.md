# 03 — Métodos de operação colaborativa e transições

## Ideia central

Escolha o método de proteção para cada fase da tarefa. As fontes históricas descrevem quatro métodos que podem se combinar; nenhum deles é uma etiqueta que elimina a apreciação de riscos.

## Fontes e precisão

S03, 5.4–5.5, pp. PDF 12–25; S08, 5.11, pp. PDF 47–50; S01, pp. PDF 17–25; S02, pp. PDF 30–36; S14/I07. Terminologia e cláusulas são das edições do acervo, não uma afirmação da redação das edições internacionais de 2025.

## Matriz de seleção

| Método | Princípio | Boa pergunta de seleção | Principal evidência |
|---|---|---|---|
| Safety-rated monitored stop — SRMS/SMS | Movimento perigoso cessado e condição monitorada antes da interação | A tarefa humana pode ocorrer com o sistema parado? | Parada, presença, cobertura e lógica de retomada |
| Hand guiding — HG | Pessoa envia comandos por dispositivo de condução | O trabalho exige controle direto pelo operador? | Dispositivo, limites, parada ao soltar e transições |
| Speed and separation monitoring — SSM | Movimento simultâneo mantendo separação protetiva | Existe espaço e detecção confiável para impedir contato? | Cálculo, parada e cobertura de todas as pessoas |
| Power and force limiting — PFL | Contatos previsíveis permanecem dentro de limites definidos | Geometria e contatos podem ser demonstrados como adequados? | Classificação e ensaio de força/pressão e medidas de projeto |

Não selecione PFL para contornar uma distância SSM inviável sem avaliar contatos. Não use SRMS quando o robô permanece em movimento dentro da região de interação da pessoa, a menos que outro método válido proteja esse movimento.

## Como aplicar cada método

### Parada monitorada de segurança

Estabeleça o espaço e a tarefa, detecte o acesso a tempo e obtenha a condição de parada antes da exposição. Mantenha a condição enquanto a pessoa estiver presente. O estado monitorado pode conservar energia nos acionamentos; isso não equivale a isolamento para manutenção. Uma pausa comum de programa não oferece a mesma evidência.

A S03 prevê retomada sem intervenção adicional em condições específicas após saída da pessoa. Separe esse caso de uma falha de segurança: em 5.4.1 a fonte exige tratamento da falha e ação deliberada de reinício com operador fora do espaço. Não aplique a permissão de retomada automática a qualquer parada.

### Condução manual

O método de produção HG é diferente de simplesmente destravar o braço para ensinar pontos. S03 descreve parada monitorada antes do ingresso, tomada de controle pelo dispositivo e retorno à parada ao liberá-lo. A velocidade monitorada e eventuais limites de posição dependem da apreciação. Avalie posição do operador, visibilidade e movimento intuitivo dos eixos.

O dispositivo inclui emergência e habilitação nas condições descritas pela fonte; as exceções de habilitação são específicas e precisam de medidas alternativas ativas. Não invente uma dispensa geral porque o braço tem modo “freedrive”.

### Monitoramento de velocidade e separação

Determine distância protetiva, tempo de reação e frenagem. Detecte pessoas e todos os elementos perigosos relevantes. Ajuste velocidade ou pare para manter separação; trate perda de detecção, ocultação, zonas cegas e mais pessoas que a capacidade suportada. Detalhes de cálculo no ch05.

### Limitação de potência e força

Descreva os contatos, elimine geometrias perigosas e estabeleça critérios por região corporal, contato e frequência. Combine medidas passivas e funções ativas; valide a configuração. O limite selecionado no controlador não é automaticamente a força real de contato em qualquer ponto do sistema. Detalhes no ch04.

## Transições são uma parte do projeto

Para cada troca de modo, registre: estado de origem, condição de entrada, proteção que estará ativa, comando deliberado quando requerido, detecção de pessoas, movimentos permitidos e resposta a falha. Nunca crie um intervalo em que o método anterior já foi desativado e o seguinte ainda não protege.

| Transição | Falha a investigar | Controle/evidência esperada |
|---|---|---|
| Automático → acesso humano | Acesso antes de terminar a parada | Detecção e distância adequadas |
| SRMS → HG | Movimento inesperado ao tomar controle | Habilitação, lógica e mapeamento de comando |
| HG → automático | Outra pessoa permanece no espaço | Detecção, saída e sequência definida |
| SSM → PFL | Velocidade ainda incompatível com contato | Limites ativos antes de permitir aproximação |
| Falha → retomada | Reset inicia movimento de surpresa | Separação entre rearme e partida conforme aplicação/edição |

## Exemplo trabalhado — inspeção e transferência

**Cenário didático:** um robô apresenta uma peça para inspeção e depois a leva a outro posto.

1. Durante a transferência, o sistema opera com a proteção definida para a área.
2. Ao chegar à região de inspeção, mantém a peça em parada monitorada antes de liberar acesso.
3. A pessoa inspeciona sem movimento do robô. A garra e a peça ainda precisam estar seguras: parada do braço não resolve perda da carga.
4. A saída e a liberação da região são confirmadas pela solução de segurança projetada.
5. A retomada segue a sequência especificada, incluindo o tratamento de presença de uma segunda pessoa.

**Variação:** se a pessoa precisa girar ou reposicionar a peça, analisar HG com dispositivo e limites adequados, ou outra solução validada. Não basta inserir uma instrução comum de movimento enquanto a pessoa segura a peça.

**Resultado:** tabela de estados da interação e requisitos de cada fase. O exemplo não define a categoria de parada de uma instalação específica nem aprova retomada automática.

## Ampliação do curso — comportamento observado versus método

S29/S30 descrevem zonas de acesso e redução de velocidade. O afastamento de um metro narrado num exemplo não é uma distância SSM universal. A dúvida apresentada pelo curso sobre chamar SSM de colaboração não altera o fato de que S03 o inclui como método: contato não é necessário em todos os métodos.

O curso também mostra condução usada para ensinar posições. Preserve a distinção entre ensino, condução em produção e funções de proteção, conforme as condições do ch03. Um vídeo narrado em que o operador empurra o braço não demonstra todos os requisitos de HG nem autoriza a retomada após qualquer contato.

## Antipadrões

- **Uma velocidade universal para colaboração:** contato, massa, geometria e método são determinantes.
- **Freedrive = HG certificado:** confunde funcionalidade de programação com método de proteção.
- **Misturar emergência e parada de produção:** cada função tem finalidade e lógica próprias.
- **“Sem contato” com pinçamento possível:** a intenção do programador não limita o alcance humano.

## Decisões a reter

1. Escolha e valide métodos por fase.
2. Trate a presença, os movimentos e as transições como requisitos.
3. Distinga retomada normal, rearme de proteção e recuperação de falha.
4. Mantenha perigos da ferramenta e do processo no escopo de qualquer método.

## Conexões

Ch04 para PFL; ch05 para SSM; ch06 para controles; ch08 para ensaios; ch12 para recuperação e operação.
