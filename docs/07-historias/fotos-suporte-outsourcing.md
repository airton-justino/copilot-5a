Fotos — Suporte Outsourcing

Eu como
Analista de FUP Fotos Interno

Quero
Receber e tratar no Case as solicitações de Suporte Outsourcing relacionadas a cancelamento, reagendamento, correção cadastral e fechamento manual de tarefa travada

Para
Executar ajustes operacionais que parceiros externos não conseguem concluir diretamente, com rastreabilidade da tratativa e do encerramento

Benefícios

Centralização do processo no Case
Rastreabilidade de validação, execução e encerramento
Reclassificação sem perda de histórico
Menor dependência de controles paralelos
Campos relevantes identificados

Status
OwnerId
Type
Reason
Subject
Description
Comments
ContactId
ContactEmail
ContactPhone
CPF__c
HouseId__c
ZendeskId__c
FlowSubType__c
Source__c
Campos novos sugeridos

Nenhum
Regras de negócio

A solicitação entra por formulário e é tratada em Case.
HouseId__c é o identificador principal do imóvel no processo.
Sem dados mínimos completos, não executar alteração sistêmica.
Quando faltarem dados, solicitar complemento antes da execução.
A execução pode envolver cancelamento/reagendamento, correção cadastral ou fechamento manual de tarefa travada.
O encerramento deve registrar resumo da tratativa e comunicação enviada.
Reclassificação durante a tratativa é permitida sem perda de histórico.
Critérios de aceite

Dado um Case de Suporte Outsourcing com HouseId__c preenchido e dados mínimos válidos, quando o analista iniciar a tratativa, então ele consegue registrar a ação executada e concluir o atendimento no mesmo Case.
Dado um Case sem HouseId__c ou sem dados críticos, quando o analista identificar a ausência, então nenhuma alteração sistêmica é realizada antes do complemento.
Dado um Case com demanda de cancelamento, reagendamento, correção cadastral ou fechamento manual, quando a ação for concluída, então o resumo da execução fica registrado no Case.
Dado um Case concluído, quando o analista encerrar, então o registro contém histórico da tratativa e referência de encerramento ao solicitante.
Pontos em aberto

Confirmar regra de obrigatoriedade de HouseId__c por etapa (abertura vs início da execução).
Confirmar campo oficial para classificação funcional principal entre Type, Reason e FlowSubType__c.
Confirmar fila específica de Suporte Outsourcing na configuração final.
Confirmar padrão operacional de evidência no Case além de descrição/comentários.