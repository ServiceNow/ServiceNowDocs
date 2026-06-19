---
title: Add the Update sequence task activity to a sequence
description: Dynamically update the sequence task records based on predefined configuration using the Update sequence task activity while designing customer engagement sequences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/add-update-sequence-task-activity.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-12"
reading_time_minutes: 2
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Add the Update sequence task activity to a sequence

Dynamically update the sequence task records based on predefined configuration using the Update sequence task activity while designing customer engagement sequences.

## Before you begin

The delegated developer roles must be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/grant-delegated-developer-permissions.md).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, then you need the playbook.admin or pd\_author role to create sequences.

## About this task

Add the Update sequence task activity with other activities in a stage or in its own stage to update the sequence task record after the previous activity or stage has run. For example, the agent accessing the workflow could skip unnecessary call attempts when a lead is successfully contacted and move directly to the tear down stage after updating the record on the parent table. This example is demonstrated in the sample Lead nurturing tele-sales sequence available with the demo data.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  In the sequence diagram, create a stage to add the activity.

    For more information, see .

6.  Within the stage, select the Add icon \[Omitted image "circle-plus-fill-24.svg"\] Alt text:.

7.  Open the activity picker by selecting the Add an activity icon \[Omitted image "square-outline-24.svg"\] Alt text:.

8.  On the Add activity screen, search for and select **Customer Engagement Sequences** &gt; **Update sequence task**.

9.  On the **Details** tab, enter a name for the activity in the **Label** field.

10. On the **Automation** tab, use the data pill picker to establish a connection between the parent table and columns to the fields listed in the following table.

<table id="table_scy_fbk_mhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

The record you want to update on the parent table. For example, to update the record on the Lead \[sn\_lead\_mgmt\_core\_lead\] table, you would select **Lead**.

</td></tr><tr><td>

Table

</td><td>

This field is automatically set to the name of the parent table.

</td></tr><tr><td>

Fields

</td><td>

Field in the parent table you want to update. For example, to mark a lead as contacted, you would select **Stage** from the Fields drop-down list and set its value to 200\_contacted.

</td></tr></tbody>
</table>11. Select **Save and close**.


**Parent Topic:**[Create a customer engagement sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/create-customer-engagement-sequence.md)

