# Modelos de trabalho

Formulários sintetizados para desenvolver e revisar uma aplicação. Campos em branco significam informação a levantar, não atendimento presumido. Nenhum modelo é laudo, ART, certificado ou autorização automática.

## 1. Ficha inicial da aplicação

| Campo | Registro |
|---|---|
| Identificação/local/data/país | A preencher |
| Responsáveis por projeto/integração/uso | A preencher |
| Robô/controlador/software | A preencher |
| EOAT, peça, massa, centro de gravidade | A preencher |
| Tarefas e fases do ciclo de vida | A preencher |
| Pessoas e quantidade máxima prevista | A preencher |
| Modos/métodos por fase | A preencher |
| Máquinas, processo, utilidades e energias | A preencher |
| Espaços/acessos/layout em planta e elevação | A preencher |
| Normas/edições/regulamentos aplicáveis | A confirmar em fontes primárias |
| Lacunas que impedem decisão específica | A registrar |

## 2. Registro de risco

| ID | Tarefa/pessoa | Perigo/situação/evento | Dano | Estimativa inicial e método | Medidas por prioridade | Novo perigo? | Evidência | Risco residual/estado |
|---|---|---|---|---|---|---|---|---|
| R-01 | A preencher | A preencher | A preencher | Critérios e hipóteses explícitos | Projeto → proteção → informação | Avaliar | ID de cálculo/ensaio/documento | Pendente até avaliação |

Não invente números para completar a tabela. Se usar método de pontuação, registre definições, origem e justificativa de cada mudança de avaliação.

## 3. Tabela de estados e transições

| Origem → destino | Pessoas presentes | Movimentos/energias permitidos | Método/funções ativas | Condição de troca | Resposta a falha | Evidência |
|---|---|---|---|---|---|---|
| Automático → acesso | A definir | A definir | A definir | Proteção eficaz antes da exposição | Estado seguro especificado | Teste/revisão |

Verifique que não existe intervalo sem proteção. Separe retomada normal de recuperação de falha.

## 4. Matriz de contatos PFL

| ID | Tarefa | Parte do sistema/superfície | Região corporal | Postura/direção | Transiente/quase estático e motivo | Frequência/escape | Critérios F/p e fonte/notas | Medidas | Ensaio/resultado |
|---|---|---|---|---|---|---|---|---|---|
| C-01 | A preencher | Braço/EOAT/peça | Específica | A preencher | Confirmar possibilidade de recuo | A avaliar | Não preencher por memória | Projeto + funções | Pendente |

Anexe desenho/foto do ponto e condição ensaiada. Registre configuração, aparato, rigidez/complacência, calibração, grandezas e incertezas. Não exponha pessoas ao contato para testar aceitação.

## 5. Memória preliminar SSM

| Dado | Valor/unidade | Origem e condição | Incerteza/limite |
|---|---|---|---|
| Ponto perigoso/pessoa/direção | A definir | Desenho e tarefa | Cobertura a confirmar |
| Tr e parcelas da cadeia | A levantar em s | Sensor + lógica + comunicação + ativação | Limite justificado |
| Ts | A levantar em s | Configuração, velocidade e carga | Variação a considerar |
| vh/vr | A definir em m/s | Hipóteses e função de monitoramento | Justificar aplicabilidade |
| Sh/Sr/Ss | A calcular/obter em m | Equações e dados de parada | Condição desfavorável |
| C/Zd/Zr | A definir em m | Dispositivo/geometria/medição | Não presumir zero |
| Sp | Soma em m | Edição/método declarado | Validar instalação |

Documente referência geométrica, campo, intrusão, acessos, várias pessoas e resposta à perda de detecção. O cálculo é preliminar até verificação dos dados e da instalação.

## 6. Especificação de função de segurança

| Campo | Registro |
|---|---|
| ID/perigos controlados | A preencher |
| Evento disparador e condições/modos | A preencher |
| Estado seguro de cada máquina/ferramenta | A definir |
| Tempo máximo e origem | A justificar |
| Desempenho requerido/norma/edição | A determinar |
| Sensor/lógica/comunicação/elementos finais | A especificar |
| Falhas, diagnóstico e resposta | A analisar |
| Rearme, partida e retorno de energia | Sequência explícita |
| Configuração/identificador | A registrar |
| Método e critério de validação | A definir antes do ensaio |

## 7. Protocolo de verificação/validação

| ID requisito/risco | Configuração | Método/instrumento | Condição de teste | Resultado esperado | Resultado observado | Incerteza/desvio | Responsável/data | Conclusão |
|---|---|---|---|---|---|---|---|---|
| A relacionar | Versões, carga, EOAT, layout | Inspeção/análise/medição/ensaio | Justificativa de representatividade | Critério prévio | Registrar | Tratar | Identificar | Aceito/pendente/não conforme |

Inclua testes de transição, falha pertinente, presença, energias e retomada. Defina condições controladas; interrompa o ensaio se a proteção planejada não estiver disponível. Correções exigem repetição dos testes afetados e atualização da configuração registrada.

## 8. Ficha de mudança

| Campo | Registro |
|---|---|
| Mudança e motivo | A preencher |
| Configuração anterior/nova | Identificadores, versões e desenhos |
| Riscos/funções/contatos/separações afetados | Análise de impacto |
| Documentos e instruções a atualizar | Lista |
| Verificação/revalidação necessária | Escopo justificado |
| Resultados e pendências | Evidências |
| Responsáveis e aceitação | Conforme governança e competência da instalação |
| Comunicação/capacitação | Pessoas/tarefas e registros |

## 9. Escopo de compra e aceitação

Registre peças e variações, qualidade, ciclo completo, volumes/mix, disponibilidade esperada, condições de ambiente, interfaces, proteções, documentação, treinamento, FAT/SAT, suporte, manutenção e limites de fornecimento. Peça evidências de experiência em aplicação semelhante e atribua responsabilidade às pendências que só podem ser verificadas no destino.

## 10. Prova de conceito (PoC)

| Campo | Registro |
|---|---|
| Hipótese técnica incerta | O que precisa ser demonstrado antes de investir |
| Peças/variações e condições | Amostra representativa e limites de escopo |
| Qualidade, ciclo completo e repetibilidade | Critérios mensuráveis prévios |
| Condições seguras do ensaio | Proteções, responsáveis e interrupção |
| Resultados e limitações | O que passou, falhou ou não foi ensaiado |
| Integração/validação ainda necessárias | Não transferir aprovação do PoC para a célula final |

## 11. Extensão do protocolo de colisão

Acrescente ao modelo 7: fonte do critério biomecânico e notas, corpo/contato representado, complacência/rigidez do aparato e superfícies, ponto/direção/postura, EOAT/carga, velocidade e modo, resposta dinâmica do instrumento, pressão quando aplicável e relação com a tabela do fabricante. Não preencha automaticamente com 75 N/mm ou 150 N da aula.
