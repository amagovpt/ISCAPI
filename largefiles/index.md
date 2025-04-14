# Integração de Serviços Comuns
A ISCAPI (Integração de Serviços Comuns API) é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de agilizar todos os processos de integração de sistemas externos à Plataforma de Serviços do  [gov.pt](https://www.gov.pt/).

- [Regressar ao ecrã inicial](../)

## Tabelas de valores
[Consultar as tabelas de valores](..\tabeladevalores)

## Plataforma de Integração
[Consultar aqui a informação sobre a Plataforma de Integração](..\iap)

## Transferência de Ficheiros
Com a funcionalidade de large files, as entidades conseguem partilhar ficheiros no contexto das mensagens trocadas.
O processo de transferência de ficheiros divide-se em 3 fases:
*	Envio da mensagem de negócio, estando no payload a informação referente aos documentos a partilhar. O sistema adormece esta mensagem, enquanto não receber todos os ficheiros indicados.
*	O envio dos ficheiros isoladamente. Este serviço não tem dependência. Uma entidade pode optar por primeiro enviar os ficheiros. Neste cenário, assim que a mensagem de negócio chega, o sistema procede imediatamente à sua transmissão.
*	O download dos ficheiros pela entidade que recebe a mensagem.

Como referido, o sistema tem 3 modos de acesso para as entidades cliente.

###	Envio da mensagem de negócio
Qualquer mensagem de negócio (desde que parametrizada para tal) pode indicar a existência de ficheiros anexos. Para isso, o payload deve contemplar um objeto do tipo AttachContext.

```markdown
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns="http://pi.ama.pt/largefiles"
targetNamespace="http://pi.ama.pt/largefiles"
elementFormDefault="qualified">
<xsd:complexType name="AttachContext">
  <xsd:sequence>
    <xsd:element name="TTL" type="xsd:int" minOccurs="0" max-Occurs="1" default="30"/>
    <xsd:element name="FileGuid" type="xsd:string" minOccurs="1" maxOccurs="unbounded"/>
  </xsd:sequence>
</xsd:complexType>
```

###	Envio do ficheiro

Se o payload da mensagem contem o elemento AttachContext formatado corretamente, a mensagem só será entregue ao sistema destino quando todos os documentos referidos na lista de elementos FileGuid tiverem sido submetidos para a Plataforma de Integração.
Para que seja corretamente anexado a uma mensagem específica, o pedido http deve conter os seguintes headers
Este serviço permite o envio e receção de ficheiros recorrendo à estrutura fixa anteriormente apresentada attachContext.
Esta estrutura apenas apresenta os dados referentes a ficheiros que já foram previamente enviados.
Assim, torna-se necessário efetuar o upload dos ficheiros antes do envio da mensagem.
Para efetuar o upload é necessário aceder ao endereço de upload de acordo com as instruções presentes.
Depois de efetuado o upload a estrutura attachContext poderá ser preenchida na mensagem com os dados do ficheiro que foi enviado

|Campo| Descrição |
|------------ | ------------|
|Hash|A hash em base64 da encriptação SHA1 do conteúdo do ficheiro|
|ID|Identificador do ficheiro no formato GUID (12345678-1234-1234-1234-123456789098)|

Não é possível a substituição de ficheiros, depois do mesmos estarem submetidos.

###	Receção do Ficheiro
Após a receção da mensagem de negócio pela entidade recetora, os ficheiros estão dis-poníveis através do respectivo endereço de download.
Para aceder ao seu conteúdo, deve ser enviado na query string do pedido http um parâmetro com o nome”Id”, contendo o GUID do ficheiro pretendido.
Quando se receciona uma mensagem com a estrutura attachContext preenchida torna-se necessário efetuar o download do ficheiro por forma a aceder ao mesmo. Para tal deverá aceder ao endereço respetivo de acordo com as instruções presentes.


## Estrutura Fixa
[Consultar aqui a informação sobre a estrutura fixa](..\estruturafixa)
