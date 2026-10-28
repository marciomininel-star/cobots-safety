# 08 — Verificação, validação e aceitação

## Ideia central

Validação exige relacionar o que foi projetado ao comportamento efetivo da aplicação. Um ciclo de produção sem incidentes não comprova as funções de proteção, os contatos PFL ou a separação SSM.

## Fontes e precisão

S08, seção 6, pp. PDF 51–53, e Anexo G normativo, pp. PDF 80–98; S03, seção 6 e 7, pp. PDF 25–26; S02, pp. PDF 57–59; S07, seção 6. O plano abaixo é uma síntese de trabalho e não reproduz nem esgota a matriz do Anexo G.

## Estruturas para usar

### Cadeia de evidências

`tarefa/perigo → medida → requisito → método de verificação → resultado → risco residual`

Use um ID estável para conectar os registros. Um documento de função pode estar correto e sua instalação estar incorreta; um ensaio simples pode passar apesar de arquitetura inadequada. Combine métodos.

| Método | O que pode demonstrar | Limite |
|---|---|---|
| Inspeção visual | Instalação, acesso, fixação e identificação | Não comprova tempos ou PL sozinha |
| Revisão documental | Correspondência entre requisitos, projeto e instruções | Precisa refletir a configuração instalada |
| Cálculo/análise | Dimensionamento e comportamento esperado | Depende de hipóteses e dados válidos |
| Medição | Grandeza observada em condição definida | Não cobre outras condições automaticamente |
| Ensaio prático | Resposta da função e sequência | Precisa de condições e critérios previamente definidos |
| Observação da operação | Uso real, intervenções e incentivos à burla | Ausência de incidente não prova redução adequada |

### Estados de evidência

Use **não avaliado**, **especificado**, **implementado**, **verificado/validado** e **pendente/não conforme** com precisão. Uma fotografia do sensor instalado não demonstra que a função inteira atende ao desempenho requerido.

## Método de planejamento

1. Consolide requisitos da edição aplicável, riscos, funções e critérios de aceitação.
2. Identifique a configuração: modelo, software, EOAT, peça, carga, layout, parâmetros de segurança e identificadores de versão.
3. Selecione métodos e instrumentos apropriados; registre calibração, faixa, resolução e incertezas relevantes.
4. Defina condições representativas e desfavoráveis justificadas: posturas, velocidades, massas, acessos e número de pessoas.
5. Planeje testes controlados de transições, retorno de energia, falhas relevantes e recuperação, sem expor pessoas ao perigo.
6. Execute, registre resultados brutos/resumidos, desvios, correções e repetição dos testes afetados.
7. Feche pendências e registre limites de uso, riscos residuais e responsabilidade pela aceitação.

**Por que funciona:** impede que um ensaio bem-sucedido substitua a pergunta sobre o que ele realmente cobriu. **Falha típica:** medir a parada vazia em uma postura e usar o valor para todas as peças e orientações.

## Ensaios por método colaborativo

| Método | Exemplos de verificações pertinentes |
|---|---|
| SRMS/SMS | Parada antes do acesso; detecção de presença; condição monitorada; resposta a violação; retomada |
| HG | Tomada/liberação de controle; habilitação quando aplicável; limites; movimentos intuitivos; transições |
| SSM | Tempo de reação; frenagem; campos; acessos; pontos perigosos; ocultações; várias pessoas; falhas |
| PFL | Contatos selecionados; força e pressão; configuração/postura; ferramenta/peça; retirada de aprisionamento |
| Qualquer método | Emergência, máquinas associadas, energia, falhas, ajustes e intervenções fora da produção |

Para força/pressão, selecione aparato que represente o contato e as características biomecânicas pertinentes, com procedimento competente. Não use o corpo de um trabalhador como instrumento. A configuração do robô e o método de medição precisam constar do registro.

## Exemplo trabalhado — teste que passa e não basta

**Cenário didático:** teste de scanner com braço sem peça demonstra parada em 0,22 s. O relatório propõe aceitar toda a célula.

