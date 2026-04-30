---
title: Configure Advanced Work Assignment route email interactions
description: Configure Advanced Work Assignment  \(AWA\) to route email interactions automatically to your agents, based on their availability, capacity, and optionally, skills.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure Advanced Work Assignment route email interactions

Configure Advanced Work Assignment  \(AWA\) to route email interactions automatically to your agents, based on their availability, capacity, and optionally, skills.

## Before you begin

Role required: admin

## About this task

The Service channel **Email** is configured during the installation of the Email Interaction for CSM application. If you want to create service channels for email, follow the procedure.

You can use the  [Advanced Work Assignment \(AWA\)](https://www.servicenow.com/docs/access?context=awa-overview&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) feature to automatically assign work items to users based on their availability and capacity.

AWA assigns work items using assignment groups, so it's important that your users and groups are set up correctly.

-   Determine the assignment group to use in the AWA service channel configuration and add users to this group.
-   Confirm that the users have at least one of the roles: sn\_customerservice.consumer\_agent or sn\_customerservice\_agent.

Setting up a service channel involves multiple steps, which are detailed in the procedure. Once the service channel setup is complete, you can use AWA to assign newly created email interactions that either unassigned or satisfy the conditions specified in the service channel.

## Procedure

1.  Create the email service channel.

    1.  Navigate to  **All** &gt; **Advanced Work Assignment ** &gt; **Settings** &gt; **Service Channels** &gt; **New**

    2.  Fill in the fields on the Service Channel form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the service channel that you’re configuring. For example, Custom-Email.|
        |Inbox order|Order in which channel items appear in the user inbox. The  **Inbox Order**  field is an integer  [field type](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). This field can store whole numbers.|
        |Application|Name of the application. For the Email Interaction channel, select Email Interaction for CSM.|
        |Active|Option for activating the service channel. When you select this option, the associated queues for the service channel can start accepting work items.|
        |Short description|Brief description of the service channel.|
        |Table|Table that stores the service channel records. To route email interactions, select the Interaction table.|
        |Assign to field|Field that references the user that the item is assigned to. For the Interaction table, this field is the ** Assigned to  field** \(assigned\_to\) field.|
        |Assignment group field|Field that references the assignment group that the item is assigned to. For the Interaction table, this field is the  **Assignment group  field** field.|
        |Advanced condition|Advanced conditions that apply to the channel.|
        |Default work item size|Amount of a user's capacity that is used if this work item is assigned. The default is 1.|
        |Default capacity|Number of items automatically assigned to agents \(pending overrides\). The default for this field depends on the type of work item.|
        |Utilization condition|Condition that determines what constitutes an active item that counts toward user workload/capacity.|

    3.  Select **Submit**.

    The system adds the Email Interaction channel to the Service Channels list. For more information, see  [Create or configure a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

2.  Configure the layout for the email interaction inbox card.

    **Note:** The Inbox layouts are configured during the installation of the Email Interaction for CSM application.

     If you want to create Inbox layouts follow the procedure in [Create or modify an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for **Email** service channel, available by default, or **Custom-Email** service channel.

3.  Create a queue for the email interaction service channel.

    1.  In the Queue related list of the service channel, select  **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the queue. For example, Email Queue.|
        |Short description|Brief explanation of the queue. For example, "Assign email interactions to front-office users".|

        For more information about configuring a queue, see  [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    3.  Select **Submit**.

4.  Create an assignment rule for the queue.

    1.  Navigate to  **All** &gt; **Advanced Work Assignment ** &gt; **Settings** &gt; **Assignment Rules **.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the assignment rule.|
        |Short description|Brief description of the assignment rule. For example, Assign the email interactions based on this configuration.|
        |Assign by|Type of assignment. Select **Most Capacity**, which routes a work item to the user who has the greatest availability for handling the work.|
        |Allow agents to reject|Option to enable agents to reject work items in their inbox.|

        For more information about creating an assignment rule, see  [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

5.  Create a group for the queue.

    1.  Navigate to  **All** &gt; **Advanced Work Assignment ** &gt; **Management** &gt; **Groups.**

    2.  Select **New**.

    3.  On the Group form, fill in the fields.

        For more information about creating a group, see [Create or change groups for Advanced Work Assignment queues](https://www.servicenow.com/docs/access?context=awa-groups&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    4.  Select **Submit**.

    5.  Select the group to display the Group form.

    6.  In the Group Members related list, add users to the group.

        The users that you add to the group for the Email Interaction Assignment queue require the roles.

        -   Customer agent \(sn\_customerservice\_agent\)
        -   Consumer agent \(sn\_customerservice.consumer\_agent\)
        -   AWA agent \(awa\_agent\)
6.  Associate the assignment rule with the queue.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  Select the queue.

        For example, Email Queue.

    3.  In the Assignment Eligibility related list on the Queue form, select **New**.

    4.  In the **Agent assignment rule** field, select the assignment rule.

    5.  In the **Groups** field, select the assignment group.

    6.  Select **Submit**.

7.  Activate the service channel.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  Select the **Available** presence state.

    3.  Add the email service channel to the **Selected** column.

    4.  Select **Update**.


## Result

After the service channel is activated, you can use it to assign work items. For more information, see [Service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

