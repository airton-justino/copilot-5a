Listing Publicado
Lari: validar estratégia de canais
Fluxos Placas  (Logística e Lockbox)
AS IS
TO BE

Início do fluxo
Cogs, fluxos de reclação LQ  

https://www.cognitoforms.com/QuintoAndarcom/Im%C3%B3veisForaDoPadr%C3%A3o
https://www.cognitoforms.com/QuintoAndarcom/QualidadeIm%C3%B3v
Macro fluxo
Fluxo detalhado
Fluxo detalhado
Ação sistêmica automática
Ações de execução análise e sondagem humana
Placas
Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado
Processos não identificados:

Gestão de Fotógrafos
Qualidade de Imóveis (pós LQ, quando há reclamação de algum stakeholder)
FotosPP - Piloto LQ <> FUP
Zapierupload sobrecarrega api necessário fazer em pacotes de 100 tkts
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Solicitação para áreas de apoio



Analista  faz download da query de agendamento
Analista faz upload dos leads para encaminhar whatsapp (twillio) em massa para captar

Cliente quer instalar placa?

Sim
Analista faz a solicitação para o parceiro via cognito
Analista preenche o formulário do case no salesforce

Inicio do Processo

Analista  faz download da querie de agendamento
Analista faz upload dos dados em uma planilha compartilhada com o time de Tools
Tools sobe automaticamente os dados para o zendesk gerando um ticket
Analista faz upload dos leads para encaminhar whatsapp em massa para captar

Cliente quer instalar placa?
s
Analista faz a solicitação para o parceiro
Analista preenche o formulário do ticket no zendesk

Agendamento de Placas

Analista  faz download da querie de agendamento
Analista faz upload dos dados em uma planilha compartilhada com o time de Tools
Tools sobe automaticamente os dados para o zendesk gerando um ticket
Analista faz upload dos leads para encaminhar whatsapp em massa para captar

Cliente quer instalar placa?
s
Analista faz a solicitação para o parceiro
Analista preenche o formulário do ticket no zendesk

integração do forms com o ticket original
Touch points com o cliente

Metabase
Google Sheets
Zendesk
Omnie
Cognito
Zendesk
Metabase
Google Sheets
Zendesk
Omnie
Cognito
Zendesk
Analista faz upload dos dados em uma planilha compartilhada com o time de Tools
Integração do forms google com o salesforce
Abertura de ticket
Sistema onde a ação é realizada
Integração
Formulário Google
Integração
Formulário Google
Não
Detalhes da ação referenciada

n
Abre o Google Sheets
Insere os dados extraídos do metabase
Retira clientes elegíveis que são B2B através de fórmula
Copia os clientes restantes para a planilha oficial de tools
Abre o Google Sheets
Copia os telefones dos clientes elegíveis
Sobe na plataforma Omnie
Faz o disparo de macro ofertando a placa.
Grupo: CNX Plaquinhas
Assunto: Agendamento Plaquinhas CNX

Divisão Salesforce: Agendamento Instalação de Placas
Follow ups com o cliente
Abre a página do metabase
Clica no botão de download
Analista confere a cidade em que o imóvel fica localizado:
a. São Paulo, RJ e Campinas
Preenche o cognito  do parceiro Promove.
b. Belo Horizonte
Preenche o formulário  do parceiro JV.

@Airton Justino De Oliveira Junior  aqui não teremos mais a limitação de subir em batches de 100 por vez?
@Izabella Oliveira será realizado a carga via Salesforce, gerando tickets automaticamente (precisaremos definir os usuários com esta permissão)
P: Oportunidade de manter no mesmo ticket o processo end to end? Solicitação + retorno da empresa.

R: Ao avaliar API, entender se será possível.
Abertura de ticket com a outra parte
n
Tools sobe automaticamente os dados para o Salesforce gerando um case via carga no salesforce
Analista preenche o formulário do ticket no zendesk

Analista preenche o formulário do case no salesforce
Encerrar o Case
Ponto de decisão

Zendesk
Grupo: CNX Plaquinhas
Assunto: Agendamento Plaquinhas CNX

Divisão Salesforce: Agendamento Instalação de Placas

O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.

Fim do fluxo
Analista preenche o formulário do ticket no zendesk

Pessoal, aqui não faz sentido:
Migrarmos a query do metabase
Fazer a retirada dos clientes B2B direto na consulta

Se não forem ações para agora, podemos deixar mapeadas em uma lista de backlog?

R: adicionado ao backlog
Backlog: integração com Twilio
P: Essas ações não podem ser automatizadas?

R: não, backlog

Zendesk

Ações nesta fase — Entrada / Contexto:
Abre a página do metabase
Clica no botão de download
Ações nesta fase:
Abre o Google Sheets
Insere os dados extraídos do metabase
Retira clientes elegíveis que são B2B através de formúla
Copia os clientes restantes para a planilha oficial de tools
Ações nesta fase:
Abre o Google Sheets
Copia os telefones dos clientes elegíveis
Sobe na plataforma Omnie
Faz o disparo de macro ofertando a placa.
Ações nesta fase:
Analista confere a cidade em que o imóvel fica localizado:
a. São Paulo, RJ e Campinas
Preenche o cognito  do parceiro Promove.
b. Belo Horizonte
Preenche o formulário  do parceiro JV.

Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
Aberto
Em Andamento
Aguardando Time Interno
Lari: validar estratégia de canais
Aguardando Cliente
Resolvido
Fechado

Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Empresa parceira Abre o Case via Cognito / API

Pós Agendamento de Placas

Analista recebe o retorno da empresa
Analista  preenche o formulário do ticket de acordo com o retorno do parceiro

P: Temos oportunidade de retornar diretamente no ticket original?

R: estudar através da análise da API
Entrada cognito deixa de ser utilizada, Empresa JV deixa de prestar serviço ao 5A

Zendesk (Cognito)
Zendesk


O time de parceiro informa se a colocação da placa foi realizada ou não.
JV: Responde através de Cognito.
Promove: API do parceiro manda um ticket em massa para o zendesk (e-mail).
Analista checa se as informações estão completas.
Acessa o ticket
Preenche o formulário na lateral, caso seja parceiro JV o preenchimento é automático, caso seja Promove o analista preenche.
Analista recebe o retorno da empresa
Analista preenche o formulário do case no salesforce
Encerrar o Case

P: A dependender da resolução não deveríamos finalizar em fases distintas? Ou estamos com alguma propriedade sendo preenchida para indicar?

R: temos essa informação sendo preenchida como campo do formulário/cognito.
No caso de não instalação, o parceiro ainda sim recebe pagamento.

Backlog: deveríamos gatilhar um novo ticket, linkado a esse principal OU priorizar esse tipo de caso dentro do metabase.
Oportunidade de Automatizar os da Promove?R: estudar através da análise da API


O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
Ações nesta fase:
O time de parceiro informa se a colocação da placa foi realizada ou não.
JV: Responde através de Cognito.
Promove: API do parceiro manda um case em massa para o salesforce (e-mail).
Analista checa se as informações estão completas.
Ações nesta fase:
Abre o case
Preenche o formulário na lateral, caso seja parceiro JV o preenchimento é automático (cognito), caso seja Promove o analista preenche.
Aberto
Em Andamento
Aguardando Time Interno
Lari: validar estratégia de canais
Aguardando Cliente
Resolvido
Fechado
Logística
Grupo: Plaquinhas - Pedido da FAQ
Assunto: Solicitar placa do QuintoAndar no imóvel

Fotógrafo, PP, ASP ou CIQ solicita placa para envio via correios

Divisão no Salesforce: Logística de Placas
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Grupo: Plaquinhas - Pedido da FAQ
Assunto: Solicitar placa do QuintoAndar no imóvel

Fotógrafo, PP, ASP ou CIQ solicita placa para envio via correios

Divisão no Salesforce: Logística de Placas
Receber a Solicitação 
Cognito



Placa já foi solicitada?


Sim
Verifica o status da placa.(Google sheets)

Retorna o cliente informando que a placa já está a caminho ou foi entregue (Template)






Solicitação de Placas

Analista recebe a solicitação de placas
Placa já foi solicitada?
s
Retorna o cliente informando que a placa já está a caminho ou foi entregue

Não



Inicio do Processo

Analista recebe a solicitação de placas
Placa já foi solicitada?
s
Retorna o cliente informando que a placa já está a caminho ou foi entregue

Zendesk



Zendesk (Cognito)
Google Sheets
Zendesk
Faz a solicitação para envio das placas (Google sheets)
Retorna o cliente informando que a placa já está a caminho. (Template)
Encerrar o Case

Zendesk (Cognito)

A solicitação pode ser feita por:
Proprietários;
Fotográfos;
Time internos:
ASP
CIQ
n
Verifica através do google sheets o status da placa.

n
Abertura case no salesforce
Faz a solicitação para envio das placas
Faz a solicitação para envio das placas
Retorna o cliente informando que a placa já está a caminho.


O mesmo cognito que é aberto para que o analista verifique a solicitação também alimenta um Google sheets para que a solicitação aconteça;
Retorna o cliente informando que a placa já está a caminho ou foi entregue




Zendesk
Zendesk
Google Sheets
Google Sheets
O mesmo cognito que é aberto para que o analista verifique a solicitação também alimenta um Google sheets para que a solicitação aconteça;
Ações nesta fase — Entrada / Contexto:
A solicitação pode ser feita por:
Proprietários;
Fotográfos;
Time internos:
ASP
CIQ
Ações nesta fase:
O mesmo cognito que é aberto para que o analista verifique a solicitação também alimenta um Google sheets para que a solicitação aconteça;
Ações nesta fase:
Verifica através do google sheets o status da placa.
Ações nesta fase:
Informa o cliente
Fecha o case

Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
Temos convicção que continuar usando o cognito é a melhor opção? Quais seriam os prós e contras de utilizarmos a estrutura de forms do Sales Force?

@ruan.ricardo @rafael.scarparo  conseguimos uma análise geral complementar de prós e contras cognito vs. solução nativa?
Aberto
Em Andamento
Aguardando Time Interno
Lari: validar estratégia de canais
Aguardando Cliente
Resolvido
Fechado

Lockbox
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Retorna o cliente e solicita as informações que estão faltando para alterar o cadastro.
Cliente de retornou?
n
Encerra o ticket

Retorna o cliente e solicita as informações que estão faltando para alterar o cadastro.
Cliente de retornou?
n
Encerra o ticket

P: Em caso de ajustes no pedido original, qual fluxo? Conseguimos mesclar cards?

R: após fechamento do ticket, cliente abrirá nova solicitação, não será mesclado. Operação conseguirá fazer a associação de tickets manualmente.


n
n
Receber a Solicitação 
Cognito
Verificar  a solicitação de envio da lockbox


Zendesk

Informações Completas?
Sim
Preencher campos recebibos
Executar alteração no Admin
Responder cliente no Case(template/macro)


Zendesk


Não
Fechamento de case

@dener, poderia trazer o tempo de encerramento médio em horas úteis?

O cliente passou todas as informações necessárias para alteração?
s
O cliente passou todas as informações necessárias para alteração?
P: Além disso, faz sentido pensarmos em uma entrada única de formulário para os processos? Unificando vários forms em apenas 1

R: Faz sentido, mas faremos em um segundo momento.
Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
Solicitar informacoes ao cliente(responder nos canais)
Inicio do Processo

Analista recebe a solicitação
s
Sim


Inicio do Processo

Analista recebe a solicitação



Grupo: Lockbox - Pedidos da FAQ
Assunto: Solicitação de Lockbox

Fotógrafo, PP, ASP, IS ou CIQ solicita placa para envio via correios

Divisão no Salesforce: Logística de Lockbox
Grupo: Lockbox - Pedidos da FAQ
Assunto: Solicitação de Lockbox

