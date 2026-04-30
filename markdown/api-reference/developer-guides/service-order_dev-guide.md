---
title: Service Order Open API Developer Guide
description: Use the Service Order Open API to create, update, and retrieve service order information.The Service Order Open API can be extended by editing script includes.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Developer guides, API implementation and reference]
---

# Service Order Open API Developer Guide

Use the Service Order Open API to create, update, and retrieve service order information.

This developer guide provides information on how to extend the [Service Order Open API](../../../inbound-rest/concept/service-order-open-api.md#) to make various customizations.

## Extending the Service Order Open API

The Service Order Open API can be extended by editing script includes.

These script includes should only be edited with an understanding of the consequences of the changes.

-   `TMFServiceOrderAPIUtil`: Contains functions to handle POST requests.
-   `TMFServiceOrderGetAPIUtil`: Contains functions to handle GET requests.
-   `ServiceOrderExtensionOOB`: Contains helper functions that support functions in `TMFServiceOrderAPIUtil` and `TMFServiceOrderGetAPIUtil`.
-   `ServiceOrderProcessor`: An empty script include file. Use this file to define any functions that you want to override from `ServiceOrderExtensionOOB`.

Extend the Service Order Open API to make the following customizations.

### Required parameters

To change which request body parameters are required or not required to create a service order, override the function `getServiceOrderSchema()` contained in the `ServiceOrderExtensionOOB` script include.

The function `getServiceOrderSchema()` reads the schema from the `TMFOrderAPIConstants` script include. `TMFOrderAPIConstants` is protected and can't be edited, so you can't just update the schema. Instead, a new schema must be read from a different file. You can override `getServiceOrderSchema()` to read a new schema. To override `getServiceOrderSchema()`, write a function with the same name in the `ServiceOrderProcessor` script include. The new function in `ServiceOrderProcessor` will be called by `TMFServiceOrderAPIUtil` to replace the default `getServiceOrderSchema()` function in `ServiceOrderExtensionOOB`.

In this example, `getServiceOrderSchema()` returns a custom schema that is defined in a new constant file.

```
// ServiceOrderProcessor

var ServiceOrderProcessor = Class.create();
ServiceOrderProcessor.prototype = Object.extendsObject(ServiceOrderExtensionOOB, {
   // Define overriding functions here
   // Function name and parameters must be identical to the function it overrides

   getServiceOrderSchema: function() {
      //Define your own custom schema in a new constant file
      return JSON.parse(Constants.SCHEMA.CREATE_SERVICE_ORDER);
   },

   type: 'ServiceOrderProcessor'
});
```

### Request body validation

To perform additional validation on the request body, override `ServiceOrderExtensionOOB` functions. `ServiceOrderExtensionOOB` contains the following four helper functions that return `true` by default.

-   `validatePostRequest()` - Called by `processPostOrder()` in `TMFServiceOrderAPIUtil`.
-   `validateServiceObj()` - Called by `processPostOrder()` in `TMFServiceOrderAPIUtil`.
-   `validateRelatedPartyObj()` - Called by `processPostOrder()` in `TMFServiceOrderAPIUtil`.
-   `validateGetRequest()` - Called by `processGetOrder()` in `TMFServiceOrderGetAPIUtil`.

If a helper function returns `false`, it stops the API operation. To apply custom validation, override `ServiceOrderExtensionOOB` helper functions by creating functions with identical names and parameters in `ServiceOrderProcessor`. These new `ServiceOrderProcessor` functions will be called by `TMFServiceOrderAPIUtil` and `TMFServiceOrderGetAPIUtil` to replace the default `ServiceOrderExtensionOOB` helper functions.

In this example, a function in `ServiceOrderProcessor` overrides a default function in `ServiceOrderExtensionOOB` to perform validation on the **serviceOrderItem** attribute.

```
// ServiceOrderProcessor

var ServiceOrderProcessor = Class.create();
ServiceOrderProcessor.prototype = Object.extendsObject(ServiceOrderExtensionOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    validatePostRequest: function(orderObject, details) {
        // Returning false terminates the POST request
        // Make sure to push error message in details array in case of error
        if (gs.nil(orderObject.serviceOrderItem)) {
            details.push(new TMFCommonOrderAPIUtil().getErrorDetailsObj(TMFOrderAPIConstants.MESSAGES.MISSING_ORDER_ITEM, '/'));
            return false;
        }
        return true;
    },

    type: 'ServiceOrderProcessor'
});
```

### Additional REST operations

To create additional operations beyond the existing GET and POST operations, [create additional scripted REST resources](../../../custom-web-services/task/t_CreateAScriptedRESTAPIResource.md) for the Service Order Open API. The logic of the new scripted REST resources should be consistent with the existing operations. Define functions for the new operations in a new script include.

### Field mapping

When creating records, the API maps request body parameters to record fields. When retrieving records, the API maps record fields to response object attributes.

`ServiceOrderExtensionOOB` contains the following functions to map a POST request body to a GlideRecord.

-   `transformOrderGr()`
-   `transformOrdLineItemGr()`
-   `transformCustLineItmContact()`
-   `transformOrderItemChar()`

`ServiceOrderExtensionOOB` contains the following functions to map a GlideRecord to a response object for GET or POST requests.

-   `transformPostOrderResponse()`
-   `transformGetOrderResponse()`
-   `transformServiceObj()`
-   `transformRelatedPartyCustomerLineItem()`
-   `transformOrderItemRelationship()`
-   `transformGetOrdLineItmResponse()`
-   `transformServiceCharacteristics()`
-   `transformServiceSpecification()`

Customize field mappings to add and retrieve data for additional fields, or to change the default mappings for fields. To customize the field mappings, override `ServiceOrderExtensionOOB` mapping functions by creating functions with identical names and parameters in `ServiceOrderProcessor`. These new `ServiceOrderProcessor` functions will be used by `TMFServiceOrderAPIUtil` and `TMFServiceOrderGetAPIUtil` to replace the default `ServiceOrderExtensionOOB` mapping functions.

In this example, two functions in `ServiceOrderProcessor` override the default functions in `ServiceOrderExtensionOOB` to create mappings for the **external\_id** and **sys\_id** fields.

```
// ServiceOrderProcessor

var ServiceOrderProcessor = Class.create();
ServiceOrderProcessor.prototype = Object.extendsObject(ServiceOrderExtensionOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    transformOrderGr: function(requestObject, orderGr) {
        orderGr.external_id = requestObject.externalId;
        return orderGr;
    },

    transformPostOrderResponse: function(orderObject, orderGr) {
        orderObject.id = orderGr.getValue('sys_id');
        return orderObject;
    },

    type: 'ServiceOrderProcessor'
});
```

