# Catálogo de fontes e cobertura

As páginas citadas nos módulos são **páginas do arquivo PDF**, contadas desde a capa. A paginação impressa pode ser diferente. IDs Sxx identificam conteúdos documentais; Ixx identificam os 12 infográficos. Caminhos e SHA-256 completos estão no [manifesto](source-manifest.json). Os originais e extrações integrais não são incluídos nesta skill.

## Inventário após a incorporação do curso

**43 documentos → 38 conteúdos distintos**, mantendo 5 caminhos duplicados, 565 páginas PDF distintas, um DOCX, **20 TXT** e 12 infográficos. Os TXT foram lidos integralmente em texto simples, sem necessidade de Docling/OCR. São 18.584 palavras adicionais conforme o extrator. Os módulos ch01–ch12 foram ampliados e ch13/ch14 adicionados. A contagem anterior abaixo documenta a primeira base.

As fontes novas são treinamento histórico com erros de transcrição, não novas normas primárias. Leia as [ressalvas do curso](curso-transcricoes.md). Para TXT use ID/arquivo e linhas físicas; quando houver uma única linha longa, use uma âncora curta de busca, sem inventar página/minuto.

## Inventário original confirmado

23 documentos fornecidos → 18 conteúdos binariamente distintos, com 5 caminhos duplicados. Há 565 páginas PDF nos conteúdos distintos, além do DOCX sem paginação estável, e 12 imagens. Versões textualmente semelhantes com hashes diferentes foram mantidas separadas.

O extrator book-to-skill foi executado em modo técnico, mas Docling não estava disponível: usou fallback. A primeira passagem processou 22 documentos/801 páginas e falhou no PDF S08. A segunda inspeção independente com PDFium recuperou texto adicional e identificou os PDFs de imagens. OCR nativo Windows recuperou 149 páginas de S06/S08/S15. OCR não garante números, unidades e estrutura de tabelas; os diagramas não foram integralmente reconstruídos. Não foram feitas instalação de dependências nem transmissão dos arquivos para serviço de OCR.

## Documentos

### S01 — Collaborative Robot Technical Specification ISO/TS 15066 Update

- **Arquivo:** `12-TR15066Overview-SafetyforCollaborativeApplications-RobertaNelsonShea.pdf`
- **Autor/instituição:** Roberta Nelson Shea / Rockwell Automation
- **Natureza/edição:** Apresentação técnica, contexto de 2016
- **Extensão:** 35 páginas PDF
- **Cobertura:** ch01–ch06
- **Qualidade/leitura:** PDFium; conteúdo textual; figuras biomecânicas são referência ilustrativa
- **Outros caminhos com o mesmo SHA-256:**
  - `D:\Onedrive\Robotica\Manuais\_Geral\Segurança\Cobots\Collaborative Robot Technical Specification ISOTS 15066 Update.pdf`
  - `D:\Onedrive\Robotica\Manuais\_Geral\Segurança\Cobots\ISO\12-TR15066Overview-SafetyforCollaborativeApplications-RobertaNelsonShea.pdf`

### S02 — Robôs Colaborativos — Novos Paradigmas de Segurança Humana

- **Arquivo:** `201015-74dt.Seguranca.pdf`
- **Autor/instituição:** Sidney Esteves Peinado / Fast Solution
- **Natureza/edição:** Treinamento, contexto 2020; não norma
- **Extensão:** 74 páginas PDF
- **Cobertura:** ch01–ch08, ch11–ch12
- **Qualidade/leitura:** PDFium; slides de segurança, ciclo e validação consultados

### S03 — ISO/TS 15066:2016 — Collaborative robots

- **Arquivo:** `ISO-TS 15066_2016.pdf`
- **Autor/instituição:** ISO
- **Natureza/edição:** Especificação técnica, edição 2016; Anexo A informativo
- **Extensão:** 40 páginas PDF
- **Cobertura:** ch01–ch08, ch11–ch12
- **Qualidade/leitura:** PDFium; fórmula p.18 e tabelas pp.30–32/36 conferidas visualmente
- **Outros caminhos com o mesmo SHA-256:**
  - `D:\Onedrive\Robotica\Manuais\_Geral\Segurança\Cobots\ISO\ISO-TS 15066_2016.pdf`