Fotógrafo, PP, ASP, IS ou CIQ solicita placa para envio via correios

Divisão no Salesforce: Logística de Lockbox
Status = Pending(aguardando retorno)
Encerrar o Case

Zendesk (Cognito)
Zendesk (Cognito)

Verificar  a solicitação de envio da lockbox
Retorna o cliente informando que a solicitação foi enviada
Solicitação chega através do cognito e o solicitante pode ser:
Proprietário 
Vistoriador
Corretor
Fotógrafo
Consultor Imobiliário
Rede (Interno)
Cliente retornou?
s




Verificar  a solicitação de envio da lockbox

Retorna o cliente informando que a solicitação foi enviada



O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.


s
Não


Zendesk
Zendesk
Comunicar cliente da não resposta (Template)
Google Sheets
Google Sheets
Cognito gera um ticket no zendesk e alimenta esta planilha;
Analista checa a planilha faz o download;
Analista encaminha a solicitação para o parceiro Go Roger através do whatsapp business
Sim
P: seguiremos o envio de informações via whatsapp?R: on hold - @rafael.scarparo verificará com Leonel
P: Pipeline do Sales force tem SLA nativo? Ou cria somente propriedades de tempo indicando entrada e saída dos cards em cada fase?

R: 
Temos contabilização de SLA por etapa e do fluxo completo, por horas úteis e horas corridas.
Ações nesta fase — Entrada / Contexto
Receber solicitação via Cognito → criar/receber Case no Salesforce (Lockbox).
Case cai na fila Lockbox - Pedidos da FAQ [SO].
Analista abre o Case e confere quem é o solicitante (PP / Vistoriador / Corretor / Fotógrafo / Consultor Imobiliário / Rede) e o objetivo do pedido (Lockbox Code, entrega, etc.).
Identifica rapidamente se é:
Pedido novo de Lockbox
Ajuste/pendência de dados (ex.: endereço, CPF, etc.)
Ações nesta fase — Triagem e Coleta de Dados
Validar dados mínimos + elegibilidade, conforme regra do Lockbox:
Imóvel apartamento
Imóvel desocupado
Possui portaria 24h ou diurna? (se “Não” → inelegível)
Checar se existe duplicidade / pedido já existente (se aplicável).
Se faltar informação:
Solicitar complemento ao solicitante (macro/template)
Mover Case para Aguardando Cliente (aguardando retorno)
Ações nesta fase — Execução (Operação/Logística)
Registrar/encaminhar a solicitação para operação logística conforme processo atual:
Se hoje isso acontece via planilha: atualizar/consultar a planilha de controle (quando aplicável).
Se existe acionamento do parceiro (ex.: Go Roger): encaminhar a demanda no canal definido pela operação (ex.: WhatsApp Business do parceiro), e anexar evidência/link no Case.
Atualizar o Case com:
Status do envio/acionamento
Evidência (print/link)
Se depender de retorno do parceiro/entrega:
mover para Aguardando Time Interno
Ações nessa fase — Retorno ao Cliente / Encerramento
Responder o solicitante com macro/template:
“Solicitação enviada/acionada”
ou “Inelegível” com motivo (sem portaria / não atende critérios)
ou “Faltam dados”
Fechamento:
Resolvido → Fechado
Se solicitante não retornar em Aguardando Cliente:
comunicar “sem retorno” (template) e encerrar conforme governança.
Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
Fluxos Listing Quality
AS IS
TO BE
Macro fluxo
Fluxo detalhado
Fluxo detalhado
Listing Quality
n
Lari: validar estratégia de canais





Inicio do Processo

Extração de Listing Metabase + Análise de IS
Importar CSV

IA aprovou?
s

Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado


Inicio do Processo

Extração de Listing Metabase + Análise de IA
Importar CSV
IA aprovou?
Fluxo 0
Fluxo 1
Fluxo 2
Fluxo 3



Metabase
Google Sheets
n
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento

Metabase
Google Sheets
Zendesk
Zendesk
Zendesk
Zendesk
Não



s
Extração no Databricks (via Hightouch)

Rodar a base de listings (anúncios) no Metabase com todos os listings criados até as 18h do dia anterior (por CIQ, proprietário ou fotógrafo). Link do Metabase
Roda automação para analise da IA dentro do sheets;
Após análise roda a segunda automação no mesmo sheets que vai criar os tickets dentro do zendesk dividindo os fluxos em:
Fluxo 0 - BPO faz analise em 10% dos listing que não passaram na IA
Fluxo 1 -  Listings que passaram pela IA, mas que ela sinalizou que precisam de "olhar humano" para possível reprovação.
Fluxo 2-  Exclusivo para listings que passaram pela IA, mas que ela identificou a presença de QR Code e precisa apenas verificar a placa.
Fluxo 3- IA aprovou Fluxo já sobe fechado no ticket do zendesk.

Inputa a base extraída no metabase no sheets e roda automação. Link do sheets

IA Aprovou?

Criar Case no SF + roteamento



Análise realizada pelo time(BPO)
Revisão do listing possível despublicação
Checagem e vínculo de placa
IA aprovou

Sim
Fluxo 0
Fluxo 1
Fluxo 2
Magic Link
Magic Link
Magic Link
Zendesk
Fluxo 0
Fluxo 1
Fluxo 2
Criar campo de observações internas
Analise de IA Integração
Sem criação de Case no SF / Sem fila
Insere as informações sobre a placa no case
Tira print do código na foto e insere como informação interna



Zendesk
Zendesk
Zendesk
Abrem as fotos no magiclink 
Organizam as fotos em ordem
Inserem legenda nos comodos em que ficaram sem legenda (se necessário também corrigem o texto)
Checam a descrição do anúncio
Assistem o video para entender se contempla os comodos e se não tem audio a ser excluido.
Abrem as fotos no magiclink 
Checam como está o estado do imóvel .
Checam a descrição do anúncio
Inserem legenda nos comodos em que ficaram sem legenda (se necessário também corrigem)
Assistem o video para entender se contempla os comodos e se não tem audio a ser excluido.




Abrem as fotos no magiclink 
Checam apenas a foto que está com o código da placa;
Preenche o formulário do zendesk com o código
Ticket sobe apenas para histórico e contabilização.
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
Análise realizada pelo time no Magic Link
Revisão do listing possível despublicação no Magic Link
Checagem e vínculo de placa no Magic Link


Análise realizada pelo time
Revisão do listing possível despublicação
Checagem e vínculo de placa



Zendesk
Magic Link
Magic Link
Listing Aprovado?
Preenche o formulário e fecha o case
Encerrar o Case

Placa colocada?
Sim





Placa colocada?
s
Preenche o formulário e encerra o ticket

Não



Sim
Não
Registrar impossibilidade de colocar placa
Zendesk
Tranfere o case


Listing aprovado?
s
Preenche o formulário e encerra o ticket

Listing aprovado?
s
Preenche o formulário e encerra o ticket

Baixar fotos via zip no admin (não é feito no magiclink porque não tem a opção de fazer o download em massa)
Salvar as fotos no Drive do listing
Excluir as fotos no admin para que o imóvel não seja publicado.
Preenche o formulário e fecha o case
n
Insere as informações sobre a placa no formulário
Tira print do código na foto e insere como informação interna



Zendesk
Zendesk
Preenche o formulário e fecha o case
n
n
Despublica o listing no Magic Link

Insere as informações no formulário e encerra o ticket.
Registrar impossibilidade de colocar placa
Despublica o listing
Despublica o listing
Fluxo 0 — BPO analisa parte do que não passou na IA
Abrir fotos no MagicLink
Organizar fotos em ordem
Inserir/corrigir legendas (se necessário)
Checar descrição do anúncio
Assistir vídeo (cômodos + áudio a remover)
Preencher formulário no MagicLink + encerrar Case no Salesforce

Fluxo 1 — IA pede “olhar humano” (possível reprovação)
Abrir fotos no MagicLink
Checar estado do imóvel com ênfase no cômodo indicado pela IA
Checar descrição do anúncio
Inserir/corrigir legendas (se necessário)
Assistir vídeo (cômodos + áudio a remover)
Preencher formulário no MagicLink + encerrar Case no Salesforce
Zendesk
Hightouch Sync #1 (persistir Listing Quality)
Sync #1 consulta Databricks.
Grava/atualiza registros no domínio/banco Listing Quality (campos iniciais).
Isso vira a base para pré-preencher o formulário no MagicLink.
Hightouch Sync #2 (criar Case no Salesforce)
Sync #2 consulta Databricks novamente (limitação do Hightouch: source é DB).
Calcula listingId + score.
Cria Case no Salesforce com esses dados.
Execução (Salesforce + MagicLink + Listing Quality API)
Salesforce: roteia/prioriza Cases para analistas (pré e pós-análise).
MagicLink: analista revisa a listing e preenche formulário (pré-preenchido via dados do Listing Quality).
Backoffice BFF → Listing Quality API: salva atualização + finalClassification.
Exceção de auditoria: anexos + justificativa via comentário do Case no Salesforce.
Evento para Partner Payments:
finalClassification = published/unpublished → emite evento
finalClassification = under_review → não emite evento
Fluxo 2 — IA detectou QR Code (verificar placa)
Abrir fotos no MagicLink
Checar apenas a foto com o código da placa
Registrar código no formulário (no MagicLink)
(Opcional do seu desenho) salvar código como observação interna no Case
Encerrar Case no Salesforce
Magic Link
Magic Link
Databricks (fonte)
Dados de listings vêm do Databricks.
Base usada para alimentar o processo de Listing Quality.
Preenche o formulário e encerra o case

Preenche o formulário e encerra o ticket

Baixar fotos via zip no admin (não é feito no magiclink porque não tem a opção de fazer o download em massa)
Salvar as fotos no Drive do listing
Excluir as fotos no admin para que o imóvel não seja publicado.

Zendesk

Preenche o formulário e encerra o ticket


Zendesk
Reclamação LQ
Aberto
Em Andamento
Lari: validar estratégia de canais
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado

Recebimento do ticket na caixa do Zendesk e abertura automática de tarefa no sistema

Avaliar tipo da demanda
Todos os dados para tratativa foram enviados?
Sim
Qual é a demanda?
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento


Cognito preenchido por parceiros ou analistas internos
Zendesk
Zendesk
@felipe.moura sei que falamos em não mexer nesses cognitos, mas especificamente aqui precisamso tirar essas duas opções
Receber a Solicitação 
Cognito



Verificar a demanda que será realizada
Informações Completas para o tipo de demanda?

Sim
Qual é a demanda?


Coginito preenchido
Não


Abretura automática do ticket
Analisar demanda
Realizar tratativa no anúncio
Encerrar tratativa





Zendesk
Zendesk
Admin/MagicLink
Admin/MagicLink
Registrar como demanda indevida e encerrar ticket
Fotos ruins
Imóvel despublicado
Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
Imóvel inabitável
Correção de dados
Fotos erradas
Problemas Originals
Incluir/Excluir fotos 360º
Não
Incluir Fotos
Imóvel Duplicado
Zendesk
O que são essas duas demanas?@Izabella Oliveira Iza, não entendi essa dúvida. Pelo que entendi do processo, essa categoria serve para trativas de categoria Originals (produto que não temos mais). Não tínhamos tickets dessa tratativa, mas o entendido é que ela acaba sendo usado como uma categoria generalista.
Analisar motivo que originou a despublicação original pelo ticket de tratativa original
Incluir fotos
Imóvel Duplicado
Imóvel inabitável
Correção de dados
Baixar fotos/vídeos a ser incluído
Comparar ID correto e ID em duplicidade
Analisar dados do formulário
Analisar dados do formulário
Analisar evidências de fotos erradas enviadas no cognito
Analisar o tipo de demanda para Originals
Comparar ID correto e ID em duplicidade
Analisar evidências de fotos erradas enviadas no cognito
Imóvel despublicado

