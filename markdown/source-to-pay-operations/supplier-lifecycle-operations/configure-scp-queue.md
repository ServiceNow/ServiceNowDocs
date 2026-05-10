---
title: Configure the Supplier Collaboration Queue
description: Configure the Supplier Collaboration Queue chat queue to ensure that the chat requests are routed and assigned to specific agents that belong to a defined group.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up Advanced Work Assignment for Supplier Lifecycle Operations, Advanced Work Assignment for Supplier Lifecycle Operations, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure the Supplier Collaboration Queue

Configure the Supplier Collaboration Queue chat queue to ensure that the chat requests are routed and assigned to specific agents that belong to a defined group.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Queues**.

2.  Select **Supplier Collaboration Queue**.

    For more information about the fields on the Supplier Collaboration Queue form, see [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-queue.md).

3.  In the **Initial agent response** field, enter the message that you want the users to see when an agent accepts a chat.

    For example: `Thank you for contacting support. I am looking into your question now and will be with you shortly.`

4.  In the **Max wait time message** field, enter the message that you want the users to see when a chat ends after the Max Wait Time has elapsed.

    This field is required if the **Max Wait Time** is greater than 0.

5.  In the **Target wait time** field, enter the estimated time \(Days or Hours, minutes, seconds\) you want allotted for an agent to accept an item in the queue.

6.  In the Max Wait Time field, enter the maximum amount of time within which all available agents have to accept or reject a chat request.

    After time runs out, the requester receives the value in either the **Max wait time message** field or the **No Agents Available Message** field defined in [Agent Chat settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ac-configure-agent-chat.md).

    **Note:** The **Max Wait Time** field is available after you associate the queue to the chat service channel.

7.  In the Assignment Eligibility related list, select **New**.

    1.  In the **Agent assignment rule** field, select **Chat - Most Capacity**.
    2.  Click the lock icon \(![Lock icon](../image/lock-icon.png)\) next to the **Groups** field.
    3.  Click the look-up icon \(![Look-up icon](../image/look-up-icon.png)\) to view the list of groups.
    4.  Select **New**.
    5.  In the **Name** field, enter a name for the group.
    6.  Fill in the remaining fields, as appropriate.
    7.  Select **Submit**.
    8.  Click the lock icon \(![Lock icon](../image/lock-icon.png)\) to lock the **Groups** field.
    9.  Right-click and select **Save**.
8.  Next to the **Groups** field, select the link to the group, which opens the group record.

    1.  In the Group Members related list, select **Edit** to add members to the group.
    2.  Select one or more users in the Collection list and move them to the Group Members List.
    3.  Select **Save**.

        **Note:** The users that you add to this assignment group are automatically granted the awa\_agent role.


**Parent Topic:**[Setting up Advanced Work Assignment for Supplier Lifecycle Operations](../concept/awa-slm-config.md)

