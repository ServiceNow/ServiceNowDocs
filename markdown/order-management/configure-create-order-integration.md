---
title: Enable order creation from a quote
description: Add the Create Order event to a blueprint layout so that users can create an order from a quote in the CPQ Quote experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-create-order-integration.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable order creation from a quote

Add the **Create Order** event to a blueprint layout so that users can create an order from a quote in the CPQ Quote experience.

## Before you begin

Role required: admin

Activate the following plugins:

-   Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).
-   Order Management plugins

## About this task

The integration and event that create an order from a quote are seeded in your blueprints. To make the capability available to users, add the seeded **Create Order** event to the layout, set its access, and then deploy the blueprint.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** and open the blueprint.

2.  Add the **Create Order** event to the layout.

3.  Set **Event Access** to **Active** in the event properties.

4.  Add a button to the layout to trigger the event.

5.  Enable the event button.

6.  From the **Event** picklist, select the **Create Order** event.

7.  In **Views**, adjust the access to the event for each stage.

8.  Select **Save**.

    The layout is saved.

9.  Select **Deploy** on the blueprint.

    The **Create Order** button appears on the Quote user interface.


## Result

The **Create Order** button is available on the quote layout for the stages you configured. Users can now create an order from a quote.

## What to do next

After you deploy the blueprint, configure the quote-to-order field mapping to define how quote data maps to the resulting order.

**Related topics**  


[Create an order from a quote line item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management-create-order-quote-line.md)