View
Registrar como demanda indevida e encerrar o case
Fotos erradas

iCloud
Admin/MagicLink
Admin/MagicLink
Admin/MagicLink
Zendesk
Admin/MagicLink
Admin/MagicLink
Admin/MagicLink
Zendesk
Fotos ruins
Executar alteração no Admin
Não conseguimos ver um caso especifico desse cenário, mas ele contempla os mesmo tipos de tratativas que tems para os demais anuncios, porém, considerando a categoria Orignals.
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
Baixar fotos/vídeos a ser incluído Icloud
Verifica no Admin
Verifica e despublica Admin/Magic Link
Executar alteração no Admin / MagicLink
Analisar evidências de fotos erradas enviadas no cognito
Analisar evidências de fotos erradas enviadas no cognito no Admin / MagicLink



Não conseguimos ver um caso especifico desse cenário, mas, a nível de Zendesk e integração, ele segue o mesmo padrão dos demais.
Não conseguimos ver um caso especifico desse cenário, mas, a nível de Zendesk e integração, ele segue o mesmo padrão dos demais.
Baixar fotos e salvá-las no drive LQ
Não conseguimos ver um caso especifico desse cenário, mas, a nível de Zendesk e integração, ele segue o mesmo padrão dos demais.
Excluir fotos
Analisar correção do anúncio






Inserir fotos no anuncio
Duplicidade confirmada?
Não
Registrar como demanda indevida e encerrar ticket

Google Drive
MagicLink
MagicLink
Analisar motivo que originou a despublicação original pelo case de tratativa original


Executar alteração no Admin
Duplicidade confirmada?
Baixar fotos e salvá-las no Google drive de LQ
Excluir fotos no MagicLink Admin






https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/220
Admin/MagicLink
Zendesk




Cognito Forms
Não
Sim


Sim



Despublicar anuncio
Baixar imagens do imóvel despublicado
Analisar correção do anúncio no MagicLink
Despublicar anuncio no Magic Link

Deletar anuncio em duplicidade
MagicLink
Sim
Sistema aceitou fotos?

Sistema aceitou fotos?
Não
Registrar como imagem fora do padrão e encerrar ticket

Google Drive
Registrar como demanda indevida
Deletar anuncio em duplicidade

Não
Baixar imagens do imóvel despublicado no Google drive






MagicLink
Zendesk

Registrar tratativa
Registrar como imagem fora do padrão

Fazer upload das fotos na pagina do imóvel

Fazer upload das fotos na pagina do imóvel Admin/MagicLink
Admin/MagicLink



Republicar o imóvel no MagicLink
Republicar o imóvel


MagicLink
Sim
Registrar tratativa e encerar ticket
Encerrar o Case com as evidências
Zendesk
Encerrar o Case com as evidências

1)Ações nesta fase — Entrada / Contexto
Status principal: Aberto (em validação)
Receber demanda via Cognito (Reclamação LQ / Qualidade de imóveis – form 220).
Criar/receber Case no Salesforce já na fila Listing Quality [FOTOS] [SO].
Analista acessa a fila/List View, abre o Case e revisa:
tipo de demanda selecionado no Cognito
ID do imóvel / links / anexos (quando houver)
Decisão inicial: Demanda devida ou indevida (ex.: fora de escopo / sem evidência mínima / pedido incoerente).
Saídas:
Indevida → registrar motivo + Resolvido/Fechado
Devida → seguir para Triagem
2) Ações nesta fase — Triagem e Coleta de Dados
Status principal: Aberto (em validação) → Em Andamento
Validar se existem dados mínimos para a demanda escolhida:
ID do imóvel
evidências/anexos (ex.: fotos erradas, fotos a incluir, evidência de duplicidade)
contexto quando “Imóvel despublicado” (link/ID do ticket original, quando aplicável)
Se incompleto:
registrar pendência e solicitar complemento (no canal definido)
mover para Aguardando Cliente
Se completo:
mover para Em Andamento
confirmar/ajustar Tipo de Demanda (reclassificação permitida; se reclassificar, o Case muda de fila automaticamente sem perder histórico).
Imóvel duplicado
comparar IDs (correto x duplicado) no Admin/MagicLink
decidir “Duplicidade confirmada?”
Não → indevida e encerrar
Sim → deletar anúncio em duplicidade (MagicLink/Admin)
Fotos erradas
analisar evidências do Cognito
excluir fotos incorretas (MagicLink/Admin) e registrar
Fotos ruins
analisar pedido/evidência
excluir fotos conforme solicitação (MagicLink/Admin)
Incluir/Excluir fotos/vídeos 360º
analisar evidências
executar inclusão/exclusão no Admin/MagicLink (conforme capacidade)
3) Ações nesta fase — Execução (Admin/MagicLink + iCloud/Drive)
Status principal: Em Andamento
Substitui o bloco errado de Google Sheets. Aqui é execução sistêmica conforme a demanda.
Caminhos por tipo de demanda (sem criar fluxos separados)
Incluir fotos
baixar fotos/vídeos (ex.: iCloud)
salvar no Drive LQ (quando necessário)
fazer upload das fotos no anúncio (Admin/MagicLink)
validar “Sistema aceitou fotos?”
Não → registrar “imagem fora do padrão” e encerrar
Sim → seguirImóvel despublicado
analisar motivo que originou a despublicação pelo ticket/case original
baixar imagens do imóvel despublicado (Drive) quando necessário


baixar imagens do imóvel despublicado (Drive) quando necessário
corrigir anúncio (MagicLink/Admin)
republicar imóvel (MagicLink)
Problemas Originals
tratar como categoria “generalista” enquanto não houver regra específica (registrar que é Originals + executar tratativa equivalente no Admin/MagicLink, quando aplicável)
Saídas:
Se depender de validação/terceiro/sistema: Aguardando Time Interno
Se depender do solicitante/complemento: Aguardando Cliente
Se concluído: seguir para Encerramento
4) Ações nesta fase — Retorno ao Cliente / Encerramento
Status principal: Resolvido → Fechado (em validação)
Registrar no Case:
resumo da tratativa
tipo de demanda final (pode ter sido reclassificado)
evidências (link/anexo/print quando aplicável)
Responder via template/macro (se existir retorno para solicitante).
Mover para Resolvido e depois Fechado (em validação).
Se reabrir/contestar: Reaberto → volta para Em Andamento (ou Aguardando Cliente se faltou dado).
Aberto
Em Andamento
Aguardando Time Interno
Lari: validar estratégia de canais
Aguardando Cliente
Resolvido
Fechado
Reclamação Imóvel fora do padrão
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Recebimento do ticket na caixa do Zendesk e abertura automática de tarefa no sistema
Avaliar evidências enviadas pelo fotógrafo
Imóvel de fato fora do padrão?
Buscar ID do imóvel e avaliar se houve uma sessão agendada para esse fotógrafo
Havia sessão agendada?
Registrar como procedente selecionando a opção “[AQ] Aprovado?” no formulário de registro e encerrar ticket
Receber a Solicitação 
Cognito



Sim
Sim


@Luana Scorza esse fluxo tem impacto no pagamento do fotógrafo, deveríamos adicionar algo para trigar para payments?





Cognito preenchido por parceiros fotógrafo
Avaliar evidências enviadas pelo fotógrafo
Imóvel de fato fora do padrão?
Sim
Buscar ID do imóvel e avaliar se houve uma sessão agendada para esse fotógrafo no Admin
Houve sessão agendada?
Sim
Registrar como procedente selecionando a opção “[AQ] Aprovado?” no formulário de registro e encerrar o case




Zendesk
Zendesk/LinkCognito
Admin
Zendesk
Não
Não
Coginito preenchido

Abretura automática do ticket
Analisar demanda
Avaliar procedência da queixa
Encerrar tratativa

Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
Não





Zendesk
Zendesk
Admin
Admin/MagicLink
Registrar como demanda indevida e encerrar ticket
Registrar como improcedente selecionando a opção “[AQ] Aprovado?” no formulário de registro e encerrar ticket
Não
Registrar como improcedente selecionando a opção “[AQ] Aprovado?” no formulário de registro e encerrar o case
Encerrar o Case

Zendesk
Zendesk


View
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.


Registrar como demanda indevida
https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/218
Ações nesta fase — Entrada / Contexto (Aberto)
Receber Case via Cognito
Validar dados mínimos e evidências
Confirmar tipo de solicitação
Direcionar: Aguardando Cliente (faltou) ou Em Andamento (ok)
Ações nesta fase — Execução (Em Andamento)
Consultar Admin/MagicLink: ID do imóvel + sessão agendada
Decidir: houve sessão? (Sim/Não)
Preencher [AQ] Aprovado? (Procedente/Improcedente)
Ações nessa fase — Retorno / Encerramento (Resolvido/Fechado)
Responder com Macro
Registrar decisão + evidências
Resolver e fechar
Cognito Forms
Ações nesta fase — Triagem e Coleta (Em Andamento)
Avaliar evidências do fotógrafo
Decidir: fora do padrão? (Sim/Não)
Atualização de dados cadastrais
TO BE
AS IS
Fluxo detalhado
Lari: validar estratégia de canais






Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado




Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento

Receber a Solicitação 
Cognito
Verificar a Solicitaçãoque será realizada

Informações Completas?
Sim
Preencher campos recebibos
Executar alteração no Admin e demais sistemas
Responder cliente no Case(template/macro) + Evidências


Dados comuns (E-mail ou Telefone)
Acesse a planilha da OPS e atualizar os dados do parceiro
Acesse o cadastro do parceiro no admin
Altere os dados cadastrais solicitados e clique em salvar
Localize o template de macro de conformação para envio ao parceiro
Retorne a tarefa do Zendesk e cole o template de macro
Configure o foms lateral do Zendesk e envie como “Resolvido”

Qual critério de infos completas em solicitações com campo aberto?r: dentro do que foi falado, o analista faz esse crivo em contato com o fotógrafo
Não











Fotografo acessa o formulário Cognito
Seleciona a opção "Dúvidas e solicitações sobre contrato de parceria"
Seleciona a opção "Atualização cadastral"
Preenche os dados a serem atualizados/alterados
A solicitação gera automaticamente um ticket no Zendesk
Campo aberto, a solicitação pdoeria ser de qualquer natureza?R: Sim, identificada durante tratativa
Google Sheets
Admin
Admin
Google Docs
Zendesk
Zendesk
Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
Solicitar informacoes ao cliente(responder nos canais)
Qual solicitação de alteração?
Sim





Cognito
Cognito
Cognito
Cognito
Zendesk
Selecione o template de “Termo de Rescisão Voluntário”
Localize o template de macro de conformação para envio ao parceiro
Status = Pending(aguardando retorno)
Encerrar o Case


Alteração de CNPJ
Acesse a planilha da OPS e busque os dados do parceiro
Acesse o cadastro do parceiro no admin
Acesse o DocSign para preparar documentos
Realize o preenchimento com o CNPJ antigo
Clique em salvar/enviar
Selecione o template de “Novo Contrato”
Realize o preenchimento com o CNPJ novo
Clique em salvar/enviar
Retorne a tarefa do Zendesk e cole o template de macro
Configure o foms lateral do Zendesk e envie como “Resolvido”
Termos assinados?
Sim
Acesse a planilha da OPS e atualize os dados do parceiro
Abra uma solicitação no Jira para alteração de dados de CNPJ


















































Cliente retornou?



Google Sheets
Admin
DocSign
DocSign
DocSign
DocSign
DocSign
DocSign
DocSign
Google Docs
Zendesk
Zendesk
Google Sheets
Jira
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.


Não
Não

Comunicar cliente da não resposta (Template)





Termo é expirado sem tratativa/assinatura


