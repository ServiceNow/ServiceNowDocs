---
title: Create a request definition
description: Create a request definition and configure it into an order task to help your agents provide additional order attributes for the order fulfillment from the CSM/FSM configurable workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Create a request definition

Create a request definition and configure it into an order task to help your agents provide additional order attributes for the order fulfillment from the CSM/FSM configurable workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Request Definition Setup** &gt; **Request Definition**.

4.  On the form, fill in the fields.

<table id="table_x4l_sdh_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique identifier for the request definition.

**Note:** You can't modify an ID after the request definition is created.

</td></tr><tr><td>

Task type

</td><td>

Task table that is associated with the service request.

 **Note:** You can create new order tasks only in the Order Task \[sn\_ind\_tmt\_orm\_order\_task\] table.

</td></tr><tr><td>

Name

</td><td>

Name to identify the request definition.

</td></tr><tr><td>

Task Fields

</td><td>

Fields of the Task table.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Repeat Step 2.

7.  Navigate to **Request Definition Setup** &gt; **Request Definition Characteristic**.

<table id="table_ybv_r5w_5sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request definition

</td><td>

 

</td></tr><tr><td>

Specification

</td><td>

Name of the product specification.

</td></tr><tr><td>

Characteristic

</td><td>

Name of the product characteristic that you want to capture the information from the customer order.

</td></tr><tr><td>

UI Visible

</td><td>

Option that designates if the **UI Visible** field appears as true in the Request Definition characteristics table and the characteristic appears in the Order Task form.

 If you clear the check box, the field value appears as false, and the characteristic doesn't appear in the order task form.

</td></tr><tr><td>

Mandatory

</td><td>

Option that designates if the **Mandatory** field appears as true in the Request Definition characteristics table. Your agent must provide the characteristic value in the order task form to close the order task.

 If you clear the check box, the field value appears as false and your agent can close the task without providing any characteristic value in the order task form.

</td></tr><tr><td>

Read-only

</td><td>

Option that designates if the **Read-only** field appears as true in the Request Definition characteristics table, and you can't edit the characteristic value in the order task form.

 If you clear the check box, the field value appears as false in the Request Definition characteristics table and you can edit the characteristic value in the order task form.

</td></tr></tbody>
</table>8.  Select **Save**.


