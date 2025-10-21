# Integração de Serviços Comuns
A ISCAPI (Integração de Serviços Comuns API) é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de agilizar todos os processos de integração de sistemas externos à Plataforma de Serviços do [gov.pt](https://www.gov.pt/).

- [Regressar ao ecrã inicial](../)

## Operações
[Consultar as operações disponíveis](../operacoes)

# Tabelas de Valores

## Meios de Pagamento

|Id| Valor |
|------------ | ------------|
|1|	Multibanco|
|2|	Cartão de Crédito|
|3|	Numerário|
|4|	Cheque|
|6|	Outros|
|7|	Transferência Bancária|
|8|	Documento Único de Cobrança- DUC|





## 	Tipos de Taxa

|Id| Valor |
|------------ | ------------|
|TA|	1º Pagamento|
|T|	2º Pagamento|

## 	Entidades
Para verificar o código de (uma) entidade(s), deverá aceder ao CES, em https://ces.ama.gov.pt/org.

## 	Tipos de Utilizador

|Id| Valor | 
|------------ | ------------|
|000000001|	CC / CMD Nacional| 
|000000014|	Advogado|  
|000000015|	Solicitador|
|000000016|	Notário| 
|00000010|	Eidas | 
|000000200|	CMD Estrangeiro | 

## 	Estado do processo

|Id| Valor |
|------------ | ------------|
|1|	Pedido em elaboração|
|2|	Aguarda emissão de pagamento|
|3|	Aguarda pagamento da taxa administrativa|
|4|	Aguarda atribuição de taxa|
|5|	Pagamento liquidado|
|6|	Cancelado|
|7|	Pedido arquivado|
|8|	Aguarda análise|
|9|	Em análise|
|10| Aguarda esclarecimentos|
|11| Aguarda audiência dos interessados|
|12| Aguarda pagamento da taxa|
|13| Pedido decidido|
|14| Processo submetido à entidade competente|
|15| Pagamento da taxa de decisão liquidado|
|16| Pedido migrado|
|19| Suspenso|
|20| Aguarda introdução de token|
|21| Pagamento fora do prazo|
|22| Deserto|
|25| Aguarda parecer da entidade visada|
|26| Aguarda evidências|

## 	Canais

|Id| ISCAPI_NAME| Valor|
|------------|------------ | ------------|
|1|PointOfCareType.Web|	Online|
|2|PointOfCareType.Presential|	Presencial|
|3|--	| Posto Pagamento|
|4|PointOfCareType.Phone|	Telefone|
|5|PointOfCareType.Fax| 	Fax|
|6|PointOfCareType.Email|	Correio Eletrónico|
|7|PointOfCareType.Mail|	Correio Postal|
|8|PointOfCareType.MobileApp|	Aplicação Móvel|
|9|PointOfCareType.SocialNetwork| 	Rede Social|


## 	Local\Ponto de Atendimento
Código identificador do Ponto de Atendimento no Catálogo de Entidades e Serviços.


## 	Códigos de erro na receção de número externo(ReplyCode)

|Id| Valor |
|------------ | ------------|
|100 |	Aguarda Intervenção Manual ou Programada|
|200|	Sucesso|
|400|	Erro Aplicacional ou Formato Inesperado|
|401|	Registo Duplicado ou inesperado|
|500|	Erro Inesperado|

## 	Códigos de erro (ErrorCode)

|Id| Valor |
|------------ | ------------|
|100 |	Aguarda Intervenção Manual ou Programada|
|400|	Erro Aplicacional ou Formato Inesperado|
|401|	Registo Duplicado ou inesperado|
|403| Acesso não autorizado|
|404| O pedido solicitado não foi encontrado|
|500|	Erro Inesperado|

## 	Códigos de erro (ISC 12)

|Código de Erro| Contexto | Mensagem de Erro |
|------------ | ------------|
|I_E|[MessageRequest]|Internal Error|
|MD_01|[MessageData]|Missing messageEntityId|
|MD_02|[MessageData]|Missing messageRelatesToEntityId|
|MD_03|[MessageData]|Missing messageDate|
|MD_04|[MessageData]|Invalid messageEntityId|
|MD_05|[MessageData]|Invalid messageRelatesToEntityId|
|RD_01|[RequestData]|Missing RequestNumber|
|RD_02|[RequestData]|Missing ProcessNumber|
|RD_03|[RequestData]|Missing entityCode|
|RD_04|[RequestData]|Missing serviceCode|
|RD_05|[RequestData]|Missing channel|
|RD_06|[RequestData]|Missing userName|
|RD_07|[RequestData]|Invalid RequestNumber|
|RD_08|[RequestData]|Invalid ProcessNumber|
|RD_09|[RequestData]|Invalid requestExternalNumber|
|RD_10|[RequestData]|ProcessNumber does not match requestNumber|
|RD_11|[RequestData]|Invalid entityCode|
|RD_12|[RequestData]|Invalid serviceCode|
|OP_01|[OperationData]|Missing OperationCode|
|OP_02|[OperationData]|Invalid OperationCode|
|OP_03|[OperationData]|Invalid OperationVersion|
|AC_01|[AttachContext]|Missing FileGuid|
|AC_02|[AttachContext]|Missing fileName|
|AC_03|[AttachContext]|Missing fileType|
|AC_04|[AttachContext]|Missing filePath|
|AC_05|[AttachContext]|File Not Found|
|ISCOP002_01|[ISCOP002SendStateUpdate][OperationData]|Missing requestNumber|
|ISCOP002_02|[ISCOP002SendStateUpdate][OperationData]|Missing compEntityReqNumber ???|
|ISCOP002_03|[ISCOP002SendStateUpdate][OperationData]|Missing changeDate|
|ISCOP002_04|[ISCOP002SendStateUpdate][OperationData]|Missing sendDate|
|ISCOP002_05|[ISCOP002SendStateUpdate][OperationData]|Missing stateCode|
|ISCOP002_06|[ISCOP002SendStateUpdate][OperationData]|Missing stateDesc|
|ISCOP002_07|[ISCOP002SendStateUpdate][OperationData]|Missing actionCode|
|ISCOP002_08|[ISCOP002SendStateUpdate][OperationData]|Missing actionDesc|
|ISCOP002_09|[ISCOP002SendStateUpdate][OperationData]|Invalid requestNumber|
|ISCOP002_10|[ISCOP002SendStateUpdate][OperationData]|Invalid compEntityReqNumber ???|
|ISCOP002_11|[ISCOP002SendStateUpdate][OperationData]|Invalid StateCode|
|ISCOP002_12|[ISCOP002SendStateUpdate][OperationData]|Invalid ActionCode|
|ISCOP003_01|[ISCOP003SendProcessNumber][OperationData]|Missing requestNumber|
|ISCOP003_02|[ISCOP003SendProcessNumber][OperationData]|Missing compEntityReqNumber ???|
|ISCOP003_03|[ISCOP003SendProcessNumber][OperationData]|Missing replyType|
|ISCOP003_04|[ISCOP003SendProcessNumber][OperationData]|Missing replyCode|
|ISCOP003_05|[ISCOP003SendProcessNumber][OperationData]|Invalid replyType|
|ISCOP005_01|[ISCOP005PaymentDataCommunication][OperationData]|Missing paymentMovementId|
|ISCOP005_02|[ISCOP005PaymentDataCommunication][OperationData]|Missing paymentDate|
|ISCOP005_03|[ISCOP005PaymentDataCommunication][OperationData]|Missing paymentValue|
|ISCOP005_04|[ISCOP005PaymentDataCommunication][OperationData]|Missing paymentTypeId|
|ISCOP005_05|[ISCOP005PaymentDataCommunication][OperationData]|Missing paymentTypeData|
|ISCOP005_06|[ISCOP005PaymentDataCommunication][OperationData]|Missing feeType|
|ISCOP005_07|[ISCOP005PaymentDataCommunication][OperationData]|Invalid paymentTypeId|
|ISCOP005_08|[ISCOP005PaymentDataCommunication][OperationData]|Invalid paymentTypeData|
|ISCOP008_01|[ISCOP008AdditionalInfoRequest][OperationData]|Missing AdditionalInfoType|
|ISCOP008_02|[ISCOP008AdditionalInfoRequest][OperationData]|Missing additionalInfoDate|
|ISCOP008_03|[ISCOP008AdditionalInfoRequest][OperationData]|Missing additionalInfoReason|
|ISCOP008_04|[ISCOP008AdditionalInfoRequest][OperationData]|Missing additionalInfoSuspension|
|ISCOP008_05|[ISCOP008AdditionalInfoRequest][OperationData]|Invalid AdditionalInfoType|
|ISCOP008_06|[ISCOP008AdditionalInfoRequest][OperationData]|Invalid additionalInfoDate|
|ISCOP008_07|[ISCOP008AdditionalInfoRequest][OperationData]|Invalid additionalInfoSuspension|
|ISCOP010_01|[ISCOP010ProcessDecision][OperationData]|Missing processDecisionType|
|ISCOP010_02|[ISCOP010ProcessDecision][OperationData]|Missing processDecisionDate|
|ISCOP010_03|[ISCOP010ProcessDecision][OperationData]|Missing processDecisionReason|
|ISCOP010_04|[ISCOP010ProcessDecision][OperationData]|Invalid processDecisionType|
|ISCOP010_05|[ISCOP010ProcessDecision][OperationData]|Invalid processDecisionDate|
|ISCOP016_01|[ISCOP016SendProcessDocuments][OperationData]|No documents to upload|
|ISCOP016_02|[ISCOP016SendProcessDocuments][OperationData]|Missing documentType|
|ISCOP016_03|[ISCOP016SendProcessDocuments][OperationData]|Invalid documentType|
|ISCOP016_04|[ISCOP016SendProcessDocuments][OperationData]|Error saving file|
|ISCOP017_01|[ISCOP017SendProcessNotifications][OperationData]|No notifications to upload|
|ISCOP017_02|[ISCOP017SendProcessNotifications][OperationData]|Missing notificationFileguid|
|ISCOP017_03|[ISCOP017SendProcessNotifications][OperationData]|Missing notificationType|
|ISCOP017_04|[ISCOP017SendProcessNotifications][OperationData]|Missing notificationSubject|
|ISCOP017_05|[ISCOP017SendProcessNotifications][OperationData]|Missing notificationRecipientType|
|ISCOP017_06|[ISCOP017SendProcessNotifications][OperationData]|Missing notificationSendEntityCode|
|ISCOP017_07|[ISCOP017SendProcessNotifications][OperationData]|Invalid notificationFileguid|
|ISCOP017_08|[ISCOP017SendProcessNotifications][OperationData]|Invalid notificationType|
|ISCOP017_09|[ISCOP017SendProcessNotifications][OperationData]|Invalid notificationRecipientType|
|ISCOP017_10|[ISCOP017SendProcessNotifications][OperationData]|Invalid notificationSendEntityCode|
|ISCOP018_01|[ISCOP018StakeHolderRequest][OperationData]|Missing stakeholderEventType|
|ISCOP018_02|[ISCOP018StakeHolderRequest][OperationData]|Missing stakeholderReason|
|ISCOP018_03|[ISCOP018StakeHolderRequest][OperationData]|Missing stakeholderApplicantMessage|
|ISCOP018_04|[ISCOP018StakeHolderRequest][OperationData]|Invalid stakeholderEventType|
|ISCOP018_05|[ISCOP018StakeHolderRequest][OperationData]|Invalid stakeholderDocument|
|ISCOP018_06|[ISCOP018StakeHolderRequest][OperationData]|No stakeholder|
|ISCOP018_07|[ISCOP018StakeHolderRequest][OperationData]|Missing stakeholderType|
|ISCOP018_08|[ISCOP018StakeHolderRequest][OperationData]|Missing stakeholderNotes|
|ISCOP018_09|[ISCOP018StakeHolderRequest][OperationData]|Invalid stakeholderType|
|ISCOP020_01|[ISCOP020SendOpinion][OperationData]|???|
|ISCOP003_01|[ISCOP003SendProcessNumber][OperationData]|Invalid requestNumber|
|ISCOP003_07|[ISCOP003SendProcessNumber][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP003_08|[ISCOP003SendProcessNumber][OperationData]|Unkown error|
|ISCOP005_09|[ISCOP005PaymentDataCommunication][OperationData]|Invalid requestNumber|
|ISCOP005_10|[ISCOP005PaymentDataCommunication][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP005_11|[ISCOP005PaymentDataCommunication][OperationData]|Unkown error|
|ISCOP014_01|[ISCOP014GetElectronicFormRequest][OperationData]|Unkown error|
|ISCOP008_08|[ISCOP008AdditionalInfoRequest][OperationData]|Invalid requestNumber|
|ISCOP008_09|[ISCOP008AdditionalInfoRequest][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP008_10|[ISCOP008AdditionalInfoRequest][OperationData]|ISCOP008AdditionalInfoRequest Registo de Intervenções|
|ISCOP010_06|[ISCOP010ProcessDecision][OperationData]|Invalid requestNumber|
|ISCOP010_07|[ISCOP010ProcessDecision][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP010_08|[ISCOP010ProcessDecision][OperationData]|Decision type cannot be empty.|
|ISCOP010_09|[ISCOP010ProcessDecision][OperationData]|Decision date cannot be empty.|
|ISCOP010_10|[ISCOP010ProcessDecision][OperationData]|Decision fundament cannot be empty.|
|ISCOP010_11|[ISCOP010ProcessDecision][OperationData]|Unkown error|
|ISCOP010_12|[ISCOP010ProcessDecision][OperationData]|[SendProcessDocumentsService] Error saving file|
|ISCOP018_10|[ISCOP018StakeHolderRequest][OperationData]|Invalid requestNumber|
|ISCOP018_11|[ISCOP018StakeHolderRequest][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP020_02|[ISCOP020SendOpinion][OperationData]|Invalid requestNumber|
|ISCOP020_03|[ISCOP020SendOpinion][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP020_04|[ISCOP020SendOpinion][OperationData]|Unkown error|
|ISCOP016_05|[ISCOP016SendProcessDocuments][OperationData]|Invalid requestNumber|
|ISCOP016_06|[ISCOP016SendProcessDocuments][OperationData]|ProcessNumber does not match requestNumber|
|ISCOP016_07|[ISCOP016SendProcessDocuments][OperationData]|DocumentType is missing from the operation data|
|ISCOP016_08|[ISCOP016SendProcessDocuments][OperationData]|Unkown error|
|ISCOP016_09|[ISCOP016SendProcessDocuments][OperationData]|[SendProcessDocumentsService] Error saving file|
|ISCOP016_10|[ISCOP016SendProcessDocuments][OperationData]|DocumentType is in the wrong format|
|ISCOP016_11|[ISCOP016SendProcessDocuments][OperationData]|DocumentType does not match any Type defined|
|ISCOP002_13|[ISCOP002SendStateUpdate][OperationData]|Unkown error|
|ISCOP014_02|[ISCOP014GetElectronicFormRequest][OperationData]|Runtime error:|
|ISCOP014_03|[ISCOP014GetElectronicFormRequest][OperationData]|Invalid requestNumber|
|ISCOP018_12|[ISCOP018StakeHolderRequest][OperationData]|[ERROT ISCOPO18 StakeholderRequest]|
|ISCOP018_13|[ISCOP018StakeHolderRequest][OperationData]|Unkown error|

##	 Códigos de Ação

|Id| Valor |
|------------ | ------------|
|1|	Preenchimento formulário|
|2|Submissão formulário|
|3|Colocar pedido em análise|
|4|Finalizar processo|
|5|Aguardar selecção de pagamento|
|6|Emitir guia de pagamento|
|7|Efectuar pagamento do pedido|
|8|Caducar pagamento|
|9|Colocar pedido em atribuição de taxa|
|10|Reatribuir pedido|
|11|Reservar pedido|
|12|Notificar para esclarecimentos|
|13|Reapreciar|
|14|Emitir decisão|
|15|Convocar audência de interessados|
|16|Registar taxa após decisão|
|17|Arquivar pedido|
|18|Libertar pedido|
|19|Submeter pedido à entidade competente|
|20|Enviar notificação|
|29|Criar pedido|
|30|Submeter pedido à análise|
|31|Submeter pedido à análise|
|32|Notificar para esclarecimentos com paragem de prazos|
|33|Comunica|
|34|Comunica|
|35|Registo de intervenção s/ suspenção de prazo|
|36|Registo de intervenção c/ suspensão de prazo|
|37|Retoma de pedido|
|38|Registo de pagamento manual|
|39|Pagamento de taxa em atraso|
|40|Atribuição manual de número de pedido externo|
|41|Correção|

##	Tipo de Taxa

|Id| Valor |
|------------ | ------------|
|TA|Taxa Administrativa|
|T|Taxa de Serviço|



##	Tipo de Documento

|Id| Valor |
|------------ | ------------|
|1|Documento de decisão|
|2|	Anexo de notificação|
|3|Notificação|
|4|Documento do formulário|
|5|Documento de processo|
|6|Documento de criação de audiência dos interessados|
|7|Documento de pronúncia de audiência dos interessados|
|8|Resposta requerente|
|9|Anexo requerente|
|10|XML declaração|
|11|PDF declaração|
|12|PDF da declaração auto gerada|
|13|Documento de resposta registo de intervenções|
|14|	Documento de evidência|
|15|	Comprovante Notif - SPNE|
|16|	Anexo do parecer do processo|
|17|	Documento de OOTS|
|18|JSON Declaração|

##	Tipo de Notificação

|Id| Valor |
|------------ | ------------|
|PointOfCareType.Email|	Correio Eletrónico|
|PointOfCareType.NotificationSystem|	Plataforma de Notificações Eletrónicas|


## Plataforma de Integração
[Consultar aqui a informação sobre a Plataforma de Integração](../iap)

## Transferência de Ficheiros
[Consultar aqui a informação sobre a transferência de ficheiros](../largefiles)

## Estrutura Fixa
[Consultar aqui a informação sobre a estrutura fixa](..\estruturafixa)
