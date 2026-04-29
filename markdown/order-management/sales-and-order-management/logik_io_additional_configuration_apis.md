---
title: Additional configuration APIs
description: These CPQ configuration APIs let you retrieve or delete an existing configuration. They complement the runtime APIs and are useful for viewing full configuration details and for removing configurations no longer needed. Use them alongside the standard create, update, reconfigure, and BOM APIs to support end-to-end configuration workflows.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Additional configuration APIs

These CPQ configuration APIs let you retrieve or delete an existing configuration. They complement the runtime APIs and are useful for viewing full configuration details and for removing configurations no longer needed. Use them alongside the standard create, update, reconfigure, and BOM APIs to support end-to-end configuration workflows.

This article is a followup to [Runtime APIs](logik_io_runtime_apis.md). For more information on authentication and setup,see that article.

These API endpoints to get a configuration and delete a configuration from CPQ are included for completeness.

## Get configuration

CPQ configurations can be retrieved from the CPQ servers by sending a GET request, which will return the entire configuration in the response. If you only need the product data of the outputs, consider using one of the GET BOM API calls.

**Note:** This does not load a configuration into the CPQ rules engine for updates to fields and re-running of rules. If you need to make updates to an existing configuration, use the Reconfigure API call.

|HTTP method|GET|
|-----------|---|
|URL|https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/&lt;uuid&gt;|
|Path parameters|&lt;uuid&gt;|32 character CPQ configuration UUID|required|
|Query parameters|N/A|

Sample URL:

[https://dev1.test.logik.io/api/71e62fe7-e59b-4a91-94af-64718e0d4eae](https://dev1.test.logik.io/api/71e62fe7-e59b-4a91-94af-64718e0d4eae)

Sample response:

```
{
"fields": [<ARRAY OF FIELD OBJECTS>],
"uuid": "08176434-9b1e-4fc8-b2c4-8aba2c35fda3", "revision": 0,
"relatedChanges": [
{
"key": "products",
"type": "PRODUCT"
}
],
"valid": true, "messages": [], "productChange": true,
"products": [<ARRAY OF PRODUCTS IN CONFIGURATION>],
"total": 30,
"layouts": [<ARRAY OF LAYOUTS>]
}

```

## Delete configuration

CPQ configurations can be deleted, but it is not typically necessary. This API deletes the configuration from CPQ and will not be available for future retrieval of the configuration, BOM, or updates to the configuration.

**Note:** This API will only delete the configuration from the CPQ servers. If the configuration has been persisted in another application \(i.e. Quotelines have been created in Salesforce, Orders have been placed in Ecommerce\), no changes will be made to that data.

|HTTP method|DELETE|
|-----------|------|
|URL|https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/&lt;uuid&gt;|
|Path parameters|&lt;uuid&gt;|32 character CPQ configuration UUID|required|
|Query parameters|N/A|

Sample URL:

https://dev1.test.logik.io/api/71e62fe7-e59b-4a91-94af-64718e0d4eae

Sample response:

```
{}
```

## Sample use cases

A new customer comes to a website, configures a product, and checks out.

1.  Start a new configuration → Create New Configuration API call
2.  Make updates to the configuration → Update Configuration API call
3.  Save the final configuration back to CPQ → Save Configuration API call

A customer returns and wants to place an order for a product similar to one that they have purchased before.

1.  Perform a reconfiguration, using an existing CPQ Configuration Id → Reconfigure API Call
2.  Save back to CPQ → Save Configuration API call

An order for a complex manufactured product is placed, and the engineering team needs to know what parts they need and which sub-assemblies to build.

Retrieve the “Manufacturing” bill of materials for an existing configuration → Get BOM API call.

