---
title: Configure Advanced Work Assignment for Accounts Payable Operations
description: Configure AWA for APO to ensure that requests or queries received via email, chat, messenger are routed to the respective APO agents belonging to defined groups.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Advanced Work Assignment for Accounts Payable Operations

Configure AWA for APO to ensure that requests or queries received via email, chat, messenger are routed to the respective APO agents belonging to defined groups.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming work to agents.

    For more information about creating service channels, see [.](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) Service channels specific to Accounts Payable Operations are:

    -   Invoice Inquiry Cases
    -   Chat
    **Note:** You can customize the service channel of your choice for any work that would have come through by any mode other than email, chat, messenger.

    After you've created the service channel, do the following.

    1.  Configure the agent capacity to determine the number of work items that can be assigned to agents belonging to a defined group. For more information, see [.](https://www.servicenow.com/docs/access?context=awa-change-agent-capacity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see [.](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information on work item, see [.](https://www.servicenow.com/docs/access?context=awa-modify-work-item-size&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
    Define or modify a work item queue, which determines the work items to be routed automatically to agents assigned to a service channel. For more information on queues, see [.](https://www.servicenow.com/docs/access?context=awa-create-queue&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

3.  To assign queues, work items to agents, follow steps 3–5 from [Configure Advanced Work Assignment for Source-to-Pay Operations](../../sourcing-procurement-operations/task/configure-awa-spo.md).


-   **[Configure the Accounts Payable Operations queues](configure-the-account-payable-operation-queues.md)**  
Configure AWA for Accounts Payable Operations queues so that email, chat, and requests raised by suppliers are routed to respective agents belonging to the Accounts Payable supplier group.
-   **[Configure Agent chat for Accounts Payable Operations](configure-agent-chat-for-accounts-payable-operations.md)**  
Configure agent chat settings to interact with an Accounts Payable Operations agent.

**Parent Topic:**[Using Accounts Payable Operations](../concept/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice](create-knowledge-base-articles-for-invoices.md)

[Invoice case categories and subcategories](../concept/working-with-cases.md)

[Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

[Using Accounts Payable Invoice Processing](../concept/use-ap-invoice-processing.md)

[Advanced Work Assignment in Accounts Payable Operations](../concept/advanced-work-assignment.md)

[Using Advanced Work Assignment for Accounts Payable Operations](../concept/using-awa-for-apo.md)

[Working with Advanced Work Assignment](working-with-advanved-work-assignment.md)

[Interaction management in Accounts Payable Operations](../concept/interaction-record.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](../concept/email-composer-apm-workspace.md)

[Playbook for updating the invoice primary data](../concept/playbooks.md)

[Using Supplier Collaboration Portal in APO](../concept/using-supplier-collaboration-portal.md)

