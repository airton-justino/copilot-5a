# 1. Objetivo

Documentar o fluxo de Reclamação LQ e seus tipos de demanda no contexto de substituicao de ferramenta, com foco funcional em processo, regras de negocio, status/filas e pontos em aberto.

# 2. Contexto

- Reclamação LQ recebe demandas relacionadas a qualidade de anuncios/imoveis por formulario Cognito (referencia de form 220 no material).
- O fluxo contempla triagem de procedencia, classificacao do tipo de demanda, tratativa operacional em Admin/MagicLink e encerramento com evidencias.
- Existe registro de transicao de Zendesk para Salesforce para o mesmo processo.
- A estrategia de canais permanece pendente de validacao.

# 3. Sistemas e canais envolvidos

## Sistemas

- Cognito Forms
- Zendesk
- Salesforce (Service Cloud)
- Admin
- MagicLink
- Google Drive (Drive LQ)
- iCloud

## Canais

- A definir

Ponto em aberto:
- Validar estrategia de canais (registro existente: "Lari: validar estrategia de canais").

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Recebimento da solicitacao no Cognito com abertura automatica de ticket no Zendesk.
2. Triagem da demanda e validacao de informacoes/evidencias.
3. Tratativa no Admin/MagicLink conforme tipo de demanda.
4. Registro da decisao (devida/indevida, procedente/improcedente) e encerramento com evidencias.

## Fluxo detalhado (AS-IS)

1. Receber ticket da caixa Zendesk originado pelo Cognito.
2. Avaliar tipo da demanda e se ha dados suficientes para tratativa.
3. Se dados incompletos:
	- Solicitar complemento ao solicitante.
	- Mover para Aguardando Cliente.
4. Se dados completos:
	- Seguir para Em Andamento.
	- Confirmar ou reclassificar Tipo de Solicitacao (sem perda de historico).
5. Executar tratativa por tipo de demanda:
	- Imovel duplicado:
	  - Comparar ID correto x ID em duplicidade no Admin/MagicLink.
	  - Se duplicidade confirmada, deletar anuncio em duplicidade.
	  - Se nao confirmada, registrar como demanda indevida e encerrar.
	- Fotos erradas:
	  - Analisar evidencias enviadas no Cognito.
	  - Excluir fotos incorretas no Admin/MagicLink e registrar tratativa.
	- Fotos ruins:
	  - Analisar pedido/evidencias.
	  - Executar exclusao/ajuste no Admin/MagicLink conforme tratativa.
	- Incluir/Excluir fotos e videos 360:
	  - Analisar evidencias.
	  - Executar inclusao/exclusao no Admin/MagicLink.
	- Incluir fotos:
	  - Baixar fotos/videos (ex.: iCloud), salvar no Drive LQ quando necessario e fazer upload no anuncio.
	  - Validar se sistema aceitou fotos.
	  - Se nao aceitou, registrar imagem fora do padrao e encerrar.
	- Imovel despublicado:
	  - Analisar motivo da despublicacao no ticket/case original.
	  - Baixar imagens do imovel despublicado quando necessario.
	  - Corrigir anuncio e republicar no MagicLink, quando aplicavel.
	- Problemas Originals:
	  - Tratar como categoria generalista (sem regra especifica dedicada no material), executando tratativa equivalente quando aplicavel.
6. Registrar no ticket:
	- Decisao final da demanda.
	- Evidencias (link/anexo/print, quando aplicavel).
7. Encerrar ticket.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Receber demanda via Cognito e criar/receber Case no Salesforce.
2. Triar dados minimos e evidencias, com roteamento por status.
3. Executar tratativa no Admin/MagicLink conforme tipo de demanda.
4. Registrar resumo, tipo final e evidencias no Case.
5. Resolver e fechar o Case.

## Fluxo detalhado (TO-BE)

1. Entrada/Contexto (Aberto):
	- Receber demanda via Cognito (Reclamacao LQ / Qualidade de imoveis - form 220).
	- Criar/receber Case no Salesforce na fila Listing Quality [FOTOS] [SO].
	- Revisar tipo de demanda, ID do imovel, links e anexos.
	- Decidir se demanda e devida ou indevida.
2. Triagem e Coleta (Aberto -> Em Andamento):
	- Validar dados minimos por tipo de demanda.
	- Se incompleto, solicitar complemento e mover para Aguardando Cliente.
	- Se completo, mover para Em Andamento.
	- Reclassificar tipo de demanda quando necessario.
3. Execucao (Em Andamento):
	- Executar tratativas no Admin/MagicLink seguindo os mesmos tipos de demanda mapeados no AS-IS.
	- Quando depender de validacao de terceiro/sistema, mover para Aguardando Time Interno.
4. Retorno e Encerramento (Resolvido -> Fechado):
	- Registrar resumo da tratativa, tipo de demanda final e evidencias.
	- Responder com template/macro quando houver retorno ao solicitante.
	- Mover para Resolvido e depois Fechado.
	- Em caso de reabertura/contestacao, retornar para Em Andamento (ou Aguardando Cliente se faltarem dados).

# 6. Regras de negocio

- A demanda deve ser classificada como devida ou indevida na entrada.
- Informacoes minimas e evidencias sao obrigatorias para seguir tratativa.
- Sem informacoes minimas, o caso deve ir para Aguardando Cliente.
- Reclassificacao de Tipo de Solicitacao e permitida a qualquer momento.
- Ao reclassificar, o mesmo Case e transferido automaticamente para a fila correta, sem perda de historico.
- Imovel duplicado exige validacao de duplicidade antes de qualquer exclusao.
- Inclusao de fotos depende de validacao do sistema; quando rejeitado, registrar como imagem fora do padrao.
- Problemas Originals segue como categoria generalista enquanto nao houver regra especifica.

# 7. Status e filas

## Status mapeados

- Aberto
- Em Andamento
- Aguardando Time Interno
- Aguardando Cliente
- Resolvido
- Fechado

## Filas

- AS-IS: caixa/fila no Zendesk (nome especifico: A definir)
- TO-BE: Listing Quality [FOTOS] [SO] no Salesforce

# 8. Pontos em aberto

- Estrategia de canais (registro: "Lari: validar estrategia de canais").
- Definicao formal de criterios minimos por tipo de demanda para considerar "informacoes completas".
- Confirmacao de padrao de retorno ao solicitante (template/macro) por tipo de demanda.
- Regra especifica para categoria Problemas Originals (atualmente tratada como generalista).

# 9. Backlog / oportunidades

- Revisar opcoes de categoria no Cognito de Reclamação LQ (registro no material sobre necessidade de retirar duas opcoes).
- Avaliar necessidade de gatilho para Partner Payments em casos com impacto operacional/financeiro (registro de questionamento no material).
- A definir