### S04 — Segurança de máquinas — Princípios gerais de projeto — Apreciação e redução de riscos

- **Arquivo:** `NBR ISO 12100 Segurança de máquinas – Princípios gerais de projeto - Apreciação e redução de riscos.pdf`
- **Autor/instituição:** ABNT/CB-04
- **Natureza/edição:** PROJETO 04:026.01-002, AGO 2013; NÃO TEM VALOR NORMATIVO
- **Extensão:** 113 páginas PDF
- **Cobertura:** ch02, ch11
- **Qualidade/leitura:** PDFium; capa conferida visualmente; três caminhos idênticos
- **Outros caminhos com o mesmo SHA-256:**
  - `D:\Onedrive\Robotica\Manuais\_Geral\Segurança\Cobots\nbr-iso-12100-sm-principios-gerais-de-projeto-apreciacao-e-reducao-de-riscos-150616192951-lva1-app6892.pdf`
  - `D:\Onedrive\Robotica\Manuais\_Geral\Segurança\Cobots\ISO\nbr-iso-12100-sm-principios-gerais-de-projeto-apreciacao-e-reducao-de-riscos-150616192951-lva1-app6892.pdf`

### S05 — Esclarecimentos sobre robôs colaborativos à luz da NR-12

- **Arquivo:** `NT_N°31 - DSST - NR-12 - Robôs industriais colaborativos.pdf`
- **Autor/instituição:** MTb / CGNOR / DSST / SIT
- **Natureza/edição:** Cópia digitalizada de nota de 2018; identificação da capa pouco legível
- **Extensão:** 8 páginas PDF
- **Cobertura:** ch11
- **Qualidade/leitura:** PDFium recuperou mais texto que a primeira extração; comparar S09 para identificação

### S06 — Segurança e Legislação

- **Arquivo:** `UR BR 2019 05 Segurança e Leglislação.pdf`
- **Autor/instituição:** Universal Robots
- **Natureza/edição:** Apresentação histórica; arquivo identificado como 2019
- **Extensão:** 11 páginas PDF
- **Cobertura:** ch06, ch11
- **Qualidade/leitura:** OCR local das 11 páginas; não usar tabelas de slide como primária

### S07 — ABNT NBR ISO 10218-1:2018 — Parte 1: Robôs

- **Arquivo:** `NBR ISO 10218-1.pdf`
- **Autor/instituição:** ABNT / ISO
- **Natureza/edição:** Publicação ABNT 2018; adoção da ISO 2011
- **Extensão:** 61 páginas PDF
- **Cobertura:** ch03, ch06, ch08, ch11
- **Qualidade/leitura:** PDFium; texto e cláusulas consultados

### S08 — ABNT NBR ISO 10218-2:2018 — Sistemas robotizados e integração

- **Arquivo:** `NBR ISO 10218-2.pdf`
- **Autor/instituição:** ABNT / ISO
- **Natureza/edição:** Publicação ABNT 2018; adoção da ISO 2011
- **Extensão:** 100 páginas PDF
- **Cobertura:** ch01–ch12
- **Qualidade/leitura:** PDF de imagens; OCR local das 100 páginas; pp.49/52 conferidas visualmente

### S09 — Nota Técnica CGNOR–DSST–SIT–MT nº 31, de 19/02/2018

- **Arquivo:** `nota tecnica nº 31.pdf`
- **Autor/instituição:** Ministério do Trabalho
- **Natureza/edição:** Cópia textual de nota histórica; autenticidade/vigência a verificar para uso legal
- **Extensão:** 7 páginas PDF
- **Cobertura:** ch11–ch12
- **Qualidade/leitura:** PDFium; identificação e conteúdo consultados

### S10 — NT Robôs Colaborativos — versão de 24/10/2017

- **Arquivo:** `NT Robôs Colaborativos_24.10.2017.docx`
- **Autor/instituição:** CGNOR / DSST / SIT / MTPS (cabeçalho)
- **Natureza/edição:** DOCX com número de nota em branco; minuta
- **Extensão:** DOCX, sem correspondência de páginas estável
- **Cobertura:** ch11
- **Qualidade/leitura:** python-docx; parágrafos e tabelas; não possui paginação PDF estável

