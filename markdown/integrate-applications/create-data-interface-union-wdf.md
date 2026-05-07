---
title: Create a data interface using UNION
description: Create a governed data interface that consolidates rows from two or more source tables with compatible schemas using UNION. Publish it to the Data Catalog so consumers can access an aggregated view through a stable schema.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 3
breadcrumb: [Managing data interfaces, Data Products, Workflow Data Fabric]
---

# Create a data interface using UNION

Create a governed data interface that consolidates rows from two or more source tables with compatible schemas using UNION. Publish it to the Data Catalog so consumers can access an aggregated view through a stable schema.

## Before you begin

Before you begin, verify the following:

-   All source tables are discoverable in the Data Catalog.
-   The source tables have compatible schemas. Columns that you map to the same target column must have compatible data types.
-   For tables in external systems, a zero copy connector for each system is configured in Connect Hub. For setup instructions, see the [Zero copy connectors documentation](../../../build/zero-copy-connectors/concept/zero-copy-connectors.md).
-   Role required: df\_data\_steward

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench**.

2.  Select **Create** &gt; **Create data interface**.

    The data interface wizard opens to the **Basic details** step.

3.  Enter the basic details for the data interface and select **Continue**.

    -   **Interface label**: Enter a name for the data interface. This label identifies the interface in the Data Catalog.
    -   **Unique name**: Auto-generated from the data interface label.
    -   **Application scope**: Select the scope in which to create the data interface.
4.  On the Select source tables page, select **Add**.

5.  Search for the source table in the Data Catalog and add tables to your selection. ![Select source tables](../image/wdf-data-interface-union-select-table.png)

6.  Review the list of tables and select **Continue**.

    The wizard advances to the combination method step.

7.  Select **Union** as the combination method and select **Continue**.

8.  Map source columns from each table to the union output schema and select **Continue**.

    The **Union mapping** step shows a row for each output column. For each row:

    -   Select the source column from each table that maps to this output column.
    -   Enter a target column name.
    -   Select the target column type.
    All source columns mapped to the same output column must have compatible data types. The system validates type compatibility and displays errors before you can continue. ![Define union mapping](../image/wdf-data-interface-union-select-columns.png)

9.  Review the target table column mapping and select **Create table**.

    The **Define target table** step shows the output schema based on your union mapping. You can adjust column labels and types before creating the table. After you select **Create table**, the source tables and column structure are locked and can't be edited. ![Define target table](../image/wdf-data-interface-union-define-table.png)

    The system creates the data interface table and the underlying Data Fabric Tables. The wizard advances to the **Connect and verify** step.

10. Connect and verify each source table.

    Repeat the following substeps for each source table.

    1.  Select **Connect and verify** next to the source table.

    2.  Select the connector for your source system from the list of available connections.

    3.  Select **Verify**.

        The table shows a **Verified** status when the connection is verified. ![Connect and verify](../image/wdf-data-interface-union-verify.png)

11. Select **Preview** to review sample data from the data interface.

    The preview shows the top 10 live records from the combined output. Verify the columns and data match what consumers expect before continuing.

12. Review the permissions and select **Continue**.

    For data interfaces built entirely on external source tables, the system automatically configures the required access roles.

    **Note:** If the data interface includes any ServiceNow tables, this step requires a manual permissions request. Copy the email template provided and send it to your Security Administrator. The Security Administrator must add the correct read roles to the composite role generated for the data interface. Select the confirmation check box before continuing.

13. Review the data interface configuration on the **Review and finalize** page and select **Done**.

    The data interface is published and the overview page opens. The data interface is now in a read-only state and cannot be edited after publishing.


## Result

The data interface is published and visible in Data Workbench. After the metadata collector runs, the data interface appears in the Data Catalog where consumers can discover and request access to it.

**Important:** There is a delay between publishing a data interface and its appearance in the Data Catalog. The metadata collector must run before the data interface is discoverable. To make the data interface available without waiting for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

## What to do next

To package this data interface into a data product, see [Create a data product](create-data-product-wdf.md).

**Parent Topic:**[Managing data interfaces](../concept/manage-data-interfaces_wdf.md)

