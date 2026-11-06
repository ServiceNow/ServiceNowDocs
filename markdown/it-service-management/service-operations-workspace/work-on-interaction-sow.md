---
title: Work on an interaction in Service Operations Workspace
description: Work on customer conversations to resolve issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/service-operations-workspace/work-on-interaction-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-09-10"
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

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d252465e60">

Option

</th><th align="left" id="d252465e63">

Description

</th></tr></thead><tbody><tr><td id="d252465e69">

**Create incident**

</td><td>

Select **Create incident**.**Note:** If you create an incident from an interaction, it is auto-assigned to the user to whom the interaction is assigned.

</td></tr><tr><td id="d252465e86">

**Create change**

</td><td>

From the **Create incident** drop-down, select **Create change**.**Note:** You can only create a change request of the pre-approved change type.

</td></tr><tr><td id="d252465e104">

**Complete**

</td><td>

Select **Complete** to mark the state of the interaction as **Closed Complete** and end the active conversation with the user.

</td></tr><tr><td id="d252465e119">

**Abandon**

</td><td>

From the **Complete** drop-down, select **Abandon**. This action marks the state of the interaction as **Closed Abandoned** and ends the active conversation with the user.

</td></tr><tr><td id="d252465e141">

**Create request**

</td><td>

From the **Create incident** drop-down, select **Create request**. For more information, see [Create a catalog request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/create-catalog-request-sow.md).

</td></tr><tr><td id="d252465e169">

**Create problem**

</td><td>

From the **Create incident** drop-down, select **Create problem**. **Note:** This option is available only when the **Allow Problem creation from Interaction** \(**glide.problem.interaction.allow\_create**\) problem property is activated from **Problem** &gt; **Problem Properties**.

</td></tr><tr><td id="d252465e202">

**View record information**

</td><td>

The related records of a requester are displayed as intended for Service Operations Workspace. You can access the **Assigned assets**, **Recent interactions**, and **Recent tasks** of the requester.**Note:**

If the type is Walk-up, you can view the walk-up summary of the interaction record.

You can view the device health of the user's assets to provide a resolution to the user. Select **Assigned assets** &gt; **View device health**. This option is available only if the DEX plugin \(sn\_dex\) is installed and DEX monitoring is enabled for the asset. For more information on Digital End-User Experience, refer .

</td></tr><tr><td id="d252465e245">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text:\) and select **Copy URL**.

</td></tr><tr><td id="d252465e262">

**Attach a record that helps in quick resolution of the interaction**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(\[Omitted image "agent-assist-icon.png"\] Alt text:\).
2.  Search for a resource and perform the required action, for example, find a relevant knowledge base article and attach a link to it to work notes.
 **Note:** The agent assist icon is available only for users with the following roles: itil or interaction\_agent.

 For information on configuring additional search resources, see [Configure search resources for an interaction in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/configure-resources-for-an-interaction.md).

</td></tr><tr><td id="d252465e298">

**Add attachments**

</td><td>

From the contextual side panel, select the attachments icon \(\[Omitted image "attachment-icon.png"\] Alt text:\). Alternatively, you can drag the attachment into the **Active Chat** window of the interaction.**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d252465e322">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(\[Omitted image "template-icon.png"\] Alt text:\) and create a template or reuse an existing one.

</td></tr></tbody>
</table>
**Parent Topic:**[Interaction Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/interaction-sow.md)

**Related topics**  


[Create an interaction in Service Operations Workspace]()

[Collaborate using Microsoft Teams from an interaction record in Service Operations Workspace]()

[Associate an interaction with a task record]()

