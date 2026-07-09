---
title: Create an order from a quote
description: The Sales CRM Quote experience supports creating an order from the current quote.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-create-order-integration.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create an order from a quote

The Sales CRM Quote experience supports creating an order from the current quote.

## Before you begin

Role required: admin

Activate the following plugins:

-   Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).
-   Order Management plugins

## About this task

The create-order-from-quote capability requires a custom integration and a custom event configured in the blueprint. Complete the following phases in order, and then deploy the blueprint.

## Procedure

1.  Create a custom integration.

    For more information about integrations, see [Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md).

    1.  Configure the following integration settings.

        |Setting|Value|
        |-------|-----|
        |HTTP Method|`POST`|
        |Additional Path|`/api/sn_quote_mgmt_adv/v1/quotes/{{txn.id}}/orders`|
        |Timeout|`5000`|
        |Line Item Details to Include|None|
        |Async|Disabled|
        |Headers|Not applicable|

    2.  Leave the **Request Transformation** unconfigured.

        No request transformation is required for this integration.

    3.  For **Connection to Endpoint**, select **serviceNowJwtConnection**.

    4.  Leave the **Response Transformation** unconfigured.

        No response transformation is required for this integration.

2.  Create a custom event.

    1.  In the event properties, set **Event Access** to **Active**.

    2.  Associate the integration you created with the event.

    3.  Add a button to the layout to trigger the event.

    4.  Enable the event button.

    5.  From the **Event** picklist, select the event you created.

    6.  In **Views**, adjust the access to the event for each stage.

    7.  Select **Save**.

        The layout is saved.

    8.  Select **Deploy** on the blueprint.


## Result

When a user selects the create-order button on a completed quote, the integration calls the Order Management create-order API and creates an order from the quote data. Orders associated with the current quote appear in the **Related Lists: Orders** section of the Contextual Side Panel \(CSP\).

## What to do next

After you deploy the blueprint, configure the quote-to-order field mapping to define how quote data maps to the resulting order.

