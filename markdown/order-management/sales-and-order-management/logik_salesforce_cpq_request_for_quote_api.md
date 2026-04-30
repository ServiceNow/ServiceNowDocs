---
title: The RFQ \(Request for Quote\) API
description: ServiceNow CPQ adds additional functionality to the Salesforce CPQ package APIs. This functionality lets you add products and data to an existing Salesforce CPQ quote.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 6
breadcrumb: [API overview and resources, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The RFQ \(Request for Quote\) API

ServiceNow CPQ adds additional functionality to the Salesforce CPQ package APIs. This functionality lets you add products and data to an existing Salesforce CPQ quote.

As part of the ServiceNow CPQ integration package with Salesforce CPQ, ServiceNow CPQ provides an API to add a ServiceNow CPQ configured product, sales BOM products and BOM data to a new or existing Salesforce CPQ quote \(`SBQQ__Quote__c`\). This provides ServiceNow CPQ functionality in addition to the Salesforce CPQ package APIs.

[Salesforce CPQ package APIs](https://developer.salesforce.com/docs/atlas.en-us.cpq_dev_api.meta/cpq_dev_api/cpq_api_get_started.htm)

View a video about the Request for Quote API:

[https://youtu.be/e0nxEITIzq8](https://youtu.be/e0nxEITIzq8)

## URL and endpoint

Two HTTP methods are exposed for the endpoint:

-   POST for creating a new quote and adding a product and configuration
-   PATCH for adding a new product and configuration to an existing quote

This API is exposed as an Apex Rest Service in the Salesforce org with a path of `/services/apexrest/LGK/request-quote`: for example, `https://<yourInstance>.salesforce.com/services/apexrest/LGK/request-quote`, where `<yourInstance>` is the personal domain of your Salesforce org.

## Setup and authorization

This API is exposed in the Salesforce org and requires authorization with Salesforce to be accessed and called. See [Salesforce Help on Authorization options for making API calls](https://help.salesforce.com/s/articleView?id=sf.remoteaccess_oauth_flows.htm&type=5). This API can also be tested using the [Salesforce Workbench Application](https://workbench.developerforce.com/).

In ServiceNow CPQ, the only step is to ensure that in Admin settings, **Push BOM Data to Logik Salesforce Object** is enabled. ServiceNow CPQ uses the data stored in the Configuration Line Items \(LGK\_\_ConfigurationLineItem\_\_c\) to create any additional sales BOM lines on the quote and write the BOM Data field on the quote line.

**Note:** The API will also respect normal Salesforce user access levels, so if the authenticated Salesforce user \(or a partner site itself, via sharing settings\) does not have certain object or field level access, the API call may fail or not behave as expected. The user calling the API needs access to the standard Salesforce CPQ and related objects as well as the ServiceNow CPQ Configuration Line Item object and its fields.

A short list of necessary objects includes:

-   Pricebook
-   Product feature \(for the “Dynamic” feature on the product\)
-   Quote
-   Product
-   Quote line
-   Config Line Item

If there is an issue with the API, make sure the user not only has access to the object or fields, but also to the specific record. This is always true, but because partner profiles start off with less access to records, they are more susceptible to the problem.

To use these APIs, create and save a ServiceNow CPQ configuration, making note of the configuration ID that will be used for the calls. Also copy the product ID of the configurable product that was used to create the configuration demo.

## Create new quote and add product

The create quote and add product API call can be very useful if ServiceNow CPQ is being used outside the traditional Salesforce CPQ context. This can enable an omni channel experience without exposing end users to the Salesforce CPQ Quote Line Editor.

<table><tbody><tr><td>

HTTP method

</td><td>

POST

</td></tr><tr><td>

URL

</td><td>

https://&lt;yourInstance&gt;.salesforce.com/services/apexrest/LGK/request-quote

</td></tr><tr><td>

Path parameters

</td><td>

N/A

</td></tr><tr><td>

Query parameters

</td><td>

N/A

</td></tr></tbody>
</table>The required parameters in the request body are:

-   **configurableProductId**

    The ServiceNow CPQ enabled configurable product ID

-   **configurationId**

    The ServiceNow CPQ configuration UUID received after saving a configuration

-   **pricebookId**

    The Salesforce ID of the Pricebook2 record that has a valid pricebook entry for the product


-   **** –
-   **** –
-   **** –

If included, **accountId** and **opportunityId** are populated on the newly created quote.

Sample URL: `https://demoloik.my.salesforce.com/services/apexrest/LGK/request-quote`

Sample request payload:

```
{
  "configurableProductId": "01t5f000003w24zAAA",
  "configurationId": "eeec456c-a4f6-407a-94b1-03e8b6cf29ea",
  "pricebookId": "01s5f000000AsLDAA0" }
```

Sample response:

```
{
  "attributes" : {
    "type" : "SBQQ__Quote__c",
    "url" : "/services/data/v57.0/sobjects/SBQQ__Quote__c/a0q5f0000057YAYAA2"
  },
  "Name" : "Q-00162",
  "Id" : "a0q5f0000057YAYAA2",
  "SBQQ__LineItemCount__c" : 3,
  "SBQQ__LineItems__r" : {
    "totalSize" : 3,
    "done" : true,
    "records" : [ {
      "attributes" : {
        "type" : "SBQQ__QuoteLine__c",
        "url" : "/services/data/v57.0/sobjects/SBQQ__QuoteLine__c/a0m5f000007ZYr6AAG"
      },
      "SBQQ__Quote__c" : "a0q5f0000057YAYAA2",
      "Id" : "a0m5f000007ZYr6AAG",
      "Name" : "QL-0001001",
      "SBQQ__ProductName__c" : "AFB"
    }, {
      "attributes" : {
        "type" : "SBQQ__QuoteLine__c",
        "url" : "/services/data/v57.0/sobjects/SBQQ__QuoteLine__c/a0m5f000007ZYr7AAG"
      },
      "SBQQ__Quote__c" : "a0q5f0000057YAYAA2",
      "Id" : "a0m5f000007ZYr7AAG",
      "Name" : "QL-0001002",
      "SBQQ__ProductName__c" : "Simple Amend Child Subscription"
    }, {
      "attributes" : {
        "type" : "SBQQ__QuoteLine__c",
        "url" : "/services/data/v57.0/sobjects/SBQQ__QuoteLine__c/a0m5f000007ZYr8AAG"
      },
      "SBQQ__Quote__c" : "a0q5f0000057YAYAA2",
      "Id" : "a0m5f000007ZYr8AAG",
      "Name" : "QL-0001003",
      "SBQQ__ProductName__c" : "Simple Amend Child Asset"
    } ]
  },
  "SBQQ__Type__c" : "Quote"
}
```

## Add product to quote

The Add Product to Quote API can be used when additional configurations are added to a single quote, either generated through the normal CPQ flow, through manual record creation, or through one that has already been created using the Create New Quote API above.

<table><tbody><tr><td>

HTTP method

</td><td>

PATCH

</td></tr><tr><td>

URL

</td><td>

https://&lt;yourInstance&gt;.salesforce.com/services/apexrest/LGK/request-quote

</td></tr><tr><td>

Path parameters

</td><td>

N/A

</td></tr><tr><td>

Query parameters

</td><td>

N/A

</td></tr></tbody>
</table>The required parameters in the request body are:

-   **configurableProductId**

    the ServiceNow CPQ enabled configurable product ID

-   **configurationId**

    The ServiceNow CPQ configuration UUID received after saving a configuration

-   **quoteId**

    The Salesforce ID of the SBQQ\_\_Quote\_\_c record to add this configuration to


If included, **quoteLineGroupId** adds the newly created quote line to the specified quote line group.

Sample URL: `https://demologik.my.salesforce.com/services/apexrest/LGK/request-quote`

Sample request body:

```
{
    "configurableProductId": "01t5f000002SwERAA0",
    "configurationId": "8978145d-35ba-4633-8139-e305ea4b9874",
    "quoteId": "a0q5f0000057YATAA2",
}
```

Sample response body:

```
{
    "attributes": {
        "type": "SBQQ__Quote__c",
        "url": "/services/data/v57.0/sobjects/SBQQ__Quote__c/a0q5f000005MNDhAAO"
    },
    "Name": "Q-00286",
    "Id": "a0q5f000005MNDhAAO",
    "SBQQ__LineItemCount__c": 1,
    "SBQQ__LineItems__r": {
        "totalSize": 1,
        "done": true,
        "records": [
            {
                "attributes": {
                    "type": "SBQQ__QuoteLine__c",
                    "url": "/services/data/v57.0/sobjects/SBQQ__QuoteLine__c/a0m5f00000AhsZsAAJ"
                },
                "SBQQ__Quote__c": "a0q5f000005MNDhAAO",
                "Id": "a0m5f00000AhsZsAAJ",
                "Name": "QL-0003664",
                "SBQQ__ProductName__c": "Cloud Workload Configurator"
            }
        ]
    },
    "SBQQ__Type__c": "Quote"
}
```

[Logik Salesforce CPQ Extension APIs Postman Collection](https://drive.google.com/file/d/1Slr7O1QIzfpAat-16x-vkuGeshzLv3Kw/view?usp=share_link):

```
{
	"info": {
		"_postman_id": "2562674d-051d-4663-b3ed-482e6be1b78f",
		"name": "Logik Salesforce CPQ Extension APIs",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json""
	},
	"item": [
		{
			"name": "Salesforce Authentication",
			"item": [
				{
					"name": "Salesforce Authentication",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"var jsonData = pm.response.json();",
									"pm.collectionVariables.set(\"salesforce_access_token\", jsonData.access_token);"
								],
								"type": "text/javascript"
							}
						}
					],
					"request": {
						"method": "POST",
						"header": [],
						"body": {
							"mode": "formdata",
							"formdata": []
						},
						"url": {
							"raw": "{{salesforce_domain}}/services/oauth2/token?username={{salesforce_username}}&password={{salesforce_password}}&grant_type=password&client_id={{salesforce_client_id}}&client_secret={{salesforce_client_secret}}",
							"host": [
								"{{salesforce_domain}}"
							],
							"path": [
								"services",
								"oauth2",
								"token"
							],
							"query": [
								{
									"key": "username",
									"value": "{{salesforce_username}}"
								},
								{
									"key": "password",
									"value": "{{salesforce_password}}"
								},
								{
									"key": "grant_type",
									"value": "password"
								},
								{
									"key": "client_id",
									"value": "{{salesforce_client_id}}"
								},
								{
									"key": "client_secret",
									"value": "{{salesforce_client_secret}}"
								}
							]
						}
					},
					"response": []
				}
			]
		},
		{
			"name": "Logik CPQ Extension APIs",
			"item": [
				{
					"name": "Create New Quote",
					"request": {
						"method": "POST",
						"header": [
							{
								"key": "Content-Type",
								"value": "application/json",
								"type": "default"
							}
						],
						"body": {
							"mode": "raw",
							"raw": "{\n    \"configurableProductId\": \"{{configurableProductId}}\",\n    \"configurationId\": \"{{configurationId}}\",\n    \"pricebookId\": \"{{pricebookId}}\",\n    \"accountId\": \"{{accountId}}\",\n    \"opportunityId\": \"{{opportunityId}}\"\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "{{salesforce_domain}}/services/apexrest/LGK/request-quote",
							"host": [
								"{{salesforce_domain}}"
							],
							"path": [
								"services",
								"apexrest",
								"LGK",
								"request-quote"
							]
						}
					},
					"response": []
				},
				{
					"name": "Add to Existing Quote",
					"request": {
						"method": "PATCH",
						"header": [
							{
								"key": "Content-Type",
								"value": "application/json",
								"type": "default"
							}
						],
						"body": {
							"mode": "raw",
							"raw": "{\n    \"configurableProductId\": \"{{configurableProductId}}\",\n    \"configurationId\": \"{{configurationId}}\",\n    \"quoteId\": \"{{quoteId}}\",\n    \"quoteLineGroupId\": \"{{quoteLineGroupId}}\"\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "{{salesforce_domain}}/services/apexrest/LGK/request-quote",
							"host": [
								"{{salesforce_domain}}"
							],
							"path": [
								"services",
								"apexrest",
								"LGK",
								"request-quote"
							]
						}
					},
					"response": []
				}
			],
			"auth": {
				"type": "bearer",
				"bearer": [
					{
						"key": "token",
						"value": "{{salesforce_access_token}}",
						"type": "string"
					}
				]
			},
			"event": [
				{
					"listen": "prerequest",
					"script": {
						"type": "text/javascript",
						"exec": [
							"let sfToken = pm.collectionVariables.get('salesforce_access_token');",
							"if(sfToken == null) {",
							"    console.error('Run Salesforce Authentication first')",
							"}"
						]
					}
				},
				{
					"listen": "test",
					"script": {
						"type": "text/javascript",
						"exec": [
							""
						]
					}
				}
			]
		}
	],
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		}
	],
	"variable": [
		{
			"key": "salesforce_domain",
			"value": "https://demologik6.my.salesforce.com"",
			"type": "default"
		},
		{
			"key": "salesforce_username",
			"value": "",
			"type": "default"
		},
		{
			"key": "salesforce_password",
			"value": "",
			"type": "default"
		},
		{
			"key": "salesforce_client_id",
			"value": "",
			"type": "default"
		},
		{
			"key": "salesforce_client_secret",
			"value": "",
			"type": "default"
		},
		{
			"key": "salesforce_access_token",
			"value": ""
		},
		{
			"key": "configurableProductId",
			"value": "",
			"type": "default"
		},
		{
			"key": "configurationId",
			"value": "",
			"type": "default"
		},
		{
			"key": "pricebookId",
			"value": "",
			"type": "default"
		},
		{
			"key": "accountId",
			"value": "",
			"type": "default"
		},
		{
			"key": "opportunityId",
			"value": "",
			"type": "default"
		},
		{
			"key": "quoteId",
			"value": "",
			"type": "default"
		},
		{
			"key": "quoteLineGroupId",
			"value": "",
			"type": "default"
		}
	]
}
```

