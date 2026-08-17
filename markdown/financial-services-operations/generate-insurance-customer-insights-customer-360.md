---
title: Generate customer insights in the Customer 360 page for Agentic Contact Center for Insurance
description: Use the Insurance CSR customer insights AI agent in the Customer 360 page to quickly access and understand a customer's insurance details. View policies, coverages, claims, and servicing history without navigating away from the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/generate-insurance-customer-insights-customer-360.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [insurance csr customer insights ai agent, generate insurance customer insights, insurance customer 360 now assist, insurance ai agent customer 360, insurance policy insights, insurance claims insights, insurance coverage insights, agentic contact center insurance ai insights]
breadcrumb: [Using Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Generate customer insights in the Customer 360 page for Agentic Contact Center for Insurance

Use the Insurance CSR customer insights AI agent in the Customer 360 page to quickly access and understand a customer's insurance details. View policies, coverages, claims, and servicing history without navigating away from the workspace.

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

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Open a customer record.

    The customer record displays in the Customer 360 page.

3.  Select **Ask Otto**.

    The ServiceNow Otto panel displays. The Insurance CSR customer insights AI agent begins analysis and displays relevant insurance information for the customer.

    **Note:** The agent retrieves data exclusively for the customer on the current Customer 360 page. The customer context is fixed for the session and does not change when you ask follow-up questions.

    The chat is specific to this customer record. If you navigate away, you can resume the chat by selecting **Ask Otto**.

    For more information, see [Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/agentic-contact-center-for-insurance-agents-overview.md).

4.  Ask the agent a question about the customer's insurance details, or select a follow-up option from the response.

    You can ask natural language questions about any area of the customer's insurance relationship. The agent returns structured responses with context-aware follow-up buttons that you can select to continue the conversation. Examples of questions you can ask include:

    -   What policies does this customer currently hold?
    -   What coverages are on the customer's home insurance policy?
    -   Are there any open claims for this customer?
    -   Who are the listed drivers on the customer's auto policy?

## Result

The agent answers your questions using information from the customer's insurance records and its configured knowledge sources.

**Related topics**  


[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/agentic-contact-center-for-insurance-agents-overview.md)

[Summarize an insurance customer profile in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/summarize-insurance-customer-profile.md)

