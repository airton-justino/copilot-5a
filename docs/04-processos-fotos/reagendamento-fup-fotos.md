# 1. Objetivo

Documentar o processo de Solicitacoes de Reagendamento - FUP Fotos, com foco funcional em recuperacao de agenda, tratamento operacional e encerramento da demanda.

# 2. Contexto

- Fluxo de entrada interna para recuperar agenda quando o agendamento original foi quebrado por motivo interno ou falha do parceiro fotografo.
- Fonte de entrada registrada: Time Interno QuintoAndar.
- Time tratador registrado: CNX Fup Fotos.
- Objetivo operacional registrado: contato ativo com o proprietario para reagendar preferencialmente em D+2 e evitar imovel parado no funil.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms (formulario: Solicitacoes de Reagendamento - FUP Fotos)
- Zendesk
- Admin (Aba Camera/Planner)
- CRM/Magic Link
- Discador Olos (campanha WEBHELP_REAGENDAMENTO)
- Twillio
- Appsheet (Support Photos) - quando houver necessidade de encaixe/SOS

## Canais

- Contato ativo com proprietario via discador/canal telefonico
- Comunicacao de FUP via template no Zendesk

Ponto em aberto:
- Validar estrategia de canais (registro existente: "Lari: validar estrategia de canais").

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Time interno preenche Cognito de Solicitacoes de Reagendamento - FUP Fotos.
2. Ticket e gerado automaticamente no Zendesk (caixa Agendamento de Fotos - FUP [SO]).
3. Analista valida motivo do reagendamento e status atual do job no Admin.
4. Analista executa contato ativo com proprietario e conduz desfecho.
5. Analista registra historico da tratativa e encerra ticket.

## Fluxo detalhado (AS-IS)

1. Receber solicitacao via Cognito/Time interno.
2. Abrir ticket na caixa Agendamento de Fotos - FUP [SO] no Zendesk.
3. Validar motivo do reagendamento (ex.: fechamento de agenda, descredenciamento, funil, imprevisto).
4. No Admin, buscar job ativo do imovel e verificar se ainda consta como Agendado (barra amarela).
5. Se job anterior estiver Agendado, cancelar/deletar para liberar agenda com motivo correto.
6. Realizar contato ativo com proprietario.
7. Conduzir o desfecho principal do processo:
	- Novo agendamento (agenda disponivel):
	  - Sondar endereco/chaves/acompanhante.
	  - Agendar novo job no Admin (Planner), com prioridade D+2 quando aplicavel.
	- Solicitacao de encaixe (sem agenda/urgencia):
	  - Acionar Appsheet (Support Photos) para alocacao manual.
	  - Informar SLA de retorno quando aplicavel.
	- Inalcancavel:
	  - Executar tentativas de contato e enviar FUP via template no Zendesk.
	- Abandono de cadastro (desistencia):
	  - Cancelar job/cadastro e registrar motivo.
8. Registrar resumo da tratativa no CRM/Magic Link.
9. No Zendesk:
	- Confirmar formulario de Agendamento de Fotos FUP.
	- Selecionar origem Solicitacoes de Reagendamento - FUP Fotos.
	- Aplicar macro de fechamento adequada ao desfecho.
	- Alterar status para Resolvido e enviar.
10. Finalizar tabulacao da chamada no discador.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Case entra via Cognito e cai em fila de atendimento (Omni/Queue).
2. Analista classifica tipo de tratativa e valida completude dos dados.
3. Analista executa reagendamento/encaixe/abandono conforme regra.
4. Analista registra comunicacao e evidencias, resolve e fecha o Case.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto (Aberto):
	- Receber case via Cognito (Solicitacoes de Reagendamento - FUP Fotos).
	- Analista assume owner e confere: ID do imovel, motivo, dados do PP e observacoes.
	- Definir tipo de tratativa dentro do fluxo:
	  - Novo agendamento.
	  - Encaixe/SOS.
	  - Abandono.
2. Triagem e Coleta (Em Andamento):
	- Validar se job existe e esta Agendado no Admin.
	- Validar se contato do PP esta utilizavel.
	- Validar se motivo do reagendamento esta claro.
	- Se faltarem dados do PP, mover para Aguardando Cliente.
3. Execucao (Em Andamento):
	- Operar no Admin para liberar agenda e reagendar quando aplicavel.
	- Realizar contato ativo conforme estrategia operacional.
	- Em caso de encaixe/SOS, acionar Appsheet e mover para Aguardando Time Interno quando depender de retorno.
	- Em caso de abandono, registrar cancelamento e motivo.
4. Retorno e Encerramento (Resolvido -> Fechado):
	- Registrar resumo da tratativa e evidencias necessarias.
	- Enviar comunicacao por template/macro.
	- Marcar Resolvido; Fechado ocorre conforme governanca.
	- Se houver contestacao/retorno, reabrir e retomar tratamento.

Observacao de fronteira de escopo:
- Quando o caso for classificado como Agendamento/Reagendamento Futuro (>9 dias), FotosPP ou Suporte Outsourcing, o tratamento deve ser encaminhado para o fluxo especifico correspondente.

# 6. Regras de negócio

- Origem do processo: Time interno via Cognito de Solicitacoes de Reagendamento - FUP Fotos.
- Reclassificacao de Tipo de Solicitacao e permitida; ao reclassificar, o mesmo case e transferido para a fila correta sem perda de historico.
- Antes de novo agendamento, o job anterior deve ser validado e, se necessario, cancelado para liberar agenda.
- Reagendamento deve priorizar D+2 quando houver disponibilidade operacional.
- Contato ativo com o proprietario e etapa obrigatoria para definicao de desfecho.
- Encerramento requer registro de historico da tratativa e comunicacao ao proprietario.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencias especificas deste processo:
	- AS-IS: Agendamento de Fotos - FUP [SO].
	- TO-BE: Omni/Queue (nome especifico da fila: A definir).

# 8. Pontos em aberto

- Estrategia de canais (registro: "Lari: validar estrategia de canais").
- Regra consolidada de quantidade de tentativas de contato (no material aparece 3 tentativas e tambem ate 15 tentativas em contextos distintos).
- Definicao final do nome da fila TO-BE em Salesforce (Omni/Queue detalhada).

# 9. Backlog / oportunidades

- A definir.
