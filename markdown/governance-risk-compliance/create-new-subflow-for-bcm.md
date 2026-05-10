---
title: Create a subflow form
description: Use the Create a subflow form to automate a manual recovery task within the business continuity plan.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automate recovery tasks, Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a subflow form

Use the Create a subflow form to automate a manual recovery task within the business continuity plan.

## Create a subflow form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

 

</td></tr><tr><td>

Subflow Name

</td><td>

Name of the subflow. For example, if you want to automate a manual task for sending an email, you can name the subflow as Send an email subflow.

</td></tr><tr><td>

Description

</td><td>

Description of the subflow.

</td></tr><tr><td>

Application

</td><td>

Application scope for creating the subflow in. For the BCM tasks, you can select GRC: Business Continuity Management.

</td></tr><tr><td>

Accessible From

</td><td>

All application scopes that the subflow can be accessed from.

</td></tr><tr><td>

Category

</td><td>

Category or logical group for the subflow. For the BCM automation tasks, you can select the **BCM: Task automation** category.

</td></tr><tr><td>

Protection

</td><td>

Option to mark the subflow as read-only. When you create the subflow in an application scope that you own, you can select a value for this field. Editing permissions and protection for the subflow. Select one of these options:-   **None**: Default value. Select this option to edit the subflow.
-   **Read-only**: Mark the subflow as read-only. Only the creator of the subflow can edit it.

</td></tr><tr><td>

Subflow annotation

</td><td>

Annotation for the subflow. The help text under the subflow title in Workflow Studio helps the flow designers to understand what the subflow does when it is used in a flow.

</td></tr><tr><td>

Run As

</td><td>

Option to define the user who runs the subflow. Select one of these options:-   **User who initiates session**: Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want to receive the approval email from the approver.
-   **System user**: Select the system user to run the subflow.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the subflow runs with. This option is only available when **Run as** is set to **User who initiates the session**. For example, a plan user should have the email\_api\_send role to send the email and the sn\_bcm.program\_manager role to read the BCM tasks.

</td></tr></tbody>
</table>For more information on creating a subflow, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md).

**Parent Topic:**[Automate recovery tasks](../task/automate-the-recovery-tasks.md)

