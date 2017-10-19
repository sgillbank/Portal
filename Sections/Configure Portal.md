sNodus PayFabric Cloud service has its own web portal where merchant can configure their PayFabric account settings, view and manage their transaction reports.

## PayFabric Portal URL:
https://www.payfabric.com/portal

## Service Mode

Under a single account login users can toggle the service mode between Sandbox & Live using the toggle switch on the top navigation bar.
By default, the account is set to sandbox mode when the account is first created.  Merchants can promote it to live mode in order to process live transactions by toggling the switch.

**Sandbox:**

![Sandbox](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/V3/Sandbox.png)

**Live:**

![Live](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/V3/Live.png)

## Devices

Any application that utilizes PayFabric in the backend for payment processing requires a set of Device ID and Password.

| Field                | Description  | 
| :--------------------|:-------------| 
| Device ID            | A unique and secure identifier to identify different applications under a single PayFabric merchant account. | 
| Device Password      | Assigned to a single device. Both Device ID and Device Password are required when integrating with PayFabric. | 

Every merchant will get a **System Default** device by default when creating a new PayFabric account. System Default device is the device which is used when a user creates a wallet entry or processes a transaction directly from the PayFabric portal.
To generate a new set of device and corresponding password navigate to Settings page. From **Settings** >  **Devices** (under **Dev Central** section), click **Generate** button then populate fields "Device Name", "Password", "Confirm Password" and click "Save". 

![Device](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/V3/DeviceManagement.png)

You may continue adding multiple devices based on your business needs. A single device corresponds to an application using PayFabric. 

## Themes

Different applications may have different demands when displaying PayFabric hosted payment page. This is where **PayFabric Theme** comes into the picture. A "Theme" can be assigned to a device to enable the PayFabric hosted page get a specific UI when loading from that device. Click [here](Themes.md) for more details.

## Gateway Profile

A payment gateway account is needed to process transactions with PayFabric. 
STEPS:
1.	If the payment gateway account is not associated to an existing PayFabric account, under **Settings** > **Gateway Account**, click ‘**+ Add New Gateway**’ to create new gateway profile.
2.	Choose ‘**Use your Existing Gateway**’ option.
3.	Fill in the remaining fields based on the payment gateway which is being used. Click [here](Gateway%20Configuration.md) for more details.

 * If a Gateway Account has already been setup, choose yours from the list of supported gateways. 
 * If a gateway account is needed, please contact Nodus Technologies Support for information on setting up a Gateway Account. 

4.	Click the ‘Save’ button to save your changes
5.	If there are multiple gateway accounts that need to be setup, such as if both Credit Cards and eChecks will be processed from this website, then repeat the steps in this section for each gateway account.

## Advanced Settings

* [PayFabric Settings](PayFabric%20Settings.md)
* [L2/3 Fields Default](L2%20and%20L3%20Fields%20Default.md)
* [Receipt Email](Payment%20Receipt.md)
* [Themes](Themes.md)
