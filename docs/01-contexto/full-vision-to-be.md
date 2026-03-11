# SUPPLY | FOTOS + LISTING QUALITY + PLACAS — FULL VISION TO-BE (EM DESENVOLVIMENTO)

## 1. Objetivo
Consolidar a visão funcional transversal TO-BE do escopo Supply no Salesforce (Case), cobrindo Fotos, Placas, Lockbox, Listing Quality e Suporte ao Fotógrafo, com padronização de fluxo, classificação e roteamento.

## 2. Escopo
- Sistema de registro: Salesforce (Case).
- Frentes cobertas:
	- Fotos: Suporte Outsourcing, Reagendamento/FAQ, Agendamento/Reagendamento Futuro, PP Multi, Envio PP Fotos.
	- Placas: Logística + Agendamento/Instalação.
	- Lockbox.
	- Listing Quality: IA, Reclamações de qualidade das fotos, Imóvel fora do padrão.
	- Suporte ao Fotógrafo.

## 3. Padrões globais
- Sistema de registro único: Salesforce (Case).
- Path (Status) único para todas as frentes, com especialização por Tipo de Solicitação e Subtipo.
- Fechamento em massa obrigatório para alto volume (List View + ação em massa), mantendo rastreabilidade (Owner, timestamps, motivo e evidência).
- Integrações externas podem criar Case automaticamente.
- Contingência: criação manual/importação quando integração estiver indisponível (quando aplicável).
- Reclassificação durante tratativa: o mesmo Case pode mudar Tipo/Subtipo e ser re-roteado sem perder histórico.
- Encerramento obrigatório com: Tipo/Subtipo final + Motivo de fechamento + Resumo + Evidência.

## 4. Path e fases do fluxo

| Ordem | Fase (Path) | Objetivo | Ações do analista | Critério para finalizar fase |
|---|---|---|---|---|
| 1 | Aberto | Case criado e roteado, com informação mínima | Validar dados, anexos/links e confirmar Tipo/Subtipo | Assumiu tratativa -> Em Andamento |
| 2 | Em Andamento | Execução ativa da tratativa | Executar ações (Admin/Magic Link/rotinas), registrar evidências e acionar áreas | Dependência interna -> Aguardando Time Interno; dependência do solicitante -> Aguardando Cliente; concluído -> Resolvido |
| 3 | Aguardando Time Interno | Pausa por dependência interna/sistema/parceiro | Abrir/acompanhar demanda interna e registrar IDs/status | Retorno recebido -> Em Andamento (ou Resolvido) |
| 4 | Aguardando Cliente | Pausa por dependência do solicitante | Solicitar dados mínimos e acompanhar retorno | Recebeu dados -> Em Andamento; sem retorno -> Resolvido (com comunicação) |
| 5 | Resolvido | Tratativa concluída e retorno registrado | Confirmar execução, comunicar e registrar resumo/evidência | Sem nova interação -> Fechado (automático após 72h, conforme governança) |
| 6 | Fechado | Encerramento final | N/A | Estado final |

## 5. Estratégia de Record Type, campos e roteamento

### Estratégia de Record Type
- Preferencial (padrão): 1 Record Type para todo o escopo (Supply | Fotos, LQ e Placas), com diferenciação por Tipo/Subtipo.
- Exceção (somente se necessário): 2 Record Types caso LQ IA exija segregação por integração/automação (exemplo citado: Listing Quality IA).

Ponto em aberto:
- Não há decisão final documentada sobre uso de 1 RT ou 2 RT no cenário LQ IA.

### Campos globais mínimos no Case (visão funcional)
- Tipo de Solicitação (picklist).
- Subtipo (picklist, quando aplicável).
- Origem (Cognito / Hightouch / Parceiro / Manual / Importação).
- HouseId__c (quando aplicável).
- Dados de contato (nome/e-mail/telefone, quando aplicável).
- Resumo da tratativa + evidências (anexos/links/prints).
- Motivo de fechamento (picklist).

### LQ IA (integração + objeto auxiliar)
- Objeto auxiliar: ListingQualityInbound__c.
- Campos no Case informados como já criados:
	- Case.HouseId__c
	- Case.AnalystQueue__c
- Roteamento: Flow pós-criação direciona Case com base em AnalystQueue__c = 0, 1, 2.

Ponto em aberto:
- Há referência incompleta no material de origem para campos do Case (trecho "Case.").
- O mapeamento explícito de AnalystQueue__c (0/1/2) para filas específicas não foi detalhado.

## 6. Filas

