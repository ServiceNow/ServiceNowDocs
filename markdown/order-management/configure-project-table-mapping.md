---
title: Configure field mappings
description: Configure the CSM table maps to associate fields in order lines, domain orders, and order tasks to projects in Service Portfolio Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Configure field mappings

Configure the CSM table maps to associate fields in order lines, domain orders, and order tasks to projects in Service Portfolio Management.

## Before you begin

Role required: admin

## About this task

Order Management provides Customer Service Management table maps for associating order line items, domain orders, and order tasks to projects and project tasks in SPM. The tables that you configure depend on whether you're using the PPM Standard application to track projects in your organization or the Customer Project Management integration to track customer projects.

-   If you're using PPM, configure the field mapping for these CSM table maps:

    |Table map|Source table|Target table|
    |---------|------------|------------|
    |Order Line Item to Project|Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]|Project \[pm\_project\]|
    |Domain Order to Project Task|Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\]|Project Task \[pm\_project\_task\]|
    |Order Task to Project Task|Order Task \[sn\_ind\_tmt\_orm\_order\_task\]|Project Task \[pm\_project\_task\]|

-   If you're using Customer Project Management, configure the field mapping for these CSM table maps:

    |Table map|Source table|Target table|
    |---------|------------|------------|
    |Order Line Item to Customer Project|Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]|Customer Project \[customer\_project\]|
    |Domain Order to Customer Project Task|Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\]|Customer Project Task \[customer\_project\_task\]|
    |Order Task to Customer Project Task|Order Task \[sn\_ind\_tmt\_orm\_order\_task\]|Customer Project Task \[customer\_project\_task\]|


The source and target tables in each table map are pre-populated.

**Note:** If you installed demo data for Order Management, the field mapping for the **Source Field** and **Target Field** display the values used for demo data. You can use the existing field mapping or change it as needed.

## Procedure

1.  Navigate to **All** and in the filter enter `csm_table_map.list`.

2.  Do one of the following:

    -   If you're using PPM, select the Order Line Item to Project table map.
    -   If you're using Customer Project Management, select the Order Line Item to Customer Project table map.
3.  Go to the **Basic Field Mapping** related list and define a field mapping.

    **Note:** If Order Management demo data is installed, the **Source Field** and **Target Field** values in the Basic Field Mapping related list display the mapping for demo data. You can use the mapping or change it as needed.

<table id="choicetable_i3m_4wt_xxb"><thead><tr><th align="left" id="d126411e284">

Option

</th><th align="left" id="d126411e287">

Steps

</th></tr></thead><tbody><tr><td id="d126411e293">

**Define a new field mapping**

</td><td>

1.  Select **New**.
2.  In the **Source Field**, select an item from the source table.

For example, select an item such as **work\_notes** from the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

3.  In the **Target Field**, select an item from the Project \[pm\_project\] table, such as **Project Name**.
4.  In the **Active**,select **True**.
5.  Select **Submit**.

In this example, the order line **Short Description** is used as the **Project Name** in SPM.

</td></tr><tr><td id="d126411e354">

**Change an existing field mapping**

</td><td>

1.  Select the field mapping record.
2.  In the **Source Field**, select a different item from the Order Line Item source table, as needed.
3.  In the **Target Field**, select a different item from the Project target table, as needed.
4.  Select **Update**.


</td></tr></tbody>
</table>4.  Do one of the following:

    -   If you're using PPM, select the Domain Order to Project table map and repeat Step 3 to define a new field mapping or update an existing mapping.
    -   if you're using Customer Project Management, select the Domain Order to Customer Project table map and repeat Step 3 to define a new field mapping or update an existing mapping.
    For example, you can select the **Short Description** field in the Domain Order source table and map it to the **Short Description** field in the Project Task target table.

5.  Do one of the following:

    -   If you're using PPM, select the Order Task to Project table map if and repeat Step 3 to define a new field mapping or update an existing mapping.
    -   If you're using Customer Project Management, select the Order Task to Customer Project table map and repeat Step 3 to define a new field mapping or update an existing mapping.
    For example, you can select the **Short Description** field in the Order Task source table and map it to the **Short Description** field in the Project Task target table.


## Result

The fields in the Order Management source tables are mapped to the fields in the SPM target table.

Changes made to a synchronized field in order task or domain order will automatically be reflected in the corresponding synchronized field in project task.

