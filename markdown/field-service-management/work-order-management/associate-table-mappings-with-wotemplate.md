---
title: Enable work order template to fetch data from the source table
description: Enable work order template to identify the source of work order and then map data from that source table to the work order fields. This can be achieved by associating a table map with the work order template.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure data mapping, Template Management, Work orders, Set up work orders and tasks, Configure, Field Service Management]
---

# Enable work order template to fetch data from the source table

Enable work order template to identify the source of work order and then map data from that source table to the work order fields. This can be achieved by associating a table map with the work order template.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Template Management** &gt; **Attribute Mapping**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table map|Name of the mapping stored in the CSM table map.|
    |Order model|Name of the work order template for which you want to use the table-mapping configurations.|

4.  Select **Submit**.


## Result

The work order template is enabled to copy data from the source table to the corresponding work order fields based on the associated table mapping. You can find this newly created attribute mapping in the Template Attribute Mapping related list in the work order template form.

