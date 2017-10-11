# Summary
For merchants want to integrate with PayFabric hosted payment page and hosted wallet page, there's a way to inject custom css code into hosted page to fit the overall style for the 3rd party applications. To implement custom theme, you will get the PayFabric account ready and do some priliminary configuration. Please go through [Quick Start](Quick%20Start.md) for starting with PayFabric.

To implement a custom theme, below are steps involved into the process:
* [Define Themes](#definetheme)
* [Apply a Theme To a Device](#applytheme)

For a list of the most used element id's in the hosted page [please see below](#field-ids).

# Define Themes

Navigate through Home > Dev Central > Themes to open below page. By clicking "Create New" button, you can add a new theme name into your account. A theme includes two parts: "custom css style" and "custom javascript". Your writing will be applied to hosted payment page. So that you can apply your own look and feel. 

![themes](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/themes.png)

Also you can choose to show/hide the related fields on hosted payment page by check/uncheck the parameters of the theme.

![ThemeParams](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/ThemeParams.PNG)

# Apply a Theme To a Device

Navigate through Home > Dev Central > Devices to open below page. This is device list in your account. By clicking the icon button in column "Default Theme", an extended region will be expanded. All available themes will be listed in this region, you can assign one of them be the default theme of a device. 

![devicetheme](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/themes1.png)

# Field IDs

The PayFabric Hosted page has a variety of different elements on the page.  Here is a list of the most common of them and their HTML Element IDs, types and the controlling CSS class name of the label and element (here after referred to as the block).

PayFabric Themes support the use of both Cascading Style Sheets (CSS) and JavaScript.  Our Hosted Pages are automatically loaded with JQuery.  You are able to use the JQuery ID and CSS Class selectors, such as `$("#SetupID_ID")` for specific Element ID's and `$(".setupid")` for the Block Class Names, for additional ID's and Class Names please see the below tables.

| Field | Block Class Name | Element ID | Element Type | Note |
| :--- | :--- | :--- | :--- | :--- |
| Gateway Account | setupid | SetupID_ID | Drop Down Box |  |
| Transaction Type | trxtype | TransactionType | Drop Down Box | |
| Batch Number | batch | BatchNumber | Text Box | |
| Pay Later | paylater | PayLater | Text Box (Date Picker) | |
| Transaction Amount | total | TrxAmount | Text Box | |
| Currency | currency | CurrencyCode | Drop Down Box | |
| Billing Information | N/A | billaddress | Grouping | See [Billing Fields](#billing-fields) |
| Shipping Information | N/A | shipaddress| Grouping | See [Shipping Fields](#shipping-fields) |
| Payment Information | N/A | payment | Grouping | See [Payment Fields](#payment-fields) |


## Billing Fields

| Field | Block Class Name | Element ID | Element Type | Note |
| :--- | :--- | :--- | :--- | :--- |
| Address Line 1 | N/A | NewBillAddresses_AddressLine1 | Text Box |  |
| Address Line 2 | N/A | NewBillAddresses_AddressLine2 | Text Box |  |
| Address Line 3 | N/A | NewBillAddresses_AddressLine3 | Text Box |  |
| City | City | NewBillAddresses_CityCode | Text Box |  |
| State/Province | State | NewBillAddresses_StateCode | Text Box |  |
| Zip/Postal Code | Zip | NewBillAddresses_ZipCode | Text Box |  |
| Country | N/A | NewBillAddresses_CountryCode | Text Box |  |
| Phone | N/A | NewBillAddresses_Phone1 | Text Box |  |
| Email | N/A | NewBillAddresses_Email | Text Box |  |


## Shipping Fields

| Field | Block Class Name | Element ID | Element Type | Note |
| :--- | :--- | :--- | :--- | :--- |
| Historic Address Selector | addresslist | shipaddresslist | Drop Down Box |  |
| Use New Address | usenewaddress | shipuse | Check Box | Visible when Use History Address checked |
| Address Line 1 | N/A | NewShipAddresses_AddressLine1 | Text Box |  |
| Address Line 2 | N/A | NewShipAddresses_AddressLine2 | Text Box |  |
| Address Line 3 | N/A | NewShipAddresses_AddressLine3 | Text Box |  |
| City | City | NewShipAddresses_CityCode | Text Box |  |
| State/Province | State | NewShipAddresses_StateCode | Text Box |  |
| Zip/Postal Code | Zip | NewShipAddresses_ZipCode | Text Box |  |
| Country | N/A | NewShipAddresses_CountryCode | Text Box |  |
| Phone | N/A | NewShipAddresses_Phone1 | Text Box |  |
| Email | N/A | NewShipAddresses_Email | Text Box |  |
| Use History Address | N/A | useoldAddress | Check Box | Visible when Use New Address checked |
| Same As Billing | N/A | asbilluse | Check Box | Visible when Use New Address checked |


## Payment Fields

| Field | Block Class Name | Element ID | Element Type | Note |
| :--- | :--- | :--- | :--- | :--- |
| Historic Card Selector | historycards | ChosenCardID | Drop Down Box |  |
| Card Information | CardContainer | N/A | Grouping | Below Fields are included in this group |
| Account # | N/A | NewCard_CardNumber | Text Box |  |
| Expiration Date | CardDate | exptime1 *and* exptime2 | Text Box |  |
| CVV | cvv2 | NewCard_SecurityCode | Text Box |  |
| Card Name | NameOnCard | N/A | Grouping |  |
| First Name | FirstName | NewCard_CardHolderFirstName | Text Box |  |
| Middle Initial | MiddleInitial | NewCard_CardHolderMiddleName | Text Box |  |
| Last Name | LastName | NewCard_CardHolderLastName | Text Box |  |
| Save Card | savecard_h6Container | NewCard_IsSaveCard | Check Box |  |
| Is Default Card | savecard_h6Container | NewCard_IsDefaultCard | Check Box | Visible when Save Card is ticked or existing card |

## JQuery Examples

To remove the Transaction Type Block from the page, try `$('.trxtype').remove();`

To make the Transaction Amount Element read-only, try `$('#TrxAmount').attr('readonly', 'true')`
