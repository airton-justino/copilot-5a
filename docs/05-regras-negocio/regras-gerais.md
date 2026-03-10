# Regras Gerais

## Objetivo

Consolidar regras de negocio transversais observadas no consolidado, evitando duplicidade nos arquivos de processo.

## Regras transversais confirmadas no material

- Reclassificacao de Tipo de Solicitacao:
	- O agente pode reclassificar a qualquer momento.
	- O mesmo ticket/case e transferido para a fila correta sem perda de historico.
- Tratativa com dados incompletos:
	- Quando faltarem dados, deve haver solicitacao de complemento e movimentacao para estado de espera do cliente.
- Encerramento por sem retorno:
	- Quando nao houver retorno do solicitante em estados de espera, pode haver encerramento com comunicacao por template.
- Uso de macro/template:
	- Encerramentos e devolutivas operacionais usam macro/template nos canais oficiais.

## Regras especificas com impacto transversal

- Lockbox (elegibilidade):
	- Imovel apartamento.
	- Imovel desocupado.
	- Portaria 24h ou diurna; sem isso, inelegivel.
- Pos Agendamento de Placas:
	- No caso de nao instalacao, ha registro de que parceiro ainda recebe pagamento.
- Listing Quality (TO-BE):
	- finalClassification published/unpublished emite evento.
	- finalClassification under_review nao emite evento.

## Regras de operacao e governanca

- Nao transformar backlog em decisao final.
- Nao misturar fluxos distintos em um mesmo documento de processo.
- Quando houver ambiguidade no consolidado, registrar como Ponto em aberto ou A definir.

## Pontos em aberto transversais

- Criterio formal de informacoes completas por processo.
- Governanca unica de encerramento sem retorno por fila.
- Detalhamento de regras de SLA por processo/status.
