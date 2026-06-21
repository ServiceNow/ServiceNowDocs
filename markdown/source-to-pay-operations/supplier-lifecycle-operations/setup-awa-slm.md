---
title: Configure Advanced Work Assignment for Supplier Lifecycle Operations
description: Configure various components, such as service channels, work item queues, and assignment rules that determine how a chat interaction should be routed to an agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/supplier-lifecycle-operations/setup-awa-slm.html
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Advanced Work Assignment for Supplier Lifecycle Operations, Advanced Work Assignment for Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure Advanced Work Assignment for Supplier Lifecycle Operations

Configure various components, such as service channels, work item queues, and assignment rules that determine how a chat interaction should be routed to an agent.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming work to agents.

    For more information, see .

    The following service channels are specific to Advanced Work Assignment for Supplier Lifecycle Operations.

    -   Supplier Cases
    -   Chat
    After you have created a service channel, do the following:

    1.  Configure the agent capacity to determine the number of work items that can be automatically assigned to agents supporting a service channel. For more information, see .
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see .
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information, see .
3.  Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.

    For more information, see .

4.  Set the Advanced Work Assignment criteria for assigning work items to agents.

    For more information, see .

5.  Configure the following parameters to improve your Advanced Work Assignment functionality:

    1.  Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox. For more information, see .
    2.  Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. For more information, see .
    3.  Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. For more information, see .
    4.  Create or manage groups that have associated Advanced Work Assignment queues. For more information, see .
    For detailed instructions on how to configure Advanced Work Assignment, see .


**Parent Topic:**[Setting up Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/awa-slm-config.md)

