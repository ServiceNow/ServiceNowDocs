---
title: Configure Advanced Work Assignment for Source-to-Pay Operations
description: Configure various components, such as service channels, work item queues, and assignment rules that determine how emails and chat interactions should be routed to agents.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Advanced Work Assignment for Source-to-Pay Operations, Advanced Work Assignment for Source-to-Pay Operations, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure Advanced Work Assignment for Source-to-Pay Operations

Configure various components, such as service channels, work item queues, and assignment rules that determine how emails and chat interactions should be routed to agents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming work to agents.

    For more information, see [Create or configure a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    The following service channels are specific to Advanced Work Assignment for Source-to-Pay Operations.

    -   Procurement Cases: For more information,see [Automatic case creation from emails](../concept/case-creation-from-emails.md).
    -   Chat. For more information,see [Using Advanced Work Assignment for Source-to-Pay Operations](../concept/using-awa-spo.md).
    **Note:** Procurement administrators can also configure custom service channels for any work that may come through modes other than emails and chat, like SMS, or phone, for example.

    After you’ve created a service channel, do the following:

    1.  Configure the agent capacity to determine the number of work items that can be automatically assigned to agents supporting a service channel. For more information, see [Override agent capacity for selected agents](https://www.servicenow.com/docs/access?context=awa-change-agent-capacity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see [Create or change an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information, see [Create or change a work item size override](https://www.servicenow.com/docs/access?context=awa-modify-work-item-size&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
3.  Define or modify a queue so that you can determine which work items are routed automatically to agents through a given service channel.

    For more information, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

4.  Set the Advanced Work Assignment criteria for assigning work items to agents.

    For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

5.  Configure the following parameters to improve your Advanced Work Assignment functionality:

    1.  Create or modify the availability states that agents use to indicate whether they can receive work, or are offline or away. Agents set these states in their Workspace Inbox. For more information, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    2.  Define the reasons that agents can use to decline work assignments that they receive in their Workspace inbox. For more information, see [Configure reasons for rejecting work items](https://www.servicenow.com/docs/access?context=awa-configure-reject-reasons&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    3.  Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. For more information, see [Configure an agent's maximum universal capacity](https://www.servicenow.com/docs/access?context=awa-universal-capacity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    4.  Create or manage groups that have associated Advanced Work Assignment queues. For more information, see [Create or change groups for Advanced Work Assignment queues](https://www.servicenow.com/docs/access?context=awa-groups&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    For detailed instructions on how to configure Advanced Work Assignment, see [Configuring Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installing-awa&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Setting up Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo-setup.md)

