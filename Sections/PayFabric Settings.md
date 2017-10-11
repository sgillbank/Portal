# Summary
Merchant navigate through **Configuration > PayFabric Settings**. The below screenshot is a typical example of settings. We will go over them one by one in following sections.

![settings](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/settings.png)

### PART A - Device Name

The dropdown will load all your devices. PayFabric support you configure different settings by devices. Every merchants will get system default device by default when they were creating a PayFabric account. Settings under "System Default" device is the default ones. However settings of other device can override the default settings. Thereby, the overridden setting will take effect if developers are calling API through the specific device.   

### PART B - Accept Card Types

By Default, PayFabric can support those card types listed on Page. However, merchant can disable one or more of them by clear the selections.

### PART C - Transaction Options

These are settings relate to process a payment transaction. Please refer to the table below

| Field                | Definition   | 
| :-------------------------|:-------------| 
| Shipping Address Required | By default, shipping address is not required as processing transactions. Checking this option to enable this logic. | 
| Partial Shipping          | This option is for capturing a pre-authorized transaction. By default, the capturing amount must be same with pre-authorization. By checking this option, merchant allow the capturing amount less than the original pre-authorization transaction. | 
| Fail On CVV2 Mismatch     | Payment gateways will verify the CSC(Card Security Code). By checking this option, PayFabric will write off your payment once the CSC verification failed by submitting a VOID transaction automatically. |
| Fail On Zip Mismatch      | Payment gateways will verify the Zip code. By checking this option, PayFabric will write off your payment once the zip code verification failed by submitting a VOID transaction automatically. |  
| Popup Message             | System will inform customer with popup message on hosted payment page and hosted wallet page.|
| Fail On Address Mismatch  | Payment gateways will verify the billing address. By checking this option, PayFabric will write off your payment once the address verification failed by submitting a VOID transaction automatically.|

> Some gateways with good fraud protection service could be able to configured to deny those transactions when the billing address, zip or cvv2 verification fail. In this case, merchants don't have to check these options.


### PART D - General Settings

| Field                          | Definition   | 
| :------------------------------|:-------------| 
| Maximum History Cards          | Restrict the maximum number of wallet entries which customer can create. The loading performance of hosted page may be lagged because your customer creating a large number of wallet entries | 
| Transaction Key Prefix         | User defined prefix for transaction key. | 
| PostURL                        | PayFabric will post transaction data fields (Non-sensitive fields) to this URL once this transaction is processed (successful or failed) |
| Batch Number Prefix            | User defined prefix for batch number |  
| Maximum Amount Per Transaction | Apply an up limit onto the maximum amount for each transaction |
| Return URL                     | A URL address that PayFabric can redirect to once a transaction is processed. the response fields will be encoded and attached into query string.|
| Maximum Shipping Address       | Restrict the maximum number of shipping address entries which customer can create. The loading performance of hosted page may be lagged because your customer creating a large number of shipping address entries|
| Config UOM Mapping for GGe4 | View [this](FirstData%20GGe4%20(Payeezy)%20UoM%20Mapping.md) article to get detailed information |

