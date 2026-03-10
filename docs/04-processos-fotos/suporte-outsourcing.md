# 1. Objetivo

Documentar o processo Suporte Outsourcing para tratativas tecnicas operacionais que parceiros externos nao conseguem concluir diretamente.

# 2. Contexto

- Fonte de entrada: Analistas BPO (Actionline | AeC) ou Time WH.
- Time tratador: FUP Fotos Interno.
- O processo cobre cancelamento/agendamento, correcao cadastral e fechamento manual de tarefa travada.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms (Suporte Outsourcing)
- Zendesk
- Salesforce
- Admin
- Magic Link / CRM Tarefas
- Twillio

## Canais

- Touch points via WhatsApp/E-mail quando faltam dados
- Macro/template de encerramento

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. BPO/WH preenche Cognito de Suporte Outsourcing.
2. Ticket e gerado em Agendamento de Fotos - FUP [SO] no Zendesk.
3. Analista valida dados e tipo de solicitacao.
4. Analista executa ajuste tecnico nos sistemas internos.
5. Analista registra historico e encerra ticket.

## Fluxo detalhado (AS-IS)

1. Receber ticket com dados obrigatorios (ID imovel, nome, e-mail, 3 primeiros digitos do CPF, motivo).
2. Validar seguranca e consistencia dos dados.
3. Decisao: dados permitem atuacao tecnica?
	- Nao: buscar dados corretos e realizar follow-up com solicitante.
	- Sim: seguir execucao.
4. Executar conforme necessidade:
	- Cancelamento/reagendamento no Admin (Aba Camera).
	- Alteracao/inclusao de informacoes cadastrais no Admin (Aba Imoveis).
	- Fechamento de tarefa travada no CRM/Magic Link.
5. Registrar comentario de tratativa no historico do imovel.
6. Finalizar ticket no Zendesk como Resolvido.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Criar/receber Case no Salesforce com dados do Cognito.
2. Validar dados e definir tipo de acao.
3. Executar tratativa no Admin/CRM/Magic Link.
4. Responder cliente e encerrar Case.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto:
	- Receber demanda via Cognito e criar/receber Case.
	- Analista acessa fila de Cases e revisa abertura.
2. Triagem e Coleta:
	- Verificar se dados estao completos.
	- Se incompleto, solicitar dados faltantes e mover para aguardando retorno.
3. Execucao:
	- Realizar acao tecnica requerida (agendamento, cancelamento, alteracao cadastral ou fechamento de tarefa).
4. Encerramento:
	- Responder por macro/template.
	- Encerrar Case.

# 6. Regras de negocio

- A acao executada depende do tipo de solicitacao informado no Cognito.
- Sem dados completos, nao executar alteracao sistemica.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencia de caixa AS-IS: Agendamento de Fotos - FUP [SO].
- Status adicional citado: Pending (aguardando retorno).

# 8. Pontos em aberto

- Definicao de SLA para fechamento automatico (registro no material como backlog).
- Criterio formal para validacao de seguranca e completude por tipo de solicitacao.

# 9. Backlog / oportunidades

- Definir SLA de fechamento automatico.
- Padronizar matriz de tipos de solicitacao com regras de execucao por sistema.
