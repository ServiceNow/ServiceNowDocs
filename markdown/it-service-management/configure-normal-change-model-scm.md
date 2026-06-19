---
title: Configure the Normal change model
description: Configure the Normal change model to define availability, approval requirements, templates, and change task behaviors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-normal-change-model-scm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 3
keywords: [Normal change model, change approvals, Assess state, Authorize state]
breadcrumb: [Configure change models, Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure the Normal change model

Configure the Normal change model to define availability, approval requirements, templates, and change task behaviors.

## Before you begin

Role required: sn\_itsm\_chg\_admin.change\_models\_config, sn\_itsm\_chg\_admin.admin, or admin

## Procedure

1.  Open the **Normal** change model in the Configuration Console.

    For navigation steps, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

2.  Configure the availability, templates, and risk-based approvals for different states, and control the automatic change task creation for Normal change requests.

<table id="table-nrml-settings"><thead><tr><th>

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

Templates have pre-filled common fields that follow the change model's workflow and approval requirements.Review the template that use this change model. To add a template, select **New template**. For steps to configure a template, see [Create and propose a change template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/create-change-template.md).

</td></tr><tr><td>

Assess

</td><td>

The Assess state requires proper documentation and readiness for authorization. Configure approvers separately for Low risk, Moderate risk, and High risk. The available approvers are:

-   **Member of assignment group**: Any member of the assignment group can approve. One approval is sufficient.
-   **Manager of assignment group**: The manager of the assignment group must approve.
-   **Change manager**: Any member of the change management group can approve.
-   **CAB member**: At least one CAB member must approve.
-   **Other group**: A specific group that you select must approve. Select an assignment group from the list on the modal window.
Default approvers for each risk level are:

-   Low risk: Member of assignment group
-   Moderate risk: Member of assignment group
-   High risk: Member of assignment group


</td></tr><tr><td>

Authorize

</td><td>

The Authorize state is the business approval gate. It verifies the change is approved to proceed to implementation.Configure approvers separately for Low risk, Moderate risk, and High risk. Select one or more approvers. The available approvers are:

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

The Scheduled state controls auto-creation of a task to verify planning and resources for the change. Select **Yes** to generate the change tasks automatically when the change enters this state. This task helps verify the change is properly planned and resources are in place before implementation.

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


## Result

The Normal change model configuration is saved. New Normal change requests reflect the updated availability option, approval requirements, and change task behaviors.

## What to do next

To configure additional change models, return to [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

**Parent Topic:**[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)

