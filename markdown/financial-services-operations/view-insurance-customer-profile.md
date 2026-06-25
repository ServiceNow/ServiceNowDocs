---
title: View an insurance customer profile in Agentic Contact Center for Insurance
description: Review a customer's AI-generated insurance profile, financial overview, and interaction history in the Customer 360 page so that you can understand the customer's insurance relationship.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/view-insurance-customer-profile.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [insurance customer 360 view customer profile, insurance customer 360 ai-generated summary, insurance customer 360 profile and status, insurance customer 360 financial overview, insurance customer 360 total premiums, insurance customer 360 claim payouts, insurance customer 360 case distribution, insurance customer 360 interaction history, customer 360 page]
breadcrumb: [Using Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# View an insurance customer profile in Agentic Contact Center for Insurance

Review a customer's AI-generated insurance profile, financial overview, and interaction history in the Customer 360 page so that you can understand the customer's insurance relationship.

## Before you begin

Role required: sn\_ins\_csr.servicing\_agent, sn\_ins\_csr.claims\_agent

## Procedure

1.  Open a customer record.

    -   From an active interaction, select the customer's name in the customer details card.
    -   Navigate directly to the consumer, account, or contact record from the workspace.
    The Customer 360 page opens in a separate tab.

2.  Review the **Customer summary** section for an AI-generated overview of the customer's insurance relationship.

    The summary includes two sections:

    -   **Profile**: A brief overview of the customer and their active insurance policy types.
    -   **Status**: The current state of the customer's active policies which have overdue premiums or upcoming renewals within a month.
    **Note:** The Customer summary section is only visible when the Insurance Customer Profile Summarization skill is activated. For details, see [Configure insurance customer profile summarization in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-customer-profile-summarization.md).

    For more information on the component, see [Summarize an insurance customer profile in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-profile.md).

3.  Review the **Overview** section to assess the customer's financial and activity totals.

    The gauges displayed depend on your assigned role:

    -   **Total premiums**: The combined premium amount across all of the customer's insurance policies, broken down by product type. Visible to all agents.
    -   **Claim payouts**: The net total of approved claim payments associated with the customer, broken down by product type. Visible to agents with a claims role only.
    -   **Case distribution**: The count of open cases associated with the customer, grouped by service type. Visible to agents with a servicing role only.
    \[Omitted image "insurance-c360-overview-gauges.png"\] Alt text: Overview section showing two gauge charts for total premiums and claim payouts.

4.  For a consumer, review the **Customer details** section for their profile information.

    The section displays the customer's name, contact details, date of birth, nationality, and address information.

5.  For an account, review the **Account details** and **Contact details** section for profile information.

    The **Account details** section displays the account name, primary contact, contact details, address information, and industry.

    The **Contact details** section displays the associated account, contact details, date of birth, nationality, and address information.

6.  Review the **Interaction history** section to see recent customer activity.

    The list shows recent interactions including phone and chat interactions. Use the search bar, filter, or calendar controls to narrow the list.


**Related topics**  


[Customer 360 page for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/customer-360-insurance-agentic-contact-centre.md)

[View insurance policies and coverages in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/view-insurance-policies-coverages.md)

[View insurance cases in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/view-insurance-cases.md)

[Summarize an insurance customer profile in Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-insurance-customer-profile.md)

