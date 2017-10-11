# Summary

PayFabric support multiple and growing payment gateways. Each gateway will have their own setup information , therefore PayFabric support these setup with a flexible way. As you are switching the "Connector" field on the Gateway Account Profiles page, the "Gateway Fields" section will be refreshed in accordance with your selection.

And currently, PayFabric support below gateways.
* Payflowpro (Paypal)
* FirstData GGe4 (Payeezy)
* USAePey
* Authorize.Net
* WorldPay
* Cybersource SOAP
* Cybersource
* Moneris
* Paymentech
* Forte
* FrontStream Fundraising Pro

We only listed the required fields as below. You might want to go back [Setup Gateway Account](Quick%20Start.md#setup-gateway-account) to review the process of creating a gateway account profile on PayFabric.

## Payflowpro

| Field         | Value                   | 
| ------------- |:---------------------------- | 
| Server.Address| Sandbox: https://pilot-payflowpro.paypal.com |
|| Production: https://payflowpro.paypal.com | 
| Partner  | `<Obtain account info from gateway provider>`      |
| Vendor   | `<Obtain account info from gateway provider>`      |
| UserID   | `<Obtain account info from gateway provider>`      |
| Password | `<Obtain account info from gateway provider>`      |

## FirstData GGe4 (Payeezy)

| Field         | Value                   | 
| ------------- |:---------------------------- | 
| Server.Url      | Sandbox: https://api.demo.globalgatewaye4.firstdata.com/transaction/v12 | 
|| Production: https://api-alt.globalgatewaye4.firstdata.com |
| APIKeyID        | `<Obtain account info from gateway provider>`      |
| HMACKey         | `<Obtain account info from gateway provider>`      |
| GatewayID       | `<Obtain account info from gateway provider>`      |
| GatewayPassword | `<Obtain account info from gateway provider>`      |

## USAePay

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| SourceKey           | `<Obtain account info from gateway provider>`      |
| TestMode            | False      |

## Authorize.Net

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address      | Sandbox: https://test.authorize.net/gateway/transact.dll |
|| Production: https://secure2.authorize.net/gateway/transact.dll | 
| Server.Port         | 443 |
| LoginID             | `<Obtain account info from gateway provider>`      |
| TransactionKey      | `<Obtain account info from gateway provider>`      |
| TestMode            | False|


## WorldPay

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Url           | Sandbox & Production: https://trans.worldpay.us/Web/services/TransactionService |
| AcctID               | `<Obtain account info from gateway provider>`      |
| SubID                | `<Obtain account info from gateway provider>`      |
| MerchantPIN          | `<Obtain account info from gateway provider>`      |

## Cybersource SOAP

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address       | Sandbox: https://ics2wstesta.ic3.com/commerce/1.x/transactionProcessor |
|| Production: https://ics2wsa.ic3.com/commerce/1.x/transactionProcessor/ | 
| MerchantID           | `<Obtain account info from gateway provider>` |
| TRANSACTION_Key      | `<Obtain account info from gateway provider>` |
| CurrencyCode         | `<Obtain account info from gateway provider>` |

## Cybersource

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address       | Sandbox: ics2test.ic3.com | 
|| Production: ics2.ic3.com|
| MerchantID           | `<Obtain account info from gateway provider>` |
| CurrencyCode         | `<Obtain account info from gateway provider>` |

For gateway cybersource, there's a small difference. Gateway requires merchant use X509 certification file. You will see the two file uploading textbox on PayFabric like below:

![fileuploading](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/gateway_cybersource.png)

You will have to upload your X509 files allocated from gateway.

## Moneris

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address       | Sandbox: https://esqa.moneris.com:43924/gateway2/servlet/MpgRequest |
|| Production: https://www3.moneris.com:43924/gateway2/servlet/MpgRequest | 
| Server.Port          | Leave Blank          |
| StoreID              | `<Obtain account info from gateway provider>` |
| APIToken             | `<Obtain account info from gateway provider>` |
| eCommerceIndicator   | `<Obtain account info from gateway provider>` |

## Paymentech

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address       | Sandbox: https://orbitalvar1.paymentech.net/authorize |
|| Production: https://orbital1.paymentech.net/authorize | 
| MerchantID           | `<Obtain account info from gateway provider>`|
| BIN                  | `<Obtain account info from gateway provider>` |
| TerminalID           | `<Obtain account info from gateway provider>` |
| IndustryType         | `<Obtain account info from gateway provider>` |
| CurrencyCode         | `<Obtain account info from gateway provider>` |
| CurrencyExponent     | `<Obtain account info from gateway provider>` |

## Forte

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Address       | Sandbox: https://sandbox.forte.net/api/v3 |
|| Production: must contact Forte Technical Support at go Live. | 
| OrganizationID       | `<Obtain account info from gateway provider>`|
| LocationID           | `<Obtain account info from gateway provider>` |
| APIAccessID          | `<Obtain account info from gateway provider>` |
| APISecureKey         | `<Obtain account info from gateway provider>` |

## FrontStream Fundraising Pro

| Field                | Value                   | 
| -------------------- |:---------------------------- | 
| Server.Url           | Sandbox: https://secureuat.artezhq.com/api/ |
|| Production: https://secure.e2rm.com/api/Donations | 
| UserName             | `<Obtain account info from gateway provider>`|
| Password             | `<Obtain account info from gateway provider>` |
| EventID              | `<Obtain account info from gateway provider>` |
| CurrencyID           | `<Obtain account info from gateway provider>` |
| OrganizationNameUDFID| `<Obtain account info from gateway provider>` |
| CustomerIDUDFID      | `<Obtain account info from gateway provider>` |
| InvoiceNumbersUDFID  | `<Obtain account info from gateway provider>` |
