# 1. Objetivo

Documentar o processo FAQ QuintoAndar para pedido de reagendamento ou solicitacao de novas fotos pelo proprio proprietario.

# 2. Contexto

- Fonte de entrada: proprietario via formulario de autoatendimento (FAQ QuintoAndar).
- Quem trata: analistas CNX de FUP Fotos.
- O processo avalia elegibilidade para nova sessao gratuita e conduz agendamento, negativa, encaixe, abandono ou encaminhamento.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito (FAQ QuintoAndar)
- Zendesk
- Admin (Aba Imoveis e Aba Camera)
- Magic Link / CRM
- Discador Olos
- Appsheet (Support Photos)

## Canais

- Ligacao ativa e WhatsApp (Twillio)
- E-mail formal via Zendesk

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Proprietario abre pedido no FAQ QuintoAndar.
2. Ticket e gerado no Zendesk (Agendamento de Fotos - FUP [SO]).
3. Analista audita historico de fotos no Admin/Magic Link.
4. Analista decide elegibilidade da nova sessao gratuita.
5. Analista executa desfecho e encerra ticket.

## Fluxo detalhado (AS-IS)

1. Receber ticket de FAQ QuintoAndar.
2. Identificar solicitacao especifica do proprietario.
3. Validar historico de fotos e data da ultima sessao.
4. Decidir elegibilidade:
	- Elegivel: imovel sem fotos profissionais, reforma comprovada, ou ultima sessao acima de 6 meses.
	- Inelegivel: fotos recentes (menos de 6 meses) e de boa qualidade.
5. Se elegivel:
	- Realizar contato para negociar data/hora.
	- Desfechos possiveis: novo agendamento, encaixe/SOS, agendamento futuro, abandono.
6. Se inelegivel:
	- Enviar negativa formal com motivos tecnicos.
	- Orientar possibilidade de envio de ate 5 fotos proprias via app.
7. Registrar comentario interno no Magic Link e encerrar ticket no Zendesk.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Criar/receber Case com origem FAQ QuintoAndar.
2. Auditar elegibilidade no Admin/Magic Link.
3. Executar desfecho operacional de agendamento/negativa.
4. Registrar evidencias e encerrar Case.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto:
	- Receber caso originado em FAQ QuintoAndar.
2. Triagem:
	- Auditar criterios de gratuidade.
3. Execucao:
	- Realizar contato ativo e executar desfecho adequado.
4. Encerramento:
	- Registrar historico da tratativa.
	- Encerrar Case.

# 6. Regras de negocio

- A elegibilidade para nova sessao gratuita deve ser validada antes de qualquer agendamento.
- Quando inelegivel, deve haver comunicacao formal com motivo tecnico.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencia especifica de fila no AS-IS: Agendamento de Fotos - FUP [SO].
- Origem obrigatoria no Zendesk: FAQ QuintoAndar.

# 8. Pontos em aberto

- Criterio unificado de elegibilidade no consolidado (aparecem referencias de 6 meses e +90 dias).
- Definicao de fila TO-BE especifica para FAQ.

# 9. Backlog / oportunidades

- Padronizar criterio temporal de elegibilidade no fluxo FAQ.
- A definir.
