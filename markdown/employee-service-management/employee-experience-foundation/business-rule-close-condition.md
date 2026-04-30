---
title: Configure business rule for close condition
description: Configure the business rule for close condition to auto-import the chats.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Customize Integrations for Employee Experience, Manage, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure business rule for close condition

Configure the business rule for close condition to auto-import the chats.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    In the Advanced tab, update the **Condition** and the **Script** fields.

<table id="table_j3d_hxy_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business rule

</td></tr><tr><td>

Table

</td><td>

Table to which the close condition is to be assigned.

</td></tr><tr><td>

Active

</td><td>

Check this box

</td></tr><tr><td>

Advanced

</td><td>

Check this box

</td></tr><tr><td>

Where to run

</td><td>

-   When: **async**
-   Update: Check this box
-   Filter Conditions: Apply the filter condition of the close condition business rule


</td></tr><tr><td>

Advanced

</td><td>

-   Condition: Copy and paste the value of the condition. Modify the values as required.

    ```
!current.avoid_closing_chat_records && new sn_tcm_collab_hook.MSTeamsImportChatUtils().hasMatchingCloseCondition(current)
    ```

-   Script: Copy and paste the value for the script. Modify the values as required.

    ```
new sn_tcm_collab_hook.MSTeamsImportChatUtils().closeChatStorageRecords(current);
    ```

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Customize IT Service Management integration with ServiceNow](../concept/customize-sn-ms-teams.md)

