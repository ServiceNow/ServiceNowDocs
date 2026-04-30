---
title: Product Order Open API Developer Guide
description: Use the Product Order Open API to create, update, and retrieve product order information.The Product Order Open API can be extended by editing script includes.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Developer guides, API implementation and reference]
---

# Product Order Open API Developer Guide

Use the Product Order Open API to create, update, and retrieve product order information.

This developer guide provides information on how to extend the [Product Order Open API](../../../inbound-rest/concept/tmf622_product_ordering-api.md#) to make various customizations.

## Extending the Product Order Open API

The Product Order Open API can be extended by editing script includes.

These script includes should only be edited with an understanding of the consequences of the changes.

-   `TMFProductOrderAPIUtil`: Contains functions to handle POST requests.
-   `TMFProductOrderGetAPIUtil`: Contains functions to handle GET requests.
-   `ProductOrderExtensionOOB`: Contains helper functions that support functions in `TMFProductOrderAPIUtil` and `TMFProductOrderGetAPIUtil`.
-   `ProductOrderProcessor`: An empty script include file. Use this file to define any functions that you want to override from `ProductOrderExtensionOOB`.

Extend the Product Order Open API to make the following customizations.

### Required parameters

To change which request body parameters are required or not required to create a product order, override the function `getProductOrderSchema()` contained in the `ProductOrderExtensionOOB` script include.

The function `getProductOrderSchema()` reads the schema from the `TMFOrderAPIConstants` script include. `TMFOrderAPIConstants` is protected and can't be edited, so you can't just update the schema. Instead, a new schema must be read from a different file. You can override `getProductOrderSchema()` to read a new schema. To override `getProductOrderSchema()`, write a function with the same name in the `ProductOrderProcessor` script include. The new function in `ProductOrderProcessor` will be called by `TMFProductOrderAPIUtil` to replace the default `getProductOrderSchema()` function in `ProductOrderExtensionOOB`.

In this example, `getProductOrderSchema()` returns a custom schema that is defined in a new constant file.

```
// ProductOrderProcessor

var ProductOrderProcessor = Class.create();
ProductOrderProcessor.prototype = Object.extendsObject(ProductOrderExtensionOOB, {
   // Define overriding functions here
   // Function name and parameters must be identical to the function it overrides

   getProductOrderSchema: function() {
      //Define your own custom schema in a new constant file
      return JSON.parse(Constants.SCHEMA.CREATE_PRODUCT_ORDER);
   },

   type: 'ProductOrderProcessor'
});
```

### Request body validation

To perform additional validation on the request body, override `ProductOrderExtensionOOB` functions. `ProductOrderExtensionOOB` contains the following four helper functions that return `true` by default.

-   `validatePostRequest()` - Called by `processCreateOrder()` in `TMFProductOrderAPIUtil`.
-   `validateProductObj()` - Called by `processCreateOrder()` in `TMFProductOrderAPIUtil`.
-   `validateRelatedPartyObj()` - Called by `processCreateOrder()` in `TMFProductOrderAPIUtil`.
-   `validateGetRequest()` - Called by `processGetOrder()` in `TMFProductOrderGetAPIUtil`.

If a helper function returns `false`, it stops the API operation. To apply custom validation, override `ProductOrderExtensionOOB` helper functions by creating functions with identical names and parameters in `ProductOrderProcessor`. These new `ProductOrderProcessor` functions will be called by `TMFProductOrderAPIUtil` and `TMFProductOrderGetAPIUtil` to replace the default `ProductOrderExtensionOOB` helper functions.

In this example, a function in `ProductOrderProcessor` overrides a default function in `ProductOrderExtensionOOB` to perform validation on the **productOrderItem** attribute.

```
// ProductOrderProcessor

var ProductOrderProcessor = Class.create();
ProductOrderProcessor.prototype = Object.extendsObject(ProductOrderExtensionOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    validatePostRequest: function(orderObject, details) {
        // Returning false terminates the POST request
        // Make sure to push error message in details array in case of error
        if (gs.nil(orderObject.productOrderItem)) {
            details.push(new TMFCommonOrderAPIUtil().getErrorDetailsObj(TMFOrderAPIConstants.MESSAGES.MISSING_ORDER_ITEM, '/'));
            return false;
        }
        return true;
    },

    type: 'ProductOrderProcessor'
});
```

### Additional REST operations

To create additional operations beyond the existing GET and POST operations, [create additional scripted REST resources](../../../custom-web-services/task/t_CreateAScriptedRESTAPIResource.md) for the Product Order Open API. The logic of the new scripted REST resources should be consistent with the existing operations. Define functions for the new operations in a new script include.

### Field mapping

When creating records, the API maps request body parameters to record fields. When retrieving records, the API maps record fields to response object attributes.

`ProductOrderExtensionOOB` contains the following functions to map a POST request body to a GlideRecord.

-   `transformOrderGr()`
-   `transformOrdLineItemGr()`
-   `getLineItemPrice()`
-   `transformPriceOrderTypeAndState()`
-   `transformCustLineItmContact()`
-   `transformOrderItemChar()`

`ProductOrderExtensionOOB` contains the following functions to map a GlideRecord to a response object for GET or POST requests.

-   `transformPostOrderResponse()`
-   `transformGetOrderResponse()`
-   `transformProductObj()`
-   `transformRelatedPartyCustomerLineItem()`
-   `transformOrderItemRelationship()`
-   `transformGetOrdLineItmResponse()`
-   `transformProductCharacteristics()`
-   `transformProductSpecification()`

Customize field mappings to add and retrieve data for additional fields, or to change the default mappings for fields. To customize the field mappings, override `ProductOrderExtensionOOB` mapping functions by creating functions with identical names and parameters in `ProductOrderProcessor`. These new `ProductOrderProcessor` functions will be used by `TMFProductOrderAPIUtil` and `TMFProductOrderGetAPIUtil` to replace the default `ProductOrderExtensionOOB` mapping functions.

In this example, two functions in `ProductOrderProcessor` override the default functions in `ProductOrderExtensionOOB` to create mappings for the **external\_id** and **sys\_id** fields.

```
// ProductOrderProcessor

var ProductOrderProcessor = Class.create();
ProductOrderProcessor.prototype = Object.extendsObject(ProductOrderExtensionOOB, {
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

    type: 'ProductOrderProcessor'
});
```

