﻿# Integração de Serviços Comuns
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
