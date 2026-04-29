---
title: Intro to runtime API calls
description: Runtime, or buyside, APIs are used to create, update, and save configurations.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Intro to runtime API calls

Runtime, or buyside, APIs are used to create, update, and save configurations.

CPQ APIs are divided into two categories: runtime APIs and admin APIs. In this article, we introduce the runtime APIs.

Runtime APIs are used to create, read, update, and delete configurations, and are the same APIs that are used in the CPQ End User Configurator. They are also commonly referred to as the “buyside“ APIs.

**Note:** For the most updated information on sample codes and other details, see [API Documentation](https://api-docs.logik.io/#introduction).

All API calls follow this base URL format: `https://<yourTenant>.<sector>.logik.io/api/`. In this URL, yourTenant represents your unique listed CPQ tenant name, and sector is the sector where your CPQ environment is located.

If you are a Salesforce user, you can find your tenant URL by clicking **Setup** in your Salesforce account. In the Quick Find box, search for or click **Custom Settings**, and then click **Manage**. Your tenant URL will be displayed.

![Runtime API Calls](../images/cpq-apis-runtime-configuration-url.png)

All runtime API calls require bearer token authentication using a unique token that is available in the runtime client. They also require that the origin URL configured in the runtime client appears in the request header.

To authenticate, collect the bearer token and the origin URL from CPQ Admin → Utilities → Runtime Client. For each API call in a Postman, add the following header:

```
Key: Origin
Value: <yourOrigin>
```

![Runtime API Calls](../images/cpq-apis-runtime-origin.png)

In the Authorization tab of Postman or your API tool, select **Bearer Token**, and then input the unique token you copied from CPQ Admin.

![Runtime API Calls](../images/cpq-apis-runtime-bearer-token.png)

**Note:** The token in the image is a dummy value that does not correspond to any actual environment. It appears only for illustrative purposes.

## Basic runtime API calls

-   The initial configure call starts the configuration process by passing the ID of the configurable product, and returns a configuration UUID for later use.

    Example \(cURL\):

    ```
    curl -X POST https://<yourTenant>.<sector>.logik.io/api/ \
    -H "Authorization: Bearer <yourBearerToken>" \
    -H "Origin: <yourOrigin>" \
    -H "Content-Type: application/json" \
    -d '{
        "sessionContext": {
            "stateful": true
        },
        "partnerData": {
            "product": {
                "configuredProductId": "{{configProductId}}",
            }
        },
        "fields": []
    }'
    ```

    Example \(response\):

    ```
    {
      "configurationId": "{uuid}"
    ```

    You also use this API call for reconfiguring, providing a previously saved configuration UUID in the POST body.

    Example reconfigure \(cURL\):

    ```
    curl -X POST https://<yourTenant>.<sector>.logik.io/api/ \
    -H "Authorization: Bearer <yourBearerToken>" \
    -H "Origin: <yourOrigin>" \
    -H "Content-Type: application/json" \
    -d '{
        "sessionContext": {
            "stateful": true
        },
        "partnerData": {
            "product": {
                "configuredProductId": "{{configProductId}}",
                "configurationAttributes": {
                    "LGK__ConfigurationId__c": "{{uuid}}"
                }
            }
        },
        "fields": []
    }'
    ```

-   The update configuration call updates an existing configuration by passing the configuration UUID and desired field values, and returns all possible fields and their values.

    Example \(cURL\):

    ```
    curl -X PATCH https://<yourTenant>.<sector>.logik.io/api/{uuid} \
    -H "Authorization: Bearer <yourBearerToken>" \
    -H "Origin: <yourOrigin>" \
    -H "Content-Type: application/json" \
    -d '{ "fields": { "color": "blue", "size": "large" } }'
    ```

    Example \(response\):

    ```
    {
      "fields": {
        "color": "blue",
        "size": "large",
        "price": "$100"
      }
    }
    ```

-   The get BOM call passes the configuration UUID and retrieves the Bill of Materials \(BOM\) for the configuration. It returns the current BOM for the configuration.

    Example \(cURL\):

    ```
    curl -X GET https://<yourTenant>.<sector>.logik.io/api/{uuid}/bom \
    -H "Authorization: Bearer <yourBearerToken>" \
    -H "Origin: <yourOrigin>"
    ```

    Example \(response\):

    ```
    {
      "bom": [
        { "item": "componentA", "quantity": 2 },
        { "item": "componentB", "quantity": 1 }
      ]
    }
    ```

-   The save call saves the configuration in CPQ. This ensures that the configuration UUID can be used and reconfigured in the future.

    This process asynchronously populates our custom objects, configuration field data sets, and configuration line items in Salesforce.

    Example \(cURL\):

    ```
    curl --location --request PATCH 'https://mpanigrahi-demo.demo01.logik.io/api/6d0ef6fd-4c88-44f3-a296-b03421c369c6' \
    --header 'Content-Type: application/json' \
    --header 'Accept: application/json' \
    --header 'Origin: https://mpanigrahi-demo.demo01.logik.io' \
    --header 'Authorization: <<RUNTIME TOKEN>>' \
    --header 'Cookie: LGKSESSION=NDA5OWJmNmEtNDhhOS00YTc4LTk3ODktZTg0OGYyOGIwMjZk' \
    --data '{"fields":[{"variableName":"name_d1","value":"megha","dataType":"text"}],"responseState":{"setPagination":{"collections":{"pageSize":10,"pageNumber":0},"fields":{"pageSize":10,"pageNumber":0},"componentTypes":{"pageSize":10,"pageNumber":0}},"defaultPagination":{"pageSize":10,"pageNumber":0},"searchValues":{}}}'
    ```

    For more details on the sample code, refer to the full API reference documentation:

    [https://api-docs.logik.io/\#introduction](https://api-docs.logik.io/#introduction)


## JSON sample

```
info:
_postman_id: e8370e58-ff12-4662-adac-3e35052b59ba name: Sample Runtime Calls
schema: https://schema.getpostman.com/json/collection/v2.1.0/collection.json item:
name: 'Logik: Initial Configure' event:
listen: test script:
exec:
"var jsonData = JSON.parse(responseBody);\r"
pm.collectionVariables.set("configId", jsonData.uuid); type: text/javascript
request: auth:
type: bearer bearer:
- key: token
value: '{{logikAccessToken}}' type: string
method: POST header:
key: content-type value: application/json type: text
key: Origin
value: '{{logikOriginHeader}}' type: text
body:
mode: raw
raw: "	{\r\n	\"sessionContext\": {\r\n	\"stateful\": true\r\n	},\r\n	\"partnerData\": {\r\n	\"product options:
raw:
language: json
url:
raw: '{{logik}}' host:
- '{{logik}}' response: []
name: 'Logik: Update Configuration' request:
auth:
type: bearer bearer:
key: token
value: '{{logikAccessToken}}' type: string
method: PATCH header:
key: content-type value: application/json type: text
key: Origin
value: '{{logikOriginHeader}}' type: text
body:
mode: raw
raw: "{\r\n	\"fields\": [\r\n	{\"variableName\":\"juBool1\",\"value\":\"True\"},\r\n	{\"variableName\":\"juBool2\",\"value options:
raw:
language: json
url:
raw: '{{logik}}{{configId}}' host:
- '{{logik}}{{configId}}' response: []
name: '(Optional): Logik: Retrieve BOM' request:
auth:
type: bearer bearer:
key: token
value: '{{logikAccessToken}}' type: string
method: GET header:
key: content-type value: application/json type: text
key: Origin
value: '{{logikOriginHeader}}' type: text
url:
raw: '{{logik}}{{configId}}/bom' host:
'{{logik}}{{configId}}' path:
bom response: []
name: 'Logik: Save' event:
listen: test script:
exec:
"var jsonData = JSON.parse(responseBody);\r"
"pm.collectionVariables.set(\"logikTotal\", jsonData.total);\r"
pm.collectionVariables.set("logikLineItems", jsonData.products); type: text/javascript
request: auth:
type: bearer bearer:
- key: token
value: '{{logikAccessToken}}' type: string
method: PATCH header:
key: content-type value: application/json type: text
key: Origin
value: '{{logikOriginHeader}}' type: text
body:
mode: raw
raw: "{\r\n	\"fields\": []\r\n}" options:
raw:
language: json
url:
raw: '{{logik}}{{configId}}?save=true' host:
'{{logik}}{{configId}}' query:
key: save value: 'true'
response: []
name: '(Optional): Logik: Reconfigure' event:
listen: test script:
exec:
"var jsonData = JSON.parse(responseBody);\r"
pm.collectionVariables.set("configId", jsonData.uuid); type: text/javascript
request: auth:
type: bearer bearer:
- key: token
value: '{{logikAccessToken}}' type: string
method: POST header:
key: Origin
value: '{{logikOriginHeader}}' type: default
key: Authorization
value: Bearer Armqrz8jv-1C05mcWmcrDnXZlV9bbOTmGg type: default
disabled: true body:
mode: raw
raw: "{\r\n \"sessionContext\": {\r\n	\"stateful\": true\r\n },\r\n \"partnerData\": {\r\n	\"product\": {\r\n	\"configuredProductId\" options:
raw:
language: json
url:
raw: '{{logik}}' host:
- '{{logik}}' response: []
```

For more information about CPQ APIs, see the following eight-slide presentation:

[Logik.io APIs](https://docs.google.com/presentation/d/1dN5rfpk4jjS__GkBcarieNUEfyVY6bAvrhxkkm9DagI/edit?slide=id.g18313200e09_0_207#slide=id.g18313200e09_0_207).

