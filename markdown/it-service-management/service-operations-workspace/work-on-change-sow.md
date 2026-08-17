---
title: Work on a change request in Service Operations Workspace
description: Modify a supported configuration item to clear a change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-operations-workspace/work-on-change-sow.html
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Change Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on a change request in Service Operations Workspace

Modify a supported configuration item to clear a change request.

## Before you begin

Role required: itil

## Procedure

1.  To open a change request, select the List icon \(\[Omitted image "sow-list.png"\] Alt text: list icon\) and then navigate to **Changes**.

    **Note:** Following lists are available:

    -   Open
    -   Closed
    -   All
2.  Select a change request from the relevant list.

    **Note:** You can also open a change request from the **Incidents**, **Problems** or **Interactions** lists.

3.  Perform any of the following actions on the change record page.

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d312130e105">

Option

</th><th align="left" id="d312130e108">

Description

</th></tr></thead><tbody><tr><td id="d312130e114">

**Create change tasks for delegation**

</td><td>

In the **Overview** tab, select **Add Task**. For more information about creating a change task, see [Create a change task in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/create-change-task-sow.md).

</td></tr><tr><td id="d312130e136">

**Compose an email from the change**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select **Compose Email**.

</td></tr><tr><td id="d312130e154">

**Create outage**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select **Create Outage**.

</td></tr><tr><td id="d312130e172">

**View dependencies**

</td><td>

View the entities associated with the CI that can be impacted as a result of the change request.In the **Impact** section of the **Details** tab, select the Configuration item dependency view icon \( \[Omitted image "dependency-icon-r.png"\] Alt text: configuration item dependency view icon \) displayed in the **Configuration item**, **Service offering**, or **Service** field, as applicable. The unified dependency Configuration Management Database \(CMDB\) map is displayed in a new tab within the workspace view.

</td></tr><tr><td id="d312130e215">

**Refresh impacted Services on a change request form**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select **Refresh Impacted Services**. For information about refreshing impacted services, see [Refresh impacted services and CIs for Change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/refresh-impacted-services-cis.md).

</td></tr><tr><td id="d312130e240">

**Cancel the change**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select **Cancel**.

</td></tr><tr><td id="d312130e258">

**Delete the change**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select select **Delete**.

</td></tr><tr><td id="d312130e276">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: more actions icon\) and select **Copy URL**.

</td></tr><tr><td id="d312130e294">

**View the record information such as SLAs**

</td><td>

From the contextual side panel, select the record Information icon \(\[Omitted image "record-info-icon.png"\] Alt text: record Information icon\).

</td></tr><tr><td id="d312130e309">

**Attach a record that helps in quick resolution of the change**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(\[Omitted image "agent-assist-icon.png"\] Alt text: agent assist icon\).
2.  Search for a resource and perform the required action, for example, link the change to an incident.


</td></tr><tr><td id="d312130e334">

**Collaborate using Microsoft Teams**

</td><td>

From the contextual side panel, select the collaborate icon \(\[Omitted image "collaborate-sidebar.png"\] Alt text: collaborate icon\).

</td></tr><tr><td id="d312130e352">

**Add attachments**

</td><td>

From the contextual side panel, select the attachments icon \(\[Omitted image "attachment-icon.png"\] Alt text: attachments icon\).**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d312130e373">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(\[Omitted image "template-icon.png"\] Alt text: templates icon\) and create a template or reuse an existing one.

</td></tr><tr><td id="d312130e388">

**Approve the change**

</td><td>

Select **Related records** tab, select **Approvers**.

</td></tr><tr><td id="d312130e406">

**Implement the change**

</td><td>

Select  **Implement**  to put the change request into action. The change request state changes to  **Implement**. The workflow creates two change tasks: **Implement**  and  **Post-implementation testing**. Review the change tasks and assign them to a user or group, as appropriate.

</td></tr><tr><td id="d312130e430">

**Review a change request**

</td><td>

Select  **Review**  after reviewing the details on the change request.

 The change request is moved to the  **Review**  state. All open change tasks are set to  **Canceled**.

</td></tr><tr><td id="d312130e455">

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

**Parent Topic:**[Change Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace]()

[Standard change catalog]()

[Create a change task in Service Operations Workspace]()

[Work on a change task in Service Operations Workspace]()

[Create a Change Advisory Board \(CAB\) definition]()

[Create a CAB meeting]()

[Conduct a CAB meeting in the CAB workbench]()

