---
title: Configure scripted extension points for the manage order operations agent
description: Configure scripted extension points so that the manage order operations chat assistant can check product availability, validate order exception requests for delivery, quantity, and shipping location, and evaluate quote thresholds against your external inventory, ERP, or pricing systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/create-atp-api-call.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management, Sales Customer Relationship Management]
---

# Configure scripted extension points for the manage order operations agent

Configure scripted extension points so that the manage order operations chat assistant can check product availability, validate order exception requests for delivery, quantity, and shipping location, and evaluate quote thresholds against your external inventory, ERP, or pricing systems.

## Before you begin

The application scope must be set to Manage Order Operations. You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

Role required: admin

## About this task

The demo data for the manage order operations agent includes sample implementations of the following scripted extension points.

|Extension point|API name|Purpose|
|---------------|--------|-------|
|Order exception check|sn\_ord\_ops\_aias.orderExceptionCheckEP|Validate quantity, delivery availability, and shipping location for order line items.|
|Threshold check for quote|sn\_ord\_ops\_aias.ThresholdCheckForQuote|Determine whether a requested quantity change crosses the configured threshold for quote-side handling.|

To enable real-world functionality such as querying on-hand quantities, delivery dates, location feasibility, and quote thresholds from external Enterprise Resource Planning \(ERP\) or pricing systems like SAP or Oracle, replace each demo implementation with your custom logic.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **Scripted Extension Points** &gt; **Scripted Extension Points**.

3.  In the **API Name** field, search for a scripted extension point you want to configure.

4.  View the sample script included in the demo data by selecting the API name of the extension point.

5.  Create your own implementation of the selected extension point by selecting the **Create implementation** related link.

6.  On the Script Include form for your chosen extension point, fill in the fields.

    For a description of the Script Include form fields, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).

7.  Edit the function in your extension-point implementation to apply your own logic, using the following function signatures.

    -   **checkOrderExceptionReq**

        Placeholder function meant to be overridden. Use this placeholder to implement the logic to:

        -   Validate the requested quantity for the specified order line items.
        -   Confirm delivery availability for the order line items.
        -   Validate the requested shipping location for the order line items.
        Input:

        ```
        {
        "<selectedLineNumber>": {
        "lines": { "<line_sys_id>": { "product_offering": <Product offering sys_id of the order line item> } },
        "requested_changes": {
        "requested_quantity": <New quantity requested by the customer>,
        "requested_shipping_location": <sys_id of the requested shipping location>,
        "requested_expected_date": <Requested delivery date in yyyy-MM-dd format>
        }
        }
        }
        ```

        Output:

        ```
        {
        "<selectedLineNumber>": {
        "canChangeQty": <Boolean; true if the quantity change is permitted>,
        "approvedQty": <Integer representing the approved quantity>,
        "isQuantityError": <Boolean; true if the quantity check failed>,
        "quantityErrorMsg": <Error message string for quantity check failures>,
        "canChangeLocation": <Boolean; true if the shipping location change is permitted>,
        "isLocationError": <Boolean; true if the location check failed>,
        "locationErrorMsg": <Error message string for location check failures>,
        "canExpedite": <Boolean; true if the requested expedition date is achievable>,
        "earliestDelivery": <Earliest possible delivery date in yyyy-MM-dd format>,
        "isDateError": <Boolean; true if the expedition date check failed>,
        "dateErrorMsg": <Error message string for expedition date check failures>
        }
        }
        ```

    -   **isAboveQuoteThreshold**

        Placeholder function meant to be overridden. Use this placeholder to implement the logic to:

        -   Compare the requested quantity change against your configured price or quantity threshold.
        -   Return whether the request requires quote-side handling.
        Input:

        ```
        casePayload:
        {
        "<selectedLineNumber>": {
        "lines": { "<line_sys_id>": {
        "quantity": <Current quantity on the order line>,
        "product_offering": <Product offering sys_id of the order line item>
        } },
        "approved_changes": {
        "quantity": <New approved quantity for the line>,
        "expected_date": <New approved delivery date in yyyy-MM-dd format>,
        "location": <sys_id of the approved shipping location>
        }
        }
        }
        threshold: <Numeric threshold value supplied by the caller, resolved from sn_ord_ops_aias.OrderExceptionConstants.PRICE_THRESHOLD>
        ```

        Output:

        ```
        <Boolean; true if any selected line's quantity delta exceeds the supplied threshold and the change should be routed for quote-side handling, false otherwise>
        ```

8.  Select **Update**.

9.  Validate your implementation by requesting order changes from the Business Portal using the Now Assist Virtual Assistant.

    For more information, see [Request order changes using Now Assist Virtual Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/request-order-changes-now-assist.md).


**Parent Topic:**[Configuring Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/now-assist-for-order-management-configuring.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Creating and adding a scripted extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/impl-scripted-ext-pts-base-code.md)

