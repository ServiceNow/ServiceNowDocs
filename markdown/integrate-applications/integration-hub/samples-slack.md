---
title: Automate and customize Slack tasks
description: Automate Slack tasks as per your requirement, using the sample these scenarios as a reference.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Automate and customize Slack tasks

Automate Slack tasks as per your requirement, using the sample these scenarios as a reference.

You can use the default outbound configurations, inbound decisions, and subflows as reference to customize tasks as per your requirement.

## Automate Slack commands

Perform these steps to automate events such as, create incident records, based on the Slack commands:

1.  Configure the Slack commands on the Slash Commands page of your custom application. For more information, see [Configure Slack app](../../integrationhub/tasks/configure-slack-workspace.md).
2.  In Workflow Studio, create a subflow configure to create the incident records as per your requirement or create a copy of the default subflow, Respond to Slack Command, and configure it.

    **Note:** Create an action and use the payload in the subflow input as per your requirement.

3.  [Configure inbound decisions in ServiceNow instance](../task/conf-inbound-slack.md).
    1.  In the **Condition**, ensure that you specify the value of **command** as `/now` and specify the required parameters.

        **Note:** You can specify up to 2 parameters in your condition to trigger the required subflow.

        ![Slack command](../image/slack-command.png)

    2.  In **Answer**, select the subflow you had configured.

When a Slack user enters the command, `/now create incident <text>`, the condition specified in inbound decision is met and the associated subflow is triggered. Similarly, you can customize subflows and inbound decisions to configure more Slack commands such as:

-   `/now list incidents` to list all active incidents assigned to the logged in user.
-   `/now help` to display all available commands and their describe usage.
-   `/now note [note]` to add notes to the required incident.
-   `/now create incident [short description] > [optional: urgency] > [optional: impact]` to create an incident with specified short description, urgency, and impact. For example, `/now create incident Email is not working > 3 > 2`.

## Automate message actions

1.  In your Slack custom application, create a shortcut that appears on messages and enter the value, `post_message_now` for **Callback ID**. For more information, see [Configure Slack app](../../integrationhub/tasks/configure-slack-workspace.md).
2.  In Workflow Studio, create a subflow configure to create the incident records as per your requirement or create a copy of the default subflow, Respond to Slack Message Action, and configure it.

    **Note:** Create an action and use the payload in the subflow input as per your requirement.

3.  [Configure inbound decisions in ServiceNow instance](../task/conf-inbound-slack.md).
    1.  In the **Condition**, ensure that you specify the value of **callback\_id** as `post_message_now` and specify the required parameters.

        ![Provide the required callback_id.](../image/message-action.png)

    2.  In **Answer**, select the subflow you had configured.

## Post an approval message

Perform these steps to automate posting an approval message on a Slack channel.

1.  In Workflow Studio, create a copy of the default subflow, Respond to Slack Approval Action, and configure it as per your requirement.

    **Note:** Create an action and use the payload in the subflow input as per your requirement.

2.  [Configure outbound configurations in ServiceNow instance](../task/conf-outbound-slack.md)
    1.  Open the default outbound configuration, **Approval Message**.
    2.  In **Action ID** , specify the unique identifier for automating the task of posting an acknowledgement message. For example, value of **Action ID** can be `approval_request`.
3.  [Configure inbound decisions in ServiceNow instance](../task/conf-inbound-slack.md).
    1.  In the **Condition**, ensure that you specify the value of **Action ID** as `approval_request`. You can specify other conditions as per your requirement.

        ![Provide value for Action ID.](../image/action-id.png)

    2.  In **Answer**, select the subflow you had configured.

When the Slack events match the relevant the action ID, the associated subflow, that is, the Respond to Slack Approval Action subflow is triggered. This subflow contains the logic to update the required record and send the relevant acknowledgement message on Slack channel.

## Assign request based on acknowledgement

Perform these steps to automate assigning request:

1.  In Workflow Studio, create a copy of the default subflow, On-Call Assign by Acknowledgement, and configure it as per your requirement.

    **Note:** Create an action and use the payload in the subflow input as per your requirement.

2.  [Configure outbound configurations in ServiceNow instance](../task/conf-outbound-slack.md).
    1.  Open the default outbound configuration, **On Call: Assign by Acknowledgement**.
    2.  In **Action ID** , specify the unique identifier for automating the task of posting an acknowledgement message. For example, value of **Action ID** can be `on_call_assign_by_acknowledgement`.
3.  [Configure inbound decisions in ServiceNow instance](../task/conf-inbound-slack.md).
    1.  In the **Condition**, ensure that you specify the value of **Action ID** as `on_call_assign_by_acknowledgement`. You can specify other conditions as per your requirement.
    2.  In **Answer**, select the subflow you had configured.

## Post an actionable message

Perform these steps to automate posting an actionable message:

1.  [Configure outbound configurations in ServiceNow instance](../task/conf-outbound-slack.md).
    1.  Open the default outbound configuration, **On Call: Assign by Acknowledgement**.
    2.  Select **Target Table** and **Fields** as per your requirement. For example, **short\_description** and **priority** from the **Task \[task\]** table.
    3.  Select **Buttons** as per your requirement. For example, `Accept` and `Reject`.
    4.  In **Action ID** , specify the unique identifier for automating the task of posting an acknowledgement message. For example, value of **Action ID** can be `on_call_assign_by_acknowledgement`.
2.  In Workflow Studio, create a copy of the default subflow, Post Actionable Message, and configure it as per your requirement.

    **Note:** Create an action and use the payload in the subflow input as per your requirement.

    1.  In the **Record Sys\_ID** input, provide the sys ID of the required record. For example, specify the sys ID of the task record.
    2.  In the **Template** input, select template you had created in the outbound configurations.
3.  [Configure inbound decisions in ServiceNow instance](../task/conf-inbound-slack.md).
    1.  In the **Condition**, ensure that you specify the value of **Action ID** as `on_call_assign_by_acknowledgement`. You can specify other conditions as per your requirement.
    2.  In **Answer**, select the subflow you had configured.

