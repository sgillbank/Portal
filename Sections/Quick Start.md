# Quick Start in five minutes
To start integration with PayFabric, developers will have to pre-configure something on PayFabric portal. The simplest scenario is you are just consuming the **Payment APIs**, in this case, you have to
* [Sign up a PayFabric Account](#sign-up)
* [Define Devices](#define-devices)
* [Setup a Gateway Account](#setup-gateway-account)


## Sign up

The process of registering an account for Sandbox PayFabric is almost the same with other web applications in general. You will navigate your browser to ``https://www.payfabric.com``, click 'Sign up' link, and populate all necessary fields of registration form to submit. Later, you will receive an activation email from support@payfabric.com, which contains an activation link you have to confirm your registration.


## Sign in

Click 'click here' link on the activation page, you can login PayFabric portal with your activated account, and you also can login later either through navigate to ``https://www.payfabric.com``, click 'Sign in' link or navigate to ``https://www.payfabric.com/portal`` directly.


## Access PayFabric Service
Click 'Access PayFabric Sandbox' to start using test PayFabric payment service.

## Define Devices
You have to create at least one device ([Glossary](https://github.com/PayFabric/Portal/#glossary)) before consuming Payment APIs. To populate a new Device ID, navigate through **Settings > DEV Central > Devices**. You will be redirected to page "Device Management". Initially, this screen has only one **Generate** button. Then you can click this button and populate fields "Device Name", "Password", "Confirm Password", and click "Save". You will get this screen. 

![device id](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/deviceid.png)

You can keep on adding multiple devices based on your business scenarios of your company. Normally, one device is corresponding to one kind of application. Different application may have different demand of displaying PayFabric hosted payment page. This is **PayFabric Theme** coming into picture. A "Theme" can be assigned to a device to enable the PayFabric hosted page get a specific UI when loading at that device. You must notice that there's a column in above grid, named "Default Theme". However you will be informed "You don't have a theme, you can go to Theme page to create one" at this moment. 

The "Themes" page can be displayed by navigating **Settings > DEV Central > Themes** on the left menu. You will be landing on below page. To create a new theme, you can click the button "Create New" and save. The below screen demos the simplest example, that is, change all the hyperlink's font color to red. And of course, you can add more css code here to affect the PayFabric hosted payment/wallet page. However, if you don't utilize the PayFabric hosted payment/wallet page, you can feel free to leave it blank.

![themes](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/themes.png)

After this step, you can go back to "Device Management" page and configure the "Default Theme" for your device. Besides configuring theme for device, you can also "Change" device name, "Reset" device password, "Revoke" the device, or "Delete" this device. "Revoke" device means regenerate the GUID, this is for better security concerns.

> Please keep your device id and password secure. If it's possible, you will want to change the device password periodically to improve the security level.


## Setup Gateway Account
Merchant's gateway account information has to be encrypted and stored into PayFabric before any payment transaction can be successfully submitted onto. By navigating through **Settings > Gateway Account**, you can open the page to create new gateway account profile by clicking "+ Add New Gateway" link > "Use your Existing Gateway" button, the below screen is displayed to you. You will populate all necessary fields in the form.

![gateway 2](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/gateway_profile.png)

The 4 fields above the section "Gateway Fields" are required by PayFabric system, whereas, those fields within the "Gateway Fields" section are required by gateway. So that, for different gateways, the gateway fields are  different. The explanation of PayFabric fields are as below, and we will introduce the gateway fields in separate chapters.

| Field                | Definition   | 
| :--------------------|:-------------| 
| Name                 | Gateway account profile name to identify the record. Must be unique. | 
| Connector            | Corresponding to payment gateways supported by PayFabric | 
| Processor            | Filtered by Connector. These are corresponding to the bank processors belong to a specific payment gateway. |
| Card Class           | Credit or ECheck. These are tender types this connector and process can support.|  

By picking up one connector, "Gateway Fields" section is displayed, where merchant will populate the necessary fields. To see in-depth details for the required fields for each gateway, check out the [Gateway Account Profiles](Gateway%20Account%20Profiles.md) page.

So, that's it! You are ready now to call the PayFabric Payment API. See more details [here](https://github.com/PayFabric/APIs/tree/v2) on the functionalities of our PayFabric API.

# Advanced Settings
For those developers who want to integrate **PayFabric Hosted Payment Page (PCI DSS Certified)** 
* [PayFabric Settings](PayFabric%20Settings.md)
* [L2/3 Default Fields](Level%202%20and%20Level%203%20Default%20Fields.md)
* [Receipt Email](Payment%20Receipt.md)
* [Themes](Themes.md)
