# 14 — Prevenção e aprendizado com incidentes

## Ideia central

Use incidentes como fontes de cenários para antecipar falhas de interação, integração e energias. Classificar o dano ajuda a investigar; a decisão de projeto exige identificar a cadeia de condições que permitiu a exposição.

## Fontes e precisão

S23, *Safety Training*; S25/S26, *Risk Assessment*; S27, *Accident Trigger*; S28, *Safety Lessons*. São transcrições de curso, sem relatórios oficiais dos acidentes anexados. Os casos abaixo reconstroem de forma concisa o relato da aula; datas, atribuições e conclusões formais não foram verificadas em investigação primária. Não atribua à aula o valor de requisito legal atual.

## Estruturas introduzidas

### Pirâmide 3E

O curso denomina **3E** a sequência **Elimination, Engineering controls, Enterprise controls**:

1. **Elimination:** retirar o perigo do projeto/processo.
2. **Engineering controls:** controlar o acesso ou o perigo por soluções de engenharia.
3. **Enterprise controls:** organizar a forma de trabalhar, procedimentos, restrições e capacitação.

Use a pirâmide para comparar a robustez de medidas propostas. Ela é uma formulação didática do curso, não uma substituição literal da estratégia em três passos da ISO 12100. Não confunda “Enterprise controls” com segurança funcional ou trate programação comum como proteção apenas porque a aula a chama controle de engenharia.

**Por que funciona:** ajuda a questionar uma resposta baseada só em avisos. **Falha típica:** culpar a pessoa por entrar numa região em que a tarefa previsível exigia acesso, sem investigar layout e energias.

### Tipos de acidente versus fontes de falha

| Classificação didática de S27 | Cenário a procurar | Fontes a investigar |
|---|---|---|
| Impacto/colisão | Movimento atinge pessoa | Mudança inesperada, comando, controle e acesso |
| Esmagamento/aprisionamento | Corpo entre partes ou contra estrutura | Trajetória, layout, saída e presença |
| Falha mecânica | Peça/ferramenta/transmissão falha ou se solta | Retenção, fixação, desgaste e manutenção |
| Outros perigos | Choque, fluido, incêndio, tropeço etc. | Energias, ambiente, utilidades e organização |

Não trate essas quatro classes como lista completa ou mutuamente exclusiva. Uma falha mecânica pode causar impacto e depois aprisionamento. A classe descreve o mecanismo de dano; não é, sozinha, causa raiz.

### Da lição ao requisito verificável

1. Descreva tarefa, pessoas e estado do sistema antes do evento.
2. Identifique o movimento/energia e a forma de exposição.
3. Separe fato narrado, hipótese e informação ausente.
4. Investigue controles, acessos, falhas, fontes de energia e layout conjuntamente.
5. Proponha medidas pela prioridade 3E/hierarquia aplicável.
6. Converta cada medida em requisito e método de comprovação.
7. Revise cenários semelhantes na célula atual e reavalie riscos.

O exercício não deve afirmar que uma única medida teria certamente impedido um acidente sem evidência suficiente. Ele serve para antecipar mecanismos semelhantes e testar a suficiência do projeto.

## Exemplo trabalhado 1 — manutenção de uma parte, energia em outra

**Relato da aula:** uma pessoa se aproxima de uma manutenção em transportador; um sensor ainda energizado pode disparar uma plataforma robotizada, criando esmagamento. A parada do transportador não representava controle de todas as energias e movimentos do conjunto.

**Aprendizado transferível:** a fronteira da intervenção não coincide necessariamente com a máquina parada. Identifique sensores, PLCs, atuadores, máquinas associadas e energias armazenadas que ainda podem produzir movimento. Inclua quem acompanha ou observa a manutenção.

| Ação proposta | Nível de decisão | Evidência a desenvolver |
|---|---|---|
| Evitar necessidade de observar de posição perigosa | Projeto/eliminação da exposição | Acesso e tarefa revistos |
| Controlar energias do sistema pertinente à intervenção | Engenharia/procedimento de isolamento apropriado | Diagrama e verificação do estado seguro |
| Proteger acesso de terceiros | Engenharia e organização | Proteções/acessos e responsabilidade claros |
| Capacitar e verificar execução | Organização | Procedimentos e comprovação por tarefa |

Uma placa “manutenção” ou uma parada parcial não demonstra por si só o estado seguro da célula.

## Exemplo trabalhado 2 — busca de ferramenta após preparação

**Relato da aula:** após troca de molde numa injetora, uma pessoa procura ferramentas, alcança a região superior e fica entre o robô de pórtico e sua estrutura. Um ciclo do robô produz esmagamento.

**Perguntas de projeto:** a busca por ferramenta e inspeção pós-setup foram previstas? O acesso por cima foi tratado? A proteção da injetora cobria o robô e sua estrutura? A pessoa podia intervir com as energias/movimentos ainda disponíveis?

**Saída didática:** incluir a inspeção pós-setup como tarefa; oferecer método de verificação/retirada fora da zona perigosa quando possível; controlar o acesso e as fontes de movimento; definir sequência de retorno. Validar também a entrada por cima, não só pela porta de produção.

Esses casos sustentam o raciocínio “sistema completo + tarefa real”. Não são provas de que uma configuração específica de grade, PL ou isolamento atende automaticamente a uma instalação diferente.

## Usar a equipe sem terceirizar o julgamento

S25 destaca integrador, instaladores, engenharia, operadores e demais interessados. Reúna experiências de produção e manutenção: falhas pequenas e intervenções frequentes mostram usos que um desenho não revela. Registre divergências e dados faltantes.

A “aceitação de risco pela empresa” mencionada no curso não permite contrariar obrigações aplicáveis nem substituir evidência técnica. O facilitador ajuda a estruturar a análise; não transforma consenso em conformidade.

## Antipadrões

- Atribuir a causa apenas ao “erro humano”.
- Copiar uma ação do caso sem conferir o mecanismo de dano local.
- Considerar parada do robô como isolamento de todo o sistema.
- Não analisar observadores, terceiros ou acesso por cima.
- Classificar acidente e encerrar a investigação sem medidas verificáveis.

## Decisões a reter

1. Use o relato para gerar cenários, não para certificar fatos históricos não verificados.
2. Investigue integrações, energias e acesso, além do componente que se moveu.
3. Prefira eliminar a exposição e usar engenharia antes de depender só de instruções.
4. Transforme lições em tarefas, requisitos e testes rastreáveis.

## Conexões

Ch02 para apreciação; ch07 para acessos; ch08 para testes; ch12 para intervenção e energias. [Ressalvas do curso](../references/curso-transcricoes.md).
