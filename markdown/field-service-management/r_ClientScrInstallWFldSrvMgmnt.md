---
title: Client scripts installed with Field Service Management
description: Client scripts are added with Field Service Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed, Reference, Field Service Management]
---

# Client scripts installed with Field Service Management

Client scripts are added with Field Service Management.

<table id="table_ClientScripts"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calculate Window End

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Automatically populates Window End Date based on the latest SLA breach date.Default value: Inactive

</td></tr><tr><td>

Populate Short Description

</td><td>

Expense Line\[fm\_expense\_line\]

</td><td>

Automatically populates the short description of expense lines with the work order short description when expense lines are manually created from work orders. Cost Management must be activated.

</td></tr><tr><td>

Hide End Date Fields

</td><td>

Work Order\[wm\_order\]

</td><td>

Hide estimated\_end when the request-driven process is used and hide expected\_end when task-driven is used.

</td></tr><tr><td>

Update UI on load and model change

</td><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>



</td></tr><tr><td>

Show/Hide Task Map section

</td><td>

Work Order Task\[wm\_task\]

</td><td>

This section of the map displays the location of the task and also shows the agents in the vicinity. This section needs to be visible only when the task is in the **Pending Dispatch** state.

</td></tr><tr><td>

Part requirement activation

</td><td>

Work Order\[wm\_order\]

</td><td>

Hides part requirements on the Work Order form if part requirements are not activated in Field Service Configuration.

</td></tr><tr><td>

Update Model and Quantity based on Asset

</td><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>



</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Field Service Management](r_InstalledWithFSM.md)

