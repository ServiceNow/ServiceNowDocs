---
title: Set a recurring price
description: A catalog item can have a recurring price in addition to an initial price.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set a recurring price

A catalog item can have a recurring price in addition to an initial price.

## Before you begin

Role required: admin

## About this task

The price and the recurring frequency are set on the catalog item record. After the price and frequency are set, the recurring price appears in the catalog, catalog search results, catalog page for the item, shopping cart, and order summary screen.

For example, a subscription to a mobile phone contract could cost $500.00, with a $30.00 monthly recurring price.

![Order summary screen](../image/SC_SetRecurringPrice-1.png)

If multiple items with the same recurring price frequency are placed in the shopping cart, they are grouped. The grouping makes it easier to view how much items cost for each frequency \(for example, weekly, monthly, and annually\). If the shopping cart contains items with and without recurring costs, they are grouped separately.

If multiple items with the same recurring price frequency are placed in the shopping cart, they are grouped. The grouping makes it easier to view how much items cost for each frequency \(for example, weekly, monthly, and annually\). If the shopping cart contains items with and without recurring costs, they are grouped separately.

![Shopping card](../image/SC_SetRecurringPrice-2.png)

On a request record, recurring prices are grouped by frequency and shown in the **Recurring Prices** related list. In the example below, two items each have a monthly recurring cost of $100.00 and their prices are grouped as a single record of $200.00 monthly. Another item with an annual recurring cost of $500.00 is listed as a separate record.

![Screenshot for recurring price](../image/RecurringPriceRollup.png)

If a request record contains multiple items with the same recurring frequency, click the arrow next to the corresponding recurring prices record to view details.

**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

