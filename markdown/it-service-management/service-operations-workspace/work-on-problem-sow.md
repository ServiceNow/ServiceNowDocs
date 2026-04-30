---
title: Work on a problem in Service Operations Workspace
description: Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Problem Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on a problem in Service Operations Workspace

Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.

## Before you begin

If you aren't using the base problem life cycle, you will continue to use the classic experience to manage problems or problem tasks through their life cycle. From the problem record page, select **Continue problem** to be redirected to the ServiceNow AI Platform user interface where you can make state transitions. For information about state transitions of a problem, see [Life cycle of a problem](../../problem-management/concept/understanding-state-mgmt-transitions.md).

The base problem life cycle is included with the Problem Management  Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin. Use the Problem Management Migration Utility [store application](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d03b7539dbbb3300f21e7ffdbf9619a8) to enable this plugin and migrate your records to the base problem life cycle.

Role required: itil, problem\_coordinator or higher \(for managing the life cycle of the problem\), problem\_admin \(for deleting the problem\)

## Procedure

1.  Open a problem.

    For information about creating a problem in Service Operations Workspace, see [Create a problem in Service Operations Workspace](create-problem-sow.md).

2.  Perform any of the following actions on the problem record page.

<table id="choicetable_ptk_vnq_cbc"><thead><tr><th align="left" id="d344212e93">

Option

</th><th align="left" id="d344212e96">

Description

</th></tr></thead><tbody><tr><td id="d344212e102">

**Create a problem task associated with the problem**

</td><td>

Select **Create problem task**, or select **New** from the **Problem Tasks** tab. For more information about creating a problem task, see [Create a problem task in Service Operations Workspace](create-problem-task-sow.md).

</td></tr><tr><td id="d344212e129">

**Assess a problem**

</td><td>

Select **Assess** and fill the mandatory fields.

</td></tr><tr><td id="d344212e141">

**Confirm a problem**

</td><td>

Select **Confirm** to move the problem from the **Assess** state to the **Root Cause Analysis** state.

</td></tr><tr><td id="d344212e159">

**Investigate the root cause of a problem**

</td><td>

-   If you are the subject matter expert for this problem area, carry out the investigation and select **Fix** to provide the cause notes and fix notes.
-   If you are not the subject matter expert and you want help from another team to investigate, create a problem task.

For more information about creating a problem task, see [Create a problem task in Service Operations Workspace](create-problem-task-sow.md).

</td></tr><tr><td id="d344212e190">

**Create a change request from the problem**

</td><td>

From the drop-down list next to **Create problem task**, select **Create change request**, or select **New** from the **Fix Tasks** tab.For information about creating a change request, see [Create a change request in Service Operations Workspace](create-change-sow.md).

</td></tr><tr><td id="d344212e220">

**Create an outage associated with the problem**

</td><td>

From the drop-down list next to **Create problem task**, select **Create outage**.

</td></tr><tr><td id="d344212e235">

**Create a known error article**

</td><td>

From the drop-down list next to **Create problem task**, select **Create known error article**.Known error articles document the root cause and the workaround of the problem. For a description of the field values, see [Known error article form](../../problem-management/reference/known-error-article-form.md).

</td></tr><tr><td id="d344212e260">

**Assign the problem to yourself**

</td><td>

Select **Assign to me**.

</td></tr><tr><td id="d344212e272">

**Mark a problem as a duplicate of an existing problem**

</td><td>

From the drop-down list next to **Cancel**, select **Mark duplicate** and fill the mandatory fields.

</td></tr><tr><td id="d344212e287">

**Cancel a problem**

</td><td>

Select **Cancel problem** and fill the mandatory fields.

</td></tr><tr><td id="d344212e300">

**Delete a problem**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Delete**.

</td></tr><tr><td id="d344212e318">

**Attach knowledge articles or records that help a quick resolution of a problem**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(![agent assist icon](../image/agent-assist-icon.png)\).
2.  Search for a resource and perform the required action.
The knowledge articles attached here are displayed in the **Related records** tab.

</td></tr><tr><td id="d344212e344">

**Add an attachment to a problem**

</td><td>

From the contextual side panel, select the attachments icon \(![attachments icon](../../itsm-workspace/image/attachment-icon.png)\).

</td></tr><tr><td id="d344212e359">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Copy URL**.

</td></tr><tr><td id="d344212e377">

**Share a workaround**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Share workaround**.

</td></tr><tr><td id="d344212e395">

**Share a fix**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Share fix**.

</td></tr><tr><td id="d344212e414">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(![templates icon](../image/template-icon.png)\).

</td></tr><tr><td id="d344212e429">

**Acknowledge the problem while recognizing there is currently no permanent resolution**

</td><td>

From the drop-down list next to **Cancel**, select **Accept risk** and fill the mandatory fields.**Note:** You can apply workaround notes to a risk-accepted problem.

</td></tr><tr><td id="d344212e446">

**Re-analyze a problem**

</td><td>

From a problem in the closed or resolved state, select **Re-analyze**. The state is changed to Root Cause Analysis.

</td></tr></tbody>
</table>
**Parent Topic:**[Problem Management in Service Operations Workspace](../concept/problem-sow.md)

**Related topics**  


[Create a problem in Service Operations Workspace](create-problem-sow.md)

[Problem Management models in Service Operations Workspace](../concept/problem-mgmt-models-sow.md)

[Create a problem task in Service Operations Workspace](create-problem-task-sow.md)

[Work on a problem task in Service Operations Workspace](work-on-problem-task-sow.md)