Sim
DocSign
Ações nesta fase — Entrada / Contexto
Receber demanda (Cognito 
Criar/receber Case no Salesforce
O analista acessa sua caixa de cases
Acessa individualmente os cases para tratativa.
Analisa informações preenchidas na abertura do caso
Analista entende qual ação será executada:
Verifica se é apenas uma dúvida ou se precisará abrir alguma tarefa ou realizar uma ação.
Ações nesta fase — Triagem e Coleta
Analista analise se os dados estão completos


Ações nesta fase — Execução Google Sheets
Em caso de solicitação de disponibilidade do fotográfo ele realiza dentro do app sheets > time recebe a tratativa > atualiza agenda no admin. 
Dúvidas a respeito de pagamentos alimenta um google sheets para o time de contestação checar e retorna o cliente.
Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
Solicitar descredenciamento ou suspensão de parceria do fotógrafo
AS IS



















Voluntario
Fotografo acessa o formulário Cognito
Seleciona a opção "Encerramento de parceria"
Preenche os dados necessarios e motivo do encerramento
A solicitação gera automaticamente um ticket no Zendesk
Preencha o formulário interno
Replique os dados necessarios e motivo do encerramento
Acesse a área de "Horário Específico" no Admin
Buque a cidade e o nome do parceiro
Bloqueie totalmente a agenda do parceiro
Acesse a "Listagem de Fotos" no Admin e busque pelo e-mail
Marque todos os status e tipos de agendamento para visualização total
Existem jobs agendados?
Sim
Cancele o job manualmente (Motivo: "Fotografo fechou agenda")
Retorne a tarefa do Zendesk e selecione a macro conforme tipo de descredenciamento
Configure o foms lateral do Zendesk e envie como “Resolvido”
Acesse o DocSign para preparar o termo de rescisão
Selecione o template de “Termo de rescisão”
Realize o preenchimento com os dados do parceiro
Clique em salvar/enviar
Após 48h
Acesse a planilha da OPS e localize o cadastro do parceiro
Acesse o cadastro do parceiro no admin
Exclua os bairros de atuação e clique em salvar
























Cognito
Cognito
Cognito
Zendesk
Google Forms
Google Forms
Admin
Admin
Admin
Admin
Admin
Não
Admin
Google Sheets
Zendesk
DocSign
DocSign
DocSign
DocSign
Google Sheets
Admin
Admin
Qual tipo de descredenciamento?



Involuntario
Time de gestão de FT preenche o formulário interno
Preenche os dados necessarios e motivo do encerramento
































Google Forms
Google Forms

Alteração de região de atuação
AS IS













Fotografo acessa o formulário Cognito
Seleciona a opção "Região de Atuação"
Preenche a região atual e a nova região de interesse
A solicitação gera automaticamente um ticket no Zendesk na caixa específica de "Alteração de RC"
Preencha o forumário de desejo de alteração de RC do parceiro
Localize o template de solicitação de de alteração
Retorne a tarefa do Zendesk e cole o template de macro
Configure o foms lateral do Zendesk e envie como “Resolvido”









Cognito
Cognito
Cognito
Zendesk
Google Forms
Google Docs
Zendesk
Zendesk

Não tem essa indicação para o FT, mais vale entender o que ele preenche































Reportar feedback sobre job e/ou cliente
AS IS


Fotografo acessa o formulário Cognito
Seleciona a opção "Elogio, Reclamação ou Sugestão de melhoria"
Preenche os dados e descreve o que deseja reportar
A solicitação gera automaticamente um ticket no Zendesk
Aplice o template/macro de sugestão recebida
Configure o foms lateral do Zendesk e envie como “Resolvido”







Cognito
Cognito
Cognito
Zendesk
Zendesk
Zendesk






Reportar problemas de usabilidade de outras ferramentas do fotógrafo | Reportar problemas de usabilidade do app do fotógrafo
AS IS


Fotografo acessa o formulário Cognito
Seleciona a opção "Problemas com bug"
Preenche os dados e anexa a evidencia
A solicitação gera automaticamente um ticket no Zendesk
Verifique o formulário anexo para identificar o parceiro, cidade e evidencia enviada
Evidencia está correta?
Sim
Verfique qual o tipo de bug/problema o parceiro está reportando
Abra chamado para o time de Produto no Jira anexando as evidências

Preencha o formulário de controle interno
Acompanhe a tratativa do chamado aberto no Jira
Após resposta
Retorne a tarefa do Zendesk e aplique a macro de confirmação
Configure o foms lateral do Zendesk e envie como “Resolvido”











Cognito

Cognito
Cognito
Zendesk
Cognito
MagicLink
Jira
Google Forms
Jira
Zendesk
Zendesk

Não




Retorne a tarefa do Zendesk e aplique a macro de negativa de evidencia
Configure o foms lateral do Zendesk e envie como “Resolvido”



Zendesk
Zendesk
Enviar relatório ou nota fiscal do fotógrafo
AS IS


Fotografo acessa o formulário Cognito
Seleciona a opção "Duvidas sobre remuneração"
Preenche os dados necessarios
A solicitação gera automaticamente um ticket no Zendesk
Verifique o formulário anexo para identificar qual o tipo de solicitação
Qual tipo de solicitação?
Problemas no envio da NF
 Realize o download da Nota Fiscal (NF) em anexo
Acesse o formulário de envio de NF
Preencha os dados do parceiro e anexe o documento baixado
Responda o ticket do zendesk confirmando o uploud
Configure o foms lateral do Zendesk e envie como “Resolvido”














Cognito
Cognito
Cognito
Zendesk
Cognito
Zendesk
Google Forms
Google Forms
Zendesk
Zendesk






Solicitação de relatório
Pesquise o parceiro pelo e-mail na base de fechamento
Realize o download do relatório individual em PDF
Responda o ticket anexando PDF e informando data limite da NF
Configure o foms lateral do Zendesk e envie como “Resolvido”






Google Sheets
Google Sheets
Zendesk
Zendesk
Dúvidas, informações ou contestações sobre pagamento do fotógrafo
AS IS


Fotografo acessa o formulário Cognito
Seleciona a opção "Duvidas sobre remuneração"
Preenche os dados necessarios
A solicitação gera automaticamente um ticket no Zendesk
identifique o imóvel e o período reclamado no formulário
Pesquise o e-mail do parceiro e o código do imóvel no relatório do mês
Dúvida ou contestação?
Contestação
O job está no relatório?
Sim
Aplique a macro orientando onde localizar o valor
Configure o foms lateral do Zendesk e envie como “Resolvido”









Cognito
Cognito
Cognito
Zendesk
Cognito
Google Sheets
Dúvida
Não
Zendesk
Zendesk

Transferir ticket para caixa: Cotestações Fotos [PRE] [FRONT]
Busque o código do imóvel e data no Admin e MagicLink
Verifique o status do job, logs de envio e análise do anuncio
Verifique as informações do imóvel no MagicLink
Calcule o valor devido na calculadora interna
Acesse o jira de remuneração e abrir "Inclusão de novos valores"
Preencha os dados do FT, Mês de referência, código e dados da vistoria
Realize a aprovação manual do chamado aberto
Aplique a macro de confirmação (Informa que cairá no próximo relatório)
Configure o foms lateral do Zendesk e envie como “Resolvido”





A contestação é procedente?
Sim











Zendesk
Admin/MagicLink
Admin/MagicLink
Não
MagicLink
Google Sheets
Jira
Jira
Jira
Zendesk
Zendesk

Aplique a macro de negativa (ex: vistoria não realizada/sem provas)
Configure o foms lateral do Zendesk e envie como “Resolvido”



Analista lê as dúvidas relatadas
Analista responde ticket e envia como resolvido


Zendesk
Zendesk

Zendesk
Zendesk
Solicitar correção/alteração de dados bancarios do fotógrafo
AS IS








Fotografo acessa o formulário Cognito
Seleciona a opção "Alteração de cadastro"
Preenche os dados necessarios

A solicitação gera automaticamente um ticket no Zendesk

Abra chamado de: "Alteração de dados cadastrais SAP"

Preencha CNPJ, dados bancários novos, chave Pix e anexe o comprovante recebido

Busque o parceiro na planilha OPS

Atualize os dados bancários na OPS
Busque o cadastro do parceiro via ID ou e-mail para edição

Clique em "Editar dados", atualize os campos bancários e clique em "Salvar"

Registrar tratativa e enviar ticket como resolvido do ticket + macro


















Cognito
Cognito
Cognito
Zendesk

Jira
Jira
Google Sheets
Google Sheets

Admin

Admin
Zendesk














Dúvidas/informações sobre placas e/ou lockbox
AS IS








Fotógrafo acessa o formulário Cognito (via link ou direcionamento do chat)
Seleciona a opção de assunto referente a Material de Apoio / Placas




Analista acessa o site da fornecedora logística (Gtex ou Gelog)


Localiza o pedido pelo CPF/CNPJ ou número do pedido e verifica o status/rastreio
Retorna ao Zendesk e redige a resposta com o status ou código de rastreio



Preenche os dados de identificação e o motivo da dúvida
A solicitação gera automaticamente um ticket na caixa de entrada
Analista abre o ticket e identifica o parceiro e o pedido
Configura o formulário lateral e envia como “Resolvido”


















Cognito
Cognito
Cognito
Zendesk
Zendesk
Web
Site Logística
Zendesk
Zendesk















Solicitar ajuda para subir fotos/vídeos
AS IS








Fotógrafo acessa o formulário Cognito após falha de upload no app
Seleciona a opção "Ajuda para subir fotos/vídeos" e anexa o link do Drive
A solicitação gera automaticamente um ticket na caixa de suporte
Analista abre o link do Drive enviado para validar se os arquivos estão lá
Tudo certo com drive?
Sim
Analista abre o formulário interno de Qualidade/Listing Quality (LQ)
Preenche os dados do imóvel e cola o link do Drive para o time de LQ atuar
Retorna ao Zendesk e informa ao fotógrafo que o material será subido em até 48h
Altera o status do ticket para "Em Espera" (até a confirmação do upload pela LQ)
Após confirmação do upload, configura o forms lateral e envia como “Resolvido”










Cognito
Cognito
Zendesk
Google Drive


Não

Cognito

Cognito


Zendesk
Zendesk


Zendesk











O sistema exibe a mensagem "Você precisa de acesso" ou a pasta está vazia
Analista clica no botão de "Solicitar Acesso" (para gerar notificação ao dono)
Retorna ao Zendesk e escreve para o fotógrafo informando que o link está bloqueado
Altera o status do ticket para "Aguardando Resposta"









Google Drive
Google Drive


Zendesk






Zendesk
Suporte Outsourcing [Suporte Outsourcing]
Visualizar
AS IS
TO BE
Macro fluxo
Fluxo detalhado
Fluxo detalhado
Lari: validar estratégia de canais

Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado
https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/243

Cognito Forms
Suporte Outsourcing
Fonte de Entrada: Analistas de BPO (Actionline | AeC) ou Time WH (CRM).
Quem Trata: FUP Fotos Interno
Resumo Geral: Funciona como um suporte técnico operacional. O parceiro externo preenche este cognito quando não tem permissão sistêmica para concluir uma ação ou quando o sistema apresenta erro.
Principais Ações: Cancelar sessões, forçar o fechamento de tarefas travadas no CRM, corrigir dados cadastrais que o parceiro não consegue editar e tratar demandas específicas do RS.


O analista da BPO preenche o formulário Cognito: Suporte Outsourcing

Geração automática do ticket na caixa Agendamento de Fotos - FUP [SO] no Zendesk

Conferir se os dados do Cognito (ID, CPF, E-mail) coincidem com o cadastro no sistema

Os dados fornecidos permitem a localização do imóvel?
Sim
Qual solicitação relizada no cognito?
Cancelar sessão ou reagendar
Registrar o comentário da tratativa no CRM e responder ao solicitante


Fim do fluxo


Contexto
Triagem e Coleta de Dados
backlog: deveríamos ter um SLA para fechamento automático?
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento

















Início do fluxoParceiro (Actionline/AeC) ou o time WH identifica necessidade de ajuste técnico ou cancelamento manual
Cognito
Zendesk
Zendesk e Magic Link

Admin (Aba Câmera)
Zendesk
Receber a Solicitação 
Cognito
Não


Informações Completas?

Sim
Preencher campos recebibos



Preenchimento do formulário Cognito pela BPO com ID do imóvel e justificativa
Recebimento do ticket na caixa do Zendesk e abertura automática de tarefa no sistema
Validação de segurança dos dados (ID, E-mail, CPF) e análise do cenário solicitado
Os dados fornecidos permitem a atuação técnica?
Atuação manual nos sistemas internos de acordo com a necessidade
Registro formal da tratativa no histórico do imóvel para fins de auditoria
O ticket chega com os dados obrigatórios: ID do imóvel, nome do proprietário, e-mail e os 3 primeiros dígitos do CPF. * O motivo da solicitação deve estar claro (Cancelar sessão, Alterar dados ou Finalizar tarefa no CRM).
Abra o ticket no Zendesk e copie o ID do imóvel. * No Magic Link, cole o ID na busca para validar o proprietário
Buscar o ID ou Telefone no Magic Link para validar se houve erro de digitação

Entre em contato com o solicitante para buscar os dados corretos





No Admin, acesse a aba Câmera.
Localize o Job através do ID do imóvel e clique no ícone da Lixeira (Delete) na barra amarela.
Selecione o motivo do cancelamento e confirme.
Caso haja uma nova data solicitada, clique em "Agendar Job fotógrafo", escolha o horário disponível no Planner e finalize o agendamento.
No Magic Link/CRM: Clique no ícone de diálogo azul na tarefa e registre: [WH] - Tratativa realizada via Suporte Outsourcing - [Descrever ação]. 
No Zendesk: No campo Formulário, mantenha Agendamento de Fotos FUP. * No Zendesk: No campo Origem da tarefa, selecione Suporte Outsourcing. 
Finalização: Insira obs interna no ticket de acordo com o cenário e mude o status para Resolvido
Não




S
Finalização do ticket no Zendesk

Fim do fluxo
Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito









Início do fluxoIdentificação de falha sistêmica ou necessidade de ajuste técnico por times externos (Actionline/AeC).
Cognito
Zendesk
Zendesk
Admin, CRM ou MagicLink
CRM ou MagicLink
Zendesk
MagicLink
Grupo WhatsApp/Gchat
Sim
Solicitar informacoes ao cliente(responder nos canais)

Sim

N
Busque pelo telefone ou e-mail no MagicLink, se o erro persistir, use o Twilio para enviar um WhatsApp ao proprietário solicitando os dados corretos.

Realizar o cancelamento/agendamento, correção cadastral ou fechamento manual de tarefas travadas
Alterar/Incluir informações de cadastro
Verificar a alteração que será realizada
Status = Pending(aguardando retorno)
Encerrar o Case




Iniciar Follow-ups com o cliente para obter os dados corretos via Touch points (WhatsApp/E-mail)
Admin (Aba Imóveis)
Cliente retornou?





O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
No Admin, acesse a aba Imóveis e busque pelo ID.
Clique no ícone da Engrenagem para abrir a página "Detalhes do imóvel".
Altere as informações necessárias (CEP, Rua, Número, Complemento ou Bairro).
Role até o fim da página e clique obrigatoriamente em "Salvar dados e continuar".
Não
Twillio/Zendesk
É um fechamento de tarefa?
Comunicar cliente da não resposta (Template)
Executar alteração no CRM Quinto Andar
Sim
Não
Executar alteração no Admin
Responder cliente no Case(template/macro)
Finalizar tarefa no CRM (Tarefa travada)
Magic Link / CRM Tarefas
Ações nesta fase — Entrada / Contexto
Receber demanda (Cognito 
Criar/receber Case no Salesforce
O analista acessa sua caixa de cases
Acessa individualmente os cases para tratativa.
Analisa informações preenchidas na abertura do caso
Analista entende qual ação será executada:
Agendamento
Alterar informações do cadastro
Cancelamento
Reagendamento
Fechamento de tarefa
Ações nesta fase — Triagem e Coleta
Analista analise se os dados estão completos
Analista solicita os dados faltantes para execução via call (twillio) / Ezsend

Ações nesta fase — Execução (Admin)
Abre a página do admin QuintoAndar
Clica na aba de fotográfo 
Inseri o ID do imóvel
Executa a tarefa e salva
Ações nesta fase — Execução (CRM)
Abre a página do CRM QuintoAndar
Clica na tarefa de FUP Fotos 
Clica em abandonar cadastrou ou marcar como feito
Executa a tarefa e salva
Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
No CRM Tarefas, pesquise o ID de 9 dígitos e selecione a opção "Todos".
Identifique a tarefa pendente (ex: "Agendar Job" ou "Fup Fotos").
Clique na tarefa e selecione a opção "Marcar como feito" (para Agendar Job) ou "Abandonar cadastro" (para Fup Fotos) para encerrar a pendência manual.
Reagendamento [Solicitações de Reagendamento - FUP Fotos]
Visualizar
AS IS
Macro fluxo
Fluxo detalhado

Lari: validar estratégia de canais
https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/244

Cognito Forms







Solicitações de Reagendamento - FUP Fotos
Fonte de Entrada: Time Interno QuintoAndar
Quem Trata: CNX Fup Fotos
Resumo Geral: É o fluxo de recuperação de agenda. Ocorre quando o agendamento original foi "quebrado" por motivos internos da empresa ou falha do parceiro fotógrafo.
Principais Ações: Tratar casos de fotógrafos descredenciados ou que fecharam a agenda de última hora. O objetivo é realizar o contato ativo via Twillo e garantir que o imóvel não fique parado no "funil", reagendando preferencialmente em D+2.
Time da Rede preenche o Cognito: Solicitações de Reagendamento - FUP Fotos
Geração automática do ticket na caixa Agendamento de Fotos - FUP [SO] no Zendesk
Validar o motivo do reagendamento e o status atual do Job no Admin
Registrar o histórico final e enviar a comunicação de encerramento ao proprietário/solicitante


Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado





O Job anterior ainda consta como "Agendado" no Admin?

Sim
Localizar a barra amarela do Job no Admin
Realizar a chamada ativa para o proprietário (até 3x ao dia)
Qual o desfecho do contato?
Contato com o proprietário


Realizar a reserva do horário no sistema


Fim do fluxo





Proprietário atende (Sucesso no contato)


Variação A: Novo agendamento (Agenda disponível)














Início do fluxoO time interno identifica a necessidade de fechar uma agenda, descredenciar um parceiro ou tratar um imprevisto

Cognito
Zendesk
Zendesk e Admin (Aba Câmera)
Admin
Twillio
Twillio
Admin (Aba Câmera)
Zendesk e CRM/Magic Link
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Não
O ticket aparece na caixa Agendamento de Fotos - FUP [SO].
Os dados do imóvel e proprietário são carregados automaticamente no discador Olos.
No Admin, insira o ID do imóvel e busque o Job ativo
No Admin, insira o ID do imóvel e busque o Job ativo (barra amarela).
Clique no ícone de Lixeira (Delete), selecione o motivo do cancelamento e confirme a exclusão.
Verifique no Magic Link se há outras tarefas duplicadas ou pendências que possam travar o novo agendamento
Aplique a sondagem para confirmar endereço, chaves e se haverá acompanhante. Caso relate NoShow do fotógrafo anterior, use o Pitch de Desculpas: "Pedimos desculpas pelo ocorrido! Isso se distancia da experiência que trabalhamos para proporcionar...".
No Admin, clique em "Agendar Job fotógrafo".
Insira o ID do imóvel e busque o Job.
No Planner, escolha um horário verde (preferencialmente D+2).
Confirme o fotógrafo e finalize.
No CRM/Magic Link: Clique no ícone de diálogo azul no histórico da tarefa e escreva o resumo da tratativa (Ex: [WH] - Sucesso no reagendamento para o dia XX/XX às XX:XXh). Clique em Salvar.
No Zendesk (Ticket): No campo Formulário, certifique-se de que a opção Agendamento de Fotos FUP está selecionada.
No Zendesk (Origem): No campo Origem da tarefa, selecione a opção Solicitações de Reagendamento - FUP Fotos.
No Zendesk (Resposta): Aplique a macro de fechamento adequada ao desfecho (Sucesso ou Abandono) para notificar o proprietário por e-mail.
No Zendesk (Status): Altere o status do ticket para Resolvido e clique em Enviar.
Na Twillio: Finalize a tabulação da chamada para liberar o sistema para o próximo atendimento.
Receber a Solicitação 
Cognito / Time interno
Qual o desfecho do contato?








Variação A: Novo agendamento (Agenda disponível)









O Job anterior ainda consta como "Agendado" no Admin?
Proprietário atende (Sucesso no contato)

Sim
Localizar a barra amarela do Job no Admin


Variação B: Solicitação de encaixe (Sem agenda ou Urgência)
Solicitar apoio para alocar um fotógrafo manualmente
Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
 Twillio
Realizar a reserva do horário no sistema Admin
 Registrar o histórico final e enviar a comunicação de encerramento ao proprietário/solicitante Template




Validar o motivo do reagendamento
Variação B: Solicitação de encaixe (Sem agenda ou Urgência)



Proprietário não atende (Inalcançável)

Envio de FUP ao proprietário
Proprietário não atende (Inalcançável)

Appsheet (Support Photos)
Sim



O solicitante preenche o Cognito: Solicitações de Reagendamento - FUP Fotos
Geração automática do ticket na caixa Agendamento de Fotos - FUP [SO] no Zendesk
Validar o motivo do reagendamento e o status atual do Job no sistema
 O Job anterior ainda consta como "Agendado" no Admin?
Realizar cancelamento manual para liberar a agenda
Realizar a chamada ativa via discador (até 15 tentativas)
Executar o novo agendamento, agendamento futuro ou abandono
Registrar o comentário da tratativa no CRM e finalizar o ticket no Zendesk
Preencher o Cognito Gestão de Fotógrafos em casos de NoShow ou má conduta do parceiro
Zendesk




S

Fim do fluxo
Clique em [+Add] no Appsheet.
Preencha: Time, Motivo (Falta de Planner ou NoShow) e ID do Imóvel.
Informe se é Job SOS (PP aguardando no local).
Avise o PP sobre o SLA de 2 horas para retorno.









Início do fluxoTime interno identifica necessidade de reagendar devido a descredenciamento, imprevisto do fotógrafo ou fechamento de agenda.
No Zendesk, clique no ícone de "Aplicativos" à direita FUP Fotos]. Selecione o template reagendamento_fotos_fup1 FUP Fotos]. Preencha os campos de Parâmetro (Nome, Endereço) e clique em Enviar FUP Fotos].
Realizar a chamada ativa para o proprietário (até 3x ao dia) Twillio

