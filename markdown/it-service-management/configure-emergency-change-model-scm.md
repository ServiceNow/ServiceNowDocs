---
title: Configure the Emergency change model
description: Configure the Emergency change model to define who can submit emergency changes, set up stakeholder notifications, configure approvals, and control automatic change task creation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-emergency-change-model-scm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 3
keywords: [Emergency change model, emergency change submitters, change notifications]
breadcrumb: [Configure change models, Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure the Emergency change model

Configure the Emergency change model to define who can submit emergency changes, set up stakeholder notifications, configure approvals, and control automatic change task creation.

## Before you begin

Role required: sn\_itsm\_chg\_admin.change\_models\_config, sn\_itsm\_chg\_admin.admin, or admin

## Procedure

1.  Open the **Emergency** change model in the Configuration Console.

    For navigation steps, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

2.  Configure the availability, templates, authorized submitters, risk-based approvals for the states, and control automatic change task creation.

<table id="table_bfl_l23_hjc"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Availability

</td><td>

The Availability setting controls whether the model is available to select while creating new change requests.Set the **Available for new change requests** toggle. Turn on to expose the model in the change type picker while creating new change requests.

When you enable the model by selecting the **Availability** check box, the corresponding global model is set to inactive and ITIL changes process is set to the simplified change model.

</td></tr><tr><td>

New

</td><td>

The New state defines who can submit emergency change, who get notified, and templates for the change model.In the **Who can submit emergency changes?** field, select users or user groups authorized to submit emergency changes. Only members of the selected groups can choose the Emergency model when creating a change. Emergency changes bypass normal schedules, so limit this to authorized teams.

**Note:** Only users with the sn\_change\_write role are available for selection.

 Under **Who should be informed about emergency changes**, configure notifications. An email is sent each time an emergency change is created.

1.  In the **Select users or groups** field, add the notification recipients.
2.  In the **Select the email template** field, select the notification template.
The templates have pre-filled common fields that follow the change model's workflow and approval requirements. Review the template that use this change model. To add a template, select **New template**. For steps to configure a template, see [Create and propose a change template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/create-change-template.md).

</td></tr><tr><td>

Authorize

</td><td>

The Authorize state is the business approval gate. It verifies the change is approved to proceed to implementation.Configure approvers separately for Low risk, Moderate risk, and High risk. Select one or more approver. The available approvers are:

-   **Member of assignment group**: Any member of the assignment group can approve. One approval is sufficient.
-   **Manager of assignment group**: The manager of the assignment group must approve.
-   **Change manager**: Any member of the change management group can approve.
-   **CAB member**: At least one CAB member must approve.
-   **Other group**: A specific group that you select must approve. Select an assignment group from the list on the modal window.
Default approvers for each risk level are:

-   Low risk: Member of assignment group
-   Moderate risk: CAB member
-   High risk: CAB member


</td></tr><tr><td>

Scheduled

</td><td>

The Scheduled state controls auto-creation of a task to verify planning and resources required for the change. Select **Yes** to generate the change tasks automatically when the change enters this state. This task helps confirm the change is properly planned and resources are in place before implementation.

</td></tr><tr><td>

Implement

</td><td>

The Implement state controls auto-creation of a task to implement the change. Select **Yes** to generate the change tasks automatically when the change enters this state. This task helps the change through execution, verification, and documentation.

</td></tr><tr><td>

Review

</td><td>

The Review state controls auto-creation of a task to review the change implementation. Select **Yes** to generate the change tasks automatically when the change enters this state. This task helps to verify the change was successful and record lessons learned.

</td></tr></tbody>
</table>3.  Select **Save**.

    To discard unsaved changes, select **Cancel**.


## Result

The Emergency change model configuration is saved. Only members of the designated submitter groups can create emergency changes, and the configured recipients receive email notifications on each creation.

## What to do next

To configure additional change models, return to [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

**Parent Topic:**[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)

