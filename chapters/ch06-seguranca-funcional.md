# 06 — Funções de segurança e sistemas de controle

## Ideia central

Especifique a função de segurança completa antes de escolher componentes. Um sensor certificado, um PLC de segurança ou um braço com funções integradas não comprovam, isoladamente, o desempenho do sistema integrado.

## Fontes e precisão

S07, 5.4–5.8 e 5.12, especialmente pp. PDF 18–26; S08, 5.2–5.3 e 5.9, pp. PDF 19–24 e 36–38; S03, 5.2–5.4, pp. PDF 12–13; S02, pp. PDF 52 e 57. As referências de PL/categoria/SIL abaixo são das edições históricas fornecidas.

## Estrutura de uma função

Descreva evento disparador, perigos controlados, estado seguro, tempo de resposta, condições/modos, desempenho requerido, interfaces, reação a defeitos e condições para rearme/partida.

**Exemplo de redação específica:** “A entrada de uma pessoa no campo de proteção da estação deve levar o braço e o posicionador ao estado seguro especificado antes de a pessoa alcançar os perigos; a permanência deve ser detectada conforme a solução; a retomada deve obedecer à sequência definida e impedir partida inesperada.” Valores e categoria de parada precisam ser preenchidos pelo projeto, não inferidos da frase.

### Cadeia de segurança

`detecção → avaliação/lógica → comunicação → elemento de saída/acionamento → comportamento físico`

Verifique a cadeia e a interface com outras máquinas. Duas entradas de segurança ligadas incorretamente podem perder diagnóstico; um contato de saída pode não retirar o perigo esperado; a parada do robô pode deixar a ferramenta girando ou o posicionador ativo.

## Categoria, PL e SIL

| Conceito | O que expressa | Não confundir com |
|---|---|---|
| Categoria arquitetural | Estrutura e comportamento perante defeitos em um método de projeto | Nível completo de desempenho |
| PL | Nível de desempenho segundo a família ISO 13849 | Quantidade de canais ou selo de componente |
| SIL | Nível de integridade segundo o método aplicável | Conversão automática de PL por semelhança nominal |
| Desempenho requerido | Meta da função para a aplicação | Capacidade máxima declarada de um produto |
| Validação | Evidência de que requisitos e medidas foram atendidos | Apenas cálculo probabilístico ou teste funcional simples |

S08, 5.2.2, estabelece na edição 2018 uma referência a PL d/estrutura categoria 3 ou SIL 2 com condições específicas. A cláusula 5.2.3 trata outros critérios mediante apreciação abrangente e documentação. Essa possibilidade não é uma licença para baixar o desempenho sem justificativa. Também não significa que qualquer “Cat. 3” alcance PL d: método, confiabilidade, diagnósticos, falhas de causa comum e implementação precisam ser considerados conforme a norma aplicável.

## Paradas e energias

Identifique a finalidade antes de especificar a categoria de parada: proteção, emergência, parada operacional ou manutenção/isolamento. As categorias 0, 1 e 2 tratam do modo de parar e do tratamento da energia dos acionamentos; não são uma escala simples de segurança maior/menor.

Parada monitorada pode manter energia. Uma parada de emergência não é o método principal para permitir acesso rotineiro, nem garante sozinha que energia armazenada foi dissipada. Para manutenção, avalie isolamento e controle de energias, retenção de cargas, gravidade, pneumática, hidráulica, capacitores e energias do processo.

A perda de energia pode criar queda de peça; restaurá-la pode produzir movimento inesperado. Especifique ambos os eventos. Rearmar um dispositivo de emergência ou proteção não deve ser confundido automaticamente com emitir uma ordem de partida; confira as condições e exceções da aplicação/edição.

## Sequência para integrar

1. Converta perigos em requisitos de funções, com IDs rastreáveis.
2. Determine desempenho requerido e critérios de aceitação por função.
3. Escolha arquitetura/componentes com dados, instruções e limites de uso.
4. Verifique interfaces de sinais, diagnóstico, tempos, alimentação, comunicação e estados em falha.
5. Analise se funções internas do robô cobrem a peça, EOAT e máquinas associadas.
6. Proteja ajustes de segurança de alteração não autorizada ou acidental e registre identificador da configuração.
7. Faça verificação de projeto e validação, com análise documental e ensaios pertinentes.

**Por que funciona:** liga o componente ao comportamento físico que evita o dano. **Falha típica:** desenhar a rede comum de produção e depois presumir que os comandos “stop” enviados pelo PLC comum são suficientes para proteger pessoas.

## Exemplo trabalhado — célula com posicionador

**Cenário didático:** uma cortina detecta acesso à área onde um robô solda uma peça em um posicionador. O robô para, mas o posicionador e o arco continuam.

**Diagnóstico:** a função foi definida como “parar robô”, quando o perigo era o conjunto de movimentos e processo. O certificado do controlador do robô não cobre essa lacuna de especificação.

**Correção de engenharia a desenvolver:** identificar as zonas e todas as fontes de dano; definir o estado seguro do robô, posicionador, fonte de solda e demais interfaces; especificar a cadeia e o desempenho de cada função; determinar tempos e acesso; testar o resultado integrado.

**Registro de teste:** condição inicial, ingresso simulado com dispositivo apropriado, comportamento esperado de cada elemento, tempo medido, falhas analisadas, rearme e configuração. Um ensaio em que apenas o robô ficou imóvel deve ser marcado insuficiente para o perigo combinado.

## Ampliação do curso — algoritmo de torque não é integridade comprovada

S33 explica combinação de torque calculado por modelo e correção de erro para reduzir torque aplicado no contato. O mecanismo é útil para entender o comportamento, mas um algoritmo funcional de detecção/limitação não comprova o PL ou SIL da função. Confira independência, diagnóstico, falhas, tempos e comportamento físico conforme o projeto e a edição aplicável; veja ch13.

S23/S26 simplificam escalas de PL e sugerem equivalências diretas com classes de risco. Não as adote: duas vias ou uma lâmpada não demonstram, isoladamente, nível de desempenho. Também não transfira exigências citadas em exemplos médicos para o campo industrial sem uma base apropriada.

## Antipadrões

- Equiparar Ethernet comum a comunicação de segurança.
- Usar detecção de colisão operacional como função de proteção sem declaração/validação.
- Copiar PL de um sensor para a função inteira.
- Neutralizar intertravamento para terminar o ciclo sem outro método projetado.
- Alterar parâmetros sem registrar configuração e impacto.

## Decisões a reter

1. Defina o estado físico seguro e quem precisa parar.
2. Trate desempenho e tempo da cadeia inteira.
3. Use os dados e instruções da versão/modelo real.
4. Valide também falhas, energias e retomadas.

## Conexões

Ch03 para transições; ch05 para tempos SSM; ch07 para interfaces; ch08 para validação. Ficha de função nos [modelos](../references/modelos-praticos.md).
