# 1. Objetivo

Documentar o processo de Atualizacao de dados cadastrais de fotografo/parceiro.

# 2. Contexto

- Entrada via Cognito em trilha de duvidas/solicitacoes de contrato de parceria.
- Fluxo contempla alteracoes de dados comuns, CNPJ e demais ajustes cadastrais.
- Ha referencia AS-IS e TO-BE no consolidado.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito
- Zendesk
- Salesforce
- Admin
- Google Sheets (planilha OPS)
- DocSign
- Jira

## Canais

- Retorno ao solicitante por macro/template

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Receber solicitacao via Cognito.
2. Validar informacoes e tipo de alteracao.
3. Executar alteracao no Admin e sistemas de apoio.
4. Retornar ao solicitante e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Fotografo preenche Cognito de Atualizacao cadastral.
2. Ticket e criado automaticamente no Zendesk.
3. Analista valida se informacoes estao completas.
4. Se incompleto, solicitar complemento e aguardar retorno.
5. Se completo, executar por tipo:
	- Dados comuns (e-mail/telefone): atualizar planilha OPS e cadastro no Admin.
	- Alteracao de CNPJ: consultar OPS, atualizar cadastro, preparar documentos no DocSign, abrir solicitacao no Jira quando aplicavel.
6. Registrar tratativa no Zendesk e enviar como Resolvido.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Criar/receber Case no Salesforce com dados do Cognito.
2. Validar completude e tipo de alteracao.
3. Executar alteracao no Admin e sistemas correlatos.
4. Responder e encerrar Case.

## Fluxo detalhado (TO-BE)

1. Receber solicitacao no Salesforce.
2. Verificar solicitacao e decidir se dados estao completos.
3. Se incompleto, solicitar dados ao cliente e mover para aguardando retorno.
4. Se completo, preencher campos recebidos e executar alteracoes.
5. Encerrar Case com evidencias da tratativa.

# 6. Regras de negocio

- Campo aberto pode conter solicitacao variada e triagem e feita pelo analista.
- Sem informacoes completas, a tratativa nao deve ser executada.
- Alteracoes documentais (ex.: CNPJ) podem demandar DocSign e Jira.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Status adicional citado no fluxo: Pending (aguardando retorno).

# 8. Pontos em aberto

- Criterio formal de informacoes completas em campo aberto.
- Padrao de categorizacao para solicitacoes fora dos tipos mais comuns.

# 9. Backlog / oportunidades

- Padronizar tipologias de alteracao no formulario para reduzir campo aberto.
- A definir.
