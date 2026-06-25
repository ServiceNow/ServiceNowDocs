---
title: Interaction page for Agentic Contact Center for Insurance
description: The Interaction page is a dedicated workspace for insurance CSR \(customer service representative\) agents. It consolidates customer identification, interaction history, and live call transcript analysis into a single view during active customer interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/interactionpage-agentic-contact-centre-for-insurance.html
release: australia
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 4
keywords: [insurance contact center, interaction page, interaction workspace, live call transcript, ai-driven assistance, customer context summary, interaction form, wrap-up, handle customer calls, active customer interaction, csr interaction, call transcript analysis]
breadcrumb: [Exploring Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Interaction page for Agentic Contact Center for Insurance

The Interaction page is a dedicated workspace for insurance CSR \(customer service representative\) agents. It consolidates customer identification, interaction history, and live call transcript analysis into a single view during active customer interactions.

The Interaction page opens automatically when a CSR accepts a customer interaction, such as an inbound voice call. CSRs use this page during an active interaction with an insurance customer. It combines policyholder information, contextual history, and AI-powered assistance in a single page. The CSR can manage the entire interaction in this page—from the first interaction to case creation and wrap-up.

## Live transcript and AI-driven assistance

During an active voice interaction, a live transcript of the conversation is captured. The transcript serves as the primary input for the AI agent that powers the Now Assist panel.

As the conversation progresses, the AI agent processes the customer's request, and displays relevant information and recommended next steps in the Now Assist panel when the CSR requests recommendations . The AI agent queries customer records, Knowledge Graph, and your configured knowledge bases.

CSRs can also type their own questions directly into the Now Assist panel at any time. The panel displays responses from the AI agent in a structured format that may include insights, recommendations, and guidance based on the content and sentiment of the conversation.

For more information, see Agentic Contact Center for Insurance .

## Policyholder context summary

The customer context summary provides the CSR with an AI-generated overview of the customer before and during the call. This context-based summary is generated from the customer's profile, policies, recent interactions, and case history at the time the interaction begins, providing the CSR with immediate context without manual research .

The customer summary includes:

-   Customer or account details
-   Similar issues that the customer has previously contacted the insurer about
-   Policies and coverages affected by the current issue
-   Related cases

The customer summary is not visible when no account or consumer has been associated with the interaction.

For more information, see  .

## Interaction form

The **Interaction** section displays a form that shows the following fields:

|Field|Description|
|-----|-----------|
|Number|The interaction record number.|
|State|The state of the record.|
|Type|The channel where the interaction was initiated.|
|Assigned to|The contributor assigned to the interaction.|
|Consumer / Account|The consumer or account record associated with the interaction.|
|Verified|Indicates whether the customer's identity has been verified by the contributor during the interaction.|
|Short description|A brief description of the nature of the interaction.|
|Work notes|Notes or remarks about the interaction .|

## Other page sections

The following table lists other sections in the Interaction page. Page content varies depending on whether the customer is an individual policyholder \( business-to-consumer \(B2C\) \) or a commercial one \( business-to-business \(B2B\) \).

|Name|Customer type|Description|
|----|-------------|-----------|
|Customer details|Account|Displays the customer name, primary contact, phone number, email address, industry, and doing-business-as name.|
|Customer|Displays the policyholder's name, address information, date of birth, nationality, phone number, and email.|
|Customer history|Both|Includes all customer activity, such as cases created, past interactions, and knowledge bases accessed.|

## Contextual side panel

The contextual side panel appears and provides access to supplementary tools and record-related information. The panel tabs are displayed in the following order:

1.  Related lists—includes Related Tasks, Recent Interactions, Open Cases, and Insurance Policies
2.  Activity stream
3.  Attachments
4.  Templates
5.  Recommended Actions

The Activity stream tab displays the activity stream for the interaction record, enabling CSRs to review and add notes without leaving the page.

## Wrap-up

The CSR wraps up the interaction when it concludes. When wrap-up codes are set up and the Wrap Up Completion Now Assist skill is configured, the CSR can generate an AI-powered chat summary. This summary provides a record of what is discussed and any action items in the interaction.

For more information, see the following topics:

-   [Interaction wrap up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-wrap-up-state.md)
-   [Use AI to generate wrap up code and notes summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-generated-wrap-up-codes-and-notes-summary.md)

**Related topics**  


[CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md)

[Exploring Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/explore-agentic-contact-center-for-insurance.md)

[Customer 360 page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/customer-360-insurance-agentic-contact-centre.md)

