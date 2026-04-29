---
title: Passing data from Salesforce to CPQ fields
description: Learn how to pass information from Salesforce into CPQ using the On Configuration/Reconfigure enrichment.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Passing data from Salesforce to CPQ fields

Learn how to pass information from Salesforce into CPQ using the On Configuration/Reconfigure enrichment.

Sometimes a CPQ configuration needs information from outside the configuration passed into the configuration on initialization. There are several ways to do this.

![Workflow](../images/cpq-enrichments-info-in-info-out.png)

If the information can be found on the Salesforce quote, use the twinning method of data transfer. External data would be assigned to a field in CPQ.

In this example, CPQ uses the On Configuration/Reconfigure enrichment \(called “Init enrichment” here\) to send an API call to the website “FakerAPI.it”. This website sends an API response with fake credit card information.

![API](../images/cpq-enrichments-faker-api.png)

Our goal is to populate a field in CPQ with the credit card type \(Visa, MasterCard, or other\).

## Setup

The first step of using an enrichment and external connection is to set it up. For instructions, see [Using external connections with OAuth support](using-external-connections-with-oauth-support.md). \(Note that the examples in this link focus mostly on the On BOM Response enrichment. This article complements the other because it focuses more on the Init enrichment.\)

The following information is used for our external connection to FakerAPI.it.

|Parameter|Value|
|---------|-----|
|Name|CardType|
|variableName|cardType|
|host|https://fakerapi.it|
|path|/api/v1/credit\_cards?\_quantity=1|
|Authentication Type|None|
|timeout|500|

Next, the field in CPQ must be created and associated with the blueprint that uses the enrichment. All four CPQ field types can be assigned data from the enrichment. The data assigned to the field from the API response just needs to match the field.

## Scripting the Init enrichment

The final step is to write the script for the Init enrichment. The enrichment's language is based on JavaScript, and users are encouraged to look at the Help section of the advanced function editor for most of the sample scripts needed. The following lines of code are not in the Help section, so are documented here.

To reference an external connection in an enrichment, use the following:

```
Var {varName} = External.{externalConnectionVariableName}(inputs)
```

If calling to Salesforce, change `External` to `Salesforce`.

```
Var {varName} = Salesforce.{externalConnectionVariableName}(inputs)
```

If there are no inputs, use empty parentheses.

In the Init enrichment, the Fields item changes to Configuration Request, which is referenced in the script as `cfgRequest`. This item is used to define fields in the CPQ configuration that is being initialized. Therefore, if external data is passed to CPQ, it is assigned from the `cfgRequest` JSON object and values have to be programmed into it. That can be scripted two ways \(Items in curly braces \( \{ \} \) and in italics are determined by the user\):

```
cfgRequest.{LogikVariableName}.set(“value”, “{value}”) ;
```

```
cfgRequest.{LogikVariableName}.value = ”{value}” ;
```

For example, suppose the company Solar Fare Well sells and installs solar panels. They want to assign two external values to their configurator: which way the roof faces and the square footage of the roof. Their Init enrichment might have the following lines of code:

```
cfgRequest.roofDirection.value= “North”;
cfgRequest.sqft.set(“value”, 500);
```

Notice that the number does not need quotes around it.

The Configuration Request item contains all the requests on the configuration. This includes fields that are twinned into CPQ. Moreover, `cfgRequest` is populated with the twinned fields before the Init enrichment script runs. This means that twinned fields can be used as variables \(inputs\) for the enrichment script and external connection, which can affect the output from the script and external connection. The following snippet shows the formatting options when getting values from `cfgRequest`.

```
var x = cfgRequest.{varName}.get(“value”);
```

```
x= cfgRequest.{varName}.value;
```

## Sample script solution

When implementing the above code, the first step is to look at the JSON response from the external connection call.

Using the external connection defined above, the following enrichment script returns an API response similar to the one that follows just below.

```
var sample=External.cardType();
return sample;
```

```
"body": {
	"total": "1",
	"code": "200",
	"data": [
		{
			"owner": "Mercedes Emmerich",
			"number": "2410279364686428",
			"expiration": "04/25",
			"type": "American Express"
		}
	],
	"status": "OK"
}
```

Note that this is not the entire API response, and that card data changes with each API call. As expected, this matches the API response from the website.

Next, we need to parse down to the card type. The formatting examples in the Advanced Function Help section can help you identify how to parse the JSON object response.

The following enrichment script returns the result that follows.

```
var sample=External.cardType();
var x=sample.body.data[0].type;
cfgRequest.cardType_adv.set("value", x);
return cfgRequest;
```

```
{
  "cardType_adv": {
    "userEdited": false,
    "value": "American Express"
  }
} 
```

So in CPQ, the cardType\_adv field is defined as “American Express”.

## Query data from Salesforce \(SOQL\)

As mentioned earlier, data that is in a Salesforce quote can be twinned into CPQ. However, if the data is found elsewhere in Salesforce, the Init enrichment has Salesforce as the external connection, and you perform a query using Salesforce Object Query Language \(SOQL\). If you are unfamiliar with the SOQL language, you can find out more at Salesforceʼs Trailhead site.

To use SOQL in the enrichment, the only difference from the examples above is a change to the external connection. In CPQ Admin, click **Utilities**, click **External Connections**, and then click **New**. This is how you normally create an external connection.

For the field integration type, select **Salesforce**. This provides a box for you to enter your SOQL query.

![External connection](../images/cpq-enrichments-integration-type-salesforce.png)

**Related topics**  


[Twinning: pulling Salesforce CPQ quote information into CPQ](twinning_how_to_pull_salesforce_cpq_quote_information_into_logik_io.md)

