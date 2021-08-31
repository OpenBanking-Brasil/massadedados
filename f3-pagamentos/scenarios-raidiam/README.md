Scenario 1:  
Consent Created Response [post-consents-1.1.json]  
Consent Creation Rejected Response [Sensedia: Does not apply. Consent is always created with AWAITING_AUTHORISATION   status.]  
Consent Authorization Rejected Response [Sensedia: Please give more details]  

 
Scenario 2:  
Consent Created Response [post-consents-2.2.json]  
Payment Creation Rejected [post-pix-payments-2.2.json]  
Consent Status Response (GET Consent) [get-consents-consentId-2.2.json]  

 
Scenario 3:  
Payment Creation Accepted [post-pix-payments-1.1.json]  
Consent Status Response [get-consents-consentId-1.1.json]  

 
Scenario 4:  
Consent Timed-out Response: (What’s the status)  
Consent Status Response (GET Consent)  

There are two cases that will result in Timed-out responses:  
1) Consent in an AWAITING_AUTHORISATION status for more than 5 minutes [post-consents-1.2.json] [get-consents-consentId-1.2.json]  
2) Consent in an AUTHORISED status for more than 60 minutes [post-consents-1.3.json] [get-consents-consentId-1.3.json]  

