# 12 — Operação, capacitação, manutenção e mudanças

## Ideia central

A segurança validada precisa sobreviver ao uso, às falhas e às alterações. Prepare pessoas e procedimentos para os estados que interrompem a produção, além do ciclo automático normal.

## Fontes e precisão

S08, 5.6–5.9 e seção 7, pp. PDF 30–38 e 54–59; S03, 5.4 e seção 7, pp. PDF 12–13 e 25–26; S02, pp. PDF 46–59 e 63–70; S09, conclusão, pp. PDF 6–7; S13, seção sobre trabalhadores, pp. PDF 16–20; S18, pp. PDF 1–3. A organização por competências e os exemplos são sínteses desta skill.

## Competência por tarefa

Não deduza aptidão para manutenção ou ajuste de segurança da capacidade de ensinar um ponto. Os materiais comerciais descrevem facilidade de programação e tempos curtos de aprendizagem; isso não comprova capacitação suficiente para uma função específica.

| Perfil/tarefa | Competência a demonstrar |
|---|---|
| Operação e abastecimento | Estados permitidos, proteções, anomalias e parada |
| Preparação/troca | Peça, ferramenta, carga, referência, receita e verificações antes de produzir |
| Recuperação de falhas | Diagnóstico permitido, estado seguro, limites de intervenção e escalonamento |
| Programação | Trajetórias, envelopes, modos, transições e impacto da mudança |
| Manutenção | Energias, retenção de carga, diagnóstico, reposição e restauração |
| Ajuste de segurança/validação | Requisitos, desempenho, configuração, ensaios e documentação |

Planeje aprendizado prático com procedimentos da instalação, supervisão e comprovação de entendimento. A proteção de pessoas próximas, limpeza e terceiros também precisa ser tratada, sem pressupor que todos conheçam o ciclo do robô.

## Procedimentos para os estados de exceção

Para cada falha previsível, defina:

1. Como reconhecer e comunicar a condição.
2. Quem pode intervir e em qual modo/estado.
3. Quais movimentos e energias precisam ser controlados ou isolados.
4. Como verificar a condição antes de entrar.
5. Como retirar peça/ferramenta sem criar queda, aprisionamento ou exposição adicional.
6. O que conferir antes de restabelecer proteções e retomar.
7. Como registrar recorrência e acionar revisão de projeto.

**Por que funciona:** reduz a improvisação quando o ciclo deixa de ser previsível. **Falha típica:** permitir que o operador entre para soltar uma peça com a expectativa de que o programa “está pausado”.

## Manutenção e energias

Considere energia elétrica, pneumática, hidráulica, gravidade, molas, cargas suspensas, calor e processo. Uma parada de emergência ou SRMS pode não produzir o isolamento necessário. O procedimento deve usar a estratégia apropriada à tarefa, com meios para impedir partida inesperada e controlar energia armazenada.

Após manutenção, confira componentes corretos, ligações, funções, ajustes, proteções e referências. Uma troca “equivalente” de sensor pode alterar tempo, campo ou diagnóstico. Uma atualização de software pode alterar comportamento ou parâmetros. Avalie impacto antes de declarar que a validação anterior continua suficiente.

## Gestão de mudanças

| Alteração | Perguntas de impacto | Evidência potencialmente afetada |
|---|---|---|
| EOAT/peça/carga | Mudou massa, geometria, retenção ou contato? | PFL, parada, envelope e dados de carga |
| Velocidade/trajetória | Mudou aproximação, energia ou ponto perigoso? | SSM, PFL e limites de espaço |
| Layout/relocação | Mudou acesso, referência ou obstáculo? | Campos, espaços e aprisionamentos |
| Sensor/lógica/rede | Mudou tempo, diagnóstico ou cobertura? | Segurança funcional e separação |
| Software/configuração | Mudou versão, checksum ou comportamento? | Correspondência com evidência validada |
| Tarefa/organização | Há outra pessoa, turno ou intervenção? | Exposição, capacitação e procedimento |

Não determine automaticamente “revalidar tudo” ou “não muda nada”. Identifique o impacto e revalide as medidas afetadas. Preserve a versão anterior e a razão da mudança; a rastreabilidade permite descobrir quais evidências perderam validade.

## Exemplo trabalhado — nova garra no mesmo programa

**Exemplo didático:** a equipe substitui uma garra de dedos por uma ferramenta de vácuo para aumentar produção e mantém o programa.

**Diferenças relevantes:** massa e centro de gravidade, geometria de contato, projeção da peça, comportamento ao faltar energia/vácuo e tempo de parada. A ferramenta pode cobrir uma região de detecção ou criar acesso antes inexistente.

**Ação:** registrar a alteração, atualizar dados de carga e desenho, revisar apreciação e funções, conferir retenção da peça, reavaliar contatos e parada, atualizar procedimentos e testar as partes afetadas. Se a ferramenta adiciona uma borda rígida, o antigo ensaio PFL não demonstra automaticamente esse contato.

**Critério de conclusão:** configuração documentada, evidências pertinentes aprovadas por responsáveis competentes, instruções atualizadas e pessoal preparado. O fato de o ciclo “rodar igual” só demonstra continuidade funcional de parte da produção.

## Inspeções e sinais de degradação

Defina inspeções e manutenção com base em instruções dos fabricantes, condições de uso e apreciação. Não invente um intervalo universal. Observe proteções danificadas, sensores deslocados, garras com desgaste, falhas recorrentes, alteração de tempos, materiais acumulados e rotinas de burla.

Uma falha repetitiva de abastecimento é informação de projeto: pode justificar alteração de dispositivo ou alimentação. Se a proteção impede uma tarefa frequente sem alternativa projetada, revise a tarefa e a solução; não normalize o desvio como rotina.

## Ampliação do curso — aprender com incidentes e anomalias

S27/S28 reforçam que parar um equipamento em manutenção pode deixar sensores, plataformas e robôs associados ativos. Inclua terceiros e acessos por cima na análise. O [ch14](ch14-prevencao-e-licoes-de-incidentes.md) converte os dois casos narrados em perguntas de tarefa, energias e projeto, sem apresentá-los como relatórios oficiais conferidos.

S37 descreve coleta de falhas repetitivas e integração de dados com processos a montante. Use esse retorno para revisar alimentação, dispositivo, manutenção e treinamento. A redução de paradas de produção não autoriza reduzir proteção ou normalizar intervenção em pontos perigosos.

## Antipadrões

- Compartilhar senha de segurança como prática de operação.
- Carregar backup sem confirmar versão/configuração e impacto.
- Aceitar falha intermitente porque “sempre voltou a funcionar”.
- Intervir em pinçamento com programa pausado sem controlar energias.
- Reutilizar a validação após relocação sem avaliar referências e acessos.

## Decisões a reter

1. Capacite por tarefa, não por facilidade do software.
2. Prepare recuperação e manutenção antes de transferir para produção.
3. Use anomalias recorrentes para revisar projeto.
4. Controle configuração e revalide impactos das mudanças.

## Conexões

Ch02 para novas tarefas; ch06 para energias e funções; ch08 para revalidação; ch11 para registros. Ficha de mudança nos [modelos práticos](../references/modelos-praticos.md).