Variação C: Abandono de cadastro (Desistência definitiva)


Envio de FUP ao proprietário

Cognito
Zendesk
Zendesk e Admin (Aba Câmera)
Zendesk e Admin (Aba Câmera)
Discador Olos (Campanha: WEBHELP_REAGENDAMENTO)
Zendesk e Admin (Aba Câmera)
Zendesk e Admin (Aba Câmera)
Cognito
O pedido é elegível para uma nova sessão gratuita?
N
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
O ticket chega com o ID do imóvel e o motivo específico (Fechamento de agenda, Descredenciamento, Funil ou Imprevisto).
Os dados do proprietário são integrados ao mailing do discador Olos para início das tentativas de contato ativo.
No Admin, insira o ID do imóvel e busque o Job ativo (barra amarela).
Clique no ícone de Lixeira (Delete), selecione o motivo do cancelamento e confirme a exclusão.
Verifique no Magic Link se há outras tarefas duplicadas ou pendências que possam travar o novo agendamento
Se não atender: No Zendesk, abra o painel de Aplicativos (lado direito) -> Selecione template reagendamento_fotos_fup1 -> Preencha os Parâmetros e clique em Enviar FUP Fotos].
Se houver atrito: Use o Pitch de Desculpas: "Pedimos desculpas pelo ocorrido! Isso se distancia da experiência que trabalhamos para proporcionar...".
Sondagem: Confirme se o PP ou um terceiro acompanhará a sessão e reforce os benefícios do anúncio gratuito.
Novo Agendamento: No Admin, clique em "Agendar Job fotógrafo" -> Selecione o horário no Planner (prioridade D+2) -> Confirme o parceiro
Agendamento Futuro (>9 dias): Use a função Snooze no CRM e preencha o formulário de Agendamentos Futuros
Abandono: No Admin, selecione o ícone de cancelamento -> Delete -> "Cadastro Abandonado" e descreva o motivo.
No Magic Link: Clique no ícone de diálogo azul na tarefa -> Registre o resumo (ex: [WH] - Reagendado para dia XX/XX) -> Salvar.
No Zendesk: Selecione a Origem da tarefa como Solicitações de Reagendamento - FUP Fotos -> Aplique a macro de resposta -> Altere para Resolvido.
No Olos/Eaglle: Tabule a chamada corretamente para liberar o sistema.
Não
Agendar um retorno futuro para quando o imóvel estiver pronto
Preenche o Cognito: Agendamento/ Reagendamento Futuro

