---
title: Create Respond automation
description: Respond to alerts automatically by notifying appropriate stakeholders, escalating them as needed based on severity and type, or other executing response actions. This process ensures that alerts are managed promptly and effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/respond-alert-sow-itom.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Respond automation

Respond to alerts automatically by notifying appropriate stakeholders, escalating them as needed based on severity and type, or other executing response actions. This process ensures that alerts are managed promptly and effectively.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

For users familiar with the classic Event Management experience, this provides an easy interface with enhanced team support for creating response automations or alert management rules. Alert management rules or response automations are configurable automated actions triggered in response to alerts which match specific conditions, helping IT teams resolve issues faster and with minimal manual effort. These advanced features are currently only available to administrators and other personas mentioned in the role required section.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon \[Omitted image "icon-itom-aiops-config.png"\] Alt text: ITOM AIOps configuration center icon.

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Respond alerts**.

4.  Select **Create automation**.

    The Respond page appears.

    \[Omitted image "respond-automation-page.png"\] Alt text: Respond automation page from where you can create automation to remediate action on alerts, escalate alerts or notify stakeholders.

5.  In the **Automation name** field, enter the name of the automation.

    By default, the **Active** check box is selected.

6.  In the **If these conditions are met** section, create filter criteria to identify the alerts you want to capture.

    **Important:** You can limit respond automations to primary alerts to prevent secondary alerts from being overwhelmed by unnecessary noise. Ensure these automations are applied only to alerts associated with CIs that are not currently undergoing maintenance.

    \[Omitted image "respond-automation-conditions.png"\] Alt text: Respond automation conditions

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

7.  In the **Then, apply the following actions** section, select one or more of the two automation actions that can be triggered by the automation.

    \[Omitted image "respond-automation-actions.png"\] Alt text: Respond automation actions

<table id="choicetable_cng_cfz_pbc"><thead><tr><th align="left" id="d187652e243">

Action

</th><th align="left" id="d187652e246">

Description

</th></tr></thead><tbody><tr><td id="d187652e252">

**Create incident and other response actions**

</td><td>

Creates an incident for the alerts that match the specified filter.For details on mapping the alert fields to the incident fields, see [Alert field mapping on the Respond page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/alert-field-mapping-respond-page.md).

**Note:** If you want incident fields to be automatically populated with default values, consider using **Create Incident \(advanced\)** in the **Response subflows** field. **Create Incident \(advanced\)** pre-populates incident fields even when you don’t explicitly customize them, which helps ensure consistent incident data and reduces configuration effort.

The **Create incident and other response actions** option also executes selected subflows from Workflow Studio for alerts that match the specified condition. For example, you may select [out-of-the-box subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/subflows-provided.md) to restart services. You can also create your own [custom subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/create-custom-create-incident-subflow.md), leveraging hundreds of integrations available in Integration Hub.

\[Omitted image "respond-automation-actions-details.png"\] Alt text: Response subflow

1.  In the **Response subflow** field, select the subflow.

Selecting the Information icon \(\[Omitted image "icon-information-1.png"\] Alt text: icon for information\) takes you to the workflow of the subflow. For example, if you select the Information icon \(\[Omitted image "icon-information-1.png"\] Alt text: icon for information\) next to Close Alert, the Close Alert workflow opens.

\[Omitted image "respond-automation-close-alerts-workflow.png"\] Alt text: Close alerts workflow

2.  In the **How should the subflow execute?** field, select **Automatically**, **Manually** or **Automatically and Manually**.

**Note:** If you select a subflow with an execution type of **Manually** or **Automatically and Manually**, and then save the automation, it appears in the Express List.

\[Omitted image "respond-automation-express-list.png"\] Alt text: Subflows in Express list.

3.  In the **Execution limit** field, specify the maximum number of times the subflow can run. After reaching the limit, the subflow will not execute again.
4.  In the **Response subflow** field, when you select **Create Incident \(advanced\)**, two check boxes appear.

    -   **Customize incident fields**
    -   **Add wait time**
When you select the **Customize incident fields** check box, a mapping section appears with the following fields:

    -   **Alert input value**: Generates the value using Now Assist or takes it from the alert.
    -   **Incident field name**: Maps the selected alert value to the specified incident field.
**Note:** At least one field mapping is required when you select the **Customize incident fields** check box. **Create Incident \(advanced\)** automatically fills incident fields with default values, even if you don’t customize them.

5.  Select the **Add wait time** check box to delay incident creation and allow alerts time to auto-resolve or downgrade.

You can define conditions that are evaluated after the wait period to determine whether an incident still needs to be created. This helps prevent unnecessary incidents for alerts that resolve on their own or reduce in severity.

To add another response action, select **+ Add response action**.

</td></tr><tr><td id="d187652e465">

**Use outbound webhooks to send data to other systems**

</td><td>

Sends notifications to other systems using outbound webhooks. For example, this capability can be used to send a chat notification, create a case, or trigger an external runbook to remediate the issue.

 For details on configuring an outbound webhook, see [Outbound webhook parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/outbound-webhook-parameters.md).

 To create an additional property, select **+ Add property**. The property can be any custom key-value pair that you want to include in the webhook payload, such as "Content-Type: application/json" or "Authorization: Bearer &lt;token&gt;".

</td></tr></tbody>
</table>    **Note:** If you don’t select at least one action, the automation is deactivated.

8.  In the **And finally** section, to continue running other response automations with same filter conditions after this automation is executed, select **Run other response automations**.

    If you select **Don't run response automations**, additional automations of this type will stop running after this automation is executed once. If the automation is managed by an administrator, it will stop running administrator-owned automations but will continue to run automations owned by other assignment groups.

9.  In the **Automation details** section, provide an order and automation description.

    \[Omitted image "respond-automation-details.png"\] Alt text: Respond automation details section

    For information on the Automation details fields, see []().

10. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed.

    The response automation that you created appears on the All response automations page where you can view, edit, or delete the existing automations.


