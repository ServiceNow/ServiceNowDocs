---
title: Create a subject criteria input
description: Create a subject criteria input to define criteria that your data filtration rules filter against.
locale: en-US
release: yokohama
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating subject criteria, Data filtration\(Legacy\), Access Management]
---

# Create a subject criteria input

Create a subject criteria input to define criteria that your data filtration rules filter against.

## Before you begin

Role required: security\_admin

## Procedure

1.  On your subject criteria record, open the **Criteria Inputs** tab.

2.  In the **Criteria Inputs** list, click **New**.

3.  Select the policy Input for the criteria you want to create.

    |Policy input|Description|
    |------------|-----------|
    |IP filter criteria|Create a policy input based on IP address|
    |Role filter criteria|Create a policy input based on use role|
    |Group filter criteria|Create a policy input based on user group|

    A **IP Filter Criteria**, **Role Filter Criteria**, or **Group Filter Criteria** form displays, depending on your selection in this step.

4.  In the filter criteria form, fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the filter criteria|
    |Application|Scoped application for the subject criteria. This field is read-only, and automatically populates with the current scoped application.|
    |Description|Description of the filter criteria|

5.  Below the form fields are tabs used to define the IP addresses, groups, or roles for the filter criteria inputs.

<table id="table_avs_1md_x4b"><thead><tr><th>

Policy input type

</th><th>

Description

</th><th>

Creation

</th></tr></thead><tbody><tr><td>

IP filter criteria

</td><td>

User IP filter criteria to create a range or subnet of IP addresses. Your subject criteria can then compare with the user's IP address against this range or subnet.

</td><td>

Use the **IP Range** or **Subnet \(CIDR\)** to define IP addresses for your input.-   **IP Range**

In the **IP Ranges** list, double-click **Insert a new row**, and enter a starting IP address in the **Start IP**. Then, press the tab key, and enter an ending IP address in the **End IP** field. Finally, press Enter to save the list entry.

-   **Subnet \(CIDR\)**

In the **Subnets** list, double-click **Insert a new row**, and enter a network IP in the **Network IP** field. Then, press the tab key, and enter a netmask in the **Netmask** field. Finally, press Enter to save the list entry.

 **Note:** Scheduled jobs being triggered by a scheduler are not intended to have data filtered using a network criteria since they do not have the context of the requesting client IP. A more appropriate type of filtration may be the Role/Group subject condition.

</td></tr><tr><td>

Role filter criteria

</td><td>

Use role filter criteria to create a selection of roles. Your subject criteria can then compare with the user's assigned roles against this selection.

</td><td>

Use the condition builder in the **Condition field** to select roles for your input.

</td></tr><tr><td>

Group filter criteria

</td><td>

Use group filter criteria to create a selection of user groups. Your subject criteria can then compare with the user's assigned groups against this selection.

</td><td>

In the **Groups for criteria** table, double-click **Insert a new row**, and select a user group. Press Enter or click the green check mark icon to save the group.

 Click the **Insert a new row** text below the first entry to create additional entries.

</td></tr></tbody>
</table>6.  After defining your input, click **Submit**.

    **Note:** In addition to creating criteria inputs for your subject criteria, you can also add existing ones. Click **Edit** in the **Criteria Inputs** tab, and select from any existing input.


