---
title: Add a matching column to the pre-import table
description: Add a column to the SG-OT Excel Pre Import table that matches the custom column on the staging table, giving the imported value a source field for mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/add-column-pre-import-table.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 1
keywords: [pre-import table, custom column, dictionary entry]
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a matching column to the pre-import table

Add a column to the SG-OT Excel Pre Import table that matches the custom column on the staging table, giving the imported value a source field for mapping.

## Before you begin

A custom column must be added to the staging table before completing this task. For more information, see [Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md).

Role required: ot\_excel\_import\_user

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Find and select the **SG-OT Excel Pre Import** table record.

    **Tip:** Use the filter conditions to help you locate the SG-OT Excel Pre Import table record. For example, you can set a filter of **\[Label\] \[contains\] \[SG-OT Excel\]**.

3.  On the **Columns** tab, select **New**.

4.  In the **Type** field, select **String**.

5.  In the **Column label** and **Max length** fields, enter the same label for the column you added in the SG OT Excel Staging table.

    The **Column name** field value is generated from the column label.

6.  Select **Submit**.


## What to do next

Map the source field on the pre-import table to the target field on the staging table in the table transform map. For more information, see [Map the custom field in the transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/map-custom-field-transform.md).

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

