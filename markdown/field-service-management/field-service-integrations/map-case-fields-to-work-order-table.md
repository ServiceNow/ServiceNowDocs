---
title: Map case fields with work order table
description: Define the fields you want to map between the case and the target work order table fields that you have already configured. This configuration automatically copies the values of mapped fields from the case to the work order when creating a work order from the case.
locale: en-US
release: yokohama
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration with Customer Service Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Map case fields with work order table

Define the fields you want to map between the case and the target work order table fields that you have already configured. This configuration automatically copies the values of mapped fields from the case to the work order when creating a work order from the case.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Case Work Order Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  <table id="table_mqn_x15_rzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping Name

</td><td>

The table map name.

</td></tr><tr><td>

API Name

</td><td>

Read only. The API for this table map.

</td></tr><tr><td>

Source Table

</td><td>

The source table for the map, such as case.

</td></tr><tr><td>

Active

</td><td>

Enables the mapping from the source to the target tables.

</td></tr><tr><td>

Application

</td><td>

Read only. The application for this table map.

</td></tr><tr><td>

Advanced Field Mapping

</td><td>

Enables advanced field mapping.

</td></tr><tr><td>

Target Table

</td><td>

The target table for the map, such as work order \[wm\_order\].

</td></tr><tr><td>

Use Advanced Condition

</td><td>

Enables advanced condition mapping, which uses a script. If enabled, add a script in the **Advanced Condition** field.

</td></tr><tr><td>

Advanced Condition

</td><td>

The script to use if the **Use Advanced Condition** field is enabled.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions that apply to the table map.

</td></tr><tr><td>

Order

</td><td>

Order of priority for processing multiple matching map definitions simultaneously to resolve dependencies.-   If there is only one matching table map, the system uses that map.
-   If there are multiple matching table maps with the same order, the system uses the map with the older created date.
-   If there are multiple matching table maps with different orders, the system uses the map with the highest order.


</td></tr></tbody>
</table>5.  Click **Submit**.

    The table map is created by mapping the selected source table to the work order table.

6.  Create field mapping to copy information from the case field to an appropriate field in the work order.

    1.  From the CSM Table Map list, select the table map created in step 2.

    2.  In the Basic Field Mapping form section, click **New**.

    3.  Select a **Source Field** and a **Target Field**.

    4.  Enable the **Active** check box.

    5.  Enter a number in the Order field.

    6.  Click **Submit**.

    7.  Repeat steps b through f for each field to be mapped.

7.  Click **Update** on the CSM Table Map form.


## Result

The mapping between the source and target tables is complete and ready to copy information from the case field to the corresponding field in the work order.

**Parent Topic:**[Integration with Customer Service Management](../concept/customer-service-integration.md)

