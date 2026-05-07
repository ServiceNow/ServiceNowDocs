---
title: Create a data interface using JOIN
description: Create a governed data interface that combines rows from two or more source tables using an INNER JOIN and publish it to the Data Catalog. Consumers can access a unified view through a stable schema.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 4
breadcrumb: [Managing data interfaces, Data Products, Workflow Data Fabric]
---

# Create a data interface using JOIN

Create a governed data interface that combines rows from two or more source tables using an INNER JOIN and publish it to the Data Catalog. Consumers can access a unified view through a stable schema.

## Before you begin

Role required: df\_data\_steward

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench**.

2.  Select **Create** &gt; **Create data interface**.

    The data interface wizard opens to the **Basic details** step.

3.  Enter the basic details for the data interface and select **Continue**.

    -   **Interface label**: Enter a name for the data interface. This label identifies the data interface in the Data Catalog.
    -   **Unique name**: Auto-generated from the data interface label.
    -   **Application scope**: Select the scope in which to create the data interface.
4.  On the Select source tables page, select **Add**.

5.  Search for the source table in the Data Catalog and add tables to your selection.

6.  Review the list of tables and select **Continue ![Select source tables page showing three selected tables with Continue button.](../image/wdf-data-interface-join-select-table.png)**.

    The wizard advances to the combination method step.

7.  Select **Join** as the combination method and select **Continue**.

    Under **Define join sequence**, the selected tables are listed in the order they are joined. The first table in the list acts as the primary source. Drag the tables to reorder them before continuing.

8.  Define the join conditions and select **Continue**.

    For each join condition, select a column from one table and the matching column from another table. The columns must have compatible data types. Select **Add matching column** to add more conditions.

    You must define at least one join condition to continue. If any selected table has no join condition, the system prompts you to confirm before proceeding. Columns from unjoined tables are excluded from the output.

    **Note:** This data interface uses INNER JOIN. Only records that have a matching value in all joined tables appear in the output. Records with no match in any joined table are excluded.

    ![Data interface wizard showing join condition configuration with column selection dropdowns and Add matching column button.](../image/wdf-data-interface-join-select_columns.png)

9.  Review the target table column mapping and select **Create table**.

    The **Define target table** step shows the selected columns with their auto-mapped target names and data types. You can adjust column labels and types before creating the table. After you select **Create table**, the source tables, join conditions, and column structure are locked and can't be edited.

    ![Define target table step showing column mapping with editable labels and data types.](../image/wdf-data-interface-join-define-table.png)

    The system creates the data interface table, the underlying Data Fabric Tables, and the database view that represents the JOIN. The wizard advances to the **Connect and verify** step.

10. Connect and verify each source table.

    Repeat the following substeps for each source table.

    1.  Select **Connect and verify** next to the source table.

    2.  Select the connector for your source system from the list of available connections.

    3.  Select **Verify**.

        The table shows a **Verified** status when the connection is confirmed.

    ![Connect and verify step showing source tables with verification status and data interface summary.](../image/wdf-data-interface-join-verify.png)

11. Select **Preview** to review sample data from the data interface.

    The preview shows the top 10 live records from the combined output. Verify the columns and data match what consumers expect before continuing.

12. Review the permissions and select **Continue**.

    For data interfaces built entirely on external source tables, the system automatically configures the required access roles.

    **Note:** If the data interface includes any ServiceNow tables, this step requires a manual permissions request. Copy the email template provided and send it to your Security Administrator. The Security Administrator must add the correct read roles to the composite role generated for the data interface. Select the confirmation check box before continuing.

13. Review the data interface configuration on the **Review and finalize** page and select **Done**.

    ![Review and finalize page displaying table details, source tables, and table structure configuration.](../image/wdf-data-interface-join-review.png)

    The data interface is published and the overview page opens. The data interface is now in a read-only state and can't be edited after publishing.


## Result

The data interface is published and visible in Data Workbench. After the metadata collector runs, the data interface appears in the Data Catalog where consumers can discover and request access to it.

**Important:** There is a delay between publishing a data interface and its appearance in the Data Catalog. The metadata collector must run before the data interface is discoverable. To make the data interface available without waiting for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

## What to do next

To package this data interface into a data product, see [Create a data product](create-data-product-wdf.md).

**Parent Topic:**[Managing data interfaces](../concept/manage-data-interfaces_wdf.md)

