# 1. Objetivo

Documentar o processo de Reclamacao Imovel fora do padrao, desde a entrada da solicitacao ate o encerramento com registro de procedencia.

# 2. Contexto

- Fluxo acionado por fotografo parceiro via Cognito.
- Objetivo da tratativa: avaliar se a reclamacao e procedente com base em evidencias e sessao agendada.
- Ha cenario AS-IS em Zendesk e registro de TO-BE com Case no Salesforce.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms (referencia de formulario: /218)
- Zendesk
- Admin
- MagicLink
- Salesforce (Service Cloud)

## Canais

- Macro/template de resposta ao solicitante

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Receber solicitacao via Cognito com abertura automatica de ticket no Zendesk.
2. Avaliar evidencias e procedencia da queixa.
3. Verificar no Admin se houve sessao agendada para o fotografo.
4. Registrar resultado no formulario e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Recebimento do ticket na caixa Zendesk.
2. Avaliar evidencias enviadas pelo fotografo.
3. Decisao: imovel de fato fora do padrao?
	- Nao: registrar como demanda indevida ou improcedente e encerrar.
	- Sim: seguir para validacao de sessao.
4. Buscar ID do imovel no Admin e avaliar se havia sessao agendada para o fotografo.
5. Preencher campo de registro [AQ] Aprovado? com resultado procedente/improcedente.
6. Encerrar ticket com evidencias.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber Case via Cognito no Salesforce.
2. Validar dados minimos e evidencias.
3. Executar verificacao de sessao agendada no Admin/MagicLink.
4. Registrar decisao e evidencias, resolver e fechar.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto:
	- Receber Case via Cognito.
	- Confirmar tipo de solicitacao.
	- Direcionar para Em Andamento ou Aguardando Cliente se faltarem dados.
2. Triagem e Coleta:
	- Avaliar evidencias do fotografo.
	- Decidir se e fora do padrao.
3. Execucao:
	- Consultar Admin/MagicLink: ID do imovel e sessao agendada.
	- Decidir houve sessao (Sim/Nao).
	- Registrar [AQ] Aprovado? (Procedente/Improcedente).
4. Encerramento:
	- Responder com macro.
	- Registrar decisao e evidencias.
	- Resolver e fechar Case.

# 6. Regras de negocio

- A avaliacao de procedencia depende de evidencias e validacao de sessao agendada.
- Campo [AQ] Aprovado? deve refletir a decisao final.
- O agente pode reclassificar o Tipo de Solicitacao a qualquer momento sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Status adicionais especificos deste processo: A definir.
- Fila especifica deste processo no TO-BE: A definir.

# 8. Pontos em aberto

- Regra de impacto em Payments quando caso for procedente.
- Criterio formal de evidencia minima para classificar fora do padrao.
- Definicao de fila TO-BE dedicada.

# 9. Backlog / oportunidades

- Integracao/automacao de disparo para Payments quando aplicavel.
- A definir.
