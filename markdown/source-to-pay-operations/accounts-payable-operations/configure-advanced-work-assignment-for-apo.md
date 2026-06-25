---
title: Configure Advanced Work Assignment for Accounts Payable Operations
description: Set up Advanced Work Assignment to automatically route Accounts Payable Operations requests from email, chat, and messenger to the appropriate agent groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/configure-advanced-work-assignment-for-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, email ingestion, Advanced Work Assignment, AWA]
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Advanced Work Assignment for Accounts Payable Operations

Set up Advanced Work Assignment to automatically route Accounts Payable Operations requests from email, chat, and messenger to the appropriate agent groups.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment**.

2.  Create a service channel to automatically route incoming work to agents.

    For more information about creating service channels, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-service-channel.md) Service channels specific to Accounts Payable Operations are:

    -   Invoice Inquiry Cases
    -   Chat
    **Note:** You can customize the service channel of your choice for any work that would have come through by any mode other than email, chat, messenger.

    After you've created the service channel, do the following.

    1.  Configure the agent capacity to determine the number of work items that can be assigned to agents belonging to a defined group. For more information, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-change-agent-capacity.md)
    2.  Create or change an inbox layout to determine the information shown on work item cards displayed in an agent's inbox. For more information, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-modify-inbox-layout.md)
    3.  Create a work item size override if you want to calculate an agent's workload using a work item size other than the default. For more information on work item, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-modify-work-item-size.md)
    Define or modify a work item queue, which determines the work items to be routed automatically to agents assigned to a service channel. For more information on queues, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md)

3.  To assign queues, work items to agents, follow steps 3–5 from [Configure Advanced Work Assignment for Source-to-Pay Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-awa-spo.md).


-   **[Configure the Accounts Payable Operations queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/configure-the-account-payable-operation-queues.md)**  
Configure Advanced Work Assignment queues to automatically route supplier communications, including email and chat to the appropriate accounts payable agents.
-   **[Configure Agent chat for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/configure-agent-chat-for-accounts-payable-operations.md)**  
Configure agent chat settings in Accounts Payable Operations to enable AP agents to interact with suppliers through live chat.

**Parent Topic:**[Use Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice]()

[Invoice case categories and subcategories]()

[Using Invoice Case Management]()

[Using Accounts Payable Invoice Processing]()

[Advanced Work Assignment in Accounts Payable Operations]()

[Using Advanced Work Assignment for Accounts Payable Operations]()

[Working with Advanced Work Assignment]()

[Interaction management in Accounts Payable Operations]()

[Composing emails with predefined content from the Source-to-Pay Workspace]()

[Universal Request in Accounts Payable Operations]()

[Playbook for updating the invoice primary data]()

[Using Supplier Collaboration Portal in APO]()

