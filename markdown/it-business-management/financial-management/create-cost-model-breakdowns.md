---
title: Create cost model breakdowns
description: Create breakdowns for the cost model statement item providing more clarity by reporting the components that constitute the cost model statement item and the cost associated with each of these components.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Define a cost model statement item, Determine the statement item type, Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create cost model breakdowns

Create breakdowns for the cost model statement item providing more clarity by reporting the components that constitute the cost model statement item and the cost associated with each of these components.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

For example, Electronic Messaging statement item can provide the breakdown details of its component services such as Data Network and Storage. Each of these items provides the associated cost calculated by the set unit cost of each item.

## Procedure

1.  Click **New** in the Cost Model Breakdowns related list to create breakdown records for the cost model statement item that you created.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the cost model breakdown.|
    |Statement item|Header under which the consumption details of the business service appear.|
    |Table|Name of the transactional table the segment refers to.|
    |Unit cost metric|Allocation metric that is used to calculate the unit cost.|
    |Segment accounts filter|Filter applied to data in the segment accounts.|
    |Buckets Filter|Filter applied to buckets that allocate expenses to the segment accounts.|
    |Sub Segment|Segments added as sub segments to allocate expenses to records in the sub segment.|
    |Sub Accounts Filter|Filter applied to data in accounts that fulfill the condition.|

3.  Click **Submit**.


**Parent Topic:**[Define a cost model statement item](define-cost-model-statement-item.md)

