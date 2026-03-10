# 1. Objetivo

Documentar o processo de Lockbox, com separacao clara entre AS-IS e TO-BE, foco em fluxo operacional, regras de negocio, status/filas e pontos em aberto.

# 2. Contexto

- O processo de Lockbox trata solicitacoes recebidas via Cognito para envio/acionamento de lockbox.
- No cenario atual, ha uso de Zendesk com apoio de Google Sheets e acionamento operacional de parceiro.
- No cenario TO-BE, ha registro de criacao/recebimento de Case no Salesforce para conduzir a tratativa.
- O processo preve solicitacao de complemento quando faltam informacoes e encerramento por sem retorno quando aplicavel.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito
- Zendesk
- Salesforce (Service Cloud)
- Google Sheets
- Admin

## Canais

- WhatsApp Business (acionamento do parceiro Go Roger)

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Receber solicitacao de Lockbox via Cognito com abertura de ticket no Zendesk.
2. Verificar solicitacao e validar se as informacoes estao completas.
3. Se incompleto, solicitar dados ao cliente e aguardar retorno.
4. Se completo, executar tratativa operacional e acionar envio.
5. Retornar cliente e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Inicio do processo com analista recebendo solicitacao.
2. Solicitação chega via Cognito; ticket e criado no Zendesk e planilha de controle e alimentada.
3. Analista verifica solicitacao de envio da lockbox.
4. Decisao: Informacoes completas?
	- Nao:
	  - Solicitar informacoes ao cliente (responder nos canais).
	  - Status de acompanhamento: Pending (aguardando retorno).
	  - Se cliente nao retornar, comunicar nao resposta por template e encerrar.
	- Sim:
	  - Preencher campos recebidos.
	  - Executar alteracao no Admin (quando aplicavel).
	  - Encaminhar solicitacao para parceiro (Go Roger) conforme operacao.
5. Analista retorna ao cliente informando que a solicitacao foi enviada.
6. Encerrar ticket/case.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber solicitacao via Cognito e criar/receber Case no Salesforce (Lockbox).
2. Triar solicitante, objetivo e elegibilidade.
3. Executar encaminhamento operacional/logistico e registrar evidencias.
4. Responder solicitante conforme resultado e encerrar.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto:
	- Receber solicitacao via Cognito.
	- Criar/receber Case no Salesforce.
	- Case cai na fila Lockbox - Pedidos da FAQ [SO].
	- Analista confere solicitante (PP, Vistoriador, Corretor, Fotografo, Consultor Imobiliario, Rede) e objetivo do pedido (ex.: Lockbox Code, entrega).
2. Triagem e Coleta de Dados:
	- Identificar se e pedido novo ou ajuste/pendencia de dados.
	- Validar dados minimos e elegibilidade:
	  - Imovel apartamento.
	  - Imovel desocupado.
	  - Portaria 24h ou diurna (se nao, inelegivel).
	- Checar duplicidade/pedido existente quando aplicavel.
	- Se faltar informacao, solicitar complemento e mover para Aguardando Cliente.
3. Execucao (Operacao/Logistica):
	- Registrar e encaminhar solicitacao conforme processo operacional.
	- Atualizar/consultar planilha de controle quando aplicavel.
	- Acionar parceiro (ex.: Go Roger) no canal definido (WhatsApp Business) e anexar evidencia/link no Case.
	- Atualizar status do envio/acionamento.
	- Se depender de retorno de parceiro/entrega, mover para Aguardando Time Interno.
4. Retorno e Encerramento:
	- Responder solicitante via macro/template:
	  - "Solicitacao enviada/acionada".
	  - "Inelegivel" com motivo.
	  - "Faltam dados".
	- Fechamento: Resolvido e depois Fechado.
	- Se nao houver retorno em Aguardando Cliente, comunicar sem retorno e encerrar conforme governanca.

# 6. Regras de negócio

- Reclassificacao de Tipo de Solicitacao e permitida a qualquer momento; ao reclassificar, o mesmo Case e transferido para a fila correta sem perda de historico.
- Se faltarem informacoes, deve haver solicitacao de complemento antes da execucao operacional.
- Sem retorno do solicitante, o fluxo pode ser encerrado com comunicacao de nao resposta.
- Elegibilidade Lockbox considera criterios minimos de tipo/condicao do imovel e portaria.
- Ajustes em pedido original nao sao mesclados apos fechamento: cliente deve abrir nova solicitacao e associacao entre tickets/cases e manual.

# 7. Status e filas

## Status mapeados

- Aberto
- Em Andamento
- Aguardando Time Interno
- Aguardando Cliente
- Resolvido
- Fechado
- Pending (aguardando retorno)

## Filas

- AS-IS (Zendesk): Grupo "Lockbox - Pedidos da FAQ"; Assunto "Solicitacao de Lockbox"
- TO-BE (Salesforce): Fila "Lockbox - Pedidos da FAQ [SO]"; Divisao "Logistica de Lockbox"

# 8. Pontos em aberto

- Seguir com envio de informacoes via WhatsApp para parceiro (registro: on hold para validacao).
- Tempo medio de encerramento em horas uteis.
- Viabilidade de entrada unica de formulario para processos (unificacao de forms) em momento futuro.

# 9. Backlog / oportunidades

- Avaliar unificacao de formularios de entrada em etapa futura.
- Formalizar decisao operacional sobre canal de acionamento do parceiro.
- A definir
