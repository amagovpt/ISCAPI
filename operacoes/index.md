# Integração de Serviços Comuns
A ISCAPI (Integração de Serviços Comuns API) é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de agilizar todos os processos de integração de sistemas externos à Plataforma de Serviços do [ePortugal](https://ePortugal.gov.pt).

- [Regressar ao ecrã inicial](../)

## Operações
As operações apresentadas representam as necessidades atuais e serão atualizadas conforme as necessidades.

## Envio de formulário
O formulário submetido na plataforma de serviços da AMA é enviado através desta operação.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|Form|Formulário eForms|1....1|

```markdown
<operationData>
  <operationCode>ISCOP001SendForm</operationCode>
  <operationVersion></operationVersion>
  <Form></Form>
</operationData>
```


## Envio de número de processo externo
A entidade que recebe o formulário deve utilizar esta operação para comunicar o nº de processo no seu sistema.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|requestNumber|string|1....1|
|compEntityReqNumber|string|1....1|
|replyType|string|1....1|
|replyCode|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP003SendProcessNumber</operationCode>
  <operationVersion>1.0</operationVersion>
  <requestNumber>694/2020</requestNumber>
  <compEntityReqNumber>PROC/487/2020</compEntityReqNumber>
  <replyType>OK</replyType>
  <replyCode>200</replyCode>
</operationData>
```

## Alteração de estado
Esta operação pode ser usada de forma bidirecional conforme os cenários , permite comunicar uma alteração de estado e
pode ser originada a partir da plataforma de serviços ou do sistema de informação da entidade parceira.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|requestNumber|string|1....1|
|compEntityReqNumber|string|1....1|
|changeDate|timestamp|1....1|
|sendDate|timestamp|1....1|
|stateCode|int|1....1|
|stateDesc|string|1....1|
|action|int|1....1|
|actionDesc|string|1....1|
|comments|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP002SendStateUpdate</operationCode>
  <operationVersion>1.0</operationVersion>
  <requestNumber>696/2020</requestNumber>
  <compEntityReqNumber>PROC/489/2020</compEntityReqNumber>
  <changeDate>2020-03-20T17:37:58</changeDate>
  <sendDate>2020-03-20T17:37:58</sendDate>
  <stateCode>13</stateCode>
  <stateDesc>Processo decidido</stateDesc>
  <actionCode>14</actionCode>
  <actionDesc>Emitir decisão</actionDesc>
  <comments />
</operationData>
```

## Solicitar meio/forma de pagamento
Esta operação pode ser usada de forma bidirecional conforme os cenários , permite solicitar os meios de pagamento para a tramitação do processo na plataforma de serviços ou no sistema de informação da entidade parceira.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|paymentValue|string|1....1|
|paymentTypeId|string|1....1|
|buyerEmail|string|1....1|
|requests|Requests|1....N|
|requestNumber|string|1....1|
|serviceCode|string|1....1|
|entityCode|string|1....1|

```markdown
<operationData>
    <operationCode>ISCOP004GetPaymentMethods</operationCode>
    <operationVersion />
    <paymentValue>120.00</paymentValue>
    <paymentTypeId>1</paymentTypeId>
    <buyerEmail />
    <requests>
      <requestNumber>1679</requestNumber>
      <serviceCode>CES:SRV:000005469</serviceCode>
      <entityCode>SIOE:ORG:070080000</entityCode>
    </requests>
</operationData>
```
**Necessário ter protocolo com a AMA para utilizar a Plataforma de Pagamentos da AMA**


## Solicitar cálculo da taxa
Esta operação pode ser usada de forma bidirecional conforme os cenários , permite solicitar o cálculo de uma taxa para a
tramitação do processo na plataforma de serviços ou no sistema de informação da entidade parceira.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|Form|ElectronicForm|1....1|
|feeType|string|1....1|
|serviceCode|string|1....1|
|entityCode|string|1....1|

```markdown
<operationData>
    <operationCode>ISCOP015RateServiceTax</operationCode>
    <operationVersion />
	<serviceCode>CES:SRV:000005469</serviceCode>
    <entityCode>SIOE:ORG:070080000</entityCode>   
    <feeType>T</feeType> 
	<Form></Form>
</operationData>
```

## Envio de meios de pagamento
Esta operação pode ser usada de forma bidirecional conforme os cenários , permite enviar os meios de pagamento.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|OperationVersion|string|1....1|
|paymentMovementId|string|1....1|
|paymentDate|string|1....1|
|paymentValue|string|1....1|
|paymentTypeId|string|1....1|
|paymentTypeData|string|1....1|
|feeType|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP005PaymentDataCommunication</operationCode>
  <operationVersion></operationVersion>
  <paymentMovementId>?</paymentMovementId>
  <paymentDate>?</paymentDate>
  <paymentValue>?</paymentValue>
  <paymentTypeId>?</paymentTypeId>
  <paymentTypeData>?</paymentTypeData>
  <feeType>T</feeType>
</operationData>
```

## Enviar notificações
Para enviar uma curta comunicação a um utilizador no âmbito de um processo.
Esta comunicação escrita não pode enviar dados do processo , apenas apelar à sua visualização no ePortugal.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|receiver|string|1....1|
|subject|string|1....1|
|body|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP013SendNotifications</operationCode>
  <operationVersion>1</operationVersion>
  <receiver>email@email.com</receiver>
  <subject>Tem uma nova notificação na Área Reservada do Licenciamento Industrital no ePortugal</subject>
  <body>Recebeu uma nova notificação em 13/03/2020 às 11:59:46, relativa ao Pedido de Vistoria, Nº 16/2019-2 do estabelecimento Idioma de tons - Estamparia, Lda com o NUEI 030308000048.
Consulte a sua Área Reservada do Licenciamento Industrial, no ePortugal, para visualizar detalhes.</body>
</operationData>
```

## Solicitar envio de formulário
**BETA**
É uma forma de solicitar o envio de um formulário, é um mecanismo disponível para a plataforma de serviços,
solicitar o envio de um formulário no âmbito de uma alteração.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|Form|Formulário eForms|1....1|

```markdown
<operationData>
  <operationCode>ISCOP014GetElectronicFormRequest/operationCode>
  <operationVersion></operationVersion>
<operationData>
```


## Envio de um erro
**BETA**
Esta operação pode ser usada de forma bidirecional e serve para a comunicação de erros na troca de mensagens.

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|processNumber|string|1....1|
|requestNumber|string|1....1|
|errorCode|string|1....1|
|errorMessage|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP012ProcessError</operationCode>
  <operationVersion></operationVersion>
  <processNumber>PROC/487/2020</processNumber>
  <requestNumber>694/2020</requestNumber>
  <errorCode></errorCode>
  <errorMessage></errorMessage>
</operationData>
```

## Pedido de acesso
**BETA**
Esta operação serve para solicitar acesso a um formulário.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|compEntityReqNumber|string|1..1|
|userType|string|1....1
|documentType|string|1....1
|documentId|string|1....1|
|comments|string|	0....1|

```markdown
<operationData>
  <operationCode>ISCOP006FormAuthRequest</operationCode>
  <operationVersion></operationVersion>
  <compEntityReqNumber>?</compEntityReqNumber>
  <userType>?</userType>
  <documentType>?</documentType>
  <documentId>?</documentId>
  <comments>?</comments>
</operationData>
```
## Resposta a pedido de acesso

**BETA**
Esta operação serve para responder a um pedido de acesso a um formulário.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|compEntityReqNumber|string|1....1|
|documentType|string|1....1|
|result|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP007FormAuthReply</operationCode>
  <operationVersion>1</operationVersion>
  <compEntityReqNumber>?</compEntityReqNumber>
  <documentType>?</documentType>
  <result>?</result>
</operationData>
```


## Pedido de esclarecimentos/elementos adicionais
**BETA**
Esta operação permite o envio de um pedido de esclarecimentos ou recolha de informação adicional para um determinado pedido.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|additionalInfoType|string|1....1|
|additionalInfoDate|string|1....1|
|additionalInfoReason|string|1....1|
|additionalInfoPreDecision|string|1....1|
|additionalInfoTermForReply|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP008AdditionalInfoRequest</operationCode>
  <operationVersion></operationVersion>
  <additionalInfoType>?</additionalInfoType>
  <additionalInfoDate>?</additionalInfoDate>
  <additionalInfoReason>?</additionalInfoReason>
  <additionalInfoPreDecision>?</additionalInfoPreDecision>
  <additionalInfoTermForReply>?</additionalInfoTermForReply>
</operationData>
```

## Resposta a pedido de esclarecimentos
**BETA**
Esta operação permite o envio de uma resposta ao pedido de esclarecimentos ou recolha de informação adicional para um determinado pedido

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|additionalInfoReplyDate|timestamp|1....1|
|additionalInfoReplyFeedback|string|1....1|
|additionalInfoReplyPreDecision|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP009AdditionalInfoReply</operationCode>
  <operationVersion></operationVersion>
  <additionalInfoReplyDate>?</additionalInfoReplyDate>
  <additionalInfoReplyFeedback>?</additionalInfoReplyFeedback>
  <additionalInfoReplyPreDecision>?</additionalInfoReplyPreDecision>  
</operationData>
```

## Registo de uma decisão
**BETA**
Esta operação permite o registo de uma decisão associada a um processo.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|processDecisionType|string|1....1|
|processDecisionDate|timestamp|1....1|
|processDecisionReason|string|1....1|

```markdown
<operationData>
<operationCode>ISCOP010ProcessDecision</operationCode>
       <operationVersion></operationVersion>
       <processDecisionType>?</processDecisionType>
       <processDecisionDate>?</processDecisionDate>
       <processDecisionReason>?</processDecisionReason>
</operationData>
```

## Envio de dados resumo
**BETA**
Esta operação permite o envio de dados de serviço de forma resumida.

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|processNumber|string|1....1|
|requestNumber|string|1....1|
|params|param|1....N|
|name|string|1....1|
|value|string|1....1|


```markdown
<operationData>
  <operationCode>ISCOP011ServiceResumeInfo</operationCode>
  <operationVersion></operationVersion>
  <processNumber>?</processNumber>
  <requestNumber>?</processNumber>
  <params>
     <param>
      <name>Nome Requerente</nane>
      <value>Exemplo</value>
    </param>
    <param>
      <name>Apelido Requerente</nane>
      <value>Exemplo 2 </value>
    </param>
    <param>
      <name>Número Telemóvel</nane>
      <value>900000000</value>
    </param>
  <params>
</operationData>
```



## Envio de documentos de um processo
**BETA**
Esta operação permite o envio de documentos de um processo

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|documentId|string|1....1|
|documentFileguid|string|1....1|
|documentEntityCode|param|1....1|
|documentDescription|string|1....1|
|documentCreateDate|string|1....1|
|documentSentDate|string|1....1|


```markdown
<operationData>
  <operationCode>ISCOP016SendProcessDocuments</operationCode>
  <operationVersion></operationVersion>
 <document>
               <!--Optional:-->
               <documentId>?</documentId>
               <documentType>?</documentType>
               <documentFileguid>?</documentFileguid>
               <documentClassification>?</documentClassification>
               <documentEntityCode>?</documentEntityCode>
               <documentDescription>?</documentDescription>
               <documentCreateDate>?</documentCreateDate>
               <documentSentDate>?</documentSentDate>
            </document>

</operationData>
```


## Envio de notificações  de um processo
**BETA**
Esta operação permite o envio de notificações de um processo

|Elemento| Tipo | Cardinalidade|
|------------|------------|------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|documentId|string|1....1|
|documentFileguid|string|1....1|
|documentEntityCode|param|1....1|
|documentDescription|string|1....1|
|documentCreateDate|string|1....1|
|documentSentDate|string|1....1|

```markdown
<operationData>
  <operationCode>ISCOP017SendProcessNotifications</operationCode>
  <operationVersion></operationVersion>
  <notification>
               <notificationId>?</notificationId>
               <notificationFileguid>?</notificationFileguid>
               <notificationType>?</notificationType>
               <notificationReceiver>?</notificationReceiver>
               <notificationSubject>?</notificationSubject>
               <notificationDescription>?</notificationDescription>
               <notificationCreateDate>?</notificationCreateDate>
               <notificationSentDate>?</notificationSentDate>
            </notification>
</operationData>
```

## Tabelas de valores
[Consultar as tabelas de valores](..\tabeladevalores)

## Plataforma de Integração
[Consultar aqui a informação sobre a Plataforma de Integração](..\iap)

## Transferência de Ficheiros
[Consultar aqui a informação sobre a transferência de ficheiros](..\largefiles)


## Estrutura Fixa
[Consultar aqui a informação sobre a estrutura fixa](..\estruturafixa)
