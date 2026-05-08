---
title: Work on a problem task in Service Operations Workspace
description: Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Problem Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on a problem task in Service Operations Workspace

Manage problems and problem tasks through their life cycle, share workarounds or fixes with related incidents, and create known error articles to help deflect incidents.

## Before you begin

If you aren't using the base problem life cycle, you will continue to use the classic experience to manage problems or problem tasks through their life cycle. From the problem task record page, select **Continue problem task** to be redirected to the ServiceNow AI Platform user interface where you can make state transitions. For information about state transitions of a problem, see [Life cycle of a problem](../../problem-management/concept/understanding-state-mgmt-transitions.md).

The base problem life cycle is included with the Problem Management  Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin. Use the Problem Management Migration Utility [store application](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d03b7539dbbb3300f21e7ffdbf9619a8) to enable this plugin and migrate your records to the base problem life cycle.

Role required: itil or problem\_task\_analyst \(for changing the state of the problem task or deleting it\)

## Procedure

1.  Open a problem.

    For information about creating a problem in Service Operations Workspace, see [Create a problem in Service Operations Workspace](create-problem-sow.md).

2.  From the **Problem Tasks** tab, open the required problem task.

3.  Perform any of the following actions on the problem task record page.

<table id="choicetable_sj2_3wq_cbc"><thead><tr><th align="left" id="d383231e102">

Option

</th><th align="left" id="d383231e105">

Description

</th></tr></thead><tbody><tr><td id="d383231e111">

**Assign a problem task to yourself**

</td><td>

Select **Assign to me**.

</td></tr><tr><td id="d383231e123">

**Assess a problem task**

</td><td>

Select **Assess** and fill the mandatory fields.

</td></tr><tr><td id="d383231e135">

**Start work on a problem task**

</td><td>

Select **Start work**.

</td></tr><tr><td id="d383231e147">

**Cancel a problem task**

</td><td>

Select **Cancel task** and fill the mandatory fields.

</td></tr><tr><td id="d383231e160">

**Delete a problem task**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Delete**.

</td></tr><tr><td id="d383231e178">

**Attach knowledge articles or records that help a quick resolution of a problem task**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(![agent assist icon](../image/agent-assist-icon.png)\).
2.  Search for a resource and perform the required action.
The knowledge articles attached here are displayed in the **Related records** tab.

</td></tr><tr><td id="d383231e204">

**Add an attachment to a problem task**

</td><td>

From the contextual side panel, select the attachments icon \(![attachments icon](../../itsm-workspace/image/attachment-icon.png)\).

</td></tr><tr><td id="d383231e219">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Copy URL**.

</td></tr><tr><td id="d383231e237">

**Complete a problem task**

</td><td>

Select **Complete** and fill the mandatory fields.

</td></tr><tr><td id="d383231e249">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(![templates icon.](../image/template-icon.png)\).

</td></tr><tr><td id="d383231e265">

**Re-assess a problem task**

</td><td>

From a problem task in the **Work in Progress** or **Closed** state, select **Re-assess**. The state is changed to Assess.

</td></tr></tbody>
</table>
**Parent Topic:**[Problem Management in Service Operations Workspace](../concept/problem-sow.md)

**Related topics**  


[Create a problem in Service Operations Workspace](create-problem-sow.md)

[Work on a problem in Service Operations Workspace](work-on-problem-sow.md)

[Problem Management models in Service Operations Workspace](../concept/problem-mgmt-models-sow.md)

[Create a problem task in Service Operations Workspace](create-problem-task-sow.md)

[Problem Management in Service Operations Workspace reference](../concept/reference-problem-management-sow.md)

