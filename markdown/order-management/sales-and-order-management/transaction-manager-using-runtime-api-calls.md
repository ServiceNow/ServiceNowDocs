---
title: Transaction Manager: Using Runtime API calls
description: See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/transaction-manager-using-runtime-api-calls.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 6
breadcrumb: [Transaction Manager, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Transaction Manager: Using Runtime API calls

See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.

CPQ APIs are divided into two categories: runtime APIs and admin APIs. This article lists the runtime APIs for Transaction Manager.

The runtime APIs are the same APIs that are used in the runtime end user experience and include the following key actions.

-   Initialize a session
    -   Purpose: Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction. If a transaction is not specified, a new transaction is created.
    -   Response: Returns a session ID, a transaction ID, and transaction information.
-   Delete a session
    -   Purpose: Deletes a session to securely end user activity, clear session-specific data, and free up system resources.
    -   Response: The session is deleted. No information is returned.
-   Create a transaction
    -   Purpose: Creates a transaction, providing the object to manage the transaction life cycle, configure and add products, and determine pricing.
    -   Response: Returns a transaction ID and transaction information.
-   Run events on a transaction \(system and custom\)
    -   Purpose: Triggers a specified event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, and validating configurations.
    -   Response: Varies by event.
-   Add products to a transactions \(upsert\)
    -   Purpose: Adds a product or products to a transaction, enabling dynamic configuration and pricing updates based on the product’s attributes.
    -   Response: Returns updated transaction data with the additional product.
-   Get a list of transactions
    -   Purpose: Retrieves a list of transactions, enabling users to view, manage, or take action on existing transactions.
    -   Response: A list of transactions with transaction IDs and other metadata.
-   Get details of a transaction
    -   Purpose: Retrieves the header information of a transaction, providing key details such as stage, account, and the summary-level data needed for display or processing.
    -   Response: All header field data for the transaction.
-   Get a transaction's lines
    -   Purpose: Retrieves the line item details for a transaction, returning product-level data such as quantities, pricing, and custom attributes for each item in the quote.
    -   Response: All line-level field data for the transaction.

## Additional non-runtime APIs

For details about the API that retrieves metrics for transactions, see [Transaction Manager: Transaction metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/cpq-transaction-manager-metrics-api.md).

## Postman collection

```
{
	"info": {
		"_postman_id": "0112bd72-984c-4285-a40f-5724e5d799cb",
		"name": "1 - Transaction Manager Headless Runtime APIs",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "40935282"
	},
	"item": [
		{
			"name": "Initialize a session",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					},
					{
						"key": "Origin",
						"value": "",
						"type": "text",
						"disabled": true
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{   \"id\": \"{{transactionId}}\",\n    //\"txnId\": \"{{transactionId}}\",\n    \"stateful\": false\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t"
					]
				}
			},
			"response": []
		},
		{
			"name": "Create a new transaction",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					},
					{
						"key": "",
						"value": "",
						"type": "text",
						"disabled": true
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{ \n    \"stateful\": false\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t"
					]
				}
			},
			"response": []
		},
		{
			"name": "Run an event (using existing session)",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"context\": {\n        \"session\": \"{{session}}\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t/{{transactionId}}/events/test_event_transitions",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{transactionId}}",
						"events",
						"test_event_transitions"
					]
				}
			},
			"response": []
		},
		{
			"name": "Run an event (needs session) with field updates",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"context\": {\n        \"session\": \"{{session}}\"\n    },\n    \"fields\": [{\n        \"variableName\": \"txn.custom.quoteName\",\n        \"value\": \"essd\",\n        \"dataType\": \"text\"\n    }],\n    \"lines\": [\n        {\n            \"uuid\": \"75b7c4f6-3de7-4d5c-8a0c-8b7f0eebec65\",\n            \"fields\": [{\n                \"variableName\": \"txn.line.custom.bomType\",\n                \"value\": \"Hardware\",\n                \"dataType\": \"text\"\n            }]\n        }\n    ]\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t/{{transactionId}}/events/save",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{transactionId}}",
						"events",
						"save"
					]
				}
			},
			"response": []
		},
		{
			"name": "Run an event w/o specified session",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"context\" : {\n        \"stateful\": false\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t/{{transactionId}}/events/save",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{transactionId}}",
						"events",
						"save"
					]
				}
			},
			"response": []
		},
		{
			"name": "Copy transaction",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"context\": {\n        \"stateful\": false\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t/{{transactionId}}/events/copyTransaction",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{transactionId}}",
						"events",
						"copyTransaction"
					]
				}
			},
			"response": []
		},
		{
			"name": "Upsert",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Content-Type",
						"value": "application/json"
					},
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"context\": {\n        \"stateful\": false\n    },\n    \"items\": [\n        {\n            \"configurationId\": \"626923a6-2bab-4755-90ae-60d40bbb55c4\"\n        },\n        {\n            \"id\": \"SimpleProductId\" //for non-configured products only\n        }\n    ]\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{baseUrl}}/api/t/{{transactionId}}/events/upsertLines",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{transactionId}}",
						"events",
						"upsertLines"
					]
				},
				"description": "Generated from cURL: curl 'https://dev3.dev.logik.io/t/txn/58bfb88e-2c77-4a07-884c-290e7dbc1d44/events/upsertLines' \\\n   -H 'Content-Type: application/json' \\\n  --data-raw '{\"context\":{\"session\":\"63d8dc25-7351-44fc-9682-f98d3402628f\"},\"items\":[{\"configurationId\":\"626923a6-2bab-4755-90ae-60d40bbb55c4\"}]}'"
			},
			"response": []
		},
		{
			"name": "Delete session",
			"request": {
				"method": "DELETE",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseUrl}}/api/t/{{session}}",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"t",
						"{{session}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get transaction",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "{{adminToken}}",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseUrl}}/api/txn/{{transactionId}}",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"txn",
						"{{transactionId}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get transaction list",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "{{adminToken}}",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseUrl}}/api/txn/{{transactionId}}",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"txn",
						"{{transactionId}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get transaction lines",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "{{adminToken}}",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [
					{
						"key": "Origin",
						"value": "{{baseUrl}}",
						"type": "text"
					},
					{
						"key": "Cookie",
						"value": "SESSION=05eb312c-e0a9-4340-b0ae-cfcc8db9e36f;",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseUrl}}/api/txn/{{transactionId}}/lines",
					"host": [
						"{{baseUrl}}"
					],
					"path": [
						"api",
						"txn",
						"{{transactionId}}",
						"lines"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Txn Metrics",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [
					{
						"key": "origin",
						"value": "dev1.dev.logik.io",
						"type": "text"
					},
					{
						"key": "X-Logik-Customer-Id",
						"value": "559633d3-408a-41c6-86e8-6b12ca396803",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseUrl}}/api/txn/metrics/v1/overview?txnId={{transactionId}}&days=30&toDate=2025-09-18T15:28:04Z",
					"protocol": "https",
					"host": [
						"{{baseUrl}}",
						"dev",
						"logik",
						"io"
					],
					"path": [
						"api",
						"txn",
						"metrics",
						"v1",
						"overview"
					],
					"query": [
						{
							"key": "txnId",
							"value": "{{transactionId}}"
						},
						{
							"key": "days",
							"value": "30"
						},
						{
							"key": "toDate",
							"value": "2025-09-18T15:28:04Z"
						}
					]
				}
			},
			"response": [
				{
					"viewsByUser": [
						{
							"userId": "dev3@dev.logik.io",
							"views": 83.0
						}
					],
					"sessionTimeByUser": [
						{
							"userId": "dev3@dev.logik.io",
							"avgMinutes": 52.8433734939759
						}
					],
					"stageTime": [
						{
							"stage": "draft",
							"avgMinutes": 106.08108108108108
						},
						{
							"stage": "stage2",
							"avgMinutes": 57.25
						},
						{
							"stage": "unknown",
							"avgMinutes": 120.5
						}
					]
				}
			]
		}
	],
	"auth": {
		"type": "bearer",
		"bearer": [
			{
				"key": "token",
				"value": "{{runtimeToken}}",
				"type": "string"
			}
		]
	},
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"packages": {},
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"packages": {},
				"exec": [
					""
				]
			}
		}
	],
	"variable": [
		{
			"key": "session",
			"value": "",
			"type": "string"
		},
		{
			"key": "transactionId",
			"value": "",
			"type": "string"
		}
	]
}
```