| Fila (Queue) | Uso |
|---|---|
| Suporte Outsourcing | Fotos: macro demandas da BPO (FUP e variações) |
| Solicitações de Reagendamento / FAQ | Fotos: reagendamento + entradas via FAQ |
| Solicitações de Agendamento/Reagendamento Futuro | Fotos: futuro (>9 dias) |
| Solicitações de Agendamento/Reagendamento PP Multi | Fotos: múltiplos imóveis / exceções |
| Envio PP Fotos | Fotos: envio/reenvio/complemento de fotos do proprietário |
| Agendamento Instalação de Placas | Placas: logística + agendamento/instalação |
| Solicitação de Lockbox | Lockbox: solicitações via Cognito/FAQ |
| LQ Qualidade de imóveis IA | Listing Quality IA: casos gerados por Hightouch/IA |
| LQ Reclamação qualidade das fotos | Listing Quality: reclamações via Cognito |
| LQ Imóvel fora do padrão | Listing Quality: report do fotógrafo via Cognito |
| Suporte Fotógrafo | Suporte ao Fotógrafo: Formulário de Parceiros |

Ponto em aberto:
- Há variação de nomenclatura no material: "Suporte Fotógrafo" e "Suporte Foto".

## 7. Fluxos TO-BE por fila

### 7.1 Suporte Outsourcing (Fila: Suporte Outsourcing)
- Entrada: Cognito Suporte Outsourcing.
- Abertura: dados de operação, canal, time e macro-demanda (cancelar/reagendar, alterar/incluir no job, finalizar tarefa CRM, agendamento RS), com HouseId, dados do proprietário, endereço, data/hora, motivo e observações conforme aplicável.
- Execução: validar dados mínimos em Aberto; executar em Admin/Magic Link em Em Andamento; usar Aguardando Cliente/Time Interno conforme dependência.
- Encerramento: Tipo/Subtipo + Motivo + Resumo + Evidência; Resolvido e Fechado conforme governança.

### 7.2 Reagendamento / FAQ (Fila: Solicitações de Reagendamento / FAQ)
- Entrada: Cognito Reagendamento (form 244) e Cognito FAQ QuintoAndar (form 91).
- Abertura:
	- Form 244: HouseId, data agendada, fotógrafo, motivo, solicitante, nova data/hora (opcional), priorização, observações.
	- Form 91: nome, HouseId, email, 3 dígitos CPF, endereço, motivos, data selecionada.
- Execução: validar status do job no Admin/Magic Link; registrar tentativas e evidências; usar Aguardando Time Interno quando depender de ajuste interno.
- Encerramento: data/hora final + evidência + comunicação; Resolvido -> Fechado.

### 7.3 Agendamento/Reagendamento Futuro (Fila: Solicitações de Agendamento/Reagendamento Futuro)
- Entrada: Cognito form 444.
- Abertura: dados do proprietário, HouseId, endereço, reforma (sim/não), motivo, checkbox >9 dias, data/hora, data de reabertura, nome/email do analista.
- Execução: controlar reabertura conforme regra operacional e confirmar manutenção da data/hora com evidências.
- Encerramento: evidência + resumo + motivo.

### 7.4 PP Multi (Fila: Solicitações de Agendamento/Reagendamento PP Multi)
- Entrada: Cognito form 256.
- Abertura: e-mail corporativo, tipo de ajuda, departamento, quantidade de imóveis, aptidão à sessão, tipo de imóvel, nome do fotógrafo, data, descrição, anexos.
- Execução: validar lista e executar no Admin; acionar interno quando necessário.
- Encerramento: lista final tratada + evidências principais.

### 7.5 Envio PP Fotos (Fila: Envio PP Fotos)
- Entrada: Cognito Envio de fotos proprietário (form 503), com anexos.
- Abertura: e-mail do proprietário, telefone, HouseId, tipo de envio (1º envio/reenvio/complemento), anexos.
- Execução: validar anexos; solicitar complemento em Aguardando Cliente quando necessário; tratar em Admin/Magic Link com evidências.
- Encerramento: manter anexos no Case para auditoria; registrar decisão final + evidência + resumo.

### 7.6 Placas | Logística + Agendamento/Instalação (Fila: Agendamento Instalação de Placas)
- Entrada: Cognito Solicitação de Placas (form 179) + operação interna/acionamento de parceiro (Promove/JV) no mesmo Case.
- Abertura: dados padrão (perfil solicitante, contato, ID, nome, endereço, tipo/tamanho/detalhes da placa) e dados condicionais por perfil (HouseId, tipo anúncio, CPF, ID fotógrafo).
- Execução: registrar pedido/status logístico; obter aceite e acionar parceiro; registrar protocolo/form/data estimada; dependência de parceiro em Aguardando Time Interno.
- Encerramento: status final + evidência; fechamento em massa quando aplicável.

