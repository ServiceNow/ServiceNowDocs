---
title: Create a data interface from a single table
description: Create a governed data interface on a single source table and publish it to the Data Catalog so consumers can access the data through a stable schema.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 3
breadcrumb: [Managing data interfaces, Data Products, Workflow Data Fabric]
---

# Create a data interface from a single table

Create a governed data interface on a single source table and publish it to the Data Catalog so consumers can access the data through a stable schema.

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

5.  Search for the source table in the Data Catalog and add tables to your selection. ![Select table](../image/wdf-data-interface-single-select-table.png)

6.  Review the list of tables and select **Continue**.

    The wizard advances to the combination method step. Because you selected one table, the system confirms that no combination method is needed and proceeds to column selection.

7.  Select the columns to include in the data interface and select **Continue**.

    Select only the columns that consumers require. Limiting columns makes the data interface easier to understand in the Data Catalog and reduces the impact of future schema changes in the source table.

    ![Select columns](../image/wdf-data-interface-single-select-columns.png)

8.  Review the target table column mapping and select **Create table**.

    The **Define target table** step shows the selected columns with their auto-mapped target names and data types. You can adjust column labels and types before creating the table. After you select **Create table**, the source table and column structure are locked and can't be edited.

    ![Define target table](../image/wdf-data-interface-single-define-table.png)

    The system creates the data interface table and the underlying Data Fabric Table. The wizard advances to the **Connect and verify** step.

9.  Connect and verify the source table.

    1.  Select **Connect and verify** next to the source table.

    2.  Select the connector for your source system from the list of available connections.

    3.  Select **Verify**.

        The table shows a **Verified** status when the connection is confirmed. ![Connect and verify](../image/wdf-data-interface-single-verify.png)

10. Select **Preview** to review sample data from the data interface.

    The preview shows the top 10 live records from the combined output. Verify the columns and data match what consumers expect before continuing.

11. Review the permissions and select **Continue**.

    For data interfaces built entirely on external source tables, the system automatically configures the required access roles.

    **Note:** If the data interface includes any ServiceNow tables, this step requires a manual permissions request. Copy the email template provided and send it to your Security Administrator. The Security Administrator must add the correct read roles to the composite role generated for the data interface. Select the confirmation check box before continuing.

12. Review the data interface configuration on the **Review and finalize** page and select **Done**. ![Review the data interface](../image/wdf-data-interface-single-review.png)

    The data interface is published and the overview page opens. The data interface is now in a read-only state and cannot be edited after publishing.


## Result

The data interface is published and visible in Data Workbench. After the metadata collector runs, the data interface appears in the Data Catalog where consumers can discover and request access to it.

**Important:** There is a delay between publishing a data interface and its appearance in the Data Catalog. The metadata collector must run before the data interface is discoverable. To make the data interface available without waiting for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

## What to do next

To package this data interface into a data product, see [Create a data product](create-data-product-wdf.md).

**Parent Topic:**[Managing data interfaces](../concept/manage-data-interfaces_wdf.md)

