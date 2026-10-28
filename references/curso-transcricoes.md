# Curso Collaborative Robot Safety Design & Deployment — leitura crítica

## Procedência e forma de citação

Vinte TXT fornecidos pelo usuário, identificados como S19–S38. Os textos apresentam Brian Carlisle/Precise Automation e Mike Garman/Buffalo Manufacturing Works–EWI, além de vozes sem identificação inequívoca. Não atribua todas as falas a um único autor. Há referência explícita a 2018 em S21; a data de cada gravação e a plataforma de origem não foram confirmadas.

Foram lidos integralmente como transcrições textuais. Vídeos, fotografias, slides, tabelas e gráficos mencionados não acompanharam estes arquivos. Uma frase que diz “nesta tabela” não disponibiliza os dados da tabela. Não reconstrua valores ausentes nem declare uma demonstração visual conferida.

Use `Sxx, nome da aula, Lx–Ly` para linhas físicas do TXT original, ou ID/arquivo e âncora curta de busca. Muitos arquivos contêm uma única linha longa; linha 1 não é página ou minuto do vídeo. O [manifesto](source-manifest.json) registra contagem de linhas, hash e caminho. Não foram criadas marcações de tempo artificiais.

## Tratamento de afirmações problemáticas

| Texto/afirmação da transcrição | Tratamento na skill |
|---|---|
| Números deformados como ISO 102018, ISO 1200, IEC 6204-1 e 150666 | Não usar como identificadores normativos. Conferir a norma pretendida na publicação primária; manter a transcrição original rastreável |
| “Part Two” associado a 10218-1 | Distinguir parte 1 e parte 2; usar S07/S08 para o acervo primário |
| PL apresentado de b a e ou como simples escala de risco | Não adotar como catálogo completo de PL nem como equivalência direta; veja ch06 |
| Lâmpada/aviso descrito como exemplo suficiente de PL b | Um dispositivo de aviso não demonstra sozinho o PL de uma função; rejeitar a extrapolação |
| Severidade S1–S3, exposição E0–E2 e evitação A1–A3 | Descrever como método didático citado, sem reproduzir matriz ausente ou mapear automaticamente para PL/categoria |
| Menção a “E3” junto à discussão de A3 | Sinal de erro textual; não inventar classe para completá-lo |
| “A empresa define risco aceitável” | Não autoriza descumprir obrigações ou substituir redução adequada por preferência empresarial |
| SSM questionado por não permitir contato | SSM é um dos métodos de operação colaborativa no acervo S03; contato não é condição necessária de toda colaboração |
| Velocidades, cargas e afastamentos apresentados como típicos | Dados de exemplos e contexto histórico; não limites universais ou especificações atuais |
| 150 N ou 150–180 N como regra geral | Não adotar como força universal; consultar região, contato, pressão e notas de S03 |
| 75 N/mm como simulador de mão | Parâmetro da metodologia descrita pelo fabricante, não rigidez de todo corpo/aplicação |
| Comparação de massas/razões em S32 | Transcrição numericamente inconsistente e sem tabela original; preservar somente raciocínio N² com hipóteses claras e exemplo próprio |
| 206 N descritos como cerca de 10% acima de 180 N em S38 | Aritmeticamente, aproximadamente 14,4%; não reproduzir o percentual como correto nem adotar 180 N como limite da aplicação |
| Seção 7 apresentada como verificação/validação em S37 | Em S03: seção 6 trata verificação/validação; seção 7 trata informação de uso |
| “Calibrado para referência NIST” e testemunho de TÜV | Alegações narradas sobre instrumento/ensaio; não equivalem a certificação de qualquer robô ou célula nem foram auditadas |
| Ensaiar com mão/dedos em pinçamento ou uma criança | Não converter em método. Usar aparato e condições de ensaio controladas; nenhuma pessoa deve ser o corpo de prova da validação |
| Robôs cirúrgicos, de serviço, móveis, militares ou transporte de pessoas | Exemplos de classificação/contexto; não ampliar automaticamente o campo das normas industriais |
| Aprovações FDA, números de mercado, economia ou emprego | Relatos históricos não verificados; não apresentados como situação atual ou recomendação médica/financeira |

Não foi necessário atualizar ou pesquisar cada afirmação histórica: a atualização é uma incorporação crítica do acervo, não uma validação de todos os fatos do curso. A nota de [vigência](vigencia.md) da base continua com consulta externa limitada de 28/10/2026.

## Conteúdos incorporados

- **ch01/ch03:** classificação, limites de escopo e diferença entre arranjo de interação e método de proteção.
- **ch02/ch14:** equipe multidisciplinar, método por tarefa, 3E e aprendizado com incidentes.
- **ch04/ch13:** energia, torque ativo, inércia refletida, complacência e aproximação a superfícies rígidas.
- **ch06:** integridade do controle distinta de algoritmo funcional de torque.
- **ch07/ch10:** acesso, apresentação de peças, atendimento de máquinas, automação parcial e prova de conceito.
- **ch08:** dados de fabricante e plano de medição por direção, configuração e contato.
- **ch11/ch12:** interpretação de fontes históricas, competências e intervenção no sistema completo.

## Princípio editorial

Preservar o raciocínio técnico do autor não exige repetir um erro como instrução. Cada ampliação distingue o que o curso narra, o que foi reconstruído didaticamente e o que precisa de evidência primária para uma decisão real.
