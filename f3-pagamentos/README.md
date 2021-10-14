# Massa fase 3 v. 1.0.1-rc1.1
Os scenarios de sucesso (fluxo feliz) foram elaborados considerando o fluxo endToend da API - Pagamentos v. 1.0.1. 
Sendo assim, para cada cenário definido, existem quatro arquivos "*.json", ou seja, um para cada endpoint da API - Pagamentos.

## Nomenclatura

O nome o arquivo .json foi formatado da seguinte forma:   

nome-do-endpoint-numerodocenario-numero-do-passo-no-fluxo  

Exemplo na ordem do fluxo de pagamento:  

1. *POST /payments/v1/consents - Exemplo: scenario-01.1-post-consents*  

2. *GET /payments/v1/consents/{consentId} - Exemplo: scenario-01.2-get-consents*  

3. *POST /payments/v1/pix/payments - Exemplo: scenario-01.3-post-pix-payments.json*  

4. *GET /payments/v1/pix/payments/{paymentId} - Exemplo: scenario-01.4-get-pix-payments.json*  

---

  ## Cenários:  

### Cenário 1: Sucesso iniciação de pagamento DICT chave aleatória

 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - localInstrument: DICT
 - DICT: chave aleatória

 ---

 ### Cenário 2: Sucesso iniciação de pagamento DICT e-mail 

 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - localInstrument: DICT
 - DICT: e-mail

 ---

### Cenário 3: Sucesso iniciação de pagamento DICT cpf
 
 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - DICT: CPF

 ---

 ### Cenário 4: Sucesso iniciação de pagamento DICT celular

 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PJ - LTDA
 - DICT: celular  

---  

### Cenário 5: Sucesso iniciação de pagamento MANU conta corrente

 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PJ - MEI
 - MANU: conta corrente  

---

### Cenário 6: Sucesso iniciação de pagamento MANU conta pagamento

 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PJ - LTDA
 - MANU: conta pagamento pré-paga

---
### Cenário 7: Sucesso iniciação de pagamento MANU conta poupança
 
 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PJ - LTDA
 - MANU: conta pagamento poupança

---

### Cenário 8: Sucesso Iniciação de pagamento INIC chave aleatória
 
 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PF
 - INIC: chave aleatória
  
---

### Cenário 9: Sucesso Iniciação de pagamento INIC chave e-mail
 
 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PF
 - INIC: chave e-mail

 ---
 
 ### Cenário 10: Sucesso Iniciação de pagamento INIC chave cnpj

 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PF
 - INIC: chave cnpj

---

### Cenário 11: Sucesso Iniciação de pagamento INIC chave celular

 - Cenário de Sucesso
 - Credtor: PJ - LTDA
 - Debtor: PF
 - INIC: chave celular

 ---
### Cenário 12: Iniciação de pagamento PF:PF com múltiplas alçadas pendente de autorização

 - Cenário de Sucesso
 - Credtor: PF
 - Debtor: PF
 - Múltiplas alçadas parcialmente aprovado
 - localInstrument: DICT

---
### Cenário 13: Iniciação de pagamento PF:PJ - múltiplas alçadas: pendente de autorização

- Cenário de Sucesso
 - Credtor: PJ
 - Debtor: PF
 - Múltiplas alçadas parcialmente aprovado
- localInstrument: INIC

----
### Cenário 14: Iniciação de pagamento PF:PF - múltiplas alçadas: rejeitado

 - Cenário de exceção
 - Credtor: PF
 - Debtor: PF
 - Múltiplas alçadas: DENIED_MULTIPLE_AUTHORISATIONS
 - localInstrument: DICT

---
### Cenário 15: Iniciação de pagamento PF:PJ - QRDN
- Cenário de Sucesso
 - Credtor: PJ
 - Debtor: PF
 - localInstrument: QRDN


---
### Cenário 16: Iniciação de pagamento PF:PJ - QRES

- Cenário de Sucesso
 - Credtor: PJ
 - Debtor: PF
 - localInstrument: QRES

---
### Cenário 17: Exceção

Consentimento com creditor.personType é diferente de PESSOA_NATURAL, PESSOA_JURIDICA

---
### Cenário 18: Exceção

Consentimento com forma de pagamento inválida  

---
### Cenário 19: Exceção 

Consentimento com forma de pagamento inválida  

---
### Cenário 20: 


---
### Cenário 21: Exceção

Iniciação de pagamento com um consentimento em Status "REJECTED"  

---
### Cenário 22: Exceção
 Iniciação de pagamento utilizando um consentimento AUTHORISED com data divergente da data utilizada na iniciação de pagamento  

---
### Cenário 23:  Exceção

Iniciação de pagamento com um consentimento AUTHORISED com dados de conta não pertencentes ao creditor/cpfCnpj informado no consentimento utilizado  

---
### Cenário 24: Exceção
 Iniciação de pagamento com um consentimento AUTHORISED informando um valor superior ao saldo existente na conta do debtor para realização do pagamento  

---
### Cenário 25:  Exceção
Iniciação de pagamento com um consentimento AUTHORISED informando o ispb do creditorAccount inválido ou inexistente  

---

### Cenário 26:  Exceção
Iniciação de pagamento com um consentimento AUTHORISED informando um tipo de conta (creditorAccount/accountType) incorreto para a conta informada para o creditor  

---
### Cenário 27: Exceção
 Iniciação de pagamento com um consentimento AUTHORISED informando payment/amount divergente do informado no consentimento utilizado  


  * Para mais informações sobre a especificação da API- Pagamentos, consulte https://openbanking-brasil.github.io/areadesenvolvedor/swagger/swagger_payments_apis.yaml
