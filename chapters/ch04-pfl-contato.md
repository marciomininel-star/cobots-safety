# 04 — PFL, contatos e limites biomecânicos

## Ideia central

PFL exige controlar as consequências dos contatos previsíveis do sistema completo. Comece por geometria, partes do corpo e aprisionamentos; somente então selecione limites e planeje a comprovação.

## Fontes e precisão

S03, 5.5.5, pp. PDF 21–25; 7.6, p. PDF 26; Anexo A, pp. PDF 27–38. S01, pp. PDF 25–33; S02, pp. PDF 37–39 e 57–59. O Anexo A é **informativo** e não é uma tabela universal de “forças seguras”. A síntese não reproduz a tabela completa nem substitui sua leitura com as notas.

## Estruturas de julgamento

### Classificação do contato

| Condição | Classe relevante | Consequência para o projeto |
|---|---|---|
| Corpo atingido pode recuar livremente | Transiente/dinâmico | Massa efetiva, velocidade relativa e energia importam |
| Corpo preso entre partes ou contra obstáculo | Quase estático | Força/pressão sustentada, parada e possibilidade de retirada importam |
| Uma mesma trajetória permite ambas | Dois cenários | Avalie os dois, não escolha apenas o mais favorável |
| Superfície cortante, perfurante ou cisalhante | Perigo adicional | Redesenhe/proteja; não trate como contato rombo apenas |

Quase estático não significa “devagar”; transiente não significa “pico de força baixo”. Uma colisão inicial pode evoluir para aprisionamento. S03 exige considerar contato com ferramenta e peça, além do braço. A massa efetiva depende do ponto de contato e da postura; não use apenas a carga útil nominal como substituto da inércia do sistema.

### Sequência PFL

1. Mapeie todos os contatos intencionais, incidentais e decorrentes de falhas relevantes, incluindo uso indevido previsível.
2. Associe cada contato à região corporal específica e à geometria/superfície que pode atingi-la.
3. Identifique aprisionamento, possibilidade de saída, direção, postura, frequência e duração.
4. Elimine arestas e pontos de esmagamento; aumente área de contato; reduza massa/energia; use materiais complacentes quando adequados.
5. Determine critérios aplicáveis de força **e** pressão e eventuais limitações ergonômicas mais restritivas.
6. Selecione funções ativas e limites com base no cenário; confira sua validade em todas as trajetórias e configurações relevantes.
7. Planeje medições representativas com aparato e critérios adequados; documente resultados, incerteza e configuração.
8. Caso a redução seja insuficiente, altere projeto, método ou proteção. Reavalie após mudanças.

**Por que funciona:** separa o perigo físico da facilidade de configurar um menu. **Falha típica:** ajustar “força = X” e supor que X seja a força máxima em todos os contatos, independentemente do ponto, eixo, postura e ferramenta.

## Força, pressão e energia

- **Força F**, em N: ação mecânica resultante no contato; não descreve sozinha a distribuição local.
- **Pressão p**, em N/cm² ou outra unidade explícita: depende da distribuição e área. Uma área pequena pode produzir pressão alta.
- **Energia cinética**, proporcional a massa e quadrado da velocidade: ajuda a explicar por que reduzir velocidade pode reduzir impacto, mas não comprova ausência de compressão sustentada.
- **Massa efetiva:** representação da inércia no ponto/direção do contato; depende do sistema e da configuração.
- **Limite biomecânico:** critério relacionado ao corpo e ao tipo de contato; não é automaticamente um limite de torque ou potência no controlador.

Para uma demonstração de pressão média, `p_média = F/A`. Não use esse quociente como substituto de pressão de pico em uma superfície irregular. Não derive uma velocidade admissível só de `E = 1/2 m v²` sem o modelo de contato e suas hipóteses.

## Como consultar o Anexo A de 2016

O anexo organiza áreas específicas em regiões corporais, apresenta limites e notas de pesquisa e discute modelos para estimar energia/velocidade. Leia as notas juntamente com a linha e o tipo de contato.