### S11 — NT Robôs Colaborativos — versão de 24/10/2017

- **Arquivo:** `NT Robôs Colaborativos_24.10.2017.pdf`
- **Autor/instituição:** CGNOR / DSST / SIT / MTPS (cabeçalho)
- **Natureza/edição:** PDF com número de nota em branco; minuta relacionada a S10
- **Extensão:** 9 páginas PDF
- **Cobertura:** ch11
- **Qualidade/leitura:** PDFium; versão relacionada, sem deduplicação textual presumida

### S12 — Portaria MTb nº 98, de 08/02/2018

- **Arquivo:** `Portaria_MTb_n._98_Altera_NR-12__Itens_da_parte_Geral.pdf`
- **Autor/instituição:** Ministério do Trabalho
- **Natureza/edição:** Alteração histórica da NR-12; cópia com inconsistência aparente no DOU
- **Extensão:** 3 páginas PDF
- **Cobertura:** ch11
- **Qualidade/leitura:** PDFium; 3 páginas; conferir ato oficial para citação legal

### S13 — Collaborative Robots: A Comprehensive Guide to Capabilities, Safety, and Applications

- **Arquivo:** `Collaborative Robots_ A Comprehensive Guide.pdf`
- **Autor/instituição:** Force Design
- **Natureza/edição:** Guia técnico/comercial; data não confirmada
- **Extensão:** 40 páginas PDF
- **Cobertura:** ch01, ch07, ch10, ch12
- **Qualidade/leitura:** PDFium; formulações simplificadas sobre métodos subordinadas à primária S03

### S14 — Safety Measures for Collaborative Robots

- **Arquivo:** `tuvsud-cobot-safety-infographic.pdf`
- **Autor/instituição:** TÜV SÜD America
- **Natureza/edição:** Infográfico, 2021
- **Extensão:** 1 páginas PDF
- **Cobertura:** ch03
- **Qualidade/leitura:** PDFium + imagem I07 lida; apresentação didática dos quatro métodos

### S15 — Modern Concepts for Implementing Robotic Arc Welding

- **Arquivo:** `8-Modern-Concepts-Implementing-Robotic-Arc-Welding.pdf`
- **Autor/instituição:** Terry K. Merrifield / Steve B. Wise, NRAWC
- **Natureza/edição:** Apresentação de conferência; data não confirmada
- **Extensão:** 38 páginas PDF
- **Cobertura:** ch09–ch10
- **Qualidade/leitura:** OCR das 38 páginas; slides visuais 17/22/24/30 conferidos; desenhos sem dimensões extraídas

### S16 — 10 passos para começar com os cobots de maneira fácil

- **Arquivo:** `E-book_10-passos-para-começar-com-cobots.pdf`
- **Autor/instituição:** Universal Robots
- **Natureza/edição:** E-book comercial; data não confirmada
- **Extensão:** 14 páginas PDF
- **Cobertura:** ch07, ch10
- **Qualidade/leitura:** PDFium; 10 dimensões preservadas; números de carga/alcance não generalizados

### S17 — Seu negócio é muito pequeno para adotar a robótica?

- **Arquivo:** `E-book_Muito-pequeno-para-robotica.pdf`
- **Autor/instituição:** Universal Robots
- **Natureza/edição:** E-book comercial; data não confirmada
- **Extensão:** 8 páginas PDF
- **Cobertura:** ch10
- **Qualidade/leitura:** PDFium; 5 perguntas preservadas; retorno e custos tratados criticamente

### S18 — Robotics: Purchasing Your First Robotic Welding System

- **Arquivo:** `Purchasing Your First Robotic Welding System.pdf`
- **Autor/instituição:** Lincoln Electric
- **Natureza/edição:** Artigo técnico/comercial; impressão web de 18/03/2015
- **Extensão:** 3 páginas PDF
- **Cobertura:** ch07, ch09–ch10, ch12
- **Qualidade/leitura:** PDFium; mitos, realidade, decisão, riscos de processo e custos consultados

## Infográficos: leitura e ressalvas

