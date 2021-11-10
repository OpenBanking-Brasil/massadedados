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
 - Credtor: PF
 - Debtor: PF
 - localInstrument: QRDN
 - chave válida no DICT

---
### Cenário 16: Iniciação de pagamento PF:PJ - QRES

- Cenário de Sucesso
 - Credtor: PF
 - Debtor: PF
 - localInstrument: QRES
 - chave válida no DICT

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
### Cenário 20: Exceção

- Cenário de Exceção cm TIMEOUT no SPI
 - Credtor: PJ
 - Debtor: PF
 - localInstrument: DICT

---
### Cenário 21: Exceção

- Cenário de Exceção com CLOSED_CREDITOR_ACCOUNT_NUMBER
- Credtor: PJ
- Debtor: PF
- localInstrument: DICT

---
### Cenário 22: Exceção

- Cenário de Exceção com INCOMPATIBLE_DATE
- Credtor: PJ
- Debtor: PF
- localInstrument: DICT

---
### Cenário 23:  Exceção

- Cenário de Exceção com EXPIRED_MULTIPLE_AUTHORISATIONS
- Credtor: PJ
- Debtor: PF
- localInstrument: DICT

---
### Cenário 24: Exceção

- Cenário de Exceção com INSUFFICIENT_FUNDS
- Credtor: PJ
- Debtor: PF
- localInstrument: DICT 

---
### Cenário 25:  Exceção

- Cenário de Exceção com INVALID_CREDITOR_CLEARING_SYSTEM_MEMBER_IDENTIFIER
- Credtor: PF
- Debtor: PF
- localInstrument: MANU

---

### Cenário 26:  Exceção

- Cenário de Exceção com INVALID_CREDITOR_ACCOUNTTYPE
- Credtor: PF
- Debtor: PF
- localInstrument: DICT 

---
### Cenário 27: Exceção
 
- Cenário de Exceção com VALOR_ACIMA_LIMITE 
- Credtor: PF
- Debtor: PF
- localInstrument: DICT
