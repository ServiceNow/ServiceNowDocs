---
title: Configure order enrichment flows using Decision Tables
description: Associate enrichment subflows with the product or service specifications by using the Order Enrichment Flow Policy in Decision Tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configure order enrichment flows using Decision Tables

Associate enrichment subflows with the product or service specifications by using the Order Enrichment Flow Policy in Decision Tables.

## Before you begin

Role required: process admin

## About this task

Add rows to the Order Enrichment Flow Policy decision table to specify which products should go through enrichment. Add the product enrichment subflow to a new row in this table with the appropriate conditions​​. Conditions can be a combination of product specification and offering information.

## Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

2.  Select the **Order Enrichment Flow Policy** decision table.

3.  In the **Specification** column of the conditions section, select the order line item to set a condition.

4.  Select the product offering in the **Offering** column.

    ![Order Enrichment Flow Policy decision table for configuring the order enrichment process.](../image/order-mgt-enrichment-decision-table.png "Decision table for order enrichment process")

5.  Select **Save**.


## Result

A list of subflows appear in the results section. These sub flows create the enrichment tasks for an order line item during the enrichment process. For more information, see Decision Builder user interface.

**Parent Topic:**[Configuring Order Management](../concept/order-mgt-configuring.md)

