# Integração de Serviços Comuns
A ISCAPI (Integração de Serviços Comuns API) é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de agilizar todos os processos de integração de sistemas externos à Plataforma de Serviços do [gov.pt](https://www.gov.pt/)..

- [Regressar ao ecrã inicial](../)

## Operações
[Consultar as operações disponíveis](..\operacoes)


## Tabelas de valores
[Consultar as tabelas de valores](..\tabeladevalores)

## Plataforma de Integração
[Consultar aqui a informação sobre a Plataforma de Integração](..\iap)

## Transferência de Ficheiros
[Consultar aqui a informação sobre a transferência de ficheiros](largefiles)

## Estrutura Fixa

## Dados da Mensagem
Estrutura para roteamento da mensagem.

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|messageEntityId|string|1....1|
|messageRelatesToId|string|1....1|
|messageRelatesToEntityId|string|1....1|
|messageDate|string|1....1|

```markdown
<messageData>
         <messageEntityId>?</messageEntityId>
         <messageRelatesToId>?</messageRelatesToId>
         <messageRelatesToEntityId>?</messageRelatesToEntityId>
         <messageDate>?</messageDate>
</messageData>
```

## Dados do Pedido
Estrutura para identificação do pedido.

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|processNumber|string|1....1|
|requestNumber|string|1....1|
|requestExternalNumber|string|1....1|
|requestDate|string|1....1|
|serviceCode|string|1....1|
|channel|string|1....1|
|localCode|string|1....1|
|userCode|string|1....1|
|userName|string|1....1|


```markdown
<requestData>
  <processNumber>?</processNumber>
  <requestNumber>?</requestNumber>
  <requestExternalNumber>?</requestExternalNumber>
  <requestDate>?</requestDate>
  <serviceCode>?</serviceCode>
  <channel>?</channel>
  <entityCode>?</entityCode>
  <localCode>?</localCode>
  <userCode>?</userCode>
  <userName>?</userName>
</requestData>
```


## Dados da Operação
Estrutura para identificação da operação

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|operationCode|string|1....1|
|operationVersion|string|1....1|

```markdown
<operationData>
         <operationCode>?</operationCode>         
         <operationVersion>?</operationVersion>
</operationData>      
```


## Dados dos ficheiros
Estrutura para envio de ficheiros
* O FileGuid mapeia com o campo do formulário ou a declaração (id de submissão. 
Identificador dos campos é repetido em cada formulário do mesmo tipo identificado o tipo de campo eforms.
* O largeFileGuid é o identificador a ser usado para obtenção dos documentos através de Large Files. Trata-se de um Identificador único.


|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|TTL|string|1....1|
|fileGuid|string|1....1|
|fileName|string|1....1|
|fileType|string|1....1|
|filePath|string|1....1|
|largeFileGuid|string|1....1|

```markdown
 <attachContext>
  <TTL>0</TTL>
  <FileGuid>da12f400-0228-4379-b689-c7c416b469d1</FileGuid>
  <fileName>1611741425824_dfab99c6-8834-4481-9374-dac0e1177b4e.pdf</fileName>
  <fileType>pdf</fileType>
  <filePath>/opt/docs/multicanal/2021/01/27/34742</filePath>
  <largeFileGuid>4caee12a-1ffe-4a22-ab19-6336568e21d7</largeFileGuid>
</attachContext>
```

Por exemplo o ficheiro  acima  mapeia com o campo req_fich_proc.
```markdown
 <Field>
              <Id>da12f400-0228-4379-b689-c7c416b469d1</Id>
              <Name>req_fich_proc</Name>
              <Files>
                <File>
                  <Name>Declaracao (71).pdf</Name>
                  <Path>dfab99c6-8834-4481-9374-dac0e1177b4e</Path>
                </File>
              </Files>
              <SubFields />
              <IsReadOnly>true</IsReadOnly>
            </Field>
```
O ficheiro de declaração\comprovativo é um caso particular pois não faz parte dos  campos do formulário.
```markdown
 <attachContext>
    <TTL>0</TTL>
    <FileGuid>3cffeb6a-8654-4309-a8d6-ff946dab4fb5</FileGuid>
    <fileName>1611741425805_Declaracao.pdf</fileName>
    <fileType>pdf</fileType>
    <filePath>/opt/docs/multicanal/2021/01/27/34742</filePath>
    <largeFileGuid>42cb4a55-ff7c-403e-8b27-dd891a175390</largeFileGuid>
  </attachContext>
```
Mapeia com o identificador único de submissão
```markdown
 <SubmissionId>3cffeb6a-8654-4309-a8d6-ff946dab4fb5</SubmissionId>
```



