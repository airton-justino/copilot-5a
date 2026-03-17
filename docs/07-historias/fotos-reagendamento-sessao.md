Fotos — Reagendamento de Sessão de Fotos

Eu como
Analista de FUP Fotos

Quero
Receber e tratar no Case as solicitações de reagendamento de sessão de fotos

Para
Recuperar a agenda do imóvel e concluir novo desfecho operacional sem deixar o imóvel parado no funil

Benefícios

Consolidação do processo de reagendamento no Case
Visibilidade de contato e desfecho
Rastreabilidade do motivo e da ação final
Melhor controle de pendências e reclassificações
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
Address_Cognito__c
HouseId__c
ZendeskId__c
FlowSubType__c
Source__c
Campos novos sugeridos

Nenhum
Regras de negócio

O reagendamento é tratado em Case.
HouseId__c é o identificador principal do imóvel no processo.
Antes do novo agendamento, validar e tratar o job anterior quando necessário.
Contato ativo com o proprietário é obrigatório para definição do desfecho.
Desfechos possíveis: novo agendamento, encaixe, inalcance ou abandono.
Se faltarem dados para contato/execução, a tratativa não avança até complementação.
Demandas fora do escopo devem ser reclassificadas sem perda de histórico.
Encerramento deve registrar desfecho e comunicação realizada.
Critérios de aceite

Dado um Case de reagendamento com HouseId__c preenchido e dados mínimos válidos, quando o analista validar o job anterior, então ele consegue registrar o desfecho da tratativa no Case.
Dado um Case sem HouseId__c ou sem dados suficientes de contato/execução, quando a lacuna for identificada, então a tratativa não segue até o complemento.
Dado um Case com contato bem-sucedido, quando houver viabilidade operacional, então o novo desfecho é registrado no Case.
Dado um Case fora do escopo de reagendamento, quando for identificado, então é reclassificado sem perda de histórico.
Dado um Case concluído, quando encerrado, então contém resumo da tratativa e evidência do desfecho.
Pontos em aberto

Confirmar obrigatoriedade de HouseId__c já na criação do Case.
Confirmar regra única de tentativas de contato (quantidade e janela).
Confirmar fila específica de Reagendamento de Sessão de Fotos na configuração final.
Confirmar uso de Address_Cognito__c como campo oficial de endereço para este fluxo.
Confirmar campo oficial de classificação funcional principal entre Type, Reason e FlowSubType__c.