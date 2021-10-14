# Massas de Dados - Open Banking Brasil

Repositório referente as massas de dados das Fases 1, 2 e 3 do Open Banking Brasil.

## Fases

A fase 1 trás informações das instituições bancárias, a fase 2 trás o fluxo de compartilhamento de dados 
enquanto que a fase 3 trás o fluxo de pagamentos. 
As massas da fase 1 foram desenvolvidas com base em instituições participantes de exemplo com dados fictícios e não reais. 
As massas da fase 2 foram desenvolvidas com base em cenários estabelecidos e personas fictícias construídas apenas para este propósito. 
E as massas da fase 3 foram desenvolvidas com base em cenários estabelecidos e personas fictícias construídas apenas para este propósito. 
É importante destacar que as fases são independentes, nem as IFs, nem as personas e nem os cenários de uma fase se cruzam em nenhuma outra.
Cada dado foi pensado exclusivamente para a fase específica.

## Organização no diretório

Os documentos das fases 1 e 2 estão disponibilizados de acordo com os endpoints enquanto que os documentos 
da fase 3 estão organizados de acordo com os cenários definidos como exemplo de pagamento. 

Os cenários de pagamento estão em um readme próprio da api de pagamentos. 

## Nomenclatura
### Fase 1

Cada documento tem o nome construído com a seguinte lógica: 

*endereco-do-endpoint-numero-da-if-ficticia.numero-do-documento-desta-if*  

Exemplo:
get-discovery-status-7.1

### Fase 2

Cada documento tem o nome construído com a seguinte lógica: 

endereco-do-endpoint-numero-da-persona.numero-do-documento-desta-persona

Quando uma persona tem mais de um documento associado a ela o sufixo final é acrescido em um.
Como o exemplo abaixo em que a persona 1 tem dois consentimentos associados a ela. 

Exemplo:
post-consents-1.1  
post-consents-1.2  

### Fase 3

A fase 3 tem a nomenclatura diferenciada, pois estamos associando o sufixo ao número do cenário montado.
Cada documento tem o nome construído com a seguinte lógica: 

prefixo-do-cenario-ordem-no-fluxo-endereco-do-endpoint

Exemplo de cenário de sucesso com os quatro passos do pagamento:

*cenario-01.1-post-consents.json*  
*cenario-01.2-post-consents.json*  
*cenario-01.3-post-consents.json*  
*cenario-01.4-post-consents.json*  
