---
title: Webhooks
description: Webhooks are endpoints that can receive a POST request whenever a configuration is saved.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Webhooks

Webhooks are endpoints that can receive a POST request whenever a configuration is saved.

CPQ supports webhooks: endpoints that can receive a POST request when a configuration is saved. Once a webhook has been configured, it is called on every save configuration action.

To enable webhooks, log a case with support. Only one webhook can be created per CPQ environment.

## Webhook use cases

Webhooks can be used to integrate data from CPQ to other downstream systems. Use cases include:

-   Displaying the CPQ native UI via direct URL and sending the config result, via webhook, to a third-party destination. See:

    [Use case: Displaying the CPQ native UI via direct URL](use_case_display_logik_io_native_ui_via_direct_url.md)

-   Sending config data directly to a quoting or order management system
-   Pushing the configuration result to middleware that can manipulate the data and pass it along to downstream systems

[Webhook demo](https://youtu.be/khjWIDJ9SHk)

## Webhook setup

![Webhook setup](../images/cpq-webhooks-setup-1.png)

-   When webhooks are enabled, they can be found in the Utilities menu in the CPQ Admin screen.
-   Summary: Webhook configuration is similar to external connections. The Name, Description and Integration type can all be defined.
-   Authentication: Webhooks support both no authentication \(None\) as well as bearer token authentication \(Bearer Token\).
-   Webhook Details: Additional details of the webhook can be specified as well to control the behavior.

## Webhook details

![Webhook setup](../images/cpq-webhooks-details.png)

1.  URL: The endpoint to receive the data from Logik on save of a configuration. Must be able to receive an HTTP POST request.
2.  Async: When enabled, ensures that the end user is redirected immediately when a configuration is completed and does not wait for a response from the server before exiting. The save process is asynchronous.

    When disabled, this ensures that the webhook process is resolved before the user is redirected. The save process is synchronous.

3.  Content: The data that CPQ should send to the endpoint.
    -   Config Data: all admin-created configuration fields and their input values
    -   BOM and System Fields: all system configuration fields and their values; the bill of materials \(as specified in the BOM Types input immediately below\)
4.  BOM Types: The BOM types to be sent in the request.
5.  Timeout: The timeout value in milliseconds
6.  Additional Headers: Additional headers that should be sent along with the request, entered as quoted key value pairs. For example, `"X-header1": "value1"`

## Example webhook body

The body that the webhook sends to the external resource looks like the following. This example covers product pickers and the built-in system fields from an environment.

```
{
  "uuid": "8014a955-49c4-4d63-a15a-8c91cef6f6f4",
  "fields": [
    {
      "userEdited": false,
      "dataType": "array",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "pp",
      "uniqueName": "pp",
      "value": ["alpha"],
      "optionSet": {
        "selectedOptions": [
          {
            "label": "alpha",
            "state": "visible",
            "value": "alpha",
            "imageUrl": null,
            "orderNumber": 10
          }
        ],
        "options": [
          {
            "label": "alpha",
            "state": "visible",
            "value": "alpha",
            "imageUrl": null,
            "orderNumber": 10
          },
          {
            "label": "beta",
            "state": "visible",
            "value": "beta",
            "imageUrl": null,
            "orderNumber": null
          }
        ]
      },
      "rows": {
        "content": [
          {
            "index": 0,
            "fields": [
              {
                "userEdited": false,
                "dataType": "text",
                "visibilityState": "visible",
                "editable": "false",
                "variableName": "pp.value",
                "uniqueName": "pp-0-pp.value",
                "value": "alpha",
                "set": "pp",
                "index": 0
              },
              {
                "userEdited": true,
                "dataType": "boolean",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.select",
                "uniqueName": "pp-0-pp.select",
                "value": true,
                "optionSet": {
                  "options": [
                    {
                      "label": "true",
                      "state": "visible",
                      "value": "true",
                      "imageUrl": null,
                      "orderNumber": null
                    },
                    {
                      "label": "false",
                      "state": "visible",
                      "value": "false",
                      "imageUrl": null,
                      "orderNumber": null
                    }
                  ]
                },
                "set": "pp",
                "index": 0
              },
              {
                "userEdited": false,
                "dataType": "number",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.quantity",
                "uniqueName": "pp-0-pp.quantity",
                "value": 1,
                "set": "pp",
                "index": 0
              },
              {
                "userEdited": false,
                "dataType": "text",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.data",
                "uniqueName": "pp-0-pp.data",
                "value": "",
                "set": "pp",
                "index": 0
              }
            ],
            "label": "alpha",
            "state": "visible",
            "value": "alpha",
            "imageUrl": null,
            "orderNumber": 10,
            "productDetails": {}
          },
          {
            "index": 1,
            "fields": [
              {
                "userEdited": false,
                "dataType": "text",
                "visibilityState": "visible",
                "editable": "false",
                "variableName": "pp.value",
                "uniqueName": "pp-1-pp.value",
                "value": "beta",
                "set": "pp",
                "index": 1
              },
              {
                "userEdited": false,
                "dataType": "boolean",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.select",
                "uniqueName": "pp-1-pp.select",
                "value": false,
                "optionSet": {
                  "options": [
                    {
                      "label": "true",
                      "state": "visible",
                      "value": "true",
                      "imageUrl": null,
                      "orderNumber": null
                    },
                    {
                      "label": "false",
                      "state": "visible",
                      "value": "false",
                      "imageUrl": null,
                      "orderNumber": null
                    }
                  ]
                },
                "set": "pp",
                "index": 1
              },
              {
                "userEdited": false,
                "dataType": "number",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.quantity",
                "uniqueName": "pp-1-pp.quantity",
                "value": 0,
                "set": "pp",
                "index": 1
              },
              {
                "userEdited": false,
                "dataType": "text",
                "visibilityState": "visible",
                "editable": "true",
                "variableName": "pp.data",
                "uniqueName": "pp-1-pp.data",
                "value": "",
                "set": "pp",
                "index": 1
              }
            ],
            "label": "beta",
            "state": "visible",
            "value": "beta",
            "imageUrl": null,
            "orderNumber": null,
            "productDetails": {}
          }
        ],
        "pageable": "INSTANCE",
        "last": true,
        "totalPages": 1,
        "totalElements": 2,
        "size": 2,
        "number": 0,
        "sort": { "empty": true, "sorted": false, "unsorted": true },
        "numberOfElements": 2,
        "first": true,
        "empty": false
      }
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productCode",
      "uniqueName": "sys.productCode",
      "value": "CC-LGK"
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "partner.quote.pricebookId",
      "uniqueName": "partner.quote.pricebookId",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "partner.quote.currencyIsoCode",
      "uniqueName": "partner.quote.currencyIsoCode",
      "value": "USD"
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productFamily",
      "uniqueName": "sys.productFamily",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productDescription",
      "uniqueName": "sys.productDescription",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "partner.quote.id",
      "uniqueName": "partner.quote.id",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productUOM",
      "uniqueName": "sys.productUOM",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "number",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productPrice",
      "uniqueName": "sys.productPrice",
      "value": 0
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productName",
      "uniqueName": "sys.productName",
      "value": "CheckConfig"
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "partner.quote.lineId",
      "uniqueName": "partner.quote.lineId",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "number",
      "visibilityState": "visible",
      "editable": "false",
      "variableName": "pp.aggregates.quantity_sum",
      "uniqueName": "pp.aggregates.quantity_sum",
      "value": 1
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.productId",
      "uniqueName": "sys.productId",
      "value": "CC-LGK"
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.actionContext",
      "uniqueName": "sys.actionContext",
      "value": ""
    },
    {
      "userEdited": false,
      "dataType": "text",
      "visibilityState": "visible",
      "editable": "true",
      "variableName": "sys.currentDate",
      "uniqueName": "sys.currentDate",
      "value": "2023-08-04"
    }
  ],
  "products": [
    {
      "id": "alpha",
      "quantity": 1,
      "bomType": "SALES",
      "type": "accessory",
      "extended": { "data": "" },
      "pricing": {
        "productSellingModelId": "OneTime_OneTime_2023_07_05",
        "endDate": null,
        "startDate": null,
        "ProductId": "01tHr000007i4B5IAI",
        "StartingUnitPriceSource": "System",
        "ListPrice": 99.99,
        "TotalLineAmount": 99.99,
        "ListPriceTotal": 99.99,
        "StartingPriceTotal": 99.99,
        "Quantity": 1.0,
        "PricingTermCount": 1,
        "NetUnitPrice": 99.99,
        "StartingUnitPrice": 99.99,
        "PricebookEntryId": "01uHr00000FYKDUIA5",
        "TotalAdjustmentDistAmount": 0,
        "TotalAdjustmentAmount": 0,
        "TotalPrice": 99.99,
        "SalesItemType": "Product"
      },
      "name": "alpha",
      "partnerId": "01tHr000007i4B5IAI",
      "productCode": "alpha",
      "externalId": "",
      "productFamily": "",
      "description": "",
      "uom": "",
      "price": 99.99,
      "extPrice": 99.99,
      "level": 0,
      "rollUpPrice": 99.99
    }
  ],
  "total": 99.99
}
```

