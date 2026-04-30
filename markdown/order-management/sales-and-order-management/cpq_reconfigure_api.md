---
title: The CPQ Reconfigure API
description: The CPQ Reconfigure API headlessly invokes CPQ services to reconfigure a quote bundle.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [API overview and resources, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The CPQ Reconfigure API

The CPQ Reconfigure API headlessly invokes CPQ services to reconfigure a quote bundle.

The CPQ Reconfigure API is a custom Salesforce API that invokes CPQ services headlessly. Unlike RFQ, this API is used to reconfigure an existing quote bundle.

## Prerequisites

The Runtime Client Token must be set in the Admin Custom Settings page in Salesforce. The token must include an origin that matches the ServiceNow CPQ URL, which cannot include a trailing slash \(/\) character.

The Runtime Configuration URL must also be set in the Admin Custom Settings page. In most cases, this should match the administration URL on the same page.

In Salesforce Setup, go to Security, and then to Remote Site Settings. Add a new remote site with your ServiceNow CPQ domain as the URL.

![Remote sites list](../images/cpq-salesforce-remote-site-settings.png)

**Important:** This API relies on **uniqueIdentifier** to match child lines. If you don't have unique **uniqueIdentifier** values for products, child lines may update incorrectly.

## API details

Endpoint: `/services/apexrest/LGK/cpq-quote-lines/reconfigure`

**Note:** Request endpoints and parameters are case sensitive.

Methods: Receives and returns `application/json`.

PATCH: The method currently only supports two fields, `configurationId` and `configurableQuoteLineId`.

Response: A quote \(`SBQQ__Q__c`\) record.

**Note:** The quote info returned will include info on all quote lines, not just the ones being added by the request. For example, if the configuration with three line items gets added to a quote that already had two lines on it, the quote info returned will included all five lines.

Request example:

```
{
	"configurationId":"86ec190e-cba8-4b1d-a2dc-ba47714a22b5",
	"configurableQuoteLineId":"a137d00000977oWAAQ"
}
```

Response example:

```
{
"attributes": {
"type": "SBQQ__Quote__c",
"url": "/services/data/v56.0/sobjects/SBQQ__Quote__c/a0zR0000003f3GLIAY"
},
"Name": "Q-00090",
"Id": "a0zR0000003f3GLIAY",
"SBQQ__LineItemCount__c": 4,
"SBQQ__LineItems__r": {
"totalSize": 4,
"done": true,
"records": [
{
"attributes": {
"type": "SBQQ__QuoteLine__c",
"url": "/services/data/v56.0/sobjects/SBQQ__QuoteLine__c/a0vR0000005LPRxIAO"
},
"SBQQ__Quote__c": "a0zR0000003f3GLIAY",
"Id": "a0vR0000005LPRxIAO",
"Name": "QL-0000122",
"SBQQ__ProductName__c": "LGK Machine"
},
{
"attributes": {
"type": "SBQQ__QuoteLine__c",
"url": "/services/data/v56.0/sobjects/SBQQ__QuoteLine__c/a0vR0000005LPRyIAO"
},
"SBQQ__Quote__c": "a0zR0000003f3GLIAY",
"Id": "a0vR0000005LPRyIAO",
"Name": "QL-0000123",
"SBQQ__ProductName__c": "Analytics Software"
},
{
"attributes": {
"type": "SBQQ__QuoteLine__c",
"url": "/services/data/v56.0/sobjects/SBQQ__QuoteLine__c/a0vR0000005LPS2IAO"
},
"SBQQ__Quote__c": "a0zR0000003f3GLIAY",
"Id": "a0vR0000005LPS2IAO",
"Name": "QL-0000124",
"SBQQ__ProductName__c": "Extended Warranty"
},
{
"attributes": {
"type": "SBQQ__QuoteLine__c",
"url": "/services/data/v56.0/sobjects/SBQQ__QuoteLine__c/a0vR0000005LPS3IAO"
},
"SBQQ__Quote__c": "a0zR0000003f3GLIAY",
"Id": "a0vR0000005LPS3IAO",
"Name": "QL-0000125",
"SBQQ__ProductName__c": "Scanner"
}
]
},
"SBQQ__Type__c": "Quote"
}
```

Requests can be made directly through Apex. The argument is a `Map<String,Object>` with the same fields used in the REST API. For example:

```
Map<String, Object> requestBody = new Map<String, Object>{
  'configurableQuoteLineId' => '01t8a000005hldvAAA',
  'configurationId' => '79a3ffdd-7dd0-41f6-8700-4bd7506407c7'    
};
String result = LGK.CpqReconfigureApiController.reconfigure(requestBody);
```

The response is a JSON formatted string representing the quote object, similar to the response in the REST APIs.

## Custom field mapping

If a field on the Quote Line object in Salesforce has a name that matches, custom values can be written from the `extended` or `pricing` information in a ServiceNow CPQ product.

