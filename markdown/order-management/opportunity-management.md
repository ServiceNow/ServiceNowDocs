---
title: Opportunity Management
description: The ServiceNow Opportunity Management application enables your sales agents and account executives to analyze customer needs and generate product recommendations for potential customers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/opportunity-management.html
release: australia
topic_type: concept
last_updated: "2026-08-07"
reading_time_minutes: 6
breadcrumb: [Sales automation, Explore, Sales Customer Relationship Management]
---

# Opportunity Management

The ServiceNow® Opportunity Management application enables your sales agents and account executives to analyze customer needs and generate product recommendations for potential customers.

An opportunity in Sales Customer Relationship Management provides complete information about a product or service based on the needs of a customer \(called a qualified lead\). A lead for a product is the minimal information that a sales agent uses to advance the conversation with a potential customer and create an opportunity.

\[Omitted image "l2c-quote-workflow.png"\] Alt text: Sales CRM workflow that shows the opportunity, quote, and order creation steps.

## Opportunity Management interface

The Opportunity Management application is integrated with the Product Catalog and product configurator to help sales agents access product offerings to build opportunities. The Opportunity Management interface contains the following tabs:

<table id="table_enp_xnv_c1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-guided-selling-opportunity.md)

</td><td>

Summary of key deal information including account, stage, amount, AI-generated opportunity insights and probability score, and guided selling actions such as stage exit criteria and playbook activities.

</td></tr><tr><td>

[Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-details-tab.md)

</td><td>

Add basic information for the opportunity.

</td></tr><tr><td>

[Catalog tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opp-mgmt-use-needs-analysis.md)

</td><td>

Search for and add product offerings to your opportunity.

</td></tr><tr><td>

[Needs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opp-mgmt-use-needs-analysis.md)

</td><td>

Lists the need templates that provide product recommendations for the opportunity.

</td></tr><tr><td>

[Line Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-line-items-tab.md)

</td><td>

Add different line items to an opportunity.

</td></tr><tr><td>

[Quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-create-quote.md)

</td><td>

Create quotes directly from opportunities.

</td></tr><tr><td>

[Contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-opportunity-associated-contact.md)

</td><td>

Create opportunity associated contacts.

</td></tr><tr><td>

[Team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-new-opportunity-team-member.md)

</td><td>

Create opportunity team members.

</td></tr><tr><td>

[Competitors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-competitors-tab.md)

</td><td>

Record competitor information.

</td></tr><tr><td>

[Emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-emails-tab.md)

</td><td>

Create emails to send to the required stakeholders.

</td></tr><tr><td>

[Allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-allocations.md)

</td><td>

Distribute sales credit across multiple contributors on a single opportunity.

</td></tr><tr><td>

[Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-tasks-tab.md)

</td><td>

Create opportunity tasks.

</td></tr><tr><td>

[Meetings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/schedule-meeting-opportunity.md)

</td><td>

Related list of all meetings scheduled and associated with the opportunity.

</td></tr><tr><td>

[Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-touchpoints-opportunity.md)

</td><td>

Related list of customer interaction records \(calls, emails, engagement activities\) logged against the opportunity.

</td></tr><tr><td>

Related Channel Partners

</td><td>

Add authorized service organizations or partner entities \(for example, referral or influencer partners\) linked to a customer opportunity. Related channel partners can be:

-   Authorized organization: Full permissions to access, view, edit, or modify opportunity details
-   Listed organization: Only for tracking purposes. No permissions to view, access, edit, or delete opportunity details

</td></tr></tbody>
</table>## Integrating pricing in Opportunity Management

Opportunity Management integrates with the pricing engine to consume the default price list and displays the total price and unit price of product offerings in your opportunity.

Based on the prices of product offerings \(POs\) that are added to the opportunity, the total price values are auto-calculated. For more information, see [Add and view the details of an opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-details-tab.md) and [Add line items to an opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-line-items-tab.md).

Pricing in Opportunity Management provides the following benefits:

-   Revenue forecasting: The pricing engine helps agents evaluate an opportunity's total worth by computing the combined prices of each offering included, which in turn helps teams to strategize resource or budget allocation for deals.
-   Deal prioritization: By analyzing the potential revenue of each opportunity, your sales team can focus on the deals based on their financial impact. For example, teams can focus on deals with higher potential revenue and higher margins.
-   Negotiation enhancement: The pricing engine gives your sales team real-time pricing insights, which enhances the negotiation process by enabling your sales team to tailor offers that meet customer needs while maintaining profitability.

To learn more about pricing, see [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-management.md).

## AI capabilities that support Opportunity Management

-   **Opportunity summary**

    Generate an AI summary for an opportunity record that enables you to get synthesized information from emails, touchpoints, deal stage, line items, and more without opening every related activity, contact, or deal record. For more information, see [Summarize an opportunity using ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md).

-   **Opportunity scores and insights**

    Review AI-generated win probability scores and contextual insights for an opportunity to assess deal health and its probability to close. Use this to prioritize pipeline opportunities and identify risks. For more information, see [View opportunity scores and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-opty-scores-insights.md).

    Because opportunity scoring \(Probability to Close\) uses Predictive Intelligence and machine learning, you must train the ML model on the existing data. For more information, see [Set up ML-based opportunity scoring and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-opty-score-insights.md).

-   **CRM conversational query**

    Ask questions and issue commands to work on an opportunity in plain language using an MCP client such as Claude Desktop. For more information, see [CRM conversational query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/crm-conversational-query.md) and [Manage opportunity records using an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-opportunity-records.md).


## What to explore next

The following topics provide more information about configuring and using Opportunity Management

-   [Configuring Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-opportunity-mgmt.md)
-   [Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-mgmt-using.md)
-   [Opportunity Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-management-reference.md)

The following topics provide links to resources for configuring and using AI capabilities with Opportunity Management

-   [AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/ai-capabilities-sales-crm.md)
-   [Configuring AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-ai-capabilities-sales-crm.md)

