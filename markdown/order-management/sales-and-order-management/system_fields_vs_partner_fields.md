---
title: ServiceNow CPQ fields, system fields, and partner fields
description: Learn about the three types of fields in ServiceNow CPQ—ServiceNow CPQ, system fields, and partner fields. Understand how each type stores, retrieves, and displays data in configurations, and how they interact with Salesforce and partner systems for seamless data integration.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 4
breadcrumb: [Configure fields, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow CPQ fields, system fields, and partner fields

Learn about the three types of fields in ServiceNow CPQ—ServiceNow CPQ, system fields, and partner fields. Understand how each type stores, retrieves, and displays data in configurations, and how they interact with Salesforce and partner systems for seamless data integration.

There are three categories of fields in the ServiceNow CPQ environment: ServiceNow CPQ fields, system fields, and partner fields.

## ServiceNow CPQ fields

A ServiceNow CPQ field is a user-defined field that is custom to the ServiceNow CPQ environment. Its type can be number, text, picklist, set, or product picker. When users create fields in CPQ, they can manually assign default values in the field definition, or they can set values through determination actions.

The following example shows how a user would set a ServiceNow CPQ field in an On Configure/Reconfigure enrichment:

```
cfgRequest.testField.set("value", "Hello World"); 
```

For a more complete description of ServiceNow CPQ fields, see [Configure fields](fields_101.md).

**Note:** In organizations that do not use Salesforce for their launch-point into ServiceNow CPQ, all fields must be initialized in their API call.

## System fields

![System fields](../images/cpq-fields-system-fields.png)

System fields are predefined. System fields cannot be assigned a default value because they leverage the SFDC product cache \(or the current date and time\) to generate their values.

The following example shows how a user would call a system field in an On Configure/Reconfigure enrichment:

```
let pC = {"input2":cfgRequest.sys.productCode.value};
```

System fields can be added directly to any layout. There are no issues with displaying them regardless of whether they contain predefined data.

In the layout editor:

![Layout editor](../images/cpq-fields-layout-editor.png)

In the Configurator UI:

![Layout editor screen](../images/cpq-fields-configurator-ui.png)

Unit of Measure is blank because in this example, it has not been defined in SFDC.

The mapping of each of these system fields to their respective SFDC object is as follows. The field API name is in parentheses.

-   sys.productUOM &gt; Product: Quantity Unit Of Measure \(QuantityUnitOfMeasure\)
-   sys.productName &gt; Product: Product Name \(Name\)
-   sys.productFamily &gt; Product: Product Family \(Family\)
-   sys.productDescription &gt; Product: Product Description \(Description\)
-   sys.productCode &gt; Product: Product Code \(ProductCode\)
-   sys.enableValidation: value defaults to true
-   sys.currentDate: Simple time API call, returns date of UTC
-   sys.actionContext &gt; Quote Line: Action Context \(LGK ActionContext c\)
-   sys.productPrice &gt; Price Book Entry: List Price \(UnitPrice\)
-   sys.productId: value depends on Admin Settings

    sys.productId changes to whatever is defined in your ServiceNow CPQ environment settings. For instance, if the Product Id field was set to Product Code, the resulting data would be Product Code, making it identical to the sys.productCode field.


![Product code](../images/cpq-fields-product-code.png)

If the Product Id field was instead set to Partner Id, the data would be pulled from the SFDC field Product2 Id \(ID as the field API name\):

![System fields screen](../images/cpq-fields-partner-id-example.png)

## Partner fields

![Partner fields](../images/cpq-fields-partner-fields.png)

Partner fields are fields that use a POST call to initialize a configuration via API. Partner fields leverage the partnerʼs data set to generate field values.

The mapping of each of these partner fields to their respective SFDC object is as follows. The field API name is in parentheses.

-   partner.quote.id Quote &gt; Record ID \(Id\)
-   partner.quote.lineId Quote Line &gt; Record ID \(Id\)
-   partner.quote.pricebookId Quote &gt; Pricebook ID \(SBQQPricebookIdc\)
-   partner.quote.currencyIsoCode Quote &gt; CurrencyIsoCode

    partner.quote.currencyIsoCode defaults to USD if your organization does not have multi-currency enabled in their Salesforce Org. To enable multi-currency, follow the steps in this Salesforce article: [Enable Multiple Currencies](https://help.salesforce.com/s/articleView?id=sales.admin_enable_multicurrency.htm&type=5).


When using these fields, it’s important to note that some of the data may not have any value \(null\) when the product is first configured. To make sure that there are no initialization errors, include null checks in any rules or scripts that utilize partner fields.

These fields cannot be directly added to a layout like system fields can. Instead, you can use ServiceNow CPQ fields to populate the data in partner fields via an initialization enrichment.

The following example initialization enrichment populates the values of the partner fields into the configurator:

```
let quoteId = cfgRequest.partner.quote.id.value;
let lineID = cfgRequest.partner.quote.lineId.value;
let currencyISO = cfgRequest.partner.quote.currencyIsoCode.value;
let priceBookID = cfgRequest.partner.quote.pricebookId.value;

if (quoteId != null) {
	cfgRequest.quoteIDTest.set("value", quoteId);
}
if (lineID != null) {
	cfgRequest.lineIDTest.set("value", lineID);
}
if (currencyISO != null) {
	cfgRequest.currencyISOCodeTest.set("value", currencyISO);
}
if (priceBookID != null) {
	cfgRequest.pricebookIDTest.set("value", priceBookID);
}
return cfgRequest;
```

Initial configuration:

![Initial configuration screen.](../images/cpq-fields-initial-config.png)

Reconfiguration:

![Partner fields](../images/cpq-fields-reconfig.png)

Line ID is now populated.

How you use partner and system fields is up to you. Some organizations find it helpful to display this information in the configurator to the end user, while others use it in the background in rules to drive pricing conditions.

**Related topics**  


[Grid-style fields and field collections](what_field_type_should_i_use_for_organizing_field_options_and_data.md)

[Configure fields](fields_101.md)

