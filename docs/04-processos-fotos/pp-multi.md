# 1. Objetivo

Documentar o processo Agendamento/Reagendamentos PP Multi para suporte a agendamento de sessoes em multiplos imoveis de um PP Multi.

# 2. Contexto

- Fonte de entrada citada: preenchimento de Cognito por parceiro BPO e areas de atendimento.
- Quem trata: Analistas de FUP Fotos.
- Cenario de uso citado: sem agenda aos sabados ou impossibilidade de agendar em 4 dias.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms (referencia /256)
- Zendesk
- Salesforce (Omni Channel no TO-BE)
- Admin
- Google Sheets (planilha Dados FT)
- Google Maps

## Canais

- WhatsApp (Twillio)

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Receber solicitacao via Cognito.
2. Analisar codigos dos imoveis e informacoes de fotografo.
3. Buscar/contatar fotografo e validar agenda.
4. Agendar sessoes para os imoveis no Admin.
5. Registrar tratativa e encerrar ticket.

## Fluxo detalhado (AS-IS)

1. Time de Vendas (IS ou CIQ) ou BPO abre Cognito conforme cenario.
2. Ticket e aberto automaticamente no Zendesk.
3. Analista verifica se houve solicitacao de fotografo especifico.
4. Se houver fotografo especifico, realizar contato via WhatsApp para combinacao.
5. Validar se fotografo aceitou e se tem agenda para data combinada.
6. Se nao houver agenda, buscar fotografo com agenda mais livre.
7. Quando necessario, incluir regiao para fotografo, buscar bairro/municipio mais proximo e codigo de regiao na planilha Dados FT.
8. Agendar sessoes individualmente para cada imovel.
9. Registrar sucesso ou impossibilidade nas observacoes internas e encerrar ticket.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Criar Case no Salesforce com dados do Cognito.
2. Distribuir Cases via Omni Channel.
3. Executar analise de agenda, contato e agendamento no Admin.
4. Registrar observacoes internas e encerrar Case.

## Fluxo detalhado (TO-BE)

1. Criar/receber Case no Salesforce com distribuicao por Omni Channel.
2. Validar dados da solicitacao.
3. Executar contato com fotografo e checar disponibilidade.
4. Agendar no primeiro dia com agenda disponivel quando nao houver data acordada.
5. Registrar sucesso no agendamento em observacoes internas (Chatter Salesforce).
6. Encerrar Case.

# 6. Regras de negocio

- Fluxo cobre multiplos imoveis de um mesmo PP Multi.
- Pode haver solicitacao de fotografo especifico.
- Quando nao houver agenda viavel, buscar alternativas de fotografo/regiao.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Referencias especificas deste processo:
	- AS-IS: ticket aberto automaticamente via integracao (Zapier).
	- TO-BE: distribuicao via Omni Channel.

# 8. Pontos em aberto

- Confirmar se registrar ID do IM ou ID da sessao no sucesso.
- Definir regra unica de abertura por origem (Time de Vendas vs BPO).

# 9. Backlog / oportunidades

- Backlog explicito no material: esse fluxo deveria ser possivel via produto.