O analista da BPO preenche o formulário Cognito: Suporte Outsourcing
Variação D: Reforma ou indisponibilidade temporária (Snooze)


Variação C: Abandono de cadastro (Desistência definitiva)

Proprietário atende, mas desiste/recusa



Proprietário atende, mas desiste/recusa

Contato com o proprietário
Encerra o case informando o proprietário

Cognito

Twillio
 Twillio
Variação E: PP envia fotos [FotosPP - Piloto LQ <> FUP]
Preenche o forms [Pré Registro - Fotos PP] via Cognito

Questione o motivo real ("O que impede de anunciar hoje?"). Se o motivo for reforma, verifique o prazo (menos ou mais de 30 dias).
Variação D: Reforma ou indisponibilidade temporária (Snooze)
Agendar um retorno futuro para quando o imóvel estiver pronto
Preenche o Cognito: Agendamento/ Reagendamento Futuro


CRM Tarefas
Cognito
Ações nesta fase — Entrada / Contexto
Status principal: AbertoO que acontece:
Case entra via Cognito (Solicitações de Reagendamento – FUP Fotos) e cai na fila (Omni/Queue).
Owner atribuído (analista assume).
Analista abre o Case e confere rapidamente:
ID do imóvel, motivo do reagendamento, dados do PP (telefone/e-mail), evidências/observações.
Se existe indicação de no-show / fechamento de agenda / descredenciamento.
Define o “tipo de tratativa” dentro do fluxo de reagendamento:
Novo agendamento (Variação A)
Encaixe / SOS (Variação B – Appsheet)
Abandono (Variação C)
Futuro/Snooze (Variação D)
FotosPP (Variação E)
Saída da fase:
Vai para Em Andamento (quando já dá para atuar), ou
Vai para Aguardando Cliente (se faltam dados do PP), ou
Vai para Aguardando Time Interno (se depende de Appsheet/Tools/operação).
2) Ações nesta fase — Triagem e Coleta
Status principal: Em Andamento (ou Aguardando Cliente/Time Interno, conforme o caso)O que acontece:
Validar se os dados estão completos para executar:
Job existe e está “Agendado” no Admin? (barra amarela)
PP tem contato válido (telefone/WhatsApp/e-mail)?
Motivo do reagendamento está claro (ex.: fechamento de agenda, descredenciamento, funil, imprevisto)?
Se faltou informação do PP:
registrar tentativa e mover para Aguardando Cliente.

3) Ações nesta fase — Execução
Status principal: Em AndamentoO que acontece (execução real):
Admin (Aba Câmera):
Buscar o Job ativo do imóvel.
Se Job anterior ainda “Agendado”: cancelar/deletar para liberar agenda (motivo correto).
Agendar novo Job: abrir Planner, escolher slot (prioridade D+2 quando aplicável), confirmar fotógrafo.
Contato com PP (Twillio/WhatsApp/Discador, conforme estratégia):
Fazer tentativas conforme regra (ex.: 3 tentativas).
Confirmar endereço, chaves/acompanhante, alinhamento.
Variações:
B (Encaixe/SOS): abrir Appsheet e solicitar alocação manual.
C (Abandono): cancelar job/tarefa e registrar motivo.
D (Futuro/Snooze): aplicar Snooze no CRM + registrar reabertura (se esse mecanismo for mantido no SF).
E (FotosPP): direcionar para o Cognito FotosPP e seguir o fluxo (gera caso/registro conforme regra definida).
Saída da fase (por status):
Se concluiu execução e já comunicou: Resolvido.
Se ficou pendente de retorno do PP: Aguardando Cliente.
Se ficou pendente do encaixe/time: Aguardando Time Interno.
4) Ações nesta fase — Retorno ao Cliente / Encerramento
Status principal: Resolvido → Fechado (e Reaberto se voltar)O que acontece:
Registrar Resumo da tratativa (o que foi feito + data/horário agendado ou decisão).
Enviar comunicação ao PP via Template/Macro (confirmação, FUP, negativa, abandono, etc.).
Anexar/registrar evidências necessárias (ex.: prints, referência do job).
Marcar Resolvido.
Fechado ocorre automaticamente conforme regra.
Se PP responder/contestar: Reaberto → volta para Em Andamento (ou Aguardando Cliente se faltou info).

No CRM, localize a tarefa aberta.
Use a função Snooze e defina a data acordada com o proprietário.
Certifique-se de que a tarefa está marcada como "Snoozada" para não voltar ao mailing antes da hora.
Variação E: PP envia fotos [FotosPP - Piloto LQ <> FUP]
Preenche o forms [Pré Registro - Fotos PP]

Cognito
Problema na Agenda (PP Multi, sem agenda aos sábados ou não conseguiu agendar em 4 dias)

Lari: validar estratégia de canais
Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado
AS IS
Para reagendamento e reagendamento a abertura é realizada pele Time de Vendas (IS ou CIQ) 
Para sem agenda oas sabados ou não conseguiu agendar em 4 dias o cognito é aberto pelo time BPO
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
View
Whatsapp business
Receber a Solicitação 
Cognito
Analisar dados de códigos de imóveis e informações de fotógrafo

Foi solicitado um fotógrafo específico?
Sim
Realizar contato com fotógrafo para cobinar sessão pelo Whatsapp (Twillio)





Agendar sessões de fotos para o dia combinado para cada um dos imóveis no Admin

Macro fluxo
Fluxo detalhado
Temos mais solicitações dentro desse fluxo [Cognito]
Não



Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito os cases devem ser distribuidos via Omini Channel
Fotógrafo aceitou?

Fotógrafo Tem agenda?
Sim

Realizar contato com fotógrafo para combinar sessão de fotos
Registrar sucesso no agendamento como “Observações Internas” Chatter Salesforce
Incluir propriedade para registrar id do IM em caso de sucesso

@felipe.moura ID do IM ou da sessão?

Buscar fotógrafo com agenda mais livre no Admin

https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/256
Cognito Forms
Não

Combinar com fotógrafo ida no dia combinado
Agendar sessões de fotos para o pimeiro dia com agenda disponível


