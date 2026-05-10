---
title: Set up an Advanced Work Assignment service channel for assigning case tasks
description: Set up an Advanced Work Assignment \(AWA\) service channel that you can use to assign case tasks to available users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [AWA for CSM, Case routing and assignment, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up an Advanced Work Assignment service channel for assigning case tasks

Set up an Advanced Work Assignment \(AWA\) service channel that you can use to assign case tasks to available users.

## Before you begin

Role required: admin

You can use the [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md) \(AWA\) feature to automatically assign work items to users based on their availability and capacity.

AWA assigns work items using assignment groups so it's important that your users and groups are set up correctly.

-   Determine the assignment group to use in the AWA service channel configuration and add users to this group.
-   Add the **Assignment Group** field to the Case Task form view and make the field mandatory.
-   Ensure that the users in the assignment group have access to case tasks.

    **Note:** By default, CSM uses assignment groups to control visibility to case tasks. Therefore the logic to assign a case task to the correct assignment group is triggered when a case task is created.


## About this task

Setting up a service channel involves multiple steps, which are detailed in the following procedure. Once the service channel setup is complete, you can use AWA to assign newly created case tasks that:

-   Are unassigned.
-   Satisfy the conditions specified in the service channel.
-   Have the configured AWA assignment group selected in the **Assignment Group** field on the Case Task form.

## Procedure

1.  Create the case task service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Service Channels** and click **New**.

    2.  Fill in the fields on the Service Channel form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the service channel that you are configuring. For example, Case Task.|
        |Inbox order|Order in which channel items appear in the user inbox. The **Inbox Order** field is an integer [field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_FieldTypes.md). This field can store whole numbers.|
        |Application|Name of the application. For the Case Task channel, select Customer Service.|
        |Active|Option for activating the service channel. When you select this option, the associated queues for the service channel can start accepting work items.|
        |Short description|Brief description of the service channel.|
        |Table|Table that stores the service channel records. To route case tasks, select the Task \(sn\_customerservice\_task\) table.|
        |Assign to field|Field that references the user that the item is assigned to. For the Task table, this field is the **Assigned to** \(assigned\_to\) field.|
        |Assignment group field|Field that references the assignment group that the item is assigned to. For the Task table, this field is the **Assignment group** field.|
        |Advanced condition|If enabled, the advanced conditions that apply to the channel. For case tasks, the parent case is active: **\[Active\] \[is\] \[true\]**.|
        |Default work item size|Amount of a user's capacity that is used if this work item is assigned. The default is 1.|
        |Default capacity|Number of items automatically assigned to agents \(pending overrides\). The default for this field depends on the type of work item.|
        |Utilization condition|Condition that determines what constitutes an active item that counts toward user workload/capacity. For case tasks: **\[State\] \[is not\] \[Closed\]**.|

    3.  Click **Submit**.

        The system adds the Case Task channel to the Service Channels list.

    For more information about creating an AWA service channel, see [Create a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md).

2.  Configure the layout for the case task inbox card.

    1.  Click **Case Task** in the Service Channel list to open the record.

    2.  In the Inbox Layout related list, click **Default Case Task layout**.

    3.  Add the following fields to the card layout.

        -   **Field 1**: Number
        -   **Field 2**: Subject
        -   **Field 3**: Parent Number
    4.  Click **Update**.

    For more information about configuring the card layout, see [Create or modify an inbox layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-modify-inbox-layout.md).

3.  Create a queue for the case task service channel.

    1.  In the Queue related list, click **New**.

    2.  Fill in the following fields on the Queue form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the queue. For example, Case Task Assignment.|
        |Short description|Brief explanation of the queue. For example, Assign case tasks to middle office users.|

    3.  Click **Submit**.

    For more information about configuring a queue, see [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-queue.md).

4.  Create an assignment rule for the Case Task Assignment queue.

    1.  Navigate to **Advanced Work Assignment** &gt; **Assignment Rules** and click **New**.

    2.  Fill in the fields on the Assignment Rule form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the assignment rule.|
        |Short description|Brief description of the assignment rule. For example, Assign the case tasks based off this configuration.|
        |Assign by|Type of assignment. Select **Most Capacity**, which routes a work item to the user who has the greatest availability for handling the work.|
        |Allow agents to reject|In the Rejection handling form section, enable this check box to enable users to reject work items in their inbox.|

    3.  Click **Submit**.

    For more information about creating an assignment rule, see [Configure agent assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-assignment-rule.md).

5.  Create a group for the Case Task Assignment queue.

    1.  Navigate to **Advanced Work Assignment** &gt; **Management** &gt; **Groups** and click **New**.

    2.  Fill in the fields on the Group form and click **Submit**.

    3.  Click the group to display the Group form.

    4.  In the Group Members related list, add users to the group.

        The users that you add to the group for the Case Task Assignment queue require the following roles:

        -   Case task agent \(sn\_customerservice.case\_task\_agent\)
        -   AWA agent \(awa\_agent\)
    For more information about creating a group, see [Create or modify groups for Advanced Work Assignment queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-groups.md)

6.  Associate the assignment rule with the Case Task Assignment queue.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues** and click the Case Task Assignment queue.

    2.  In the Assignment Eligibility related list on the Queue form, click **New**.

    3.  Select the case task assignment rule in the **Agent assignment rule** field.

    4.  Select the case task assignment group in the **Groups** field.

    5.  Click **Submit**.

7.  Activate the service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  Click the **Available** presence state and add the case task service channel to the **Selected** column.

    3.  Click **Update**.

    Once the service channel is activated, you can use it to assign work items. For more information, see [Service channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-service-channels.md).


