# Padrões de trabalho

Procedimentos sintetizados das fontes, com roteamento para os módulos que contêm justificativas e referências. Não substituem procedimentos validados da instalação.

## Definir a aplicação antes do equipamento

**Quando usar:** pedido genérico sobre “segurança de cobot” ou dispensa de grade.

**Como:** listar tarefa, pessoas, modos, braço, EOAT, peça, máquinas, energias e ambiente; desenhar espaços/acessos; identificar perigos por fase; só então comparar métodos.

**Trade-offs:** exige dados de processo; evita uma resposta rápida baseada no nome comercial. Leia ch01/ch02.

## Registro tarefa–perigo–evidência

**Quando usar:** apreciação inicial ou revisão de célula.

**Como:** criar linha por cenário; identificar pessoa, situação/evento, dano e estimativa; aplicar projeto, proteção e informação nessa prioridade; avaliar novos perigos; associar evidência e risco residual.

**Trade-offs:** muitos cenários podem compartilhar medidas, mas não comprima linhas que têm exposições ou falhas diferentes. Leia ch02; use o modelo de registro.

## Método por fase com transições explícitas

**Quando usar:** carregamento alternado, inspeção, HG ou combinação SSM/PFL.

**Como:** montar tabela de estados; definir presença, movimento permitido, função ativa e condição de troca; verificar que a proteção seguinte já está eficaz ao desativar a anterior; tratar falha e retomada separadamente.

**Trade-offs:** combinações podem melhorar produtividade, mas aumentam complexidade e validação. Leia ch03/ch06.

## Mapa de contatos PFL

**Quando usar:** contato permitido ou previsível.

**Como:** mapear superfície/ponto, parte do corpo, direção, postura, frequência e possibilidade de aprisionamento; distinguir transiente/quase estático; eliminar geometrias perigosas; selecionar critérios com notas; planejar medição de força e pressão; documentar configuração.

**Trade-offs:** contato real varia com postura e ferramenta; ensaios e modelo precisam representar condições relevantes. Leia ch04/ch08.

## Memória de separação SSM

**Quando usar:** movimento simultâneo sem contato.

**Como:** definir pessoas e pontos perigosos; levantar Tr/Ts e dados de parada; calcular Sh+Sr+Ss+C+Zd+Zr com unidades e incertezas; verificar geometria, intrusão, cobertura e falhas; validar limites constantes ou dinâmicos.

**Trade-offs:** solução constante pode ser mais simples e ocupar mais espaço; dinâmica exige maior complexidade de medição/controle. Leia ch05/ch08.

## Especificação da função completa

**Quando usar:** integração de scanner, cortina, porta, parada ou limites seguros.

**Como:** descrever perigo, evento, estado seguro, modos, tempo, desempenho, interfaces, falha e rearme; verificar a cadeia sensor–lógica–comunicação–atuadores; ligar cada requisito a teste/análise.

**Trade-offs:** certificados e dados de componentes ajudam, mas não eliminam cálculo/validação do conjunto. Leia ch06.

## Redesenhar acesso antes de instruir afastamento

**Quando usar:** mão, cabeça ou corpo podem entrar em pinçamento.

**Como:** alterar trajetória/layout/dispositivo para eliminar o ponto; preservar acesso e ergonomia; avaliar novos perigos; acrescentar funções e proteções para o que restar; informar riscos residuais.

**Trade-offs:** pode demandar mudança de dispositivo e ciclo, mas reduz dependência de comportamento perfeito. Leia ch02/ch04/ch07.

## Prova de processo com variação real

**Quando usar:** compra e soldagem, principalmente primeira célula.

**Como:** escolher família de peças e variação admissível; definir qualidade, ciclo completo, troca e disponibilidade; demonstrar acesso/fixação/parâmetros; distinguir validação de processo e de segurança; incorporar FAT/SAT ao escopo.

**Trade-offs:** demonstração representativa custa esforço inicial e reduz a surpresa após compra. Leia ch09/ch10.

## Recuperação de falhas como tarefa projetada

**Quando usar:** enrosco, peça perdida, falha de alimentação ou intervenção manual.

**Como:** definir quem intervém, modo, energias e acesso; impedir partida inesperada; prever retirada/escape; verificar restauração de proteções e retomada; registrar recorrência para melhoria de projeto.

**Trade-offs:** parar com frequência pode indicar problema de processo; não resolva recorrência por normalizar burla. Leia ch12.

## Validação rastreável e gestão de mudanças

**Quando usar:** aceitação, manutenção relevante, nova peça/EOAT ou relocação.

**Como:** identificar versão/configuração; selecionar evidências por requisito; justificar condições de teste; registrar desvios; corrigir e retestar impactos; atualizar instruções e riscos residuais; preservar configuração aprovada.

**Trade-offs:** revalidação deve ser proporcional ao impacto, sem presumir que toda alteração é irrelevante ou exige repetir tudo. Leia ch08/ch12.

## Classificar autoridade antes de citar

**Quando usar:** consulta sobre NR-12, ISO, nota técnica ou material de fornecedor.

**Como:** conferir capa/conteúdo e edição; identificar minuta/projeto; resolver cópias pelo catálogo; consultar primária vigente quando a decisão for atual; citar cláusula e página; marcar síntese/exemplo como tal.

**Trade-offs:** a informação histórica continua útil, mas não deve ser apresentada como obrigação atual sem verificação. Leia ch11 e vigência.

## Investigar energia, transmissão e torque

**Quando usar:** peça leve, colisão inesperadamente alta ou comparação entre robôs.

**Como:** separar massa da peça/EOAT/elos e inércia refletida; identificar direção/postura, velocidade, torque ativo e complacência; usar modelos apenas com hipóteses; solicitar dados e ensaiar a configuração.

**Trade-offs:** o raciocínio N² mostra tendência de um eixo, não caracteriza sozinho produtos ou manipuladores. S32/S33; ch13.

## Converter incidente em cenário de projeto

**Quando usar:** revisão de manutenção, acesso ou lição aprendida.

**Como:** distinguir relato e hipótese; identificar tarefa, energias e exposição; analisar a cadeia causal; priorizar Elimination, Engineering e Enterprise controls; ligar medidas a requisitos/testes e rever cenários semelhantes.

**Trade-offs:** analogia gera perguntas, mas não prova a causa de um caso histórico nem atendimento atual. S27/S28; ch14.
