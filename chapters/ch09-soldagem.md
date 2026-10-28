# 09 — Soldagem robotizada: processo, segurança e qualidade

## Ideia central

Automatizar o movimento da tocha não elimina os perigos do arco nem estabiliza sozinho a qualidade da junta. Selecione aplicação, dispositivo, processo, proteção e competências como um conjunto.

## Fontes e precisão

S18, pp. PDF 1–3, Lincoln Electric, cópia web impressa em 2015; S15, apresentação de Terry K. Merrifield e Steve B. Wise, pp. PDF 8–18 e 20–35; S03, 4.3, pp. PDF 10–11; S08, Anexo A, pp. PDF 61–68; I11. S15 foi recuperada por OCR; seus slides visuais de dispositivos e alcance foram conferidos em amostras. Os “8 conceitos” do nome de arquivo não foram convertidos artificialmente em oito regras numeradas: o conteúdo está organizado por temas e um caso Eaton.

## Estruturas de decisão

### Viabilidade da junta antes da compra

S18 propõe revisar peças, acesso à junta, repetibilidade, fixação, distorção e processo. A experiência do soldador compensa variações que podem não ser absorvidas por uma trajetória programada.

1. Defina famílias de peças e critérios de qualidade da solda.
2. Verifique acesso da tocha, orientação e alcance ao longo da junta, inclusive com dispositivo e cabos.
3. Meça variações de peça, preparação, folga e posicionamento; não avalie apenas uma amostra ideal.
4. Desenvolva fixação e sequência considerando deformação, carregamento, respingos e retirada.
5. Selecione processo/consumíveis e sensores pertinentes à variação residual.
6. Faça prova de processo com critérios de qualidade e produtividade acordados.

**Por que funciona:** evita transferir variação não controlada para programação corretiva interminável. **Falha típica:** comprar o braço e descobrir depois que o dispositivo bloqueia o acesso ou que a preparação de junta não é repetível.

### Causa e efeito do caso Eaton

S15, p. PDF 17, estrutura causas em produto, materiais, máquinas e pessoas; os slides seguintes mostram revisão de dispositivo, posicionamento e estudo de alcance. Use esse raciocínio antes de culpar o robô.

| Grupo | Pergunta operacional | Possível desenvolvimento |
|---|---|---|
| Produto | A junta permite acesso e fabricação consistente? | Ajustar desenho, folga e acessibilidade |
| Materiais | Limpeza e consumíveis são estáveis? | Controlar preparação e suprimento |
| Máquinas/processo | Parâmetros e alimentação são consistentes? | Padronizar procedimento e equipamentos |
| Pessoas | Há competência e critérios compartilhados? | Capacitar e definir responsabilidades |
| Fixação/alcance | A peça pode ser orientada sem colisões? | Revisar gabarito, posicionador e layout |

Sensoriamento, busca de junta, seguimento e programação offline podem ajudar, mas não substituem acesso viável e processo estável. Selecione tecnologia para a fonte de variação observada, não para uma lista de acessórios.

## Segurança do processo

| Perigo | Por que PFL não basta | Medidas a desenvolver na apreciação |
|---|---|---|
| Radiação do arco | Não é um contato mecânico com o braço | Proteção de operadores e pessoas próximas; barreiras/telas e controle de acesso apropriados |
| Fumos e gases | Limitar força não controla exposição | Captura/exaustão, ventilação e avaliação do processo/material |
| Respingo e calor | Robô parado pode continuar perigoso | Proteção, distâncias, manuseio e resfriamento |
| Choque elétrico | Função do braço não cobre o circuito de solda | Projeto/inspeção elétrica e procedimento adequado |
| Incêndio | Faíscas e materiais combustíveis permanecem | Controle do entorno e medidas próprias do processo |
| Posicionador e fixadores | Criam movimentos/aprisionamentos adicionais | Integração e funções de segurança da célula |

Essa tabela é uma síntese qualitativa dos perigos identificados nas fontes. Não é um projeto de exaustão nem estabelece limites de exposição ou especificações de filtros/telas; esses itens exigem fontes e dimensionamento específicos. Não prometa operação próxima a pessoas com arco ativo só porque o fornecedor denomina o conjunto “welding cobot”.

## Exemplo trabalhado — peça fina com variação de folga

**Reconstrução didática inspirada em S15/S18, sem reproduzir um projeto do autor:** a empresa relata porosidade e falta de fusão após automatizar uma peça fina. A primeira proposta é trocar o robô.

**Investigação:** inspecionar preparação/limpeza, gás, consumíveis, folga, dispositivo, acesso e parâmetros. Comparar amostras e localizar variação por lote/posição. A trajetória repetível pode revelar variação que o soldador antes compensava.

**Decisão:** estabilizar causas de processo e fixação, desenvolver procedimento e só então avaliar necessidade de sensores ou ajuste de tecnologia. Testar uma amostra representativa das variações aceitas, não apenas a melhor peça.

**Segurança em paralelo:** escolher proteção do arco e fumos, estados de acesso, integração de posicionador e recuperação de falhas. A pessoa pode carregar com processo inativo sob solução apropriada e permanecer protegida quando o arco opera; o arranjo final depende do projeto.

**Critérios:** qualidade conforme requisito do produto, repetibilidade, ciclo completo com troca/carregamento, disponibilidade, resposta de segurança e capacidade de recuperação. Os dados não fornecidos permanecem pendentes.

## Seleção do integrador

S15 destaca experiência específica de processo e a cooperação entre engenharia e compras. Solicite demonstração com peças semelhantes, competência em soldagem/robótica, dispositivos/posicionadores, suporte, documentação e critérios de aceitação. Menor preço sem explicação técnica não é evidência de viabilidade.

## Ampliação do curso — divisão de tarefas e limites do processo

S34/S36 usam tarefas repetitivas e demanda ergonômica como motivadores para automação e citam soldagem e acabamento. Use isso para investigar exposição e divisão de trabalho. Não adote como fato atual as previsões de mão de obra nem como regra técnica que toda operação de um tipo exige ou dispensa colaboração. Esmerilhamento, polimento, solda e dosagem devem ter seus perigos de ferramenta e processo avaliados, além do contato mecânico.

## Antipadrões

- “O robô resolve todos os problemas de solda”.
- Confundir facilidade de ensinar trajetória com competência de soldagem.
- Usar previsão histórica de escassez de soldadores como dado atual.
- Omitir exaustão, proteção de terceiros ou posicionador do orçamento.
- Avaliar produtividade apenas pelo tempo de arco, ignorando preparação e troca.

## Decisões a reter

1. Comprove junta, acesso, repetibilidade e fixação antes da compra.
2. Trate perigos de processo separadamente do movimento.
3. Escolha sensores para variações demonstradas.
4. Contrate competência e evidências de processo, além do hardware.

## Conexões

Ch07 para integração; ch08 para aceitação; ch10 para compra; ch12 para competências e manutenção.