Não
Agendamento/Reagendamentos PP Multi
Fonte de Entrada: Preenchimento de cognito pelo parceiro BPO e áreas de atendimento em geral.
Quem Trata: Analistas de FUP Fotos.
Resumo Geral: É o fluxo de supoerte a agendamentos de sessões para vários im[oveis de um PP Multi.
Principais Ações: Validar informações do cogniti, bscar agendar e fotógrado, agendar sessões no admin, dar a devolutiva da tratativa no fluxo..


O robô direciona o ticket automaticamente para a fila de atendimento no Zendesk na data programada





Analisar dados de códigos de imóveis e informações de fotógrafo

Foi específicado um fotógrafo específico?
Sim
Realizar contato com fotógrafo para combinar sessão
Fotógrafo aceitou?

Sim
Necessário incluir região para o fotógrafo?
Não
Fotógrafo tem agenda para data combinada?
Sim
Agendar sessões de fotos para o dia combinado
Backlog: esse fluxo não deveria ser possível via produto?
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.








Início do fluxoTime de Vendas (IS ou CIQ) preenche cognito como agendamento de múltiplos imóveis
Zendesk
Zendesk
WhatsApp
Admin
Registrar sucesso no agendamento como “Observações Internas”

Sim
Não

Não

Fim do fluxo
Buscar fotógrafo com agenda mais livre
Zendesk





Incluir região da sessão na página de usuário para o fotógrafo
Agendar sessões de fotos para o primeiro dia com agenda disponível
Ticket aberto automáticamente via integração zapier
Análise de códigos dos imóveis e preferência de fotógrafo
Agendar sessões individualmente para cada imóvel
Admin
Sim
Ainda temos fotógrafos disponíveis na região?
Combinar com fotógrafo ida no dia combinado




Contarar fotógrafo para combinar sessão
Registrar tratativa e encerrar ticket

Fim do fluxo






Início do fluxoPreenchimento do cognito para agendamento de múltiplos imóveis
Admin
WhatsApp
Admin
Ações nesta fase — Entrada / Contexto
Receber demanda (Cognito 
Criar/receber Case no Salesforce
O analista acessa sua caixa de cases
Acessa individualmente os cases para tratativa.
Analisa informações preenchidas na abertura do caso
Analista entende qual ação será executada:
Agendamento
Alterar informações do cadastro
Cancelamento
Reagendamento
Ações nesta fase — Triagem e Coleta
Analista analise se os dados estão completos
Analista solicita os dados faltantes para execução via call (twillio) / Ezsend

Ações nesta fase — Execução (Admin)
Abre a página do admin QuintoAndar
Clica na aba de fotográfo 
Inseri o ID do imóvel
Executa a tarefa e salva

Zendesk
Zendesk
WhatsApp
Admin
Zendesk
Não
Ações nessa fase: 
Responder ao cliente (Template/ Macro)
Encerrar o Case
Ainda temos regiões próximas para buscar encaixe?
Não
Registrar impossibilidade de agendamento como “Observasões internas” e enviar ticket como “Resolvido”


Realizar o agendamento da sessão

Fim do fluxo
Zendesk
Admin
Sim


Buscar bairro/município mais próximo
Remover região incluída da página de usuário
GoogleMaps
Admin

Procurar código de região pelo nome do bairro/município na planilha “Dados FT”
GoogleSheets
Agendamento/ Reagendamento Futuro [Agendamento/Reagendamentos Futuros]
Lari: validar estratégia de canais
AS IS


View

Aberto
Em Andamento
Aguardando Time Interno
Aguardando Cliente
Resolvido
Fechado
Macro fluxo
Fluxo detalhado
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Realizar o adiamento da tarefa no CRM para pausar o mailing
Não

O case é reaberto no Salesforce  na data programada

Realizar 3 tentativas de contato telefônico para confirmar se a data e o horário ainda estão mantidos Twillio
PP atendeu?


Sim

PP aceitou data e horário?

Sim
Variação A: Realizar a reserva do horário no Admin
Responder cliente no Case(template/macro)








https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/444
Receber a Solicitação 
Cognito
Variação C: Abandono de cadastro (Desistência definitiva)
Cognito Forms






Encerrar o case
Agendamento/Reagendamentos Futuros
Fonte de Entrada: Time WH (WebHelp) via atendimento ativo/receptivo.
Quem Trata: Analistas de FUP Fotos.
Resumo Geral: É o fluxo de gestão de fila a longo prazo. Utilizado quando o proprietário quer as fotos, mas não pode nos próximos 9 dias (limite do sistema Admin).
Principais Ações: Validar a necessidade (ex: reforma ou viagem), realizar o Snooze da tarefa no CRM e programar a reabertura do ticket para D-2 da data escolhida. Na reabertura, o analista confirma com o proprietário e oficializa o agendamento no Admin.
O analista preenche o Cognito: Agendamento/Reagendamentos Futuros para registrar a solicitação
O robô direciona o ticket automaticamente para a fila de atendimento no Zendesk na data programada
Realizar 3 tentativas de contato telefônico para confirmar se a data e o horário ainda estão mantidos
Notificar o cliente sobre o agendamento concluído e atualizar o CRM
O analista da BPO preenche o formulário Cognito: Suporte Outsourcing




Realizar o adiamento da tarefa no CRM para pausar o mailing






Qual o desfecho do contato?
Variação A: Agendamento após sucesso ou não da ligação

Realizar a reserva do horário no sistema


Fim do fluxo





Variação B: Solicitação de encaixe (Sem agenda ou Urgência)











Início do fluxoProprietário informa que só poderá receber o fotógrafo após o 10º dia (ex: devido a reformas, viagens ou saída de inquilino).
Retirar o imóvel do mailing ativo do discador e Criam case no Salesforce via cognito
Variação D: PP envia fotos [FotosPP - Piloto LQ <> FUP]
backlog: transferir ticket automaticamente para outras filas

CRM Tarefas / MagicLink
Cognito
Zendesk
Twillio
Admin (Aba Câmera)
Zendesk
Solicitar apoio para alocar um fotógrafo manualmente AppSheet

Preenche o forms [Pré Registro - Fotos PP]
Definir a data de reabertura do ticket para garantir o agendamento no momento certo.
Colete com o PP 3 opções de horários para a data futura desejada.
No formulário Cognito, preencha: ID do imóvel, E-mail do PP, 3 primeiros dígitos do CPF e as datas/horários acordados.
Importante: Defina a "Data de reabertura do ticket" para D-2 (dois dias antes da data escolhida para a sessão).

No Admin, clique em "Agendar Job fotógrafo".
Insira o ID do imóvel e busque o Job.
No Planner, escolha o dia/horário verde/amarelo 
Confirme o fotógrafo e finalize.
No Zendesk, aplique a macro de "Agendamento Realizado".
Verifique se os dados do fotógrafo (Nome, Telefone, RG) foram carregados e envie ao cliente.
No campo Origem da tarefa, selecione Agendamento/Reagendamentos Futuros.
Altere o status do ticket para Resolvido.
No Magic Link, registre: [WH] - Agendamento futuro realizado para dia XX/XX.




No CRM, localize a tarefa do imóvel e utilize a função Snooze.
No formulário Cognito, preencha a Data de reabertura do ticket como D-2 em relação à data do agendamento (ex: se o agendamento for para o dia 25, a reabertura deve ser no dia 23).
Certifique-se de preencher o e-mail e os 3 primeiros dígitos do CPF para fins de segurança.
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.
Variação E: Reforma ou indisponibilidade temporária (Snooze)

Preenchimento do Cognito: Agendamento/Reagendamentos Futuros
Retirar o imóvel do mailing ativo do discador e reagendar ticket zendesk
O ticket reabre na caixa do Zendesk e a tarefa "desperta" no CRM na data programada

Realizar 3 tentativas de contato telefônico para confirmar o agendamento
Executar o novo agendamento, agendamento futuro ou abandono
Registrar o comentário da tratativa no CRM e finalizar o ticket no Zendesk

Fim do fluxo
Solicitar apoio para alocar um fotógrafo manualmente









Início do fluxoPP solicita data além do horizonte visível do Planner (10+ dias)
Variação B: Solicitação de encaixe (Sem agenda ou Urgência)

Cognito
CRM Tarefas / MagicLink e Zendesk
Zendesk
Discador Olos (Campanha: WEBHELP_REAGENDAMENTO)
Zendesk e Admin (Aba Câmera)
Zendesk e Admin (Aba Câmera)

Appsheet (Support Photos)
No formulário, defina a Data de reabertura do ticket para D-2 em relação à data da sessão.
O ticket gerado no Zendesk entrará em status de espera automatizada pelo sistema.
Localize a tarefa no Magic Link e aplique a função Snooze para a mesma data de reabertura do ticket (D-2)
Isso garante que o PP não receba ligações automáticas do mailing durante a espera
Caso o PP não atenda após as 3 tentativas, o analista deve prosseguir com o agendamento baseado no combinado do primeiro contato.
Novo Agendamento: No Admin, clique em "Agendar Job fotógrafo" -> Selecione o horário no Planner (prioridade D+2) -> Confirme o parceiro
Agendamento Futuro (>9 dias): Use a função Snooze no CRM e preencha o formulário de Agendamentos Futuros
Abandono: No Admin, selecione o ícone de cancelamento -> Delete -> "Cadastro Abandonado" e descreva o motivo.
No Magic Link: Clique no ícone de diálogo azul na tarefa -> Registre o resumo (ex: [WH] - Reagendado para dia XX/XX) -> Salvar.
No Zendesk: Selecione a Origem da tarefa como Solicitações de Reagendamento - FUP Fotos -> Aplique a macro de resposta -> Altere para Resolvido.
No Olos/Eaglle: Tabule a chamada corretamente para liberar o sistema.
Clique em [+Add] no Appsheet.
Preencha: Time, Motivo (Falta de Planner ou NoShow) e ID do Imóvel.
Informe se é Job SOS (PP aguardando no local).
Avise o PP sobre o SLA de 2 horas para retorno.
Ações nesta fase — Entrada / Contexto
Receber solicitação via Cognito (Agendamento/Reagendamentos Futuros) e criar/receber Case no Salesforce.
Analista acessa a fila/Omni e abre o Case.
Conferir campos mínimos: ID imóvel, e-mail PP, 3 dígitos CPF, datas/horários, Data de reabertura (D-2).
Identificar que é Reagendamento Futuro (>9 dias).
Ações nesta fase — Triagem e Coleta
Analista analise se os dados estão completos
Analista solicita os dados faltantes para execução via call (twillio) / Ezsend
Ações nesta fase — Execução (CRM/MagicLink + Discador + Admin)
No CRM/MagicLink: aplicar Snooze da tarefa para D-2 (mesma data de reabertura do Case) para pausar mailing.
Garantir que o imóvel/tarefa fique fora da campanha do discador durante a espera (conforme regra atual).
Mover o Case para Aguardando Time Interno até D-2.
Em D-2 (reabertura): realizar 3 tentativas de contato.
Se necessário: no Admin (Aba Câmera) executar o desfecho:
Novo agendamento, ou
Novo reagendamento futuro (novo Snooze), ou
Abandono (cancelar/delete e motivo).
Registrar resumo no CRM/MagicLink e responder PP (macro/template).
Encerrar o Case (Resolvido → Fechado).
O analista da BPO preenche o formulário Cognito: Suporte Outsourcing
Ações nesta fase — Triagem e Coleta de Dados
Validar se os dados estão completos e coerentes (datas no futuro, D-2 correto).
Se faltar dado: solicitar complemento ao PP (canal padrão) e mover para Aguardando Cliente.
Se OK: seguir execução e registrar observações internas.
Variação C: Abandono de cadastro (Desistência definitiva)


Cognito
Variação D: PP envia fotos [FotosPP - Piloto LQ <> FUP]
Preenche o forms [Pré Registro - Fotos PP]

Cognito
Variação E: Reforma ou indisponibilidade temporária (Snooze)
Pedido de reagendamento ou solicitação de novas fotos
FAQ QuintoAndar [Pedido de reagendamento ou solicitação de novas fotos]
cognitoforms.com
FAQ QuintoAndar (Novas Fotos / Reagendamento)
Fonte de Entrada: O próprio Proprietário (PP) via formulário de autoatendimento no site/app.
Quem Trata: Analistas da CNX de FUP Fotos (Caixa de Tickets Zendesk).
Resumo Geral: É a demanda direta do cliente. Geralmente são proprietários com imóveis já publicados que querem renovar o anúncio ou que tiveram um imprevisto e usaram o canal de ajuda para pedir reagendamento.
Principais Ações: Validar se o imóvel tem reforma ou se a última sessão tem +90 dias. Se o PP fornecer as 3 datas no formulário, a tratativa é facilitada: se ele não atender o telefone após 3 tentativas, o analista agenda na melhor data sugerida e avisa por e-mail.
AS IS
Macro fluxo
Fluxo detalhado





Elegível: Imóvel nunca teve fotos profissionais, reforma comprovada por fotos anexas, ou última sessão há mais de 6 meses.
Inelegível: Fotos profissionais recentes (menos de 6 meses) e de boa qualidade.











A demanda é integrada via Cognito: FAQ QuintoAndar
Um ticket é gerado no Zendesk na visualização Agendamento de Fotos - FUP [SO].



Validar no Admin e no Magic Link o histórico de fotos do imóvel
O pedido é elegível para uma nova sessão gratuita?
Sim
Realizar contato telefônico ativo ou via WhatsApp para negociar a nova data


Qual o desfecho do contato?
Proprietário atende (Sucesso no contato)

Contato com o proprietário
Variação A: Novo agendamento (Agenda disponível)

Realizar a reserva do horário no sistema
Registrar o histórico final e enviar a comunicação de encerramento ao proprietário/solicitante


Fim do fluxo












Início do fluxoProprietário preenche o formulário de contato na Central de Ajuda.
Cognito
Zendesk
Admin (Aba Imóveis) e Magic Link
Twillio
Twillio
Admin (Aba Câmera)
Zendesk e CRM/Magic Link
No Admin, verifique a data do último "Job" concluído e visualize as fotos atuais do anúncio.
Se o proprietário alegar reforma, verifique se há fotos anexadas ao ticket que comprovem a mudança.
Não
Ligue para o PP -> Acorde a data e o período
Caso ele não atenda, envie o template de WhatsApp confirmando que o pedido foi aceito e solicitando sugestões de horários.
Aplique a sondagem para confirmar endereço, chaves e se haverá acompanhante. Caso relate NoShow do fotógrafo anterior, use o Pitch de Desculpas: "Pedimos desculpas pelo ocorrido! Isso se distancia da experiência que trabalhamos para proporcionar...".
No Admin, clique em "Agendar Job fotógrafo".
Insira o ID do imóvel e busque o Job.
No Planner, escolha um horário verde (preferencialmente D+2).
Confirme o fotógrafo e finalize.
No Zendesk, no campo Origem da tarefa, selecione obrigatoriamente FAQ QuintoAndar.
No Magic Link, insira o comentário interno: [WH] - FAQ - [Desfecho: Agendado ou Negativa Enviada].
Altere o status do ticket para Resolvido.
Caso tenha agendado, certifique-se de que os dados do fotógrafo foram enviados ao cliente.

O analista deve abrir o ticket e identificar a solicitação específica do proprietário (ex: "Quero novas fotos pois reformei o imóvel").

A demanda entra via Cognito: FAQ QuintoAndar
Geração automática do ticket na caixa Agendamento de Fotos - FUP [SO] no Zendesk

 O analista audita o anúncio no Admin para verificar se o pedido cumpre os requisitos de gratuidade (Reforma, Tempo > 6 meses ou Erro Técnico).
O pedido do proprietário é aceito?
S
Realizar contato telefônico ou via WhatsApp para negociar data e hora
Executar o novo agendamento, agendamento futuro ou abandono
Registrar o comentário da tratativa no CRM e finalizar o ticket no Zendesk

Fim do fluxo








Início do fluxoProprietário preenche formulário no FAQ solicitando nova sessão de fotos.
Cognito
Zendesk
Admin MagicLink
Discador Olos ou Zendesk
Zendesk e Admin (Aba Câmera)
Zendesk e Admin (Aba Câmera)
Envio de e-mail formal (Zendesk) explicando a negativa
Variação B: Solicitação de encaixe (Sem agenda ou urgência)
Solicitar apoio para alocar um fotógrafo manualmente

N
Proprietário não atende (Inalcançável)

Envio de FUP ao proprietário

O ticket cai na caixa Agendamento de Fotos - FUP [SO] no Zendesk.
O ticket cai na caixa Agendamento de Fotos - FUP [SO] no Zendesk.
O analista deve visualizar as fotos atuais no Admin antes de realizar qualquer contato.
Ligue para o PP -> Acorde a data e o período
Caso ele não atenda, envie o template de WhatsApp confirmando que o pedido foi aceito e solicitando sugestões de horários.
Novo Agendamento: No Admin, clique em "Agendar Job fotógrafo" -> Selecione o horário no Planner (prioridade D+2) -> Confirme o parceiro
Agendamento Futuro (>9 dias): Use a função Snooze no CRM e preencha o formulário de Agendamentos Futuros
Abandono: No Admin, selecione o ícone de cancelamento -> Delete -> "Cadastro Abandonado" e descreva o motivo.
No Magic Link: Clique no ícone de diálogo azul na tarefa -> Registre o resumo (ex: [WH] - Reagendado para dia XX/XX) -> Salvar.
No Zendesk: Selecione a Origem da tarefa como Solicitações de Reagendamento - FUP Fotos -> Aplique a macro de resposta -> Altere para Resolvido.
No Olos/Eaglle: Tabule a chamada corretamente para liberar o sistema.
Appsheet (Support Photos)
Zendesk
Zendesk

Utilize a macro de negativa do FAQ -> Explique que o imóvel já possui fotos de alto padrão que atendem aos requisitos de anúncio.
Oriente o PP que ele pode subir até 5 fotos próprias (via app) para complementar o anúncio, caso queira mostrar um detalhe específico da reforma.
No Zendesk, clique no ícone de "Aplicativos" à direita FUP Fotos]. Selecione o template reagendamento_fotos_fup1 FUP Fotos]. Preencha os campos de Parâmetro (Nome, Endereço) e clique em Enviar FUP Fotos].
Clique em [+Add] no Appsheet.
Preencha: Time, Motivo (Falta de Planner ou NoShow) e ID do Imóvel.
Informe se é Job SOS (PP aguardando no local).
Avise o PP sobre o SLA de 2 horas para retorno.