### 7.7 Lockbox (Fila: Solicitação de Lockbox)
- Entrada: Cognito Solicitar Porta-chaves (Lockbox) (form 66).
- Abertura: perfil solicitante, ID fotógrafo (quando aplicável), portaria 24h/diurna, dados pessoais, HouseId, lockbox code, situação do imóvel, endereço de entrega.
- Execução: validar elegibilidade (sem portaria 24h/diurna -> inelegível, com encerramento por motivo); executar encaminhamento/logística e registrar evidências.
- Encerramento: status + evidência + resumo.

### 7.8 Listing Quality | IA (Fila: LQ Qualidade de imóveis IA)
- Entrada: Databricks -> Hightouch -> ListingQualityInbound__c.
- Abertura: Hightouch cria Case com HouseId__c e AnalystQueue__c.
- Roteamento: Flow pós-criação por AnalystQueue__c = 0, 1, 2.
- Execução: validar dados mínimos e links (Magic Link/Admin); executar análise e registrar decisão/evidência conforme fluxo 0/1/2.
- Contingência: criação manual/importação em lote se integração indisponível.

Ponto em aberto:
- O material não explicita a correspondência entre cada valor 0/1/2 e filas específicas.

### 7.9 Listing Quality | Reclamação qualidade das fotos (Fila: LQ Reclamação qualidade das fotos)
- Entrada: Cognito Reclamação LQ (form 220).
- Abertura: e-mail corporativo, departamento, motivo/ajuda, tipo de imóvel, canal da reclamação, HouseId (quando aplicável), anexos/evidências (quando houver).
- Execução: validar escopo/evidência; demanda indevida com encerramento por motivo; tratativa em Admin/Magic Link; solicitar complemento quando necessário.
- Encerramento: resumo + evidência + motivo; Resolvido -> Fechado.

### 7.10 Listing Quality | Imóvel fora do padrão (Fila: LQ Imóvel fora do padrão)
- Entrada: Cognito Imóvel fora do padrão (form 218).
- Abertura: nome, email, ID do fotógrafo, HouseId, motivo do report, descrição, anexos.
- Execução: validar evidência; consultar Admin/Magic Link; registrar decisão (procedente/improcedente).
- Encerramento: decisão + evidência + resumo.

### 7.11 Suporte ao Fotógrafo (Fila: Suporte Foto/Suporte Fotógrafo)
- Entrada: Cognito Formulário de Parceiros.
- Abertura: tipo de prestador, email de cadastro, categoria, subtipo, mensagem/detalhes, anexos.
- Execução: classificar Tipo/Subtipo e tratar por categoria; Aguardando Time Interno para dependência interna; Aguardando Cliente para dependência do parceiro.
- Encerramento: resumo + evidência (quando aplicável) + motivo.

Ponto em aberto:
- Definir nomenclatura única da fila entre "Suporte Foto" e "Suporte Fotógrafo".

## 8. Governança
- Métricas baseadas em Path: tempo por fase, reaberturas e aging.
- Obrigatório no encerramento: Tipo/Subtipo final + Motivo + Resumo + Evidência.
- Fechamento em massa: validar preenchimento dos campos obrigatórios antes da ação em lote.
- Fechamento automático: após 72h sem nova interação, conforme governança.

Ponto em aberto:
- Regras operacionais detalhadas para exceções do fechamento automático (se houver) não estão explicitadas.

## 9. Catálogo de Tipo de Solicitação e Subtipo

### Regras do catálogo
- Tipo de Solicitação define a fila (Queue).
- Subtipo define a variação do fluxo dentro da fila.

### 9.1 Tipo de Solicitação (11 valores)
Usar exatamente os valores abaixo:
- Suporte Outsourcing
- Solicitações de Reagendamento / FAQ
- Solicitações de Agendamento/Reagendamento Futuro
- Solicitações de Agendamento/Reagendamento PP Multi
- Envio PP Fotos
- Agendamento Instalação de Placas
- Solicitação de Lockbox
- LQ Qualidade de imóveis IA
- LQ Reclamação qualidade das fotos
- LQ Imóvel fora do padrão
- Suporte Foto

Campo sugerido: Case.TipoSolicitacao__c (picklist).