**Revisão da evidência:** não há identificação da carga, posturas, velocidades, cadeia de latências, resolução de intrusão, ponto de referência, acessos laterais ou presença de uma segunda pessoa. O número medido não sustenta a conclusão global.

**Plano corrigido:** selecionar configurações pertinentes ao pior caso, obter dados de parada, medir/confirmar latências, revisar cálculo e campo, testar acessos e comportamentos em falha. A aceitação deve distinguir o resultado válido daquele ensaio e o que ainda falta demonstrar.

**Registro didático resumido:**

| Item | Resultado | Estado |
|---|---|---|
| Parada no ensaio vazio | 0,22 s na configuração registrada | Evidência parcial |
| Parada com ferramenta/peça reais | Sem dados | Pendente |
| Cobertura lateral | Acesso não analisado | Pendente |
| Retorno após ocupação | Sequência ainda não testada | Pendente |
| Conclusão da aplicação | Critérios não demonstrados | Sem liberação técnica por este registro |

Esse exemplo não estabelece uma quantidade universal de repetições ou margem de segurança. Essas escolhas precisam ter base no método de ensaio, dados do equipamento, norma e apreciação.

## FAT e SAT

Use FAT para verificar o escopo acordado no fornecedor e SAT para a instalação no local, com suas utilidades, interfaces e acesso real. Os termos ajudam a contratar e organizar o trabalho; não substituem os requisitos de verificação/validação. Identifique o que só pode ser demonstrado no destino e não marque como concluído na fábrica.

## Ampliação do curso — dados de colisão e método do fabricante

S37/S38 descrevem a metodologia da Precise Automation, não um procedimento normativo universal. A narração considera a complacência do corpo, robô e superfícies e usa simulador com mola, medidor de força com retenção de pico e referência de calibração. Para uma aplicação real, selecione aparato/procedimento adequados ao contato e ao critério; pico retido, faixa e calibração não demonstram sozinhos resposta dinâmica ou pressão local.

Solicite dados de colisão por carga, ferramenta, direção X/Y/Z, movimentos em juntas/Cartesiano, velocidade e situação de contato. Confira se a tabela do fabricante cobre a configuração e a geometria da célula. Distinguir contato com recuo de aprisionamento é essencial: S38 relata forças distintas na mesma velocidade em dois arranjos, mas os vídeos e dados completos não foram enviados.

No plano, registre rigidez/complacência do aparato e do contato representado, condições de montagem, ponto/direção, faixa, capacidade dinâmica pertinente, calibração, repetibilidade, incerteza e critério. Meça pressão quando necessária, além da força. Não use uma bancada totalmente rígida e depois simplesmente descarte o resultado alto: justifique a representatividade do conjunto pelo cenário e pelo método competente.

O valor de 75 N/mm e a regra de 150–180 N são hipóteses da aula; não simulam todo corpo e contato. Nem 50 mm de aproximação, 80% de velocidade ou aparência de parada suave aprovam outra aplicação. S38 relata testemunho/certificação externa do ensaio; não há certificado anexado para auditar seu escopo. Rastreabilidade de calibração não equivale a certificação da célula.

S37 confunde a numeração: em S03, a seção 6 trata verificação/validação e a seção 7 informação de uso. Não perpetue a referência errada. As demonstrações com pessoas em pinçamento devem ser substituídas por ensaios instrumentados controlados; detalhes de dinâmica no ch13.

## Antipadrões

- Mudar o programa depois do ensaio sem analisar impacto.
- Aceitar só os testes de produção sem os estados de falha.
- Selecionar o menor resultado em vez de justificar a condição desfavorável.
- Inventar margem percentual ou número de repetições como regra normativa.
- Usar checklist genérico como laudo automático.

## Decisões a reter

1. Defina critérios antes de medir.
2. Identifique a configuração validada.
3. Cubra interfaces e estados fora do ciclo normal.
4. Feche desvios com evidência e reteste o que foi afetado.

## Conexões

Ch04/ch05 para grandezas; ch06 para funções; ch11 para dossiê; ch12 para manutenção da validade. Modelo de protocolo em [modelos práticos](../references/modelos-praticos.md).
