---
title: Work on a change request in Service Operations Workspace
description: Modify a supported configuration item to clear a change request.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Change Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on a change request in Service Operations Workspace

Modify a supported configuration item to clear a change request.

## Before you begin

Role required: itil

## Procedure

1.  Open a change request.

2.  To open a change request, select the List icon \(![list icon](../image/sow-list.png)\) and then navigate to **Changes**.

    **Note:** Following lists are available:

    -   Open
    -   Closed
    -   All
3.  Select a change request from the relevant list.

    **Note:** You can also open a change request from the **Incidents**, **Problems** or **Interactions** lists.

4.  Perform any of the following actions on the change record page.

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d307014e117">

Option

</th><th align="left" id="d307014e120">

Description

</th></tr></thead><tbody><tr><td id="d307014e126">

**Create change tasks for delegation**

</td><td>

In the **Overview** tab, select **Add Task**. For more information about creating a change task, see [Create a change task in Service Operations Workspace](create-change-task-sow.md).

</td></tr><tr><td id="d307014e148">

**Compose an email from the change**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Compose Email**.

</td></tr><tr><td id="d307014e166">

**Create outage**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Create Outage**.

</td></tr><tr><td id="d307014e184">

**View dependencies**

</td><td>

View the entities associated with the CI that can be impacted as a result of the change request.In the **Impact** section of the **Details** tab, select the Configuration item dependency view icon \( ![configuration item dependency view icon](../../incident-management/image/dependency-icon-r.png) \) displayed in the **Configuration item**, **Service offering**, or **Service** field, as applicable. The unified dependency Configuration Management Database \(CMDB\) map is displayed in a new tab within the workspace view.

</td></tr><tr><td id="d307014e227">

**Refresh impacted Services on a change request form**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Refresh Impacted Services**. For information about refreshing impacted services, see [Refresh impacted services and CIs for Change](../../change-management/task/refresh-impacted-services-cis.md).

</td></tr><tr><td id="d307014e252">

**Cancel the change**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Cancel**.

</td></tr><tr><td id="d307014e270">

**Delete the change**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select select **Delete**.

</td></tr><tr><td id="d307014e288">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Copy URL**.

</td></tr><tr><td id="d307014e306">

**View the record information such as SLAs**

</td><td>

From the contextual side panel, select the record Information icon \(![record Information icon](../image/record-info-icon.png)\).

</td></tr><tr><td id="d307014e321">

**Attach a record that helps in quick resolution of the change**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(![agent assist icon](../image/agent-assist-icon.png)\).
2.  Search for a resource and perform the required action, for example, link the change to an incident.


</td></tr><tr><td id="d307014e346">

**Collaborate using Microsoft Teams**

</td><td>

From the contextual side panel, select the collaborate icon \(![collaborate icon](../image/collaborate-sidebar.png)\).

</td></tr><tr><td id="d307014e364">

**Add attachments**

</td><td>

From the contextual side panel, select the attachments icon \(![attachments icon](../../itsm-workspace/image/attachment-icon.png)\).**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d307014e385">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(![templates icon](../image/template-icon.png)\) and create a template or reuse an existing one.

</td></tr><tr><td id="d307014e400">

**Approve the change**

</td><td>

Select **Related records** tab, select **Approvers**.

</td></tr><tr><td id="d307014e418">

**Implement the change**

</td><td>

Select  **Implement**  to put the change request into action. The change request state changes to  **Implement**. The workflow creates two change tasks: **Implement**  and  **Post-implementation testing**. Review the change tasks and assign them to a user or group, as appropriate.

</td></tr><tr><td id="d307014e442">

**Review a change request**

</td><td>

Select  **Review**  after reviewing the details on the change request.

 The change request is moved to the  **Review**  state. All open change tasks are set to  **Canceled**.

</td></tr><tr><td id="d307014e467">

**Close a change request**

</td><td>

Select  **Close**  after entering the  **Close code ** and  **Close notes ** in the  **Closure Information ** section.

 The change request is closed.

</td></tr></tbody>
</table>    The following action buttons are displayed only if the On Hold field is configured for the change request form in SOW:

    -   Schedule
    -   Request approval for access
    -   Request approval for authorize
    -   Implement
    -   Review
    -   Close

**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace](create-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Create a change task in Service Operations Workspace](create-change-task-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

[Create a Change Advisory Board \(CAB\) definition](cm-create-cab-definition-sow.md)

[Create a CAB meeting](cm-create-cab-meeting-sow.md)

[Conduct a CAB meeting in the CAB workbench](cm-manage-cab-meeting-workbench-sow.md)

