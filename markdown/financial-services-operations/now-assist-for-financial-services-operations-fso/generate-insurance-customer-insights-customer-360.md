---
title: Generate customer insights in the Customer 360 page for Agentic Contact Center for Insurance
description: Use the Insurance CSR customer insights AI agent in the Customer 360 page to quickly access and understand a customer's insurance details, including policies, coverages, claims, and servicing history, without navigating away from the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/generate-insurance-customer-insights-customer-360.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [insurance csr customer insights ai agent, generate insurance customer insights, insurance customer 360 now assist, insurance ai agent customer 360, insurance policy insights, insurance claims insights, insurance coverage insights, agentic contact center insurance ai insights]
breadcrumb: [Agentic Contact Center for Insurance AI agents overview, AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Generate customer insights in the Customer 360 page for Agentic Contact Center for Insurance

Use the Insurance CSR customer insights AI agent in the Customer 360 page to quickly access and understand a customer's insurance details, including policies, coverages, claims, and servicing history, without navigating away from the workspace.

## Before you begin

Role required: sn\_ins\_csr.servicing\_agent, sn\_ins\_csr.claims\_agent

## About this task

When requested, the Insurance CSR customer insights AI agent consolidates the customer's insurance data and delivers structured responses to CSR questions. The agent retrieves data exclusively for the identified consumer or account on the Customer 360 page.

The agent can answer questions about the following areas of a customer's insurance relationship:

-   Policy information, including auto, home, life, disability, and travel policies
-   Coverages and coverage options
-   Insured assets, such as vehicles and properties
-   Policy participants, including drivers, beneficiaries, and insured persons
-   Servicing cases
-   Product catalog details, including available coverages, deductibles, limits, and defaults for insurance products

\[Omitted image "insurance-c360-now-assist-panel.png"\] Alt text: Insurance Customer 360 view displaying a list of four active policies in the Now Assist Panel in response to a user query to the Insurance CSR customer insights AI agent.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Open a customer record.

    The customer record displays in the Customer 360 page.

3.  Select **Ask Now Assist**.

    The Now Assist panel displays. The Insurance CSR customer insights AI agent begins analysis and displays relevant insurance information for the customer.

    **Note:** The agent retrieves data exclusively for the customer on the current Customer 360 page. The customer context is fixed for the session and does not change when you ask follow-up questions.

    The chat is specific to this customer record. If you navigate away, you can resume the chat by selecting **Ask Now Assist**.

    For more information, see [Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md).

4.  Ask the agent a question about the customer's insurance details, or select a follow-up option from the response.

    You can ask natural language questions about any area of the customer's insurance relationship. The agent returns structured responses with context-aware follow-up buttons that you can select to continue the conversation. Examples of questions you can ask include:

    -   What policies does this customer currently hold?
    -   What coverages are on the customer's home insurance policy?
    -   Are there any open claims for this customer?
    -   Who are the listed drivers on the customer's auto policy?

## Result

The agent answers your questions using information from the customer's insurance records and its configured knowledge sources.

**Parent Topic:**[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md)

**Related topics**  


[Agentic AI use cases for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/usecase-now-assist.md)

[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md)

[Summarize an insurance customer profile in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-profile.md)

