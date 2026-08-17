---
title: Summarize an insurance customer interaction in Agentic Contact Center for Insurance
description: Use the Insurance interaction context summary skill to generate an AI-powered summary of a customer's insurance context, recent cases, and call reason during live interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/summarize-insurance-customer-context.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [insurance interaction context summary, summarize insurance customer interaction, relevant details for this call, insurance interaction page ai summary, now assist insurance interaction skill, insurance csr interaction summary, agentic contact center insurance context summary]
breadcrumb: [Using Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Summarize an insurance customer interaction in Agentic Contact Center for Insurance

Use the Insurance interaction context summary skill to generate an AI-powered summary of a customer's insurance context, recent cases, and call reason during live interactions.

## Before you begin

Role required: sn\_ins\_csr.personal\_agent, sn\_ins\_csr.business\_agent

## About this task

The Insurance interaction context summary skill is used as part of Agentic Contact Center for Insurance to provide insurance customer service representatives \(CSRs\) with real-time interaction summaries and relevant customer context.

The summary is displayed in the **Relevant details for this call** card in the Interaction page. The card is generated automatically when an interaction begins and is updated as the conversation progresses. When the Insurance interaction context summary skill is not activated, this card is not displayed. For information about activating the skill, see [Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-interaction-summary-skill.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Accept an inbound call or create an interaction record to open the Interaction page.

3.  After verifying the customer's identity, review the **Relevant details for this call** card.

    The card displays the following sections:

    -   **Customer**: How long the customer has been with the organization.
    -   **Contacting about**: The customer's likely reason for calling, derived from the live call transcript. When no transcript is available, this section is populated from the interaction short description.
    -   **Related contact**: The most recent previous contact with the customer regarding the same product, including the date and subject of that contact.
    -   **Related cases**: The last three cases related to the product the customer is currently inquiring about, including the case number, status, date raised, and reason.
    -   **Related products**: The insurance product the customer is currently inquiring about, including the product name and premium due date.
    **Note:** The **Relevant details for this call** card is not displayed until the customer's identity has been verified. The card is also not displayed when no call context is available and no short description has been provided on the interaction record.


## What to do next

To get additional AI-powered assistance during the call, select **Ask Otto** in the Interaction page. For more information, see [Request AI agent support in the Interaction page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/request-insurance-ai-agent-interaction-workspace.md).

**Related topics**  


[Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-interaction-summary-skill.md)

[Request AI agent support in the Interaction page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/request-insurance-ai-agent-interaction-workspace.md)

