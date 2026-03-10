# 1. Objetivo

Documentar o processo de Logistica de Placas para solicitacao e acompanhamento de envio de placa.

# 2. Contexto

- Demanda de envio de placa via correios.
- Solicitacoes podem vir de proprietarios, fotografos e times internos.
- Fluxo com base em Cognito, Zendesk e Google Sheets.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito
- Zendesk
- Google Sheets
- Salesforce

## Canais

- Template/macro de retorno ao solicitante

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Receber solicitacao via Cognito.
2. Verificar se placa ja foi solicitada.
3. Se necessario, registrar solicitacao de envio.
4. Informar cliente e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Analista recebe solicitacao de placas no Zendesk.
2. Decisao: placa ja foi solicitada?
	 - Sim:
		 - Verificar status no Google Sheets.
		 - Informar cliente que placa esta a caminho ou entregue.
	 - Nao:
		 - Registrar solicitacao de envio no Google Sheets.
		 - Informar cliente que solicitacao foi enviada.
3. Encerrar ticket.
4. Observacao operacional: Cognito alimenta Google Sheets para execucao da solicitacao.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber solicitacao via Cognito.
2. Criar/receber Case no Salesforce.
3. Repetir verificacoes operacionais de status/envio.
4. Retornar cliente e encerrar Case.

## Fluxo detalhado (TO-BE)

1. Abertura de Case no Salesforce com dados do Cognito.
2. Verificar status da placa ou registrar nova solicitacao conforme regra.
3. Responder cliente com template/macro.
4. Encerrar Case.

# 6. Regras de negocio

- Solicitacao pode ser feita por proprietario, fotografo, ASP ou CIQ.
- Verificacao de status deve ocorrer antes de nova solicitacao.
- Cognito e usado como entrada operacional no AS-IS.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencias especificas do processo:
	- Grupo: Plaquinhas - Pedido da FAQ.
	- Assunto: Solicitar placa do QuintoAndar no imovel.
	- Divisao Salesforce: Logistica de Placas.

# 8. Pontos em aberto

- Analise de pros e contras Cognito vs formulario nativo Salesforce.
- Definicao de SLA de envio e rastreio da placa.

# 9. Backlog / oportunidades

- Revisao de modelo de entrada (Cognito vs formulario Salesforce).
- A definir.
