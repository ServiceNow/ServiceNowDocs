---
title: Interaction page for Agentic Contact Center for Banking
description: The Interaction page provides customer service representatives \(CSRs\) with a consolidated view of customer details, live call transcript analysis, and AI-driven assistance during active customer interactions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Interaction page for Agentic Contact Center for Banking

The Interaction page provides customer service representatives \(CSRs\) with a consolidated view of customer details, live call transcript analysis, and AI-driven assistance during active customer interactions.

CSRs use this page during an active interaction with a banking customer. It combines customer information, contextual history, and AI-powered assistance in a single page. When a CSR accepts an inbound call, the page opens automatically and displays the identified customer's details. The CSR can manage the entire interaction in this space—from first contact to case creation and wrap-up.

![Agentic contact center interface showing an active call with customer details and AI-generated assistance.](../images/agentic-contact-center-interaction.png)

## Live transcript and AI-driven assistance

During an active voice interaction, a live transcript of the conversation is captured. The transcript serves as the primary input for the AI agent that powers the Now Assist panel.

As the conversation progresses, the AI agent reads the transcript, interprets the customer's request, and surfaces relevant information and recommended next steps in the Now Assist panel whenever the CSR agent prompts it for recommendations. The AI agent references customer records, Knowledge Graph, and your configured knowledge bases.

CSRs can also type their own questions directly into the Now Assist panel at any time. The panel displays responses from the AI agent in a structured format that may include insights, recommendations, and guidance based on the content and sentiment of the conversation.

For more information, see [Agentic Contact Center for Banking AI agents overview](../../fso-now-assist/concept/agentic-contact-center-for-banking-agents-overview.md).

## Customer context summary

![Customer context summary panel showing customer information, contact reason, related cases, and related products with balances.](../images/agentic-contact-center-interaction-context-summary.png)

The customer context summary provides the CSR with an AI-generated overview of the customer before and during the call. This context-based summary is generated from the customer's profile, products, recent interactions, and case history at the time the interaction begins, giving the CSR immediate context without manual research.

The customer summary includes:

-   Customer or account details
-   Similar issues that the customer has previously contacted the bank about
-   Products affected by the current issue
-   Related cases

The customer summary is not visible when no account or consumer has been associated with the interaction.

For more information, see [Summarize customer interaction context in the Interaction page](../../fso-now-assist/task/summarize-customer-context-fso.md).

## Interaction form

The **Interaction** section displays form that shows the following fields:

|Field|Description|
|-----|-----------|
|Number|The interaction record number.|
|State|The state of the record.|
|Type|The channel where the interaction was initiated.|
|Assigned to|The contributor assigned to the interaction.|
|Consumer / Account|The consumer or account record associated with the interaction.|
|Verified|Indicates if the customer's identity has been verified by the contributor during the interaction.|
|Short description|A brief description of the nature of the interaction.|

## Other page sections

The following table lists other sections in the Interaction page. Its contents vary depending on whether the customer is a retail consumer \(B2C\) or a commercial account \(B2B\).

|Name|Customer type|Description|
|----|-------------|-----------|
|Customer details|Account|Displays the account name, primary contact, phone number, email address, industry, and doing-business-as name.|
|Customer|Displays the consumer's name, address information, date of birth, nationality, phone number, and email.|
|Customer history|Both|Includes all activities of the customer, including cases created, past interactions, and knowledge bases accessed.|

## Contextual side panel

The contextual side panel appears on the right side of the page and provides access to supplementary tools and record-related information. The panel tabs are displayed in the following order:

1.  Related lists—includes Related Tasks, Recent Interactions, Open Cases, and Financial Accounts
2.  Activity stream
3.  Attachments
4.  Templates
5.  Recommended Actions

The Activity stream tab displays the activity stream for the interaction record, allowing CSRs to review and add notes without leaving the page.

## Wrap-up

The agent wraps up the interaction when it concludes. When wrap-up codes are set up and the Wrap Up Completion Now Assist skill is configured, the agent can generate an AI-powered chat summary. This summary provides a record of what was discussed and any action items in the interaction.

For more information, see the following topics:

-   [Interaction wrap up](https://www.servicenow.com/docs/access?context=interaction-wrap-up-state&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Use AI to generate wrap up code and notes summary](https://www.servicenow.com/docs/access?context=ai-generated-wrap-up-codes-and-notes-summary&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

**Parent Topic:**[Financial Services](../../fso-common/concept/fso-overview.md)

**Related topics**  


[Exploring Agentic Contact Center for Banking](exploring-agentic-contact-center-for-banking.md)

[Customer 360 page for Agentic Contact Center for Banking](customer-360-agentic-contact-center-for-banking.md)

[CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

