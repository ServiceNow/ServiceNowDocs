---
title: Configure extension point for Product search API
description: The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point enables Shopping Hub to search a punchout supplier's catalog through the supplier's search API and to display the product details that the supplier returns, such as name, price, SKU, and image.View the format of the sn\_spend\_intg.ThirdPartySystemApiExtension extension point.Create script include that enables you to display all the products details for the punchout supplier in Shopping Hub.Create an extension instance to associate the punchout supplier's script include with the sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-11-05"
reading_time_minutes: 7
breadcrumb: [Configure punchout third-party site purchases, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure extension point for Product search API

The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point enables Shopping Hub to search a punchout supplier's catalog through the supplier's search API and to display the product details that the supplier returns, such as name, price, SKU, and image.

Use this extension point when a punchout supplier provides a search API. You write a script include that implements the extension point methods for each supplier, and then link the script include to the extension point with an extension instance. SPO then uses your script include to search the supplier's catalog and to display the products in Shopping Hub. SPO does not provide an implementation of this extension point.

## How the product search works

1.  A shopper searches for a product in Shopping Hub.
2.  SPO finds the punchout suppliers whose third-party registration has the **APIs exchange** check box selected and whose API connection has a **Punchout group** that the shopper belongs to. SPO skips an API connection that does not have a **Product search API** value.
3.  For each supplier, SPO looks for an implementation whose `getSupplierId` method returns the sys\_id of that supplier.
4.  SPO calls the `buildSearchRestMessage` method to build the search request, sends the request to the supplier, and passes the response body to the `transformSearchResultsResponse` method.
5.  Shopping Hub displays the products that the `transformSearchResultsResponse` method returns in the search results.

## Before you begin

-   The **Punchout** check box is selected on the supplier record.
-   The supplier has a third-party registration with the **APIs exchange** check box selected, and an API connection that has the **Product search API** URL and a **Punchout group** that includes the shoppers. For more information, see [Configure punchout for third-party site purchases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.md).

## Methods to implement

|Method|Required|Description|
|------|--------|-----------|
|`getSupplierId()`|Yes|Returns the sys\_id of the supplier record as a string. SPO uses the implementation whose value exactly matches the supplier of the third-party registration. Return the sys\_id, not the supplier name.|
|`initialize()`|Yes|The standard script include initializer. SPO calls it on every implementation before it matches the supplier.|
|`buildSearchRestMessage(restMessage, searchEndpointUrl, searchTerm)`|Yes|Configures the search request. `restMessage` is an empty REST message object, `searchEndpointUrl` is the **Product search API** value, and `searchTerm` is the keyword that the shopper entered, already URL-encoded. Set the endpoint, HTTP method, headers, and request body, and return the `restMessage` object.|
|`transformSearchResultsResponse(responseBody, supplierId)`|Yes|Converts the response body of the supplier, which is passed as a string, into an array of product objects. If the method does not return an array, Shopping Hub does not display any products.|
|`buildProductDetailRestMessage(restMessage, productDetailsUrl, productSku)` and `transformProductDetailResponse(responseBody, productSku)`|Only if you use the Product details API|Build the request for the details of a product and convert the response.|
|`buildPlaceOrderRestMessage(restMessage, placeOrderUrl, orderGr, orderLinesGr)`, `doesPlaceOrderAPIReturnsOrderConfrmDetails()`, and `transformPlaceOrderResponse(responseBody)`|Only if you use the Place order request API|Build the order request, indicate whether the supplier response contains the order confirmation details, and convert the response.|

SPO does not call the **Access token API** URL and does not pass the **Access token API** or **API Key/Client ID** values to your script include. If the supplier requires authentication, your script include must obtain the access token itself, for example, in the `buildSearchRestMessage` method.

## Product object

Each object in the array that the `transformSearchResultsResponse` method returns describes one product. Include the following fields:

-   `sysId`: A unique ID for the product. Shopping Hub uses it to display the product details from the search results.
-   `name`, `sku`, and `supplier`: Required to display the product details. The `supplier` object includes the supplier `id`.
-   `price`, `image`, `description`, `unit`, `category`, and `productType` \(`good` or `service`\).
-   `source`: Set to `api`.

The object can also include fields such as `deliveryInfo`, `minrefprice`, `maxrefprice`, and `score`. To view the example script that shows the full product object, see the steps in this topic.

## If Shopping Hub does not display any products

-   Check the system log for the message `Implementation not found for supplier`. This message means that no active implementation returned the sys\_id of the supplier from the `getSupplierId` method.
-   Check that the `buildSearchRestMessage` method returns the `restMessage` object and that the `transformSearchResultsResponse` method returns an array.
-   Check that the shopper belongs to the **Punchout group** of the API connection, and that the **Product search API** field and the **APIs exchange** check box are set.
-   SPO does not check the HTTP status of the supplier response. If the supplier URL or the authentication is not correct, your script receives an error response. Check the Outbound HTTP Requests log to confirm that the request was sent and to view the response.

**Parent Topic:**[Configure punchout for third-party site purchases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.md)

## View the third-party system API extension point format

View the format of the sn\_spend\_intg.ThirdPartySystemApiExtension extension point.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search for `sn_spend_intg.ThirdPartySystemApiExtension` and then select the link to open the extension point.

    View the format of the extension point script.


## Create script include for punchout supplier products

Create script include that enables you to display all the products details for the punchout supplier in Shopping Hub.

### Before you begin

Role required: admin

### About this task

Ensure that the application scope is set to Shopping Hub.

### Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Script Includes**.

2.  Select **New**.

3.  On the Script Include form, fill in the fields.

<table id="table_mfv_c51_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the script include.

</td></tr><tr><td>

API Name

</td><td>

Read-only and auto-populated API name.

</td></tr><tr><td>

Application

</td><td>

The application where this script include resides. For example, Shopping Hub.

</td></tr><tr><td>

Accessible from

</td><td>

Sets which applications can access this script include.

</td></tr><tr><td>

Glide AJAX callable

</td><td>

Makes the script include available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL.

</td></tr><tr><td>

Mobile callable

</td><td>

Option to make the script include available on the mobile device.

</td></tr><tr><td>

Sandbox enabled

</td><td>

Option to let a client make changes to their script include without causing global affecting.

</td></tr><tr><td>

Active

</td><td>

Enables the script include when selected. Deselect the active field to disable the script include.

</td></tr><tr><td>

Description

</td><td>

Provides descriptive content regarding the script include.

</td></tr><tr><td>

Script

</td><td>

The server-side script to run when called from other scripts.The script must define a single JavaScript class or a global function. The class or function name must match the Name field.

</td></tr><tr><td>

Protection policy

</td><td>

Protection policy for script includes published as part of a custom application.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Create extension instance for the scripted extension point

Create an extension instance to associate the punchout supplier's script include with the sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point.

### Before you begin

Role required: admin

### About this task

An extension instance is a registered instance of a scripted extension point that links a script include with a scripted extension point.

**Note:** Ensure that the application scope is set to Shopping Hub.

### Procedure

1.  Select All and in the search filter, enter `sys_extension_instance.LIST`, and then press enter or return on your keyboard.

2.  Select **New**.

3.  In the **Point** field, enter `sn_spend_intg.ThirdPartySystemApiExtension`.

4.  In the **Class** field, select the script include that you created.

    For more information, see [Create script include for punchout supplier products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md).

5.  In the **Order** field, enter a number.

    When multiple extension instances are available, the one with the least order value takes precedence.

6.  Select the **Active** check box.

7.  Select **Submit**.


