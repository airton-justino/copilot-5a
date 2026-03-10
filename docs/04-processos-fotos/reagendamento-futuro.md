# 1. Objetivo

Documentar o processo Agendamento/Reagendamentos Futuros para gestao de casos em que o proprietario so pode receber fotografo apos 9 dias.

# 2. Contexto

- Fonte de entrada: Time WH (WebHelp) via atendimento ativo/receptivo.
- Quem trata: Analistas de FUP Fotos.
- Uso principal: quando data desejada esta fora do horizonte do Planner (10+ dias).

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms (referencia /444)
- Zendesk
- Salesforce
- CRM Tarefas / MagicLink
- Admin (Aba Camera)
- Discador Olos (WEBHELP_REAGENDAMENTO)
- Appsheet (Support Photos)

## Canais

- Contato telefonico ativo (Twillio/Discador)
- Macro/template de retorno

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Registrar solicitacao futura via Cognito.
2. Aplicar Snooze/adiamento para pausar mailing.
3. Reabrir ticket na data programada (D-2).
4. Confirmar data com proprietario e executar desfecho.
5. Registrar e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Proprietario informa indisponibilidade para proximos 9 dias.
2. Analista preenche Cognito Agendamento/Reagendamentos Futuros.
3. Ticket e direcionado para fila na data programada.
4. Aplicar Snooze da tarefa no CRM/MagicLink para D-2.
5. Na reabertura, realizar 3 tentativas de contato para confirmar horario.
6. Desfechos possiveis:
	- Novo agendamento no Admin.
	- Novo reagendamento futuro (novo Snooze).
	- Abandono de cadastro.
	- Solicitacao de encaixe/SOS via Appsheet, quando necessario.
7. Registrar comentario no CRM/MagicLink e finalizar ticket no Zendesk.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber solicitacao via Cognito e criar/receber Case no Salesforce.
2. Validar campos minimos e data de reabertura D-2.
3. Manter case em espera ate reabertura.
4. Em D-2, executar contato e desfecho no Admin.
5. Encerrar Case.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto:
	- Criar/receber Case no Salesforce.
	- Conferir ID imovel, e-mail PP, 3 digitos CPF, datas/horarios, data D-2.
2. Triagem:
	- Validar coerencia de datas.
	- Solicitar complemento se faltarem dados.
3. Execucao:
	- Aplicar Snooze para pausar mailing ate D-2.
	- Mover para Aguardando Time Interno durante espera.
	- Em D-2, realizar 3 tentativas de contato.
	- Executar novo agendamento, novo reagendamento futuro ou abandono.
4. Encerramento:
	- Registrar resumo.
	- Responder PP por macro/template.
	- Encerrar Case.

# 6. Regras de negocio

- Processo aplicavel para horizonte acima de 9 dias.
- Data de reabertura do ticket/case deve ser D-2 da data acordada.
- Durante espera, tarefa deve permanecer fora do mailing ativo.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencia de origem no Zendesk: Agendamento/Reagendamentos Futuros.

# 8. Pontos em aberto

- Definicao final de automacao de transferencia de ticket para outras filas.
- Regra de continuidade quando PP nao atende apos 3 tentativas (confirmacao formal).

# 9. Backlog / oportunidades

- Backlog explicito: transferir ticket automaticamente para outras filas.
