---
title: Enable order creation from a quote
description: Add the Create Order event to a blueprint layout so that users can create an order from a quote in the CPQ Quote experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-create-order-integration.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable order creation from a quote

Add the **Create Order** event to a blueprint layout so that users can create an order from a quote in the CPQ Quote experience.

## Before you begin

Role required: admin

Activate the following plugins:

-   Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).
-   Order Management plugins

Configure the following dependencies:

-   Enable the `transaction.oneQuoting.orders.enabled` tenant setting.
-   Configure the **serviceNowJwtConnection** connection in **CPQ Administration** &gt; **Utilities** &gt; **Connection**.

## About this task

The integration and event that create an order from a quote are seeded in your blueprints. To make the capability available to users, add the seeded **Create Order** event to the layout, set its access, and then deploy the blueprint.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction**.

2.  Navigate to **Events**, select the **Create Order** event, set **Event Access** to **Active**, and save the event.

3.  Add the **Create Order** event to the layout.

    1.  Add a button to the layout.

    2.  Open the button properties.

    3.  Toggle the **Event Button** property to **Active**.

    4.  From the **Event** picklist, select the **Create Order** event.

    5.  Save the button properties.

    6.  Save the layout.

4.  In **Views**, adjust the access to the **Create Order** event for each stage.

5.  Select **Deploy** on the blueprint.

    **Create Order** is enabled on the quote, and the **Create Order** button appears on the Quote user interface.


## Result

The **Create Order** button is available on the quote layout for the stages you configured. Users can now create an order from a quote.

## What to do next

After you deploy the blueprint, configure the quote-to-order field mapping to define how quote data maps to the resulting order.

**Parent Topic:**[Configuring ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-crm-tm-quoting-configure.md)

**Related topics**  


[Create an order from a quote line item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management-create-order-quote-line.md)

