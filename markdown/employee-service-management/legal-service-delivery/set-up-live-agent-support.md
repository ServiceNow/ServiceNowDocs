---
title: Configure live agent support settings for legal services
description: Configure settings to enable live agent support for legal services.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Live agent support for legal services, Legal Virtual Agent Conversations, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure live agent support settings for legal services

Configure settings to enable live agent support for legal services.

## Before you begin

-   Ensure that you have the following applications installed:
    -   Legal Request Management
    -   Legal Virtual Agent Conversations
    -   Legal Counsel Center
-   Ensure you select **Load demo data** while installing Agent Chat.
-   Ensure the user has legal fulfiller \(sn\_lg\_ops.legal\_fulfiller\) role to use the Agent Chat.

Role required: admin

## Procedure

1.  Install Agent Chat along with the demo data.

    For more information, see [Agent Chat](https://www.servicenow.com/docs/access?context=migrate-from-connect-support&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

2.  Configure the assignment rule to provide the criteria for routing the chat conversations to live agents in the Legal department.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Assignment Rules**.

    2.  Open the base system assignment rule **Legal Chat Assignment Rule**.

    3.  Update fields as required.

        For more information on the fields, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    4.  Click **Update**.

3.  Configure the work item queue and the associated assignment eligibility.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  Open the base system Queue **Legal Chat**.

    3.  Update fields as required.

        For more information on the fields, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    4.  Click **Update**.

    5.  In the Assignment Eligibility related list, open the base system record **Legal Department**.

    6.  Update fields as required.

        For more information on the fields, see [Define Assignment Eligibility](https://www.servicenow.com/docs/access?context=awa-specify-assignment-eligibility&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


**Parent Topic:**[Live agent support for legal services](../concept/legal-va-live-agent.md)

