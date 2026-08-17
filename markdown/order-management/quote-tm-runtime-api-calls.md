---
title: ServiceNow Quote Experience runtime API calls
description: Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a Postman collection for testing in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-runtime-api-calls.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience runtime API calls

Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a Postman collection for testing in CPQ.

## API overview

CPQ APIs are divided into two categories: runtime APIs and admin APIs. Runtime APIs are the same APIs used in the runtime quote experience. The following table lists the runtime APIs for ServiceNow Quote Experience.

|API action|Purpose|Response|
|----------|-------|--------|
|Initialize a session|Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction. If no transaction is specified, a new transaction is created.|Returns a session ID, a transaction ID, and transaction information.|
|Delete a session|Deletes a session to securely end user activity, clear session-specific data, and free up system resources.|Session is deleted. No information is returned.|
|Create a transaction|Creates a transaction, providing the object to manage the transaction lifecycle, configure and add products, and determine pricing.|Returns a transaction ID and transaction information.|
|Run events on a transaction|Triggers a specified system or custom event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, and validating configurations.|Varies by event.|
|Add products to a transaction \(upsert\)|Adds one or more products to a transaction, enabling dynamic configuration and pricing updates based on the product's attributes.|Returns updated transaction data with the additional products.|
|Get a list of transactions|Retrieves a list of transactions, enabling users to view, manage, or take action on existing transactions.|A list of transactions with transaction IDs and metadata.|
|Get details of a transaction|Retrieves the header information of a transaction, including stage, account, and summary-level data.|All header field data for the transaction.|
|Get a transaction's lines|Retrieves the line item details for a transaction, including product data, quantities, pricing, and custom attributes for each line.|All line-level field data for the transaction.|

**Note:** Event APIs are authorized via session cookie only. Avoid building a scenario in which the user initiates an event that also fires an event API on the same transaction — such an implementation can result in unpredictable behavior.

## Additional APIs

For details about the API that retrieves metrics for transactions, see [Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-metrics-api.md).

## Postman collection

The following Postman collection provides ready-to-use API requests for the ServiceNow Quote Experience runtime APIs.

```
{
  "info": {
    "_postman_id": "0112bd72-984c-4285-a40f-5724e5d799cb",
    "name": "1 - ServiceNow Quote Experience Headless Runtime APIs",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
    "_exporter_id": "40935282"
  },
  "item": [
    {
      "name": "Initialize a session",
      "request": {
        "method": "POST",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "body": {
          "mode": "raw",
          "raw": "{\"id\": \"{{transactionId}}\", \"stateful\": false}",
          "options": {"raw": {"language": "json"}}
        },
        "url": {"raw": "{{baseUrl}}/api/t","host": ["{{baseUrl}}"],"path": ["api","t"]}
      }
    },
    {
      "name": "Create a new transaction",
      "request": {
        "method": "POST",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "body": {
          "mode": "raw",
          "raw": "{\"stateful\": false}",
          "options": {"raw": {"language": "json"}}
        },
        "url": {"raw": "{{baseUrl}}/api/t","host": ["{{baseUrl}}"],"path": ["api","t"]}
      }
    },
    {
      "name": "Run an event (using existing session)",
      "request": {
        "method": "POST",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "body": {
          "mode": "raw",
          "raw": "{\"context\": {\"session\": \"{{session}}\"}}",
          "options": {"raw": {"language": "json"}}
        },
        "url": {
          "raw": "{{baseUrl}}/api/t/{{transactionId}}/events/test_event_transitions",
          "host": ["{{baseUrl}}"],"path": ["api","t","{{transactionId}}","events","test_event_transitions"]
        }
      }
    },
    {
      "name": "Upsert lines",
      "request": {
        "method": "POST",
        "header": [
          {"key": "Content-Type","value": "application/json"},
          {"key": "Origin","value": "{{baseUrl}}","type": "text"}
        ],
        "body": {
          "mode": "raw",
          "raw": "{\"context\": {\"stateful\": false},\"items\": [{\"configurationId\": \"626923a6-2bab-4755-90ae-60d40bbb55c4\"},{\"id\": \"SimpleProductId\"}]}",
          "options": {"raw": {"language": "json"}}
        },
        "url": {
          "raw": "{{baseUrl}}/api/t/{{transactionId}}/events/upsertLines",
          "host": ["{{baseUrl}}"],"path": ["api","t","{{transactionId}}","events","upsertLines"]
        }
      }
    },
    {
      "name": "Copy transaction",
      "request": {
        "method": "POST",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "body": {
          "mode": "raw",
          "raw": "{\"context\": {\"stateful\": false}}",
          "options": {"raw": {"language": "json"}}
        },
        "url": {
          "raw": "{{baseUrl}}/api/t/{{transactionId}}/events/copyTransaction",
          "host": ["{{baseUrl}}"],"path": ["api","t","{{transactionId}}","events","copyTransaction"]
        }
      }
    },
    {
      "name": "Delete session",
      "request": {
        "method": "DELETE",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "url": {"raw": "{{baseUrl}}/api/t/{{session}}","host": ["{{baseUrl}}"],"path": ["api","t","{{session}}"]}
      }
    },
    {
      "name": "Get transaction",
      "request": {
        "auth": {"type": "bearer","bearer": [{"key": "token","value": "{{adminToken}}","type": "string"}]},
        "method": "GET",
        "header": [{"key": "Origin","value": "{{baseUrl}}","type": "text"}],
        "url": {"raw": "{{baseUrl}}/api/txn/{{transactionId}}","host": ["{{baseUrl}}"],"path": ["api","txn","{{transactionId}}"]}
      }
    },
    {
      "name": "Get transaction lines",
      "request": {
        "auth": {"type": "bearer","bearer": [{"key": "token","value": "{{adminToken}}","type": "string"}]},
        "method": "GET",
        "header": [
          {"key": "Origin","value": "{{baseUrl}}","type": "text"},
          {"key": "Cookie","value": "SESSION=05eb312c-e0a9-4340-b0ae-cfcc8db9e36f;","type": "text"}
        ],
        "url": {"raw": "{{baseUrl}}/api/txn/{{transactionId}}/lines","host": ["{{baseUrl}}"],"path": ["api","txn","{{transactionId}}","lines"]}
      }
    }
  ],
  "auth": {
    "type": "bearer",
    "bearer": [{"key": "token","value": "{{runtimeToken}}","type": "string"}]
  },
  "variable": [
    {"key": "session","value": "","type": "string"},
    {"key": "transactionId","value": "","type": "string"}
  ]
}
```

