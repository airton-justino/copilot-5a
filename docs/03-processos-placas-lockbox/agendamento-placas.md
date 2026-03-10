# 1. Objetivo

Documentar o processo de Agendamento de Placas, diferenciando AS-IS e TO-BE, com foco em fluxo operacional, regras de negocio, status/filas e oportunidades de evolucao.

# 2. Contexto

- O processo inicia com extracao de base de agendamento e contato ativo com clientes elegiveis para oferta de instalacao de placa.
- No AS-IS, a operacao utiliza planilha intermediaria com o time de Tools para geracao de ticket no Zendesk.
- No TO-BE, ha indicacao de carga via Salesforce para geracao automatica de Case.
- O processo possui decisao operacional explicita: "Cliente quer instalar placa?".

# 3. Sistemas e canais envolvidos

## Sistemas

- Metabase
- Google Sheets
- Omnie
- Cognito
- Zendesk
- Salesforce

## Canais

- WhatsApp em massa (disparo via Omnie)

Ponto em aberto:
- Validar estrategia de canais (registro existente: "Lari: validar estrategia de canais").

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Extrair base de agendamento no Metabase.
2. Preparar base no Google Sheets e encaminhar para Tools.
3. Gerar ticket automaticamente no Zendesk.
4. Realizar disparo de contato para oferta de placa.
5. Se cliente quiser instalar placa, acionar parceiro e preencher formulario do ticket.
6. Responder cliente e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Analista abre pagina do Metabase e faz download da query de agendamento.
2. Analista abre Google Sheets e insere os dados extraidos do Metabase.
3. Analista retira clientes elegiveis B2B por formula.
4. Analista copia clientes restantes para planilha oficial de Tools.
5. Tools sobe automaticamente os dados para o Zendesk, gerando ticket.
6. Analista copia telefones dos clientes elegiveis no Google Sheets.
7. Analista sobe os contatos na plataforma Omnie e faz disparo de macro ofertando a placa.
8. Ponto de decisao: cliente quer instalar placa?
	 - Sim: analista confere cidade do imovel e aciona parceiro correto:
		 - Sao Paulo, RJ e Campinas: preencher Cognito do parceiro Promove.
		 - Belo Horizonte: preencher formulario do parceiro JV.
	 - Nao: A definir (nao detalhado no material).
9. Analista preenche formulario do ticket no Zendesk e conclui tratativa.
10. Retorno ao cliente com template/macro e encerramento.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Extrair base de agendamento.
2. Carregar dados no Salesforce para geracao automatica de Case.
3. Realizar contato para oferta de placa.
4. Se cliente quiser instalar, acionar parceiro.
5. Preencher formulario do Case no Salesforce e encerrar.

## Fluxo detalhado (TO-BE)

1. Analista faz download da query de agendamento.
2. Analista faz upload dos leads para encaminhar WhatsApp em massa para captacao.
3. Dados sao carregados no Salesforce para geracao automatica de Case (com permissao de usuarios a definir).
4. Ponto de decisao: cliente quer instalar placa?
	 - Sim: analista faz solicitacao para parceiro via Cognito.
	 - Nao: A definir (nao detalhado no material).
5. Analista preenche o formulario do Case no Salesforce.
6. Encerrar o Case.

# 6. Regras de negocio

- Elegibilidade B2B e tratada na etapa de preparacao de base (retirada via formula no AS-IS).
- A solicitacao ao parceiro varia por cidade:
	- Sao Paulo, RJ e Campinas: parceiro Promove.
	- Belo Horizonte: parceiro JV.
- O agente pode reclassificar o Tipo de Solicitacao a qualquer momento; ao reclassificar, o mesmo Case e transferido automaticamente para a fila correta, sem perda de historico.
- No TO-BE, a geracao automatica de Case por carga em Salesforce depende de permissao de usuarios.

# 7. Status e filas

## Status mapeados

- Aberto
- Em Andamento
- Aguardando Time Interno
- Aguardando Cliente
- Resolvido
- Fechado

## Filas

- AS-IS (Zendesk): Grupo "CNX Plaquinhas"; Assunto "Agendamento Plaquinhas CNX"
- TO-BE (Salesforce): Divisao "Agendamento Instalacao de Placas"

# 8. Pontos em aberto

- Estrategia de canais (registro: "Lari: validar estrategia de canais").
- No TO-BE, definicao dos usuarios com permissao para carga que gera Cases automaticamente no Salesforce.
- Confirmacao sobre eliminacao da limitacao de carga em batches de 100.
- Definicao do comportamento quando cliente nao quer instalar placa.
- Viabilidade de manter processo end-to-end (solicitacao + retorno da empresa) no mesmo ticket/case, condicionada a avaliacao de API.

# 9. Backlog / oportunidades

- Integracao com Twilio (registro explicito como backlog).
- Migrar query do Metabase e retirar clientes B2B direto na consulta (registro como backlog).
- Oportunidades de automacao adicionais mapeadas e registradas como backlog no material.