Todos foram lidos visualmente nos anexos. Informações pequenas, referências e números não foram transcritos como requisitos sem confirmação em fonte primária. I06/I10 são recorte e versão completa relacionados; S14/I07 são versões relacionadas em formatos diferentes. A relação temática não foi contada como duplicata binária.

### I01 — 1654696621694.jpg
- **Crédito identificado:** Jeff Winter (crédito visual)
- **Dimensões originais:** 1280 × 719 px
- **Uso/limite:** Comparação de capacidades de robôs/pessoas; benefícios condicionados à aplicação.

### I02 — features_of_human_robot_interaction_types_cobots_applications_ppt_show_infographic_template_slide01.jpg
- **Crédito identificado:** Template de apresentação; autoria não confirmada
- **Dimensões originais:** 1280 × 720 px
- **Uso/limite:** Contém Add text here e lacunas; não usar como requisitos ou matriz normativa.

### I03 — Infographic_Cobots_Safety-and-Risk-Assessment_JPG.jpg
- **Crédito identificado:** Mechanical Engineering / ASME; exemplos de UR
- **Dimensões originais:** 925 × 2481 px
- **Uso/limite:** A aplicação precisa ser apreciada; arquiteturas e sensores são exemplos, não características universais.

### I04 — Types-of-collaboration-with-robots-1.jpg
- **Crédito identificado:** Autoria não confirmada
- **Dimensões originais:** 800 × 618 px
- **Uso/limite:** Taxonomia didática de interação; eixo de segurança intrínseca não é prova normativa de segurança crescente.

### I05 — OnRobot_Infographic_Difference_Collaborative_Applications_.jpg
- **Crédito identificado:** OnRobot, contexto 2019
- **Dimensões originais:** 932 × 2000 px
- **Uso/limite:** Material comercial de EOAT; vantagens, preços e modelos não são recomendações atuais.

### I06 — nist-cobot-infographic-top-segment.jpg
- **Crédito identificado:** NIST / MEP
- **Dimensões originais:** 750 × 909 px
- **Uso/limite:** Recorte visual do tema de I10; previsões e dados históricos, não estatísticas atuais.

### I07 — Tuvsud-cobot-safety-infographic-1000x1414.jpg
- **Crédito identificado:** TÜV SÜD America, 2021
- **Dimensões originais:** 1000 × 1414 px
- **Uso/limite:** Equivalente temático de S14, sem identidade binária presumida; quatro métodos históricos.

### I08 — Force-Designs-A-Guide-on-Collaborative-Robots-2.png
- **Crédito identificado:** Force Design
- **Dimensões originais:** 800 × 1750 px
- **Uso/limite:** Aplicações e benefícios potenciais; não generalizar facilidade, custo ou segurança.

### I09 — 78251967_3353094161431480_7760112889976848384_n.png
- **Crédito identificado:** Omron (crédito visual)
- **Dimensões originais:** 800 × 2000 px
- **Uso/limite:** Qualidade, segurança e flexibilidade; prazos e certificação do produto não validam a célula.

### I10 — nist_cobotinfographic-digital_8.5x22-final.png
- **Crédito identificado:** NIST / MEP
- **Dimensões originais:** 1275 × 3300 px
- **Uso/limite:** Infográfico completo com dados de 2017 e previsões para 2025; mobilidade/exoesqueletos não ampliam automaticamente o escopo desta skill.

### I11 — Sem título.png
- **Crédito identificado:** Hirebotics
- **Dimensões originais:** 600 × 1597 px
- **Uso/limite:** Infográfico comercial de soldagem; escassez prevista e implantação rápida não são fatos atuais ou aceitação de segurança.

### I12 — cobot.png
- **Crédito identificado:** SICK / Clearpath (créditos visuais)
- **Dimensões originais:** 2048 × 7171 px
- **Uso/limite:** Introdução e robótica móvel; avaliar plataforma e navegação separadamente do braço fixo.

## Hierarquia editorial de uso

Dê precedência à publicação primária aplicável para requisitos; use apresentações e guias para explicação. Quando houver divergência, não faça média entre fontes: identifique a diferença de escopo/edição e confirme na primária. Por exemplo, S13 aproxima HG de programação e simplifica a retomada de parada; ch03 usa as condições específicas de S03. O projeto S04 não comprova atendimento a uma NBR publicada.

