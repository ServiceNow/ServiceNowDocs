---
title: Runtime APIs
description: Runtime APIs
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Runtime APIs

Runtime APIs

CPQ provides a set of APIs for building front-end applications and manipulating configurations. These are commonly referred to as buyside or runtime APIs and are used by customers or end users to create, update and save CPQ configurations.

Runtime APIs support the standard create, read, update, and delete functions for CPQ configurations, along with the ability to retrieve bill of materials \(BOM\) data from CPQ.

**Note:** These APIs are legacy APIs. For the most updated information, see the complete CPQ API reference:

[Logik.io API Reference](https://api-docs.logik.io/#introduction)

To make CPQ runtime APIs accessible and provide a quick start to end developers, see our open source repositories for API collections that can easily be imported and used to start testing:

[API-Documentation/runtime/Logik Configurator Runtime APIs.postman\_collection.json](https://github.com/logikioopensource/API-Documentation/blob/main/runtime/Logik%20Configurator%20Runtime%20APIs.postman_collection.json)

## Runtime API setup

The base URL format for all runtime API calls is `https://<tenant>.<sector>.logik.io/api/`, where `<tenant>` is the listed tenant name and`<sector>` is the appropriate sector that the environment is located on \(usually `test` or `prod`\).

In Salesforce, you can find the CPQ tenant URL by going into Setup, searching for Custom Settings in the Quick Find box, and then clicking **Manage** next to CPQ Tenant.

Runtime API calls are authenticated through a combination of a bearer token and the defined origin in the runtime client. The origins of the runtime application are specified when a runtime client is created in the CPQ Admin settings.

To authorize these API calls, you must add two headers to the each runtime API request:

|Header|Key|Value|
|------|---|-----|
|Origin Header|origin|&lt;runtimeClientOrigin&gt;|
|Authorization Header|authorization|Bearer &lt;runtimeToken&gt;|

Sample headers:

-   origin: localhost
-   authorization: Bearer vEqzz4BVkb15Le11En8axEuN71FA6Vt\_cw

## Create a configuration

To start a new configuration via the APIs, the create configuration call passes the ID of the configurable product. In response, it receives a CPQ configuration ID that can be used to specify this configuration in later calls.

<table id="table_mtd_mls_mhc"><tbody><tr><td>

HTTP method

</td><td>

POST

</td></tr><tr><td>

URL

</td><td>

https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/

</td></tr><tr><td>

Path parameters

</td><td>

N/A

</td></tr><tr><td>

Query parameters

</td><td>

N/A

</td></tr></tbody>
</table>The two key pieces of the payload are:

-   The ID of a CPQ enabled product, with a blueprint that is deployed
-   The CPQ configuration UUID that is being reconfigured

Sample URL:

`https://dev1.test.Logik/api/`

Sample payload:

```
{
  "sessionContext": 
  { 
    "stateful": true
  },
  "partnerData": 
  { 
    "product":
    {
      "configuredProductId": "<Id of a Logik.io Enabled Product>", 
    }
  },
  "fields": []
}
```

**Note:** The configuration can also be initialized by passing field values to the fields array in the following format:

```
{
  “variableName”: “<Field Name>”, “value”: “<Field Value>”
}
```

Sample response:

```
{
  "fields": [<ARRAY OF FIELD OBJECTS>],
  "uuid": "08176434-9b1e-4fc8-b2c4-8aba2c35fda3", 
  "revision": 0,
  "relatedChanges": 
  [
    {
      "key": "products",
      "type": "PRODUCT"
    }
  ],
  "valid": true, 
  "messages": [], 
  "productChange": true,
  "products": [<ARRAY OF PRODUCTS IN CONFIGURATION>],
  "total": 30,
  "layouts": [<ARRAY OF LAYOUTS>]
}
```

## Reconfigure a configuration

The reconfigure API call is similar to the create configuration call. The reconfigure call passes the ID of the configurable product and an existing CPQ configuration ID, and in return receives a new Configuration ID with the same field data as the prior configuration but allowing for changes to be made.

**Note:** The UUID field in the response payload contains the new CPQ configuration ID. The new configuration ID should be used for all operations going forward in the reconfiguration process, including update, save, and retrieve BOM.

<table id="table_vtd_mls_mhc"><tbody><tr><td>

HTTP method

</td><td>

POST

</td></tr><tr><td>

URL

</td><td>

https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/

</td></tr><tr><td>

Path parameters

</td><td>

N/A

</td></tr><tr><td>

Query parameters

</td><td>

N/A

</td></tr></tbody>
</table>The two key pieces of the payload are:

-   The ID of a CPQ enabled product, with a blueprint that is deployed
-   The CPQ configuration UUID that is being reconfigured

Sample URL:

`https://dev1.test.Logik/api/`

Sample payload:

```
{
  "sessionContext": 
  { 
    "stateful": true
  },
  "partnerData": 
  { 
    "product": 
    {
      "configuredProductId": "<Id of a Logik.io Enabled Product>", 
      "configurationAttributes": 
      {
        "LGK__ConfigurationId__c": "<uuid>"
      }
    }
  },
  "fields": []
}
```

Sample response:

```
{
  "fields": [<ARRAY OF FIELD OBJECTS>],
  "uuid": "d98d60cd-9379-4b7b-86fd-de828c340f80", 
  "revision": 0,
  "relatedChanges": 
  [
    {
      "key": "products",
      "type": "PRODUCT"
    }
  ],
  "valid": true, 
  "messages": [], 
  "productChange": true,
  "products": [<ARRAY OF PRODUCTS IN CONFIGURATION>],
  "total": 30,
  "layouts": [<ARRAY OF LAYOUTS>]
}
```

## Update a configuration

Updating a configuration requires a configuration to be loaded using either the create configuration or reconfigure API calls. The Update Configuration call passes a CPQ Configuration ID and any desired field values, and in response receives the updated configuration from CPQ.

<table id="table_pwh_rts_mhc"><tbody><tr><td>

HTTP method

</td><td colspan="4">

PATCH

</td></tr><tr><td>

URL

</td><td colspan="4">

https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/

</td></tr><tr><td>

Path parameters

</td><td colspan="4">

N/A

</td></tr><tr><td rowspan="3">

Query Parameters

</td><td>

Name

</td><td>

Allowed Value

</td><td>

Required?

</td><td>

Default if not specified

</td></tr><tr><td>

delta

</td><td>

true \| false

</td><td>

optional

</td><td>

true

</td></tr><tr><td>

save

</td><td>

true \| false

</td><td>

optional

</td><td>

false

</td></tr></tbody>
</table>Query parameters:

**delta**

If delta=true, CPQ sends back only data that has changed based on the update that was sent. This is the default behavior.

If delta=false, CPQ sends back the entire configuration and BOM data in response.

**save**

If save=true, CPQ saves this configuration and \(depending on the settings\) performs additional actions such as sending the data to a webhook or writing the data into custom objects in Salesforce. This is the behavior of the save configuration call.

If save=false, CPQ updates this configuration and sends the updated data back in the response. This is the default behavior, and this is the behavior of the update call.

Sample URL:

`https://dev1.test.logik.io/api/fbc3d32c-7f86-4461-b144-986a0e8a5768`

Sample payload:

```
{
  "fields": 
  [
    {
      "variableName": "orderQty", 
      "value": 3
    }
  ]
}
```

Sample response:

```
{
  "fields": [],
  "uuid": "fbc3d32c-7f86-4461-b144-986a0e8a5768", 
  "revision": 0,
  "relatedChanges": 
  [
    {
      "key": "products",
      "type": "PRODUCT"
    }
  ],
  "valid": true, 
  "messages": [], 
  "productChange": true, 
  "products": null
}
```

## Save a configuration

Saving a configuration is a subset of the update configuration. It requires a configuration to be loaded using either the create configuration or reconfigure API calls. The save configuration call passes a CPQ configuration ID and any desired field values, and in response receives the updated configuration from CPQ.

**Note:** The only difference between a normal update call and a save call is the addition of the query parameter **save=true** in the URL. If set to false or excluded, this is a normal update call.

If you are using Salesforce as a backend, when the save API is called, CPQ asynchronously creates and populates the CPQ custom objects Configuration Field Data Sets and Configuration Line Items with the appropriate data.

If your CPQ instance has a webhook configured, when the save API is called, the data is sent to the endpoint specified in the webhook setting. See [Webhooks](cpq-webhooks.md).

**Note:** This ends the configuration session. Further edits or updates to the configuration must be started from the create configuration or reconfigure API calls.

<table id="table_mrm_2ss_mhc"><tbody><tr><td>

HTTP method

</td><td colspan="4">

PATCH

</td></tr><tr><td>

URL

</td><td colspan="4">

https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/

</td></tr><tr><td>

Path parameters

</td><td colspan="4">

N/A

</td></tr><tr><td rowspan="3">

Query Parameters

</td><td>

Name

</td><td>

Allowed Value

</td><td>

Required?

</td><td>

Default if not specified

</td></tr><tr><td>

delta

</td><td>

true \| false

</td><td>

optional

</td><td>

true

</td></tr><tr><td>

save

</td><td>

true \| false

</td><td>

optional

</td><td>

false

</td></tr></tbody>
</table>Query parameters:

**delta**

If delta=true, CPQ sends back only data that has changed based on the update that was sent. This is the default behavior.

If delta=false, CPQ sends back the entire configuration and BOM data in response.

**save**

If save=true, CPQ saves this configuration and \(depending on the settings\) performs additional actions such as sending the data to a webhook or writing the data into custom objects in Salesforce.

If save=false, CPQ updates this configuration and sends the updated data back in the response. This is the behavior of the update call.

Sample cURL request:

```
curl --location --request PATCH 'https://mpanigrahi-demo.demo01.logik.io/api/6d0ef6fd-4c88-44f3-a296-b03421c369c6' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--header 'Origin: https://mpanigrahi-demo.demo01.logik.io' \
--header 'Authorization: <<RUNTIME TOKEN>>' \
--header 'Cookie: LGKSESSION=NDA5OWJmNmEtNDhhOS00YTc4LTk3ODktZTg0OGYyOGIwMjZk' \
--data '{"fields":[{"variableName":"name_d1","value":"megha","dataType":"text"}],"responseState":{"setPagination":{"collections":{"pageSize":10,"pageNumber":0},"fields":{"pageSize":10,"pageNumber":0},"componentTypes":{"pageSize":10,"pageNumber":0}},"defaultPagination":{"pageSize":10,"pageNumber":0},"searchValues":{}}}'
```

Sample response:

```
{
"fields": [<ARRAY OF FIELD OBJECTS>],
"uuid": "8817655d-7a11-41ef-a9fd-59c2855a3e4b", 
"revision": 1,
"valid": true, 
"messages": [], 
"productChange": false,
"products": [<ARRAY OF PRODUCTS IN CONFIGURATION>],
"total": 0
}
```

## BOM APIs

The BOM APIs are useful for retrieving the final output of configuration. The BOM APIs can be used to retrieve the entire BOM, or specific subsets, such as sales or manufacturing BOMs.

The Get BOM call passes a CPQ Configuration ID and in return receives the current BOM generated by the current state of the configuration. There are 3 built in BOM types: “all”, “sales” and “manufacturing”. Additional BOM types can be dynamically added by setting the bomType field on the product.

**Note:** If the BOM type is not included, the API returns the entire BOM.

<table id="table_dvd_mls_mhc"><tbody><tr><td>

HTTP method

</td><td colspan="3">

GET

</td></tr><tr><td>

URL

</td><td colspan="3">

https://&lt;tenant&gt;.&lt;sector&gt;.logik.io/api/&lt;uuid&gt;/bom/&lt;bomType&gt;

</td></tr><tr><td rowspan="3">

Path Parameters

</td><td>

Name

</td><td>

Allowed Value

</td><td>

Required?

</td></tr><tr><td>

&lt;uuid&gt;

</td><td>

32 character CPQ configuration UUID

</td><td>

required

</td></tr><tr><td>

&lt;bomType&gt;

</td><td>

name of the BOM to retrieve

</td><td>

optional

</td></tr><tr><td>

Query parameters

</td><td colspan="3">

N/A

</td></tr></tbody>
</table>Sample response:

```
{"products": [
        {
            "id": "01t5f000006QKysAAG",
            "quantity": 1,
            "bomType": "Sales",
            "orderNumber": 10,
            "type": "accessory",
            "name": "Amend Flow Bundle Sub",
            "partnerId": "01t5f000006QKysAAG",
            "productCode": "AFBC-SC",
            "externalId": "",
            "productFamily": "Miscellaneous",
            "description": "",
            "uom": "",
            "price": 5,
            "extPrice": 5,
            "level": 0,
            "rollUpPrice": 5
        },
        {
            "id": "01t5f000006QKz2AAG",
            "quantity": 1,
            "bomType": "Sales",
            "orderNumber": 20,
            "type": "accessory",
            "name": "Amend Flow Bundle Asset",
            "partnerId": "01t5f000006QKz2AAG",
            "productCode": "AFBC2-SC",
            "externalId": "",
            "productFamily": "Miscellaneous",
            "description": "",
            "uom": "",
            "price": 25,
            "extPrice": 25,
            "level": 0,
            "rollUpPrice": 25
        }
    ]}
```

For information about additional configuration APIs and sample scenarios, see [Additional configuration APIs](logik_io_additional_configuration_apis.md).

