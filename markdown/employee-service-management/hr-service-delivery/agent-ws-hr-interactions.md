---
title: Using interactions in HR Service Delivery Agent Workspace
description: Use interaction records to create an HR case or reference employee information to decide to create a case or request from different types of employee communications.You can create interaction records from the HR Service Delivery Agent Workspace form.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Using interactions in HR Service Delivery Agent Workspace

Use interaction records to create an HR case or reference employee information to decide to create a case or request from different types of employee communications.

An interaction is a request for assistance made through chat, phone, or in person. You can route interactions by skill, group, or directly to an HR agent.

You can also create an interaction for simple requests where you decide you might not want to create an HR case or associated tasks.

Interaction records are automatically created when you are using agent chat.

**Note:** Agent Assist is available for interactions.

For more information on interactions, see [Interaction records in Agent Workspace](https://www.servicenow.com/docs/access?context=interaction-message-agent-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Create interactions in HR Service Delivery Agent Workspace

You can create interaction records from the HR Service Delivery Agent Workspace form.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  To create an interaction, select the ![Create case icon](../image/IconCreateRecordMenu.png) Create case icon.

3.  Select **Interaction**.

    ![HR Agent Workspace - Interaction](../reference/images/agent-ws-hr-interaction.png)

4.  In the details section, enter information about the interaction.

    ![HR Agent WS - New interaction](../reference/images/agent-ws-hr-new-interaction.png)

5.  Fill in the fields.

<table id="table_m1m_n1b_5jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Every interaction record defaults to the Details form, showing initial interaction record information.

</td></tr><tr><td>

Number

</td><td>

The number assigned to the interaction record.

</td></tr><tr><td>

Type

</td><td>

The type of communication responsible for the interaction record. The values are:-   None
-   Chat


</td></tr><tr><td>

State

</td><td>

The status of the interaction record.-   New
-   Work in Progress
-   Closed Complete
-   Closed Abandoned


</td></tr><tr><td>

Opened for

</td><td>

The employee the interaction is about.

</td></tr><tr><td>

Assigned to

</td><td>

The HR agent responsible for the interaction.

</td></tr><tr><td>

Short description

</td><td>

A short description about the interaction.

</td></tr><tr><td>

Work notes

</td><td>

Information specific to the interaction and can help other HR agents. Work notes are not visible to the Opened for person.

</td></tr></tbody>
</table>6.  Select **Save**.

    |Tab|Description|
    |---|-----------|
    |Related Tasks|Any tasks or cases opened from the interaction, for example, a new incident or new case.|
    |User's Tasks|Incidents related to the interaction.|
    |User's Interactions|Logs all interactions tied to each specific user.|
    |Cases opened for "Opened for"|Shows all HR cases related to the Opened for person.|

7.  You can select from the following: ![HR Agent Workspace - more icon](../reference/images/EllipsisIcon.png) more icon.

    ![HR Agent Workspace - Interaction buttons](../reference/images/agent-ws-hr-interaction-buttons.png)

8.  Select **Create HR Case** to create a case based on the interaction.

    **Create Incident** is part of demo data and not available to HR Service Delivery Agent Workspace.

9.  Select the ![HR Agent Workspace - more icon](../reference/images/EllipsisIcon.png) more icon to display additional actions you can take.

<table id="table_w54_1nb_5jb"><thead><tr><th>

Choice

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Standard Change

</td><td>

Part of demo data and not available to HR Service Delivery Agent Workspace.

</td></tr><tr><td>

Associate Record

</td><td>

Use to associate an interaction to an HR case. After linking, the interaction appears under the **Interactions** tab for an HR case. Select **Task** under **Record Type** then optionally select a task record. You can also associate an interaction record that contains a knowledge article. Under **Record Type**, select **Knowledge** then select a knowledge article.

</td></tr><tr><td>

Delete

</td><td>

Select to delete the interaction record.

</td></tr></tbody>
</table>10. Select **Save** to save work entered for an interaction.

11. To view interactions, select the **Interactions for Subject Person** tab on the child tab.

    ![HR Agent Workspace - Interaction tab](../reference/images/agent-ws-hr-interact-tab.png)


