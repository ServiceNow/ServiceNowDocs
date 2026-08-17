---
title: Request AI agent support in the Interaction page
description: Request AI-powered assistance during customer interactions to receive real-time insights, intent identification, and recommended responses. The Banking CSR support AI agent analyzes call context and transcripts to provide next-step guidance and suggested actions within the Interaction page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/request-ai-agent-interaction-workspace.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Request AI agent support in the Interaction page

Request AI-powered assistance during customer interactions to receive real-time insights, intent identification, and recommended responses. The Banking CSR support AI agent analyzes call context and transcripts to provide next-step guidance and suggested actions within the Interaction page.

## Before you begin

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

## About this task

When an interaction with a customer begins, the Banking CSR support AI agent will begin identifying customer intent from the call context and transcript. It will present insights from its findings, then provide next-step guidance with recommendations and suggested responses.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Initiate an interaction when a customer contacts you.

3.  In the Interaction page, select **Ask Otto**.

    **Note:** By default, **Ask Otto** is available when:

    -   The interaction **Type** is Phone.
    -   The **Consumer** or **Account** field is not empty.
    -   The interaction **State** is Work in Progress.
    -   The **Assigned to** value is not set to virtual agent.
    The ServiceNow Otto panel displays. The Banking CSR support AI agent starts processing information in data sources and the interaction. It displays information related to the customer's request and presents a list of follow-up options.

    The chat will be specific to this interaction record. If you navigate away, you can resume the chat by selecting **Ask Otto**.

4.  Select a follow-up option by selecting a pill or list option, or by directly responding to the AI agent in the chat.


## Result

The AI agent answers your questions using information from its configured knowledge sources.

**Parent Topic:**[Using Agentic Contact Center for Banking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/using-agentic-contact-center-for-banking.md)

**Related topics**  


[Agentic Contact Center for Banking AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/agentic-contact-center-for-banking-agents-overview.md)

