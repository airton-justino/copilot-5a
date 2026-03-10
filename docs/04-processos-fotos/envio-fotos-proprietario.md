# 1. Objetivo

Documentar o processo Envio de fotos proprietario (FotosPP - Piloto LQ <> FUP) como contingencia de publicacao quando nao ha sessao de fotografo viavel.

# 2. Contexto

- Aplicavel quando ha barreiras para receber fotografo (ex.: localizacao, viagem, atrito com cancelamentos).
- Fonte de entrada citada: formulario de pre-registro e/ou Cognito FotosPP.
- Quem trata: Analistas de FUP Fotos.

# 3. Sistemas e canais envolvidos

## Sistemas

- Google Forms (Pre Registro - Fotos PP)
- Google Sheets (Planilha de Controle de Fotos PP)
- Cognito Forms (FotosPP - Piloto LQ <> FUP, referencia /503)
- Admin / MagicLink
- Zendesk
- Salesforce

## Canais

- WhatsApp (Twillio)

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Time solicitante registra caso no pre-registro.
2. FUP recebe dados e contata proprietario por WhatsApp.
3. Proprietario envia fotos.
4. Analista avalia criterios de aceite/reprova.
5. Se aprovado, faz upload, legendagem e republicacao.
6. Registrar historico em ticket e encerrar.

## Fluxo detalhado (AS-IS)

1. Identificar dados do proprietario e ID do imovel na planilha de controle.
2. Validar premissas basicas do imovel (residencial, regiao atendida, sem conflito de sessao ativa).
3. Solicitar fotos ao proprietario via Twillio (orientacao de quantidade e formato).
4. Regra de prazo: proprietario tem ate 2 dias para envio.
5. Avaliar fotos recebidas:
	- Criterios de aceite: pequenas avarias/bagunca leve podem ser aceitas.
	- Criterios de reprova: mofo/infiltracao excessiva, fiacao exposta, bagunca de mudanca severa, buracos, marcas d'agua de outras imobiliarias.
	- Formato: JPG/JPEG e largura minima de 1152px.
6. Se aprovado:
	- Subir fotos no Admin/MagicLink na ordem de comodos.
	- Legendar, definir capa e republicar anuncio.
	- Marcar tarefa de Agendar Job como feita no CRM.
7. Registrar no Cognito FotosPP para historico e finalizar ticket Zendesk.
8. Se reprovado ou sem retorno em 2 dias:
	- Comunicar impedimento/encerramento ao proprietario via WhatsApp.
	- Encerrar tratativa.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber solicitacao via Cognito e criar Case no Salesforce.
2. Validar dados e fotos enviadas.
3. Executar publicacao no Admin/MagicLink quando aprovado.
4. Encerrar Case.

## Fluxo detalhado (TO-BE)

1. Criar Case no Salesforce com dados do Cognito.
2. Validar enquadramento e qualidade das imagens.
3. Executar upload/publicacao quando aprovado.
4. Encerrar Case com registro historico.

# 6. Regras de negocio

- Processo e contingencia, nao fluxo padrao de sessao fotografica.
- Ha tipos de envio: Primeiro Envio, Reenvio de Ajuste e Complemento.
- Sem resposta do proprietario em 2 dias, contato deve ser encerrado.
- Reclassificacao de tipo de solicitacao pode ocorrer sem perda de historico.

# 7. Status e filas

- Status e filas transversais: consultar docs/05-regras-negocio/status-sla-filas.md.
- Status adicionais citados no processo: Em Espera e Pendente.
- Referencia de fila citada: Listing Quality [FOTOS] [SO] para historico.

# 8. Pontos em aberto

- Estrategia de canais do fluxo (validacao pendente).
- Confirmacao de fluxo unico de entrada (Google Forms vs Cognito).

# 9. Backlog / oportunidades

- Backlog explicito: preencher todas as informacoes no Cognito, sem dividir entre Cognito e Salesforce.