### 9.2 Subtipo por Tipo de Solicitação

#### Suporte Outsourcing
- Cancelar sessão de fotos
- Reagendar sessão de fotos
- Alterar/Incluir informações no job
- Finalizar tarefa no CRM
- Agendamento RS
- Outros

#### Solicitações de Reagendamento / FAQ
- Reagendamento — Descredenciamento
- Reagendamento — Fechamento de agenda
- Reagendamento — Funil
- Reagendamento — Outros
- FAQ — Reforma após últimas fotos
- FAQ — Benfeitorias do inquilino
- FAQ — Agendamento/Reagendamento
- FAQ — Agendamento/Reagendamento B2B Prime
- FAQ — Outros

#### Solicitações de Agendamento/Reagendamento Futuro
- Agendamento Futuro (>9 dias)
- Reagendamento Futuro (>9 dias)

#### Solicitações de Agendamento/Reagendamento PP Multi
- Avisar fotógrafo: atraso/cancelamento
- Agendamento de múltiplos imóveis
- Imóvel grande: aumentar tempo de sessão
- Não conseguiu agendar em 4 dias
- Sem agenda aos sábados
- Outros

#### Envio PP Fotos
- 1º envio
- Reenvio de ajuste (primeiro envio)
- Reenvio de ajuste (após mensagem de ajuste)
- Complemento de fotos

#### Agendamento Instalação de Placas
- Placas — Logística (Solicitação/Envio/Status)
- Placas — Agendamento/Instalação
- Placas — Pós-agendamento / Retorno do parceiro

#### Solicitação de Lockbox
- Pedido novo
- Ajuste de dados do pedido (endereço/CPF/etc.)
- Inelegível (sem portaria 24h/diurna)

#### LQ Qualidade de imóveis IA
- LQ IA — Fluxo 0
- LQ IA — Fluxo 1
- LQ IA — Fluxo 2

#### LQ Reclamação qualidade das fotos
- Incluir fotos
- Excluir fotos
- Fotos erradas
- Fotos ruins
- Imóvel duplicado
- Correção de dados
- Imóvel despublicado
- Problemas Originals
- Incluir/Excluir fotos 360º
- Outros / Não classificado
- Demanda indevida

#### LQ Imóvel fora do padrão
- Report procedente
- Report improcedente
- Demanda indevida / Sem evidência

#### Suporte Foto
- Agenda:
	- Alteração de horário semanal
	- Alteração de horário específico
	- Reagendamento
- Contrato de Parceria:
	- Alteração cadastral
	- Alteração dados bancários
	- Credenciamento
	- Descredenciamento
- Remuneração:
	- Bonificação
	- Contestação do relatório
	- Envio de nota fiscal
	- Pagamento
- Elogio/Reclamação/Sugestão:
	- Elogio
	- Sugestão de melhoria
	- Reclamação
- Suporte a fotos:
	- Ajuste de sessão
	- Acesso sistema: Aplicativo
	- Acesso sistema: Plusoft
	- Acesso ao Youtube
	- Área de atuação
	- Feedback de sessão
	- Material de apoio (plaquinhas e lockbox)
	- Mudança de região
	- Relatar problema (equipamento/transporte/roubo)
	- Reportar problema com job ou imóvel
- Problemas com proprietário:
	- Relatar assédio
	- Importunação de proprietário
	- Outros

Ponto em aberto:
- Validar se a nomenclatura oficial do Tipo de Solicitação será "Suporte Foto" (catálogo) ou variação de fila "Suporte Fotógrafo".

## 10. Campos recomendados
Campos recomendados para suportar o catálogo sem transformar tudo em Subtipo:
- Categoria__c (especialmente para Suporte Foto): Agenda / Contrato / Remuneração / etc.
- Motivo__c (Reagendamento / Lockbox / LQ Reclamações).
- SolicitantePerfil__c: Proprietário / Fotógrafo / Time interno / etc.
- CanalEntrada__c: Receptivo chat/call, ativo, etc.
- Parceiro__c (Placas): Promove / JV.
- CidadeRegiao__c (Placas/LQ).

## 11. Automação de roteamento
- Regra simples: quando TipoSolicitacao__c = X, Owner = fila X (Queue correspondente).
- Exceção LQ IA: manter Flow existente usando AnalystQueue__c (0/1/2) para roteamento.

Ponto em aberto:
- Definir precedência entre roteamento por TipoSolicitacao__c e roteamento por AnalystQueue__c quando ambos estiverem preenchidos no mesmo Case.
