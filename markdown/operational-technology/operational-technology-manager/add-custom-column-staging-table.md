---
title: Add a custom column to the staging table
description: Add a custom column to the SG OT Excel Stagings table to store an additional value imported from the Microsoft Excel spreadsheet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/add-custom-column-staging-table.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 2
keywords: [staging table, custom column, dictionary entry]
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a custom column to the staging table

Add a custom column to the SG OT Excel Stagings table to store an additional value imported from the Microsoft Excel spreadsheet.

## Before you begin

Role required: ot\_excel\_import\_user

## Procedure

1.  Create a column in the SG OT Excel Staging table.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Find and select the **SG OT Excel Staging** table record.

        **Tip:** Use the filter conditions to help you locate the SG OT Excel Staging table record. For example, you can set a filter of **\[Label\] \[contains\] \[SG OT Excel\]**.

    3.  On the **Columns** tab, select **New**.

    4.  In the **Type** field, select **String**.

    5.  In the **Column label** field, enter a label for the new column.

        The **Column name** field value is generated from the column label.

    6.  In the **Max length** field, enter the maximum number of characters for the column.

        For example, `100`.

    7.  Select **Submit**.

    After refreshing the SG OT Excel Staging table record, the new column appears under the **Columns** tab.

2.  Add the column to the SG OT Excel Stagings table.

    1.  Open the **SG OT Excel Stagings** table by navigating to **All**.

    2.  In the **Filter** field, add `sg_ot_excel_staging.list` then press the Enter key.

    3.  Select the **Personalize List** \[Omitted image "gear.png"\] Alt text: icon.

    4.  Under **Available**, locate and select the column you created.

    5.  Use the **Add** arrow to add the column to **Selected**.

    6.  Select **OK**.


## Result

The column you created is now available in the SG OT Excel Stagings table.

## What to do next

Add a matching column to the SG-OT Excel Staging Import \[sn\_otsm\_sgc\_sg\_ot\_excel\_pre\_import\] table so the imported value has a source field to map from. For more information, see [Add a matching column to the pre-import table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/add-column-pre-import-table.md).

-   **[Add a matching column to the pre-import table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/add-column-pre-import-table.md)**  
Add a column to the SG-OT Excel Pre Import table that matches the custom column on the staging table, giving the imported value a source field for mapping.
-   **[Map the custom field in the transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/map-custom-field-transform.md)**  
Map the custom source field on the pre-import table to the target field on the staging table so the imported value transforms into the correct staging column.

**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/configuring-service-graph-connector-for-excel.md)

