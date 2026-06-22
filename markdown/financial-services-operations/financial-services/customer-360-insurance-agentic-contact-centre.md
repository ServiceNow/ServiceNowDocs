---
title: Customer 360 page for Agentic Contact Center for Insurance
description: The Customer 360 page gives policy servicing and claims servicing CSRs a consolidated view of a customer's profile, policies, coverage, and AI-generated summary, drawn from core insurance and CRM. The view is based on the scope of the respective roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/customer-360-insurance-agentic-contact-centre.html
release: australia
product: Financial Services
classification: financial-services
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 3
keywords: [customer 360, customer profile, insurance summary, policy details, insurance transaction history, insurance policies, ai-generated customer summary, total policies, total cover, view all insurance, view customer cases]
breadcrumb: [Exploring Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Customer 360 page for Agentic Contact Center for Insurance

The Customer 360 page gives policy servicing and claims servicing CSRs a consolidated view of a customer's profile, policies, coverage, and AI-generated summary, drawn from core insurance and CRM. The view is based on the scope of the respective roles.

CSR agents get a unified view of a customer's relationship on the Customer 360 page. CSRs can open it by selecting the customer's name from the Interaction page contact card, or navigate to it directly when reviewing a customer outside of a call. The page is for both individual and corporate insurance customers and provides consolidated information from core insurance and CRM based on the scope of the user role.

The customer summary is an AI-generated summary that provides the CSR with a concise overview of the customer's relationship with the insurer. The details provided in the summary are based on the scope of the role. The following details are displayed for both roles:

-   Details: customer contact details, address, nationality, and date of birth.
-   Interaction history: customer interaction history \(which can be filtered using different options\) with timelines and brief caption about interaction, in the interaction history panel .
-   Household members: details of individuals linked to the consumer, such as family members or authorized representatives.
-   Summary: customer vintage and brief summary of the customer's active policies, upcoming or overdue premium, if any.
-   Overview: metric cards with graphical representations of the customer's total premium paid and cases, with policy level splits.
-   Policies and Coverages: drop-down list containing all policies held by the customer, plus any policies they are acting as a participant in. When a policy is selected, a card displays the product name, policy number, coverage amount, and policy status.
-   Cases: view of this section depends on the scope of the role.
    -   Policy servicing CSRs can view the list of policy servicing cases, including those created by other agents or customers through the self-service portal or any claims they act as a participant in. \[Omitted image "servicing-agent.png"\] Alt text: Policy servicing CSR workspace showing customer details, an AI-generated summary, interaction history, and premium and service cases overview charts. For details, refer to the surrounding text.
    -   Claims servicing CSRs can view the list of claims related cases including those created by other agents or customers through the self-service portal or any claims they act as a participant in. \[Omitted image "customer-summary.png"\] Alt text: Claims CSR workspace showing customer details, an AI-generated summary, interaction history, and premium and claim payout overview charts. For details, refer to the surrounding text.

The list shows details like customer name, case number, lodgement date and time, case type, status, and assigned handler. Cases are sorted with the most recent first. CSRs can also filter cases using the available filters.

**Note:** The policy servicing CSR can view only policy-related cases and the claims servicing CSR can view only claims cases.

The Household members section is visible only if the CSM Household plugin is installed and is applicable only to B2C customers. See [Configuring households](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-households.md) for more information about the Household plugin.

**Warning:** AI-generated summaries may not always be accurate. CSRs must review the underlying policy and case data before acting on any AI-generated content.

## Contextual side panel

The contextual side panel appears on the page and provides access to supplementary tools and related record information. The following default CSM components are available in the panel:

-   Activity stream
-   Attachments
-   Templates
-   Recommended Actions
-   Related items

## Actions

The following table shows the available actions in the Customer 360 page.

|Name|Description|
|----|-----------|
|Ask Now Assist|Opens the Now Assist panel and initiates the Insurance CSR customer insights AI agent. The AI agent uses the customer's profile and policy data to surface contextual responses. For more information, see [Generate customer insights in the Customer 360 page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/generate-insurance-customer-insights-customer-360.md).|
|Create case|Opens the Create case window to create a case for the customer.|

**Related topics**  


[CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md)

