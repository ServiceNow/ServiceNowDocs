---
title: Request AI agent support in the Interaction page for Agentic Contact Center for Insurance
description: Request AI-powered assistance during insurance customer interactions to receive real-time insights, intent identification, and recommended responses. The Insurance CSR support AI agent analyzes call context and transcripts to provide next-step guidance and suggested actions within the Interaction page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/request-insurance-ai-agent-interaction-workspace.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [insurance csr support ai agent, request insurance ai agent interaction page, insurance interaction page now assist, insurance csr live call assistance, get customer request insurance, insurance ai agent transcript, agentic contact center insurance ai support]
breadcrumb: [Agentic Contact Center for Insurance AI agents overview, AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Request AI agent support in the Interaction page for Agentic Contact Center for Insurance

Request AI-powered assistance during insurance customer interactions to receive real-time insights, intent identification, and recommended responses. The Insurance CSR support AI agent analyzes call context and transcripts to provide next-step guidance and suggested actions within the Interaction page.

## Before you begin

Role required: sn\_ins\_csr.personal\_agent, sn\_ins\_csr.business\_agent

## About this task

When an interaction with an insurance customer begins, the Insurance CSR support AI agent identifies customer intent from the live call context and transcript. It surfaces insights from its findings, then provides next-step guidance with recommendations and suggested responses.

The agent operates in two input modes:

-   **Typed query**: The CSR types a question directly into the Now Assist panel at any point during the call.
-   **Button-triggered**: The CSR selects **Get customer request** and the agent reads the latest call transcript to infer the customer's most recent question, without the CSR needing to rephrase it manually.

The agent responds only to questions within insurance scope and only about the customer on the current interaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Initiate an interaction when a customer contacts you.

3.  In the Interaction page, select **Ask Now Assist**.

    **Note:** By default, **Ask Now Assist** is available when:

    -   The interaction **Type** is Phone.
    -   The **Consumer** or **Account** field is not empty.
    -   The interaction **State** is Work in Progress.
    -   The **Assigned to** value is not set to virtual agent.
    The Now Assist panel displays. The Insurance CSR support AI agent starts processing information from the call transcript and the customer's insurance data. It displays information relevant to the customer's request and presents follow-up options as selectable pills.

    The chat is specific to this interaction record. If you navigate away, you can resume the chat by selecting **Ask Now Assist**.

    For more information, see [Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md).

4.  Get a response from the agent using one of the following methods:

    -   Type a question directly into the Now Assist panel and press Enter to submit it.
    -   Select **Get customer request** to have the agent read the latest call transcript and infer the customer's most recent question automatically.

        The agent retrieves new transcript segments since the last pull and uses them to identify the customer's current request without requiring manual input from the CSR.

5.  Select a follow-up option by selecting a pill or list option, or by directly responding to the agent in the chat.


## Result

The agent answers your questions using information from the customer's insurance records and its configured knowledge sources. Responses are structured for quick review during a live call.

**Parent Topic:**[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md)

**Related topics**  


[Agentic AI use cases for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/usecase-now-assist.md)

[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md)

[Summarize an insurance customer interaction in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-context.md)

