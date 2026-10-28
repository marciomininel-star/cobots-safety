# 01 — Aplicação, escopo e espaços

## Ideia central

A unidade de decisão de segurança é a aplicação robotizada ao longo do ciclo de vida. “Cobot” indica capacidades do equipamento; as condições de uso, a ferramenta e o processo determinam os perigos da instalação.

## Fontes e precisão

S01, pp. PDF 6–12 e 33–34; S03, cláusulas 3–4, pp. PDF 7–11; S08, 4.2–4.4, pp. PDF 14–18; S13, pp. PDF 5–15. I01–I04 e I12 são apoio visual, com ressalvas no catálogo. A organização e o exemplo abaixo são sínteses desta skill.

## Estruturas para decidir

### Sistema + tarefa + espaço

Use esta decomposição ao receber uma solicitação como “esse cobot pode operar sem grade?”:

1. Identifique o manipulador, controlador, versão de software e funções de segurança realmente disponíveis.
2. Acrescente EOAT, troca de ferramentas, peça, carga, dispositivos de fixação, máquinas e utilidades.
3. Descreva a tarefa de cada pessoa e os movimentos de cada equipamento por fase.
4. Delimite espaços tridimensionais e caminhos de acesso, inclusive por trás, por baixo e por cima.
5. Liste os perigos e identifique qual método protege cada interação.
6. Determine quais evidências faltam para aceitar a aplicação.

Isso funciona porque impede que uma característica isolada do braço esconda o perigo criado pela peça ou bancada. Falha típica: escolher a marca e depois procurar argumentos para dispensar proteções.

### Espaços têm funções diferentes

| Espaço | Pergunta que responde | Cuidado de projeto |
|---|---|---|
| Máximo | Até onde o sistema pode alcançar? | Inclua ferramenta e peça, não só flange |
| Restrito | Quais limites não serão ultrapassados? | Documente os meios limitadores e a parada |
| De operação | Onde o programa efetivamente trabalha? | Caminho programado não é, por si só, limite seguro |
| Protegido | Que área é definida pelas proteções de perímetro? | Acesso, aberturas e presença precisam ser tratados |
| Colaborativo | Onde a interação prevista ocorre? | Defina pessoas, tarefas e método válido em cada fase |

Não use uma captura de tela do percurso como prova do espaço restrito. As definições e traduções variam entre edições; cite a edição quando uma distinção sustentar um requisito.

## Conceitos essenciais

- **Robô:** manipulador e seu controle; a ferramenta/peça alteram a análise do sistema.
- **Sistema robotizado:** conjunto integrado para a aplicação, com interfaces e equipamentos relevantes.
- **Uso pretendido:** tarefa e condições especificadas pelo projeto.
- **Uso indevido razoavelmente previsível:** comportamento previsível, mesmo que não desejado, que precisa entrar na análise.
- **Interação espacial:** compartilhamento de espaço; não prova proteção suficiente.
- **Interação temporal:** ocupação simultânea ou alternada; muda a estratégia de proteção.
- **Perigo de processo:** fonte de dano própria da soldagem, corte, usinagem, calor etc.
- **Pessoa exposta:** inclui operador, preparador, mantenedor, limpeza, terceiros e pessoas próximas.

## Como interpretar os infográficos

As figuras de “coexistência → cooperação → colaboração” ajudam a descrever a tarefa, mas seus eixos não provam que um nível maior de colaboração seja intrinsecamente mais seguro. I04 usa esse tipo de progressão; traduza-a em perguntas sobre presença, movimento, contato e proteção.

I02 é um template incompleto: contém campos “Add text here”, erros e lacunas. Não use suas células como requisitos. I03 ressalta corretamente que a aplicação completa precisa ser apreciada, mas descrições de sensores e arquitetura são exemplos de produto. I12 mistura robótica industrial e mobilidade; a base normativa de um braço fixo não cobre automaticamente a plataforma móvel.

I01, I05 e I08 apresentam vantagens potenciais. Trate custo, flexibilidade e velocidade de implantação como hipóteses a verificar na aplicação, não como propriedades universais. I06/I10 contêm números de mercado e previsões históricas: não os apresente como estatísticas atuais.

## Exemplo trabalhado — transferência de peça

**Cenário didático:** um braço transfere uma chapa da mesa A para uma prensa, enquanto uma pessoa abastece a mesa.

**Leitura insuficiente:** “o braço tem limitação de força, logo a estação é colaborativa e não precisa de proteção”.

**Análise por sistema:** a chapa tem uma borda cortante; a garra pode aprisionar dedos; a prensa tem movimento independente; a mão pode permanecer no dispositivo após abastecer; o cotovelo do braço se aproxima de um pilar durante retorno.

**Decisões:** redesenhar/proteger a borda e os pontos de pinçamento; estabelecer uma estratégia segura para acesso à prensa; avaliar o envelope do braço e peça; especificar interface de segurança entre as máquinas; escolher método por fase. O abastecimento alternado pode favorecer parada monitorada, enquanto a transferência ocorre em espaço protegido. A escolha final depende de dados e validação, não do nome “cobot”.

**Artefato de saída:** desenho em planta e elevação, tabela de fases, inventário de componentes, acessos e perigos, mais lista de lacunas. Essa saída alimenta o ch02.

## Ampliação do curso — classificação sem extrapolação

S19/S21/S22 apresentam a evolução de braços industriais, SCARA, cartesianos, plataformas móveis e robôs de serviço. Use a classificação para perguntar por cinemática, alcance, energia, ambiente e interação; ela não é uma classificação de segurança. Um manipulador pequeno de alta velocidade pode ser perigoso, e carga nominal não define sozinha a consequência do contato.

As referências a 2018, capacidades e fabricantes pertencem ao contexto narrado. Exemplos cirúrgicos, transporte de pessoas ou mobilidade não tornam a ISO 10218 uma base suficiente para esses usos. O acervo desta skill continua centrado em aplicações industriais. As classes apresentadas ajudam a delimitar quando é necessária outra base técnica.

## Antipadrões

- **Certificado do braço como certificado da célula:** ignora interfaces, ferramentas e perigos introduzidos na integração.
- **Contato sempre desejável:** vários métodos colaborativos são construídos para evitar contato.
- **Manutenção fora do escopo:** deixa sem tratamento as tarefas que mais alteram os estados de proteção.
- **Confiar em “o operador sabe”:** não controla alcance, retorno de energia ou acesso de outra pessoa.

## Decisões a reter

1. Descreva tarefa e perigos antes de responder sobre grades.
2. Modele braço, EOAT e peça como fontes possíveis de contato.
3. Separe o espaço usado pelo programa do espaço limitado com função adequada.
4. Registre pressupostos de pessoas, acessos e modos.

## Conexões

Ch02 transforma o escopo em apreciação; ch03 seleciona métodos; ch07 desenvolve layout; ch11 trata edições e evidência documental.