Na p. PDF 29, o texto diz que a presença de dados de face/crânio/testa não autoriza contato nessas áreas. Não use esses números para aprovar impactos na cabeça. A cláusula 5.5.5.3 também trata prevenção de exposição de regiões sensíveis. O conjunto de dados não representa todas as pessoas nem prova adequação de contatos repetitivos; a própria fonte observa limites ergonômicos potencialmente mais baixos.

Não generalize o multiplicador transiente para todas as linhas: há campos não aplicáveis e condições. Pressão e força têm escalas, unidades e abrangências diferentes. Valores copiados de uma silhueta em slide não mantêm essas notas.

## Exemplo trabalhado — garra junto à bancada

**Exemplo didático, sem valores normativos:** a garra conduz uma peça leve perto de uma bancada. Uma pessoa pode apoiar a mão na borda.

**Cenário A:** garra toca antebraço em região aberta com recuo livre. Classificação preliminar: transiente, sujeita a confirmar trajetória e postura. **Cenário B:** dedos ficam entre peça e bancada. Classificação: quase estático, ainda que a peça seja leve e o movimento lento.

**Intervenção preferida:** deslocar a trajetória e redesenhar o dispositivo para eliminar o vão de aprisionamento, sem introduzir novo acesso perigoso. Depois avaliar superfícies, velocidade, funções limitadoras e contatos residuais.

**Demonstração dimensional:** uma força hipotética de 60 N distribuída uniformemente em 6 cm² produz média de 10 N/cm²; em 0,6 cm², produz 100 N/cm². Esses valores **não são limites de aceitação**. A mesma força pode concentrar pressão local muito diferente.

**Plano de evidência:** registrar ponto/direção, corpo representado, rigidez/complacência do aparato, ferramenta/peça, postura e velocidade; medir força e pressão conforme método competente; comparar aos critérios aplicáveis com suas notas e incertezas. Se o cenário B continuar possível e não houver retirada segura, a detecção de colisão não encerra o risco.

## Ampliação do curso — dinâmica além da carga nominal

S32/S33 destacam energia cinética, torque aplicado pelo motor e distância disponível para desacelerar. Ferramenta, elos e inércia refletida da transmissão participam do contato; a peça leve não basta para concluir baixa força. O [ch13](ch13-dinamica-inercia-e-controle.md) desenvolve o raciocínio e um exemplo com unidades.

S30/S31 sugerem diferenciar transferência aberta de aproximação final ao gabarito. Desenvolva trajetória, geometria e limites para a região de pinçamento; não copie afastamentos/percentuais dos exemplos. Um limite comum de receita não equivale a uma função monitorada de segurança.

Os valores de 150 N, 75 N/mm e velocidades de 1–2 m/s usados no curso não são limites universais. Revestimento e complacência podem ajudar, mas exigem avaliação de força, pressão, durabilidade e contato. As demonstrações humanas de S30/S33/S34 não são um método de validação.

## Antipadrões

- Ensaiar impacto em uma pessoa para “sentir se dói”.
- Aplicar o maior valor da tabela a todo o corpo.
- Medir uma trajetória e extrapolar para toda a aplicação.
- Usar espuma como justificativa sem avaliar envelhecimento, geometria e condição real.
- Tratar luva ou EPI como correção universal de contato perigoso.
- Esquecer perda da peça, arestas, calor ou ferramentas ativas.

## Decisões a reter

1. Aprisionamento muda a análise mesmo em baixa velocidade.
2. Controle força e pressão, com as condições do contato.
3. Elimine contatos perigosos antes de buscar um número permissivo.
4. Ajuste do controlador, cálculo e medição são evidências distintas.

## Conexões

Ch02 para risco; ch05 para alternativa sem contato; ch07 para geometria; ch08 para validação; matriz de contato nos [modelos](../references/modelos-praticos.md).
