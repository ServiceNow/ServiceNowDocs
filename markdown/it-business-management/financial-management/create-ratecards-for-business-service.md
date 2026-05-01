---
title: Create ratecards to fix price for your business service
description: Create a ratecard that lists prices for your business service or business service components. As a service owner, you can create a ratecard for a statement item, which represents the business service that you own. The ratecard is based on the pricing policy method attached to the statement item for a fiscal period.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Service charging - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create ratecards to fix price for your business service

Create a ratecard that lists prices for your business service or business service components. As a service owner, you can create a ratecard for a statement item, which represents the business service that you own. The ratecard is based on the pricing policy method attached to the statement item for a fiscal period.

## Before you begin

Role required: service\_charging\_analyst, service\_charging\_owner

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

The ratecard for a fiscal period defaults to the next fiscal period if you do not set a new pricing policy for the statement item before the charges of the next fiscal period are published.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Service Charging** &gt; **Service Charge Rate Cards**.

2.  Click **New** to create a service charge price rate card or click a record that you want to edit.

3.  Fill in the form fields.

<table id="table_ky4_r25_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Statement item

</td><td>

Select the statement item for which you want to create a rate card.

</td></tr><tr><td>

Item table name

</td><td>

-   If it is a service catalog statement item, then the item table name is catalog item.
-   If it is a cost model statement item, then the item table name is the transaction table name of the segment.
-   If it is a consumption statement item, then the item table name is the consumption table.


</td></tr><tr><td>

Service charging type

</td><td>

Defaults from the statement item. It can be percentage based or unit price based.

</td></tr><tr><td>

Fiscal period

</td><td>

Period for which the rate card is valid.

</td></tr><tr><td>

Statement item breakdown

</td><td>

The breakdown line details of the statement item.

</td></tr><tr><td>

Item name

</td><td>

Refers to a record in the item table.

</td></tr><tr><td>

Percentage

</td><td>

A percentage of the average unit cost, which you can set at the statement item level, statement item breakdown level, or item level of the consumption based statement item or catalog based statement item; or, at the account level of the cost model based statement item.

</td></tr><tr><td>

Unit price

</td><td>

Set the unit price only for the item level pricing policy. The unit price represents the price displayed to the business users.

</td></tr><tr><td>

Short description

</td><td>

Meaningful short description for the rate card.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## What to do next

As a service charging analyst, you can [view all the showback statements](view-all-showback-statements.md) that are generated. The showback users can view the showback statements only when you publish the showback statements that you have generated.

**Parent Topic:**[Service charging - Legacy](../concept/service-charging.md)

