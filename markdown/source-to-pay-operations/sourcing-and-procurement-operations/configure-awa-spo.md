---
title: Configure Advanced Work Assignment for Source-to-Pay Operations
description: Configure various components, such as service channels, work item queues, and assignment rules that determine how emails and chat interactions should be routed to agents.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up Advanced Work Assignment, Advanced Work Assignment Source-to-Pay Operations, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure Advanced Work Assignment for Source-to-Pay Operations

Configure various components, such as service channels, work item queues, and assignment rules that determine how emails and chat interactions should be routed to agents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming work to agents.

    For more information, see [Create or configure a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md).

    The following service channels are specific to Advanced Work Assignment for Source-to-Pay Operations.

    -   Procurement Cases: For more information,see [Automatic case creation from emails](../concept/case-creation-from-emails.md).
    -   Chat. For more information,see [Using Advanced Work Assignment for Source-to-Pay Operations](../concept/using-awa-spo.md).
    **Note:** Procurement administrators can also configure custom service channels for any work that may come through modes other than emails and chat, like SMS, or phone, for example.

    After you’ve created a service channel, do the following:

    1.  Configure the agent capacity to determine the number of work items that can be automatically assigned to agents supporting a service channel. For more information, see [Override agent capacity for selected agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-change-agent-capacity.md).
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see [Create or change an inbox layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-modify-inbox-layout.md).
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information, see [Create or change a work item size override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-modify-work-item-size.md).
3.  Define or modify a queue so that you can determine which work items are routed automatically to agents through a given service channel.

    For more information, see [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-queue.md).

4.  Set the Advanced Work Assignment criteria for assigning work items to agents.

    For more information, see [Configure agent assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-assignment-rule.md).

5.  Configure the following parameters to improve your Advanced Work Assignment functionality:

    1.  Create or modify the availability states that agents use to indicate whether they can receive work, or are offline or away. Agents set these states in their Workspace Inbox. For more information, see [Configure agent presence states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-configure-agent-presence.md).
    2.  Define the reasons that agents can use to decline work assignments that they receive in their Workspace inbox. For more information, see [Configure reasons for rejecting work items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-configure-reject-reasons.md).
    3.  Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. For more information, see [Configure an agent's maximum universal capacity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-universal-capacity.md).
    4.  Create or manage groups that have associated Advanced Work Assignment queues. For more information, see [Create or change groups for Advanced Work Assignment queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-groups.md).
    For detailed instructions on how to configure Advanced Work Assignment, see [Configuring Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installing-awa.md).


**Parent Topic:**[Setting up Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo-setup.md)

