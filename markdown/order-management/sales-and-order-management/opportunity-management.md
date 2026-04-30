---
title: Opportunity Management
description: The  ServiceNow Opportunity Management application enables your sales agents and account executives to analyze customer needs and generate product recommendations for potential customers.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Opportunity Management

The  ServiceNow® Opportunity Management application enables your sales agents and account executives to analyze customer needs and generate product recommendations for potential customers.

An opportunity in Sales Customer Relationship Management provides maximum information about a product or service based on the needs of a customer \(called a qualified lead\). A lead for a product is the minimal information that a sales agent uses to advance the conversation with a potential customer and create an opportunity.

![Sales and Order Management workflow that shows the opportunity, quote, and order creation steps.](../image/l2c-quote-workflow.png "Opportunity workflow in Sales Customer Relationship Management")

## Opportunity Management interface

The Opportunity Management application is integrated with the Product Catalog and product configurator to help sales agents access product offerings to build opportunities easily and conveniently. The Opportunity Management interface contains the following tabs:

<table id="table_enp_xnv_c1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Details tab](opportunity-management-details-tab.md)

</td><td>

Add basic information for the opportunity.

</td></tr><tr><td>

Catalog tab

</td><td>

Search for and add product offerings to your opportunity.

</td></tr><tr><td>

[Needs tab](../task/opp-mgmt-use-needs-analysis.md)

</td><td>

Lists the need templates that provide product recommendations for the opportunity.

</td></tr><tr><td>

[Line Items tab](opportunity-management-line-items-tab.md)

</td><td>

Add different line items to an opportunity.

</td></tr><tr><td>

[Competitors tab](opportunity-management-competitors-tab.md)

</td><td>

Record competitors information.

</td></tr><tr><td>

[Tasks tab](opportunity-management-tasks-tab.md)

</td><td>

Create opportunity tasks.

</td></tr><tr><td>

Team

</td><td>

Create opportunity team members.**Note:** Following member roles \(Related party types\) and responsibility are shipped by default:

-   Account Executive
-   Solution Sales Executive
-   Price Band Approver

Additional roles can be configured; however, user access through these roles via the responsibility framework is supported starting from the Zurich Patch 3 release.

</td></tr><tr><td>

Contacts

</td><td>

Create opportunity associated contacts.

</td></tr><tr><td>

[Emails tab](opportunity-management-emails-tab.md)

</td><td>

Create emails to send to the required stakeholders.

</td></tr><tr><td>

[Quotes tab](opportunity-management-create-quote.md)

</td><td>

Create quotes directly from opportunities.

</td></tr></tbody>
</table>## Integrating pricing in Opportunity Management

Opportunity Management integrates with the pricing engine to consume the default price list and displays the total price and unit price of product offerings in your opportunity.

Based on the prices of product offerings \(POs\) that are added to the opportunity, the total price values are auto-calculated. For more information, see [Add and view the details of an opportunity](opportunity-management-details-tab.md) and [Add line items to an opportunity](opportunity-management-line-items-tab.md).

Pricing in Opportunity Management provides the following benefits:

-   Revenue forecasting: The pricing engine helps agents evaluate an opportunity's total worth by computing the combined prices of each offering included, which in turn helps teams to strategize resource or budget allocation for deals.
-   Deal prioritization: By analyzing the potential revenue of each opportunity, your sales team can focus on the deals based on their financial impact. For example, teams can focus on deals with higher potential revenue and higher margins.
-   Negotiation enhancement: The pricing engine gives your sales team real-time pricing insights, which enhances the negotiation process by enabling your sales team to tailor offers that meet customer needs while maintaining profitability.

To learn more about pricing, see [Pricing Management](pricing-management.md).

## Use the product configurator

The product configurator lets your agents configure products in the following ways:

-   Browse and add configurable product offerings from the catalog to create opportunity lines.
-   Select product options and view product relationships.

The product configurator uses Sales Customer Relationship Management primitives to create and update opportunity lines and characteristics.

## What to do next

To learn about setting up Opportunity Management, see [Install and configure Opportunity Management](configure-opportunity-mgmt.md).

