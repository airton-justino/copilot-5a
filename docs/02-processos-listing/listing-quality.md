# 1. Objetivo

Documentar o processo de Listing Quality no contexto de substituicao do Zendesk por Salesforce, com visao funcional do fluxo operacional, regras de negocio, status/filas e oportunidades de evolucao.

# 2. Contexto

- Processo com inicio em extracao de base de listings para analise de qualidade.
- O processo possui cenarios AS-IS e TO-BE mapeados no material fonte.
- No AS-IS, ha uso de Metabase, Google Sheets e Zendesk com automacoes para distribuicao em fluxos.
- No TO-BE, ha indicacao de criacao de Case no Salesforce com roteamento por fluxo e execucao operacional no Magic Link.
- A estrategia de canais esta registrada como validacao pendente.

# 3. Sistemas e canais envolvidos

## Sistemas

- Metabase
- Google Sheets
- Zendesk
- Magic Link
- Databricks (fonte de dados)
- Hightouch (Sync #1 e Sync #2)
- Salesforce (Service Cloud)
- Listing Quality API
- Backoffice BFF

## Canais

- A definir

Ponto em aberto:
- Validar estrategia de canais (registro existente: "Lari: validar estrategia de canais").

# 4. Fluxo AS-IS

## Macro fluxo (AS-IS)

1. Extracao de listings no Metabase.
2. Input da base no Google Sheets e execucao de automacoes.
3. Classificacao por IA e distribuicao em Fluxo 0, Fluxo 1, Fluxo 2 e Fluxo 3.
4. Tratativa operacional em Zendesk e Magic Link conforme fluxo.
5. Encerramento do ticket.

## Fluxo detalhado (AS-IS)

1. Rodar base de listings no Metabase com listings criados ate as 18h do dia anterior (origens citadas: CIQ, proprietario ou fotografo).
2. Inputar a base no Google Sheets e rodar automacao de analise de IA.
3. Rodar segunda automacao no mesmo Google Sheets para criar tickets no Zendesk e dividir os fluxos:
	- Fluxo 0: BPO analisa 10% dos listings que nao passaram na IA.
	- Fluxo 1: listings que passaram na IA, mas exigem "olhar humano" para possivel reprovacao.
	- Fluxo 2: listings com deteccao de QR Code para checagem de placa.
	- Fluxo 3: IA aprovou; ticket sobe fechado para historico/contabilizacao.
4. Executar tratativa por fluxo:
	- Fluxo 0: abrir fotos no Magic Link, organizar ordem, inserir/corrigir legendas quando necessario, checar descricao, assistir video (comodos e audio), preencher formulario e encerrar.
	- Fluxo 1: abrir fotos no Magic Link, checar estado do imovel com enfase no ponto sinalizado pela IA, checar descricao, inserir/corrigir legendas quando necessario, assistir video, preencher formulario e encerrar.
	- Fluxo 2: abrir foto com codigo da placa, registrar codigo no formulario, inserir observacao interna com print quando aplicavel, encerrar.
	- Fluxo 3: sem tratativa humana; encerramento automatico para historico/contabilizacao.
5. Em casos de reprovacao com despublicacao no AS-IS:
	- Despublicar listing no Magic Link.
	- Baixar fotos via zip no admin (quando necessario para volume).
	- Salvar fotos no drive do listing.
	- Excluir fotos no admin para evitar publicacao.
6. Registrar impossibilidade de colocacao de placa quando aplicavel.

# 5. Fluxo TO-BE

## Macro fluxo (TO-BE)

1. Extracao de dados no Databricks com sincronizacoes Hightouch.
2. Criacao de Case no Salesforce com roteamento por score/listing.
3. Analise operacional no Magic Link com formulario pre-preenchido.
4. Persistencia de classificacao final em Listing Quality.
5. Encerramento no Salesforce e emissao de evento para Partner Payments quando elegivel.

## Fluxo detalhado (TO-BE)

1. Hightouch Sync #1 consulta Databricks e grava/atualiza registros no dominio Listing Quality (campos iniciais).
2. Hightouch Sync #2 consulta Databricks, calcula listingId + score e cria Case no Salesforce.
3. Salesforce roteia/prioriza Cases para analistas (pre e pos-analise).
4. Analista executa revisao no Magic Link e preenche formulario com apoio dos dados pre-preenchidos de Listing Quality.
5. Backoffice BFF integra com Listing Quality API para salvar atualizacao e finalClassification.
6. Excecao de auditoria: anexos e justificativa via comentario no Case do Salesforce.
7. Regra de evento para Partner Payments:
	- finalClassification = published ou unpublished: emite evento.
	- finalClassification = under_review: nao emite evento.
8. Encerrar Case no Salesforce conforme resultado da analise.

# 6. Regras de negocio

- A IA e o principal mecanismo de triagem inicial dos listings.
- Fluxo 0 deve considerar amostragem de 10% dos listings que nao passaram na IA.
- Fluxo 1 trata casos com sinalizacao de necessidade de analise humana.
- Fluxo 2 trata exclusivamente verificacao de QR Code/placa.
- Fluxo 3 representa aprovacao pela IA sem necessidade de tratativa humana.
- O agente pode reclassificar o Tipo de Solicitacao a qualquer momento; ao reclassificar, o mesmo Case e transferido automaticamente para a fila correta, sem perda de historico.
- Quando houver necessidade de despublicacao, a tratativa deve registrar evidencias e executar os passos operacionais previstos.
- No TO-BE, emissao de evento para Partner Payments depende de finalClassification.

# 7. Status e filas

## Status mapeados

- Aberto
- Em Andamento
- Aguardando Time Interno
- Aguardando Cliente
- Resolvido
- Fechado

## Filas

- AS-IS (Zendesk): A definir
- TO-BE (Salesforce): roteamento por listingId + score (detalhamento de nomes de filas: A definir)

# 8. Pontos em aberto

- Estrategia de canais do processo (registro: "Lari: validar estrategia de canais").
- Detalhamento dos nomes das filas no Salesforce para cada fluxo.
- Definicao final sobre onde registrar observacoes internas de placa no TO-BE (obrigatorio ou opcional).
- Regras operacionais de encerramento por tipo de resultado (aprovado, reprovado, despublicado) no TO-BE.

# 9. Backlog / oportunidades

- Criar campo de observacoes internas (registro existente no fluxo).
- A definir
