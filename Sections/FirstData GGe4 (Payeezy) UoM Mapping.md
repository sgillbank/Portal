# Background

If your application is sending [Level 3 transaction fields](Level%202%20and%20Level%203%20Default%20Fields.md) onto PayFabric and your gateway is First Data GGe4, you must make sure the "ItemUOM" transaction field is set to correct code. Otherwise, your transaction will not get upgraded interchange rate during settlement. And this happen only your customer is using "Business/Corporate Card". A full list of UoM code is [here](https://firstdata.zendesk.com/entries/23393247-Units-of-Measure). Below is a screenshot of this page.

![uomcode](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/uommapping.png)

# PayFabric UoM Mapping

Sometimes, for developers who are programming payment application against an ERP system, they will find the UoM code in ERP are different from the ones accepted by FirstData GGe4. In this situation, developers can utilize this out-of-box PayFabric features to achieve the target of UoM code transforming. For example, in your ERP system, you have a UoM code "Case" and whereas FirstData GGe4 doesn't have this code. Then you can map "Case" to "BX" as below.

![uommapping](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/uommapping2.png)

In your application code, you can feel free to send ERP UoM code into "ItemUOM" field. PayFabric will help you translate to FirstData UoM code based on your settings. 

