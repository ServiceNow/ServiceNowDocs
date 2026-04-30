---
title: Add joins between ERP tables
description: Link multiple ERP \(Enterprise Resource Planning\) tables from the system of record to build an ERP model in Zero Copy Connector for ERP using table joins.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, join, table, read, operation]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Add joins between ERP tables

Link multiple ERP \(Enterprise Resource Planning\) tables from the system of record to build an ERP model in Zero Copy Connector for ERP using table joins.

## Before you begin

Table joins require a read operation that uses table read entities. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

When you add table joins, the parent table is the first table listed on the **Manage entities** tab of the ERP model manager page. Child tables pull information from the parent table.

**Note:**

-   If you have more than one table for an operation, you must join the tables.
-   You can create table joins only for table read operations, not for operations that use a BAPI \(Business Application Programming Interface\).

Role required: sn\_erp\_integration.erp\_admin

## About this task

Table joins link different tables through shared fields. Joins enable you to access data from multiple tables based on logical relationships between them. The relationship can be conditional, which you specify using join conditions. Use inner joins or outer joins. An inner join returns records that have matching values in both tables. Outer joins combine left and right join results to return all rows with matches or NULLS.

Join fields defines the common attribute or key used to connect records in a child table with their corresponding parent records.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model that you want to add a join to.

4.  Select the **Manage model** button.

5.  Select the **Read** operation that you're adding the table join to.

6.  Add the tables to join as **Table read** operation entities if they haven't yet been added to the model.

    For more information, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

    ![Multiple tables are joined.](../image/erpc-tables-with-joins-ys2.png)

7.  Rearrange the tables on the **Manage entities** tab to place the parent table for the join as the first table listed on the ERP model manager page.

    **Important:** Reordering deletes any existing table joins for the reordered entities.

    1.  Select the **Rearrange order** button.

    2.  Drag the tables to the order that you want, with the parent table as the first table listed on the page.

    3.  Select the **Confirm reorder** button.

8.  Select the **Specify inputs** tab, which is where you update input parameters to specify table join as a parameter.

    The input parameters for each table appear.

9.  Create a table join parameter.

    1.  In the **Output parameter\(s\)** section, identify the parameter that will be the parent join field and note its name.

    2.  Add a new mapped field row in the table by selecting the add \(+\) icon.

    3.  Enter or select the parent join **Field name** in the new field row.

    4.  Select **Join** from the **Type** field.

        The value in the child table **Mapped value** field updates automatically with the joined field name.

        For example, in the SAP Material Stock model, you can specify **Material** as the parent field in the **Field name** field, and join it to the material ID by entering `mard_material_matnr` in the parent **Mapped value** field.

    5.  Select **Save**.

    ![Specify inputs page showing all tables and fields.](../image/erpc-join-parameters.png "Table join fields")

10. Add or update any output parameters as needed in the Output parameters section.

    The joined parameter that you added to as an input is automatically added to the **Choose output** tab.

    For more information, see [Choose output parameters for a model](erp-canvas-manage-outputs.md).


## Result

After you're done creating table joins, you can specify where the returned ERP data goes, and build flows that retrieve and output the data. For more information, see the following topics:

-   [Specifying where the ERP system data is saved](../concept/erpc-call-response-data.md)
-   [Building flows to read or update the ERP system](../concept/erp-canvas-build-flow-operation.md)

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

