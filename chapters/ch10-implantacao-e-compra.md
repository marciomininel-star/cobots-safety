# 10 — Implantação, compra e escolha da primeira aplicação

## Ideia central

Escolha uma tarefa cujo processo, segurança, integração e resultado possam ser demonstrados. Compare soluções completas com critérios comuns; preço do braço e promessa de retorno rápido não representam o custo da célula.

## Fontes e precisão

S16, pp. PDF 3–13, Universal Robots; S17, pp. PDF 2–7; S18, pp. PDF 1–3, Lincoln Electric; S15, pp. PDF 8–16; S13, pp. PDF 10–11 e 16–20; I05, I08–I11. São em grande parte fontes técnicas de fornecedores e materiais comerciais, não estudos comparativos independentes ou cotações atuais.

## Os 10 passos da fonte S16

Preserve as dez dimensões como um roteiro de investigação, com interpretação crítica:

| Dimensão da fonte | Decisão de projeto/compra |
|---|---|
| 1. Taxa de transferência | Medir ciclo completo, variação, disponibilidade e gargalo |
| 2. Alcance e carga útil | Incluir EOAT, peça, centro de gravidade e condições do fabricante |
| 3. Peças e apresentação | Definir variação admissível e alimentação repetível |
| 4. Colaboração com humanos | Mapear tarefas, método e perigos reais |
| 5. Conectividade e integração | Especificar sinais de processo e funções de segurança |
| 6. Garras e efetores finais | Projetar retenção, fechamento, geometria e troca |
| 7. Montar e cercar | Definir base, localização e proteções pela apreciação |
| 8. Ambiente | Conferir condições ambientais e compatibilidade |
| 9. Programação e lógica | Incluir modos, recuperação e tratamento de falhas |
| 10. Necessidades futuras | Prever variantes sem prometer reutilização sem reavaliação |

A fonte cita alcances/cargas e práticas comerciais da época; não são limites gerais da tecnologia. A recomendação de simplificar apresentação de peças ajuda a reduzir complexidade de processo; não justifica omitir sensores necessários à segurança.

## As cinco perguntas de S17

“Preciso de automação?”, “Quais opções de robôs?”, “Posso pagar?”, “Quais processos automatizar?” e “Cobots são o melhor para minha empresa?” organizam a seleção. Use-as para comparar alternativas, incluindo melhoria do processo manual, automação dedicada, célula protegida e solução colaborativa.

Não aceite sem análise a separação comercial de custos em que o cobot aparece sem despesa de proteção/integração. Esses custos dependem da aplicação. Também não generalize promessas de payback em meses ou de funcionamento contínuo: disponibilidade, manutenção, mudanças e necessidade de pessoas alteram o resultado.

## Método para especificar uma compra

1. Registre produto, volumes/mix, turnos, ciclo, qualidade e problemas atuais com dados.
2. Escolha famílias de peças e variações representativas.
3. Faça estudo preliminar de segurança e integração para não omitir custos.
4. Defina prova de processo e critérios mensuráveis de aceitação.
5. Solicite propostas com limites de fornecimento explícitos: EOAT, dispositivos, proteções, exaustão quando aplicável, instalação, software, documentação, treinamento, suporte e manutenção.
6. Compare competência do integrador, explicação da solução e evidências, além do preço.
7. Planeje FAT/SAT, responsabilidades e tratamento de pendências.
8. Prepare operação e manutenção antes da transferência para produção.

**Por que funciona:** torna as propostas comparáveis. **Falha típica:** escolher o menor preço de hardware e descobrir que proteções, gabarito, treinamento e testes eram itens fora do escopo.

## Matriz de comparação

