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

### Cenário 1: Sucesso iniciação de pagamentos: 

 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - localInstrument: DICT
 - DICT: chave aleatória

 ---

 ### Cenário 2: Sucesso iniciação de pagamentos: 

 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - localInstrument: DICT
 - DICT: e-mail

 ---

### Cenário 3: Sucesso iniciação de pagamento:
 
 - Cenário de Sucesso
 - Credtor: PESSOA_NATURAL
 - Debtor: PJ - LTDA
 - DICT: CPF

 ---

3) PJ-LTDA - Iniciação de Pagamento para Pessoa Jurídica - LTDA com creditor para PESSOA_NATURAL e debtorAccount de Conta de Pagamento Pré-Paga  

4) PJ-LTDA - Iniciação de Pagamento para Pessoa Jurídica - LTDA com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta Corrente  

5) PJ-LTDA - Iniciação de Pagamento para Pessoa Jurídica - LTDA com creditor para PESSOA_JURIDICA MEI e debtorAccount de Conta Corrente  

6) PJ-LTDA - Iniciação de Pagamento para Pessoa Jurídica - LTDA com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta Poupança  

7) PJ-LTDA - Iniciação de Pagamento para Pessoa Jurídica - LTDA com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta de Pagamento Pré-Paga  

8) PJ-MEI - Iniciação de Pagamento para Pessoa Jurídica - MEI com creditor para PESSOA_NATURAL e debtorAccount de Conta Corrente  

9) PJ-MEI - Iniciação de Pagamento para Pessoa Jurídica - MEI com creditor para PESSOA_NATURAL e debtorAccount de Conta Poupança  

10) PJ-MEI - Iniciação de Pagamento para Pessoa Jurídica - MEI com creditor para PESSOA_NATURAL e debtorAccount de conta de Pagamento Pré-Paga  

11) PF - Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_NATURAL e debtorAccount de Conta Corrente  

12) PF - Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_NATURAL e debtorAccount de Conta Corrente  

13) PF- Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_NATURAL e debtorAccount de Conta Poupança  

14) PF - Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta Corrente  

15) PF - Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta Poupança  

16) PF - Iniciação de Pagamento paraa Pessoa Natural com creditor para PESSOA_JURIDICA LTDA e debtorAccount de Conta de Pagamento Pré-Paga  

17) PF- Iniciação de Pagamento para Pessoa Natural com creditor para PESSOA_JURIDICA MEI e debtorAccount de Conta Poupança  

18) Criar consentimento com forma de pagamento inválida  

19) Criar consentimento com data de pagamento inválida  

20) Criar Iniciação de pagamento com um consentimento em Status "CONSUMED"  

21) Criar Iniciação de pagamento com um consentimento em Status "REJECTED"  

22) Criar Iniciação de pagamento utilizando um consentimento AUTHORISED com data divergente da data utilizada na iniciação de pagamento  

23) Criar Iniciação de pagamento com um consentimento AUTHORISED com dados de conta não pertencentes ao creditor/cpfCnpj informado no consentimento utilizado  

24) Criar Iniciação de pagamento com um consentimento AUTHORISED informando um valor superior ao saldo existente na conta do debtor para realização do pagamento  

25) Criar Iniciação de pagamento com um consentimento AUTHORISED informando o ispb do creditorAccount inválido ou inexistente  

26) Criar Iniciação de pagamento com um consentimento AUTHORISED informando um tipo de conta (creditorAccount/accountType) incorreto para a conta informada para o creditor  

27) Criar Iniciação de pagamento com um consentimento AUTHORISED informando payment/amount divergente do informado no consentimento utilizado  


  * Para mais informações sobre a especificação da API- Pagamentos, consulte https://openbanking-brasil.github.io/areadesenvolvedor/swagger/swagger_payments_apis.yaml