Envio de e-mail formal via Zendesk comunicando a negativa e os motivos técnicos.
Variação C: Abandono de cadastro (Desistência definitiva)

O analista da BPO preenche o formulário Cognito: Suporte Outsourcing


Zendesk (Macro de FAQ)
Proprietário atende, mas desiste/recusa
Contato com o proprietário

Cognito
Utilize a macro de negativa do FAQ -> Explique que o imóvel já possui fotos de alto padrão que atendem aos requisitos de anúncio.
Oriente o PP que ele pode subir até 5 fotos próprias (via app) para complementar o anúncio, caso queira mostrar um detalhe específico da reforma.
Twillio
Questione o motivo real ("O que impede de anunciar hoje?"). Se o motivo for reforma, verifique o prazo (menos ou mais de 30 dias).
Variação D: Reforma ou indisponibilidade temporária (Snooze)
Agendar um retorno futuro para quando o imóvel estiver pronto
Preenche o Cognito: Agendamento/ Reagendamento Futuro


CRM Tarefas
Cognito
No CRM, localize a tarefa aberta.
Use a função Snooze e defina a data acordada com o proprietário.
Certifique-se de que a tarefa está marcada como "Snoozada" para não voltar ao mailing antes da hora.

Variação E: PP envia fotos [FotosPP - Piloto LQ <> FUP]
Preenche o forms [Pré Registro - Fotos PP]

Cognito
Envio de fotos proprietário [FotosPP - Piloto LQ <> FUP]
Lari: validar estratégia de canais
AS IS
Aberto
Em Andamento
Em Espera
Pendente
Resolvido
Fechado
Visualizar
Contexto
Triagem e Coleta de Dados
Executar edição no sistema operacional
Retorno ao Cliente / Encerramento
Macro fluxo
Fluxo detalhado
backlog: preencher todas as informações no cognito, não dividir entre cognito e SF
Receber a Solicitação 
Cognito


https:​​/​/www​.cognitoforms​.com​/f​/iuJz5jJtq0aZ​_9F​_TYGtfQ​/503

Criar Case no Salesforce (Service Cloud) com os campos que foram preenchidos no cognito
Encerrar o Case

Cognito Forms

Envio de fotos proprietário [FotosPP - Piloto LQ <> FUP]
Fonte de Entrada: Cognito específico preenchido pelo time (contendo E-mail, Telefone, ID, Tipo de Envio e Anexos).
Quem Trata: Analistas de FUP Fotos.
Quando é Aplicável : No momento da tentativa de agendamento/reagendamento, se o proprietário apresentar barreiras intransponíveis para receber o fotógrafo (ex: mora em outra cidade, imóvel está em local de difícil acesso, o PP já está muito atritado com cancelamentos ou vai viajar).
Resumo Geral: É a solução de contingência self-service. Em vez de abandonar o cadastro por falta de agenda, o analista oferece ao proprietário a opção de enviar fotos próprias via WhatsApp (Twilio) ou pelo link do Cognito para que o imóvel seja publicado imediatamente.
Principais Ações e Tipos de Envio:
Primeiro Envio: Quando o fluxo começa do zero com as fotos iniciais.
Reenvio de Ajuste: Caso as fotos enviadas anteriormente tenham sido reprovadas (ex: borradas, com pessoas ou na vertical).
Complemento: Quando o anúncio já tem fotos, mas o proprietário quer adicionar mais cômodos.
Publicação: O analista valida a qualidade, sobe as imagens no Admin/Magiclink na ordem correta dos cômodos, define a capa, republica o anúncio e fecha a tarefa no CRM.

 Validar se o imóvel cumpre os requisitos básicos (residencial, região atendida e sem reformas em andamento)





O time solicitante preenche um formulário com os dados básicos do Proprietário e do imóvel
O time de FUP recebe esses dados via planilha de controle para iniciar a tratativa


O analista de FUP acessa a planilha de controle para identificar os novos casos


Contato com o proprietário via WhatsApp
Avaliar enquadramento, iluminação e condições de conservação do imóvel

As fotos e o imóvel foram aprovados?
Sim
Upload e ativação do anúncio
Preencher o formulário Cognito: FotosPP - Piloto LQ <> FUP
O sistema processa o formulário e cria automaticamente o ticket na caixa Listing Quality [FOTOS] [SO]


Encerrar ticket no Zendesk



Fim do fluxo











A demanda entra via Google Forms [Pré Registro - Fotos PP]
O time de FUP recebe esses dados via planilha de controle para iniciar a tratativa
Realiza contato via WhatsApp solicitando fotos
As fotos e o imóvel foram aprovados?

Preencher o formulário Cognito: FotosPP - Piloto LQ <> FUP
Início do fluxoO time solicitante identifica a necessidade do fluxo de fotos PP e preenche um formulário Google solicitando contato







S
Uploud de fotos e publicação
Encerrar ticket no Zendesk

Fim do fluxo









Início do fluxoO time solicitante identifica a necessidade do fluxo de fotos PP e preenche um formulário Google solicitando contato
Google Forms
Google Sheets
Admin (Aba Imóveis) e Magic Link

Twillio [WhatsApp]

Twillio [WhatsApp]
Admin / MagicLink
Cognito
Zendesk
Zendesk
O agente pode reclassificar o Tipo de Solicitação a qualquer momento. Ao reclassificar, o mesmo Case é automaticamente transferido para a fila correta, sem perda de histórico.

Google Forms
Google Sheets
Admin/MagicLink
Twillio [WhatsApp]
Admin/MagicLink
Cognito
Zendesk
Acesse a Planilha de Controle de Fotos PP através do link oficial. 
Identifique os dados do proprietário (E-mail e Telefone) e o ID do imóvel de 9 dígitos. 
Valide se o imóvel está dentro das premissas básicas (Residencial e em região atendida)
Valide no Admin se o imóvel está livre para receber fotos (sem sessões profissionais ativas que gerem conflito)
O PP tem até dois dias para enviar as fotos após o primeiro contato
Não
No Admin/Magiclink, suba as fotos na ordem correta: Sala, Quartos, Banheiros, Cozinha, Área de serviço, Outros e Fachada. 
Legende cada imagem, valide o cômodo e defina a Foto de Capa. 
Clique em "Republicar anúncio" e confirme a publicação. 
No CRM, localize a tarefa "Agendar Job de Fotógrafo" e marque como Feito
N
Critérios de Reprova: Verifique se há mofo/infiltração excessiva, fiação exposta, bagunça de mudança, buracos em tetos/paredes ou marcas d'água de outras imobiliárias. 
Critérios de Aceite: Pequenas avarias (cascas de tinta), bagunças leves do dia a dia ou fios de bocal de lâmpada são aceitáveis. 
Garanta que as imagens estão em formato JPG/JPEG e com largura mínima de 1152px
Abra o formulário Cognito: FotosPP - Piloto LQ <> FUP
Preencha e-mail, telefone e ID do imóvel
Selecione "Primeiro envio" e anexe as fotos (mínimo 1 por cômodo)
Acesse a Planilha de Controle de Fotos PP através do link oficial. 
Identifique os dados do proprietário (E-mail e Telefone) e o ID do imóvel de 9 dígitos. 
Valide se o imóvel está dentro das premissas básicas (Residencial e em região atendida)
Valide no Admin se o imóvel está livre para receber fotos (sem sessões profissionais ativas que gerem conflito)
O PP tem até dois dias para enviar as fotos após o primeiro contato
Realizar upload, legendagem, definição de capa e republicação do anúncio no Admin. Fechar a tarefa de "Agendar Job" no CRM
Preencher o formulário Cognito: FotosPP - Piloto LQ <> FUP com os dados do PP e as imagens
 O formulário gera automaticamente um ticket no Zendesk para fins de registro histórico
 Inicie a conversa no Twilio solicitando as fotos (3 a 5 por cômodo, horizontais na proporção 3:2). 
Se o PP não responder em 2 dias: Informe que o contato está sendo encerrado por falta de retorno e devolva a demanda para o time solicitante
Localizar o ticket recém-criado no Zendesk 
Realizar o fechamento manual (status Resolvido)
 Inicie a conversa no Twilio solicitando as fotos (3 a 5 por cômodo, horizontais na proporção 3:2). 
Se o PP não responder em 2 dias: Informe que o contato está sendo encerrado por falta de retorno e devolva a demanda para o time solicitante
Localizar o ticket criado no Zendesk e realizar o fechamento manual (Status: Resolvido)

Comunicação ao proprietário sobre o impedimento da publicação
Comunicação ao proprietário sobre o impedimento da publicação
Twillio [WhatsApp]
Twillio [WhatsApp]
Analista abre case para registro histórico
Encerra o case como resolvido
Caso o proprietário não responda ao pedido de fotos por 2 dias, o contato deve ser encerrado
Caso o proprietário não responda ao pedido de fotos por 2 dias, o contato deve ser encerrado
 Informe ao PP via WhatsApp o motivo da recusa (ex: fotos com mofo, bagunça excessiva ou buracos no forro) e peça correção
 Informe ao PP via WhatsApp o motivo da recusa (ex: fotos com mofo, bagunça excessiva ou buracos no forro) e peça correção