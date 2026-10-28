# Decisões rápidas — Cobots_Safety

| Se observar… | Faça… | Porque… |
|---|---|---|
| “É cobot, então é seguro” | Liste tarefa, peça, EOAT e ambiente | Segurança depende da aplicação |
| Pessoa só precisa interagir com sistema parado | Avalie SRMS/SMS e presença/retomada | Movimento simultâneo pode ser desnecessário |
| Movimento simultâneo sem contato | Avalie SSM e espaço de parada | A pessoa avança durante reação e frenagem |
| Contato previsível | Mapeie PFL por corpo, superfície e cenário | Não existe força única para toda situação |
| Aprisionamento possível | Elimine a geometria ou controle o cenário quase estático | Baixa velocidade não garante saída |
| Ferramenta/peça afiada, quente ou ativa | Trate perigo específico e proteção | Limitar força do braço não elimina esse perigo |
| Só há certificado do braço | Solicite evidência da célula e funções integradas | Componentes não representam toda a aplicação |
| Sensor ligado a I/O comum | Verifique a cadeia e o desempenho declarado | Coordenação de processo não equivale a proteção |
| Programa pausado para desobstrução | Defina estado/controle de energias da intervenção | Pausa pode permitir retomada inesperada |
| Novo EOAT, peça, carga, trajetória ou local | Avalie impacto e revalide o afetado | Contatos, parada e acesso podem mudar |
| Peça leve e impacto alto | Investigue inércia refletida e torque ativo | Carga nominal não descreve toda a dinâmica |
| Vídeo com mãos/criança como teste | Solicite ensaio instrumentado e condições | Demonstração humana não valida segurança |
| PoC bem-sucedida | Registre seu escopo e valide a célula final | Prova de processo não cobre toda integração |
| Fonte se diz “projeto/minuta” | Use para estudo, não para comprovar obrigação | Publicação final não está demonstrada |

## Escolha por necessidade

1. Pode eliminar a interação perigosa pelo projeto? Priorize essa mudança.
2. A interação é com sistema parado? Investigue SRMS/SMS.
3. A pessoa precisa comandar movimento? Investigue HG.
4. Pessoas e sistema se movem, com separação possível? Investigue SSM.
5. Contato continua previsível? Investigue PFL; se geometria/limites não forem adequados, altere projeto ou proteção.
6. Há fases diferentes? Combine métodos e valide transições; não deixe lacunas de proteção.

## Checagens numéricas que evitam erros

| Situação | Regra de decisão |
|---|---|
| SSM da edição 2016 | `Sp = Sh+Sr+Ss+C+Zd+Zr`; nenhuma parcela sem origem |
| Tempo SSM | Reação Tr e frenagem Ts são diferentes; humano avança durante ambos |
| Velocidade humana 1,6 m/s | Referência condicionada da fonte; confirme norma/aplicação, não universalize |
| Velocidade TCP | Confira cotovelo, peça e todos os pontos perigosos |
| Força e área | Pressão média `F/A` não comprova pico local |
| Anexo A de 15066:2016 | Leia notas, corpo e contato; não extrapole multiplicador a toda linha |
| PL d/cat. 3 em fonte antiga | Confira função, método e edição; categoria não é PL |

## Sinais de que a decisão ainda está aberta

- Só há ensaio vazio, sem configuração relevante.
- Ninguém sabe a versão ou identificador da configuração testada.
- Reset/retorno de energia não foram avaliados.
- Presença e pontos cegos não tratados.
- Proposta não inclui proteção, integração e validação.
- Valor de contato veio de uma silhueta ou transcrição sem notas/tabela.
- A regra usa 150 N, 75 N/mm ou velocidade de vídeo como valor universal.
- A conclusão cita a minuta de 2017 ou o projeto 12100 como publicação final.

**Saída prática:** decisão provisória + motivo + medidas prioritárias + evidência faltante + critério de aceitação. Valores didáticos não são configurações aprovadas.
