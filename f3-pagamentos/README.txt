Os scenarios de sucesso (fluxo feliz) foram elaborados considerando o fluxo endToend da API - Pagamentos. 
Sendo assim, para cada cenário definido, existem quatro arquivos "*.json", ou seja, um para cada endpoint da API - Pagamentos.

1. POST /payments/v1/consents - Exemplo: scenario-01.1-post-consents

2. GET /payments/v1/consents/{consentId} - Exemplo: scenario-01.2-get-consents

3. POST /payments/v1/pix/payments - Exemplo: scenario-01.3-post-pix-payments.json

4. GET /payments/v1/pix/payments/{paymentId} - Exemplo: scenario-01.4-get-pix-payments.json

Para mais informações sobre a especificação da API- Pagamentos, consulte "https://openbanking-brasil.github.io/areadesenvolvedor/swagger/swagger_payments_apis.yaml"


Utilizando como exemplo o Scenario 01, a estrutura do diretório e conteúdo serão:

<Scenario-01>
  scenario-01.1-post-consents.json
  scenario-01.2-get-consents.json
  scenario-01.3-post-pix-payments.json
  scenario-01.4-get-pix-payments.json