## Exemplos e cobertura

As tabelas operacionais, formulários, cenários de transferência/garra/SSM/compra e exemplos de falha nos módulos são **sínteses didáticas desta skill**. Não foram atribuídos indevidamente como casos reais dos autores. O caso Eaton é identificado como fonte de raciocínio e figuras, com reconstrução didática explicitamente separada. Não há código de comando de robô, parâmetros de instalação prontos ou reprodução integral de normas.

A skill preserva os principais métodos e decisões do acervo, sem pretender reproduzir cada cláusula, cada figura ou toda a tabela biomecânica. Para requisito exato, abra o original pelo caminho do manifesto e confirme edição, cláusula, página, notas e imagem.


## Fontes adicionais — curso de projeto e implantação

### S19 — 01 Collaborative Robot Safety Design & Deployment.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 545 palavras; sem paginação ou timestamps.
- **Cobertura:** ch01, ch11.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S20 — 02 Automation Accelerator Proof of Concept.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 27 linhas físicas; 369 palavras; sem paginação ou timestamps.
- **Cobertura:** ch10.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S21 — 03 Robot Classification Part 1.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 986 palavras; sem paginação ou timestamps.
- **Cobertura:** ch01, ch03, ch11.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S22 — 04 Robot Classification Part 2.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 947 palavras; sem paginação ou timestamps.
- **Cobertura:** ch01, ch11.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S23 — 05 Safety Training.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 905 palavras; sem paginação ou timestamps.
- **Cobertura:** ch02, ch03, ch06, ch14.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S24 — 06 Safety Standards.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 992 palavras; sem paginação ou timestamps.
- **Cobertura:** ch02, ch04, ch11, ch14.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S25 — 07 Risk Assessment Part 1.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 959 palavras; sem paginação ou timestamps.
- **Cobertura:** ch02, ch14.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S26 — 08 Risk Assessment Part 2.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 685 palavras; sem paginação ou timestamps.
- **Cobertura:** ch02, ch06.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S27 — 09 Accident Trigger.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 1170 palavras; sem paginação ou timestamps.
- **Cobertura:** ch12, ch14.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S28 — 10 Safety Lessons.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 718 palavras; sem paginação ou timestamps.
- **Cobertura:** ch12, ch14.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S29 — 11 Designing Safe Workcells - Part 1.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 934 palavras; sem paginação ou timestamps.
- **Cobertura:** ch03, ch07.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S30 — 12 Designing Safe Workcells - Part 2.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 74 linhas físicas; 930 palavras; sem paginação ou timestamps.
- **Cobertura:** ch03, ch04, ch05, ch07.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S31 — 13 Designing Safe Workcells - Part 3.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 594 palavras; sem paginação ou timestamps.
- **Cobertura:** ch04, ch07.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S32 — 14 Force-Limited Robots - Part 1.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 996 palavras; sem paginação ou timestamps.
- **Cobertura:** ch04, ch13.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S33 — 15 Force-Limited Robots - Part 2.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 1273 palavras; sem paginação ou timestamps.
- **Cobertura:** ch04, ch06, ch13.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S34 — 16 Force-Limited Robots - Part 3.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 768 palavras; sem paginação ou timestamps.
- **Cobertura:** ch04, ch09, ch10, ch13.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S35 — 17 Applications.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 1416 palavras; sem paginação ou timestamps.
- **Cobertura:** ch07, ch10.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S36 — 18 Machine Tending.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 77 linhas físicas; 997 palavras; sem paginação ou timestamps.
- **Cobertura:** ch07, ch09, ch10.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S37 — 19 Testing - Part 1.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 1 linhas físicas; 831 palavras; sem paginação ou timestamps.
- **Cobertura:** ch08, ch10, ch12, ch13.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

### S38 — 20 Testing - Part 2.txt

- **Natureza:** Transcrição de treinamento; contexto histórico com menção a 2018; gravação individual não datada.
- **Extensão/localização:** 90 linhas físicas; 1191 palavras; sem paginação ou timestamps.
- **Cobertura:** ch08, ch13.
- **Leitura:** Texto integral lido; sem vídeos, slides/tabelas citados ou timestamps; erros e ressalvas em curso-transcricoes.md.

