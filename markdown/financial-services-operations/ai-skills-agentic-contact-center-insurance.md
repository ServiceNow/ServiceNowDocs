---
title: AI skills in Agentic Contact Center for Insurance
description: AI skills in Agentic Contact Center for Insurance generate real-time customer summaries and interaction context for insurance customer service representatives. These skills consolidate customer identity, policy portfolio, and call context into actionable overviews that eliminate manual data searches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/ai-skills-agentic-contact-center-insurance.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [Exploring Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# AI skills in Agentic Contact Center for Insurance

AI skills in Agentic Contact Center for Insurance generate real-time customer summaries and interaction context for insurance customer service representatives. These skills consolidate customer identity, policy portfolio, and call context into actionable overviews that eliminate manual data searches.

## Insurance Customer Profile Summarization

Provides a customer service representative \(CSR\) with a concise, comprehensive summary of an insurance customer's identity and policy portfolio, eliminating the need to search across multiple data sources. It combines customer identity information and an overview of owned and associated policies to produce a unified and actionable overview for the CSR.

The summary includes the following information:

-   Customer tenure with the organization
-   Active insurance policy types
-   Current policy state, including upcoming renewals and active endorsements

The generated customer summary displays in the **Customer summary** section of the Customer 360 page as part of Agentic Contact Center for Insurance.

This skill is also used as a dependency for the Insurance interaction context summary skill. It must be activated before the Insurance interaction context summary skill can be configured.

## Insurance Interaction Context Summary

Provides a CSR with real-time interaction summaries and relevant customer context on the Interaction page. This is generated when a call is assigned to a CSR. The summary focuses on the context of the incoming call, providing the CSR with a snapshot of the customer's insurance situation when the call begins.

The summary includes the following information:

-   Customer tenure, providing an indication of how long the customer has been with the organization
-   The customer's likely reason for calling, derived from the live call transcript
-   Most recent related contact, including date and subject
-   Last three related cases, including case number, status, date raised, and reason
-   The insurance product the customer is currently inquiring about, including product name and premium due date

The generated context summary displays in the **Relevant details for this call** card in the Interaction page as part of Agentic Contact Center for Insurance. The card is not displayed until the customer's identity has been verified, and is not shown when no call context is available and no short description has been provided on the interaction record.

**Related topics**  


[Configure insurance customer profile summarization in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-customer-profile-summarization.md)

[Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-interaction-summary-skill.md)

