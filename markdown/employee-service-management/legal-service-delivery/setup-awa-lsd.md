---
title: Set up Advanced Work Assignment for Legal Service Delivery
description: Configure various components, such as service channels, work item queues, and assignment rules that determine how a legal request should be routed to an agent.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Advanced Work Assignment for Legal Service Delivery, Advanced work assignment for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Set up Advanced Work Assignment for Legal Service Delivery

Configure various components, such as service channels, work item queues, and assignment rules that determine how a legal request should be routed to an agent.

## Before you begin

Role required: admin

The base system includes the Advanced Work Assignment solution for General Legal Requests and Ethics Complaints. You can also configure it for other types of legal requests.

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming legal requests to agents.

    For more information, see [Create or configure a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    The following service channels are available in the base system Advanced Work Assignment for Legal Service Delivery.

    -   Legal Request
    -   Chat
    After you have created a service channel, do the following:

    1.  Configure the agent capacity to determine the number of work items that can be automatically assigned to agents supporting a service channel. For more information, see [Override agent capacity for selected agents](https://www.servicenow.com/docs/access?context=awa-change-agent-capacity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see [Create or change an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information, see [Create or change a work item size override](https://www.servicenow.com/docs/access?context=awa-modify-work-item-size&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
3.  Make your service channel available in Agent Workspace by adding it to the Presence States.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Presence States**.

    2.  Select **Available**.

    3.  On the form, move the following to selected list.

        -   Legal Request
        -   Chat
    4.  Select Active \(if not already selected\).

    5.  Select **Update**.

4.  Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.

    For more information, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    The following queues are available in the base system for Advanced Work Assignment for Legal Service Delivery.

    -   General Legal Request
    -   Ethics Complaint
5.  Set the Advanced Work Assignment criteria for assigning work items to agents.

    For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    An assignment rule Capacity and skill based assignment for Legal Requests is available in the base system for Advanced Work Assignment for Legal Service Delivery.

6.  Use Skill Determination Rules as an alternative way to map skills to an legal request case.

    If you are going to use skill determination rules to map a skill to an legal request, activate Skills Management. For more information, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    Skill determination rule for Legal is available in the base system for Advanced Work Assignment for Legal Service Delivery.

7.  Configure the following parameters to improve your Advanced Work Assignment functionality:

    1.  Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox. For more information, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Add the service channel to
    2.  Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. For more information, see [Configure reasons for rejecting work items](https://www.servicenow.com/docs/access?context=awa-configure-reject-reasons&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    3.  Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. For more information, see [Configure an agent's maximum universal capacity](https://www.servicenow.com/docs/access?context=awa-universal-capacity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    4.  Create or manage groups that have associated Advanced Work Assignment queues. For more information, see [Create or change groups for Advanced Work Assignment queues](https://www.servicenow.com/docs/access?context=awa-groups&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

        The following queues are available in the base system for Advanced Work Assignment for Legal Service Delivery.

        -   Legal - Ethics
        -   Legal Department
    For detailed instructions on how to configure Advanced Work Assignment, see [Configuring Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installing-awa&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


