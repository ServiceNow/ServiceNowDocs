---
title: Drill down within a statement item
description: You can drill down within a statement item to visualize a subset of its data.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Drill down within a statement item

You can drill down within a statement item to visualize a subset of its data.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

Drill down within a statement item to see the entity or the key field that has the data retrieved from the source table. You can also see the basis on which the mapping is done to the particular field that has the relevant data to retrieve. You can also edit and change the drilldown method and use the weighted method. In such a case, the system uses the weighted metric to retrieve data from the source table.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Statement Item Drilldowns**.

2.  Click **New** to create a statement item or click the name of an existing statement item drilldown that you want to edit.

3.  Click the type of statement item that you want to drill down.

4.  Based on the type of statement item drilldown that you select, fill in the relevant form fields.

<table id="table_z1n_pvn_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the statement item drilldown.

</td></tr><tr><td>

Drilldown basis

</td><td>

Lower level access of the item based on the mapped field or the weighted metric method.For more information, see [Allocation metrics](../concept/c_AllocationMetrics.md).

</td></tr><tr><td>

Table

</td><td>

Source table that has the statement item information.

</td></tr><tr><td>

Type

</td><td>

Type of the statement item, determined based on the source from where the information is retrieved.You cannot edit the field as you have already selected the type of statement item drilldown that you want to perform.

</td></tr><tr><td>

Mapping field

</td><td>

Maps to the field in the table which has the drilldown data.

</td></tr><tr><td>

Weighted Metric

</td><td>

Drilldown on calculations based on an aggregate value from a segment.

</td></tr><tr><td>

Cost model

</td><td>

Cost model for which the drilldown can be applied.

</td></tr></tbody>
</table>5.  Click **Submit** to enter a record or **Update** if you have edited an existing record.


## What to do next

After you define the statement items, associate the statement items to the [showback statements](define-showback-statement.md). You can use the showback statement to report consumed services to the business unit head, which displays the detailed service charge lines that the unit has utilized as a part of the business service. For example, Email service is a business service. When a business unit uses the email service, then the service charges for consuming the email services are reported as a showback statement to the business unit head or the department head.

**Parent Topic:**[Financial charging application setup - Legacy](../concept/financial-reporting-appln-setup.md)

