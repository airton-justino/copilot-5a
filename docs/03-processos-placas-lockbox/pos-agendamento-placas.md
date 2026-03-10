# 1. Objetivo

Documentar o processo de Pos Agendamento de Placas, focado no retorno do parceiro apos solicitacao de instalacao.

# 2. Contexto

- Processo ocorre apos o Agendamento de Placas.
- O parceiro informa se a colocacao da placa foi realizada ou nao.
- Existem referencias AS-IS e TO-BE no consolidado.

# 3. Sistemas e canais envolvidos

## Sistemas

- Zendesk
- Salesforce
- Cognito
- API do parceiro (Promove)

## Canais

- Retorno via Cognito (JV)
- Retorno por API/e-mail (Promove)

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Analista recebe retorno da empresa parceira.
2. Analista verifica completude das informacoes no ticket.
3. Analista preenche formulario do ticket de acordo com parceiro.
4. Encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Retorno de parceiro chega no Zendesk.
2. Decisao operacional por parceiro:
	 - JV: resposta via Cognito (preenchimento automatico).
	 - Promove: retorno via API/e-mail (preenchimento manual pelo analista).
3. Analista acessa ticket e preenche formulario lateral.
4. Registrar resultado: placa instalada ou nao instalada.
5. Encerrar ticket.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Retorno de parceiro gera/atualiza Case no Salesforce.
2. Analista confere completude de dados.
3. Analista preenche formulario do Case e finaliza.

## Fluxo detalhado (TO-BE)

1. Receber retorno da empresa.
2. Abrir Case no Salesforce.
3. Preencher formulario conforme retorno do parceiro.
4. Encerrar Case.

# 6. Regras de negocio

- O time parceiro informa se a colocacao da placa foi realizada ou nao.
- Para JV, preenchimento pode ser automatico via Cognito.
- Para Promove, preenchimento e manual enquanto automacao nao estiver definida.
- No caso de nao instalacao, ha registro de que parceiro ainda recebe pagamento.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencias de fila/divisao no material:
	- Grupo Zendesk: CNX Plaquinhas.
	- Assunto: Agendamento Plaquinhas CNX.
	- Divisao Salesforce: Agendamento Instalacao de Placas.

# 8. Pontos em aberto

- Retornar diretamente no ticket/case original (analise de API).
- Definicao de fases de encerramento por tipo de resolucao.
- Criterio formal de informacoes completas.

# 9. Backlog / oportunidades

- Gatilhar novo ticket linkado ao principal ou priorizar no Metabase para casos especificos.
- Automatizar tratativas da Promove via API.
