---
title: Work on an interaction in Service Operations Workspace
description: Work on customer conversations to resolve issues.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Interaction Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on an interaction in Service Operations Workspace

Work on customer conversations to resolve issues.

## Before you begin

Role required: itil or admin

## Procedure

1.  Open an interaction.

2.  Perform any of the following actions on the interaction record page.

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d362282e58">

Option

</th><th align="left" id="d362282e61">

Description

</th></tr></thead><tbody><tr><td id="d362282e67">

**Create incident**

</td><td>

Click **Create incident**.**Note:** If you create an incident from an interaction, it will be auto-assigned to the user to whom the interaction is assigned.

</td></tr><tr><td id="d362282e84">

**Create change**

</td><td>

From the **Create incident** drop-down, select **Create change**.**Note:** You can only create a change request of the pre-approved change type.

</td></tr><tr><td id="d362282e102">

**Complete**

</td><td>

Click **Complete** to mark the state of the interaction as **Closed Complete** and end the active conversation with the user.

</td></tr><tr><td id="d362282e117">

**Abandon**

</td><td>

From the **Complete** drop-down, select **Abandon**. This action marks the state of the interaction as **Closed Abandoned** and ends the active conversation with the user.

</td></tr><tr><td id="d362282e139">

**Create request**

</td><td>

From the **Create incident** drop-down, select **Create request**. For more information, see [Create a catalog request in Service Operations Workspace](create-catalog-request-sow.md).

</td></tr><tr><td id="d362282e167">

**Create problem**

</td><td>

From the **Create incident** drop-down, select **Create problem**. **Note:** This option is available only when the **Allow Problem creation from Interaction** \(**glide.problem.interaction.allow\_create**\) problem property is activated from **Problem** &gt; **Problem Properties**.

</td></tr><tr><td id="d362282e200">

**View record information**

</td><td>

The related records of a requester are displayed as intended for Service Operations Workspace. You can access the **Assigned assets**, **Recent interactions**, and **Recent tasks** of the requester.**Note:**

If the type is Walk-up, you can view the walk-up summary of the interaction record.

You can now view the device health of the user's assets to provide a resolution to the user. Select **Assigned assets** &gt; **View device health**. This option is available only if the DEX plugin\[sn\_dex\] is installed and DEX monitoring is enabled for the asset. For more information on Digital End-User Experience, refer [Digital End-User Experience](../../digital-end-user-experience/concept/dex-landing.md).

</td></tr><tr><td id="d362282e272">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Copy URL**.

</td></tr><tr><td id="d362282e290">

**Attach a record that helps in quick resolution of the interaction**

</td><td>

1.  From the contextual side panel, click the agent assist icon \(![agent assist icon](../image/agent-assist-icon.png)\).
2.  Search for a resource and perform the required action, for example, find a relevant knowledge base article and attach a link to it to work notes.
 **Note:** The agent assist icon is available only for users with the following roles: itil or interaction\_agent.

 For information on configuring additional search resources, see [Configure search resources for an interaction in Service Operations Workspace for ITSM](configure-resources-for-an-interaction.md).

</td></tr><tr><td id="d362282e327">

**Add attachments**

</td><td>

From the contextual side panel, click the attachments icon \(![attachments icon](../../itsm-workspace/image/attachment-icon.png)\). Alternatively, you can drag and drop the attachment into the **Active Chat** window of the interaction.**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d362282e352">

**Create templates for reuse**

</td><td>

From the contextual side panel, click the templates icon \(![templates icon](../image/template-icon.png)\) and create a template or reuse an existing one.

</td></tr></tbody>
</table>
**Parent Topic:**[Interaction Management in Service Operations Workspace](../concept/interaction-sow.md)

**Related topics**  


[Create an interaction in Service Operations Workspace](create-interaction-sow.md)

[Collaborate using Microsoft Teams from an interaction record in Service Operations Workspace](collaborate-interaction-ms-teams-sow.md)

[Associate an interaction with a task record](associate-interaction-record-sow.md)