| Critério | Evidência a solicitar | Sinal de fragilidade |
|---|---|---|
| Capacidade de processo | Demonstração com variação real | Apenas vídeo de uma peça ideal |
| Segurança | Escopo de apreciação, funções e validação | “Cobot não precisa de segurança adicional” |
| Integração | Interfaces e estados de falha | “Ligamos no Ethernet” sem detalhamento |
| Qualidade | Critérios de produto e medição | Só tempo de ciclo |
| Operação | Recuperação, treinamento e manutenção | Dependência permanente de um programador externo |
| Custos | Investimento e custos recorrentes por item | Preço restrito ao braço |
| Suporte | Responsabilidades e capacidade de atendimento | Promessa comercial sem cobertura definida |

Pesos de avaliação devem refletir o projeto. A skill não estabelece uma pontuação universal de fornecedores.

## Exemplo trabalhado — retorno com segurança no orçamento

**Exemplo didático, em valores hipotéticos; não é cotação nem aconselhamento financeiro.** Investimento total de R$ 240 mil inclui robô, ferramenta, dispositivo, integração, proteção, validação e treinamento. Benefício líquido anual estimado de R$ 96 mil resulta de ganhos realizáveis menos custos recorrentes adicionais.

`payback simples = investimento / benefício líquido anual`

`240.000 / 96.000 = 2,5 anos`

Esse cálculo não considera valor do dinheiro no tempo, impostos ou risco e não é o mesmo que ROI. Se o benefício cair para R$ 60 mil/ano, o payback simples passa a 4 anos. Se não houver benefício líquido positivo, essa divisão não sustenta um prazo de retorno.

**Como usar:** desagregar hipóteses de disponibilidade, demanda, qualidade e mão de obra realocada; evitar contar o mesmo ganho em capacidade e economia de trabalho duas vezes. Não tratar capacidade adicional como receita certa sem demanda. Não retirar uma proteção necessária para tornar a conta favorável.

## Ampliação do curso — prova de conceito e automação parcial

S20 distingue **consultoria de seleção** de **prova de conceito (PoC)**. Quando a tecnologia para o processo é incerta, prove a hipótese antes do investimento principal. Defina peças/variações, pergunta técnica, critérios de qualidade e ciclo completo, recursos e resultado esperado. Registre o que foi e não foi demonstrado; PoC não substitui segurança, validação ou aceitação da célula final.

S34 apresenta **3D: dull, dangerous, dirty**, acrescentando **demanding** para exigência/ergonomia. Use-os para buscar candidatos e investigar trabalho residual, sem escolher automaticamente a tarefa mais perigosa como primeira implantação. S36 recomenda ganhos iniciais demonstráveis para desenvolver competência.

S35 descreve automação parcial com humanos nas tarefas complexas e robôs nas repetitivas. Isso pode evitar automatizar toda a linha de uma vez; cada interface e presença humana ainda precisa de projeto. No exemplo narrado, operações de 10 s podem ser divididas entre duas estações para acompanhar uma etapa de 5 s. Esse balanceamento idealizado não inclui falhas, transporte, disponibilidade e variabilidade: use como hipótese de capacidade, não garantia de throughput.

S37 sugere prever conectividade durante o projeto e desenvolver monitoramento de produção após estabilizar o processo. Dados de falhas recorrentes podem orientar melhorias a montante, mas analytics e rede comum não substituem funções de segurança. Não copie capacidades de peso, picks/min ou economia de espaço citadas como limites atuais da tecnologia.

## Antipadrões

- Escolher a primeira aplicação apenas por ser a mais perigosa ou a mais complexa.
- Usar estatísticas de mercado antigas para decidir viabilidade local.
- Comprar hardware antes de confirmar acesso, repetibilidade e fixação.
- Prometer substituição de trabalhadores sem definir trabalho residual e capacitação.
- Confundir prova de processo com validação de segurança.

## Decisões a reter

1. Prefira uma primeira aplicação com critérios claros e variação conhecida.
2. Inclua a célula completa e seu ciclo de vida no orçamento.
3. Exija evidência de processo e segurança do integrador.
4. Reavalie benefícios com hipóteses conservadoras e verificáveis.

## Conexões

Ch02 para escopo de segurança; ch07 para integração; ch08 para aceitação; ch09 para soldagem; ch12 para sustentação.
