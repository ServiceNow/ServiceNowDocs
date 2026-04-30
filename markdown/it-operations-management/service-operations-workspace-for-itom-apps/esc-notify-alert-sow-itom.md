---
title: Create Respond automation
description: Respond to alerts automatically by notifying appropriate stakeholders, escalating them as needed based on severity and type, or other executing response actions. This process ensures that alerts are managed promptly and effectively.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Alert automation in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Respond automation

Respond to alerts automatically by notifying appropriate stakeholders, escalating them as needed based on severity and type, or other executing response actions. This process ensures that alerts are managed promptly and effectively.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

For users familiar with the classic Event Management experience, this provides an easy interface with enhanced team support for creating response automations or alert management rules. Alert management rules or response automations are configurable automated actions triggered in response to alerts which match specific conditions, helping IT teams resolve issues faster and with minimal manual effort. These advanced features are currently only available to administrators and other personas mentioned in the role required section.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Alert Automation icon \(![Alert automation icon](../../event-management/image/alert-automations-icon.png)\).

3.  On the Alert automations page, select **Respond**.

4.  Select **Create automation**.

    The Respond page appears.

    ![Respond automation page from where you can create automation to remediate action on alerts, escalate alerts or notify stakeholders.](../image/respond-automation-page.png)

5.  In the **Automation name** field, enter the name of the automation.

6.  Activate the automation by selecting the **Active** check box.

7.  In the **If these conditions are met** section, create filter criteria to identify the alerts you want to capture.

    **Important:** You can limit respond automations to primary alerts to prevent secondary alerts from being overwhelmed by unnecessary noise. Ensure these automations are applied only to alerts associated with CIs that are not currently undergoing maintenance.

    ![Respond automation conditions](../image/respond-automation-conditions.png)

    1.  From the **Assignment group** field menu, select the assignment group to determine which team’s alerts will trigger the automation.

        The **Assignment group** represents a specific team responsible for handling certain alerts. By selecting an assignment group, you ensure that only the alerts assigned to that particular team will trigger the automation. This way, the automation is targeted and only activates for relevant alerts associated with the selected team.

        **Note:**

        -   If you’re logged in to the instance with an administrator role \(evt\_mgmt\_admin\), all of the assignment groups are available. Additionally, you can select **All groups** to enable generating alerts for any of the available groups.
        -   If you’re an operator, only the group you’re a part of is available.
        -   Only members of the selected group or administrators can update or delete the automation.
    2.  For the **Parent** field value, select whether the alert for which you want a response is grouped under a parent alert.
    3.  For the **Maintenance** field value, select whether the alert for which you want a response is under maintenance.
    4.  To add another set of conditions, select **+ New condition set**. You can also manually add an additional info field if you don’t see it in the drop-down list.

        Set up the conditions by selecting the field, operator, and field value. Then, add more conditions using OR or AND operators.

8.  In the **Then, apply the following actions** section, select one or more of the three automation actions that can be triggered by the automation.

    ![Respond automation actions](../image/respond-automation-actions.png)

<table id="choicetable_cng_cfz_pbc"><thead><tr><th align="left" id="d484589e243">

Action

</th><th align="left" id="d484589e246">

Description

</th></tr></thead><tbody><tr><td id="d484589e252">

**Create an incident**

</td><td>

Creates an incident for the alerts that match the specified filter.For details on mapping the alert fields to the incident fields, see [Alert field mapping on the Respond page](../reference/alert-field-mapping-respond-page.md).

To include additional fields in the incident, select **+ Add**.

</td></tr><tr><td id="d484589e275">

**Use outbound webhooks to send data to other systems**

</td><td>

Sends notifications to other systems using outbound webhooks. For example, this capability can be used to send a chat notification, create a case, or trigger an external runbook to remediate the issue.

 For details on configuring an outbound webhook, see [Outbound webhook parameters](../reference/outbound-webhook-parameters.md).

 To create an additional property, select **+ Add property**. The property can be any custom key-value pair that you want to include in the webhook payload, such as "Content-Type: application/json" or "Authorization: Bearer &lt;token&gt;".

</td></tr><tr><td id="d484589e303">

**Run other response actions**

</td><td>

Executes selected subflows from Workflow Studio for alerts that match the specified condition. For example, you may [out-of-the-box subflows](../../event-management/reference/subflows-provided.md) to restart services. You can also create your own [custom subflows](../../event-management/task/create-custom-create-incident-subflow.md), leveraging hundreds of integrations available in Integration Hub.

 ![Response subflow](../image/respond-automation-actions-details.png)

 1.  In the **Response subflow** field, select the subflow.
2.  In the **When should the subflow execute?** field, select **Automatically**, **Manually** or **Automatically and Manually**.

**Note:** If you select a subflow with an execution type of **Manually** or **Automatically and Manually**, and then save the automation, it appears in the Express List.

![Subflows in Express list.](../image/respond-automation-express-list.png)

3.  In the **Execution limit** field, specify the maximum number of times the subflow can run. After reaching the limit, the subflow will not execute again.
 To add another response action, select **+ Add response action**.

 To learn how to create your own subflow, see [Create a custom subflow for alerts](../../event-management/task/create-custom-create-incident-subflow.md).

</td></tr></tbody>
</table>    **Note:** If you don’t select at least one action, the automation is deactivated.

9.  In the **And finally** section, to continue running other response automations with same filter conditions after this automation is executed, select **Run other response automations**.

    If you select **Don't run response automations**, additional automations of this type will stop running after this automation is executed once. If the automation is managed by an administrator, it will stop running administrator-owned automations but will continue to run automations owned by other assignment groups.

10. In the **Automation details** section, provide an order and automation description.

    ![Respond automation details section](../image/respond-automation-details.png)

    For information on the Automation details fields, see [../reference/automation-details-fields.md](../reference/automation-details-fields.md).

11. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed.

    The response automation that you created appears on the All response automations page where you can view, edit, or delete the existing automations.


