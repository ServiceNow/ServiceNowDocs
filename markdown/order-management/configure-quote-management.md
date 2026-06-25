---
title: Configuring Quote Management
description: Learn how to set up Quote Management so that your sales agents can create and manage customer quotes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-quote-management.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring Quote Management

Learn how to set up Quote Management so that your sales agents can create and manage customer quotes.

Admins and Quote Management administrators complete the following configuration tasks to set up Quote Management.

<table id="table_b23_thc_zzb"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/installing-quote-management.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/installing-quote-management.md)

</td><td>

Install Quote Management from the ServiceNow® Store Store. It provides these key features for your agents:-   Build quotes with products and pricing, then present them to customers.
-   Use the product configurator to select simple and configurable product offerings.
-   Add pricing adjustments to products.
-   Convert quotes to product orders once customers have approved.

</td><td>

Admin

</td></tr><tr><td>



</td><td>

Set the roles for Quote Management users and your product catalog and pricing administrators.

</td><td>

Admin

</td></tr><tr><td>

[Configuring product offerings and catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-managing-product-catalogs.md)

</td><td>

Create the product offerings and catalogs, unless they've been previously defined.

</td><td>

Product catalog admin

</td></tr><tr><td>

[Configuring product pricing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-price-list-line.md)

</td><td>

Define the price lists, pricing strategies, and other pricing features that you want to use, unless they've been previously defined.-   Set the [price lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-price-list.md) and pricing strategies that control how pricing is applied to quotes.
-   If you're using cost books, create the [cost books](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-cost-books.md) that define the unit costs for product offerings.

</td><td>

Pricing admin

</td></tr><tr><td>

Activate cost books and cost margins

</td><td>

Use the **sn\_quote\_mgmt\_core.enable\_cost\_margin\_calculation** system property to activate the cost book and cost margin features in Quote Management. These features enable sales agents to view product unit costs and cost margins when creating sales quotes.

</td><td>

Quote Management admin

</td></tr><tr><td>

[Activate location-based transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-activate-location-filter.md)

</td><td>

Use the **sn\_sales\_common.enable\_location\_based\_transactions** system property to activate location-based transactions in Quote Management.

</td><td>

Admin

</td></tr><tr><td>

[Configure quote PDF documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management-configure-pdf-documents.md)

</td><td>

Set up PDF template, signers, and Docusign.-   [Create PDF templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgt-setup-pdf-document-templates.md)
-   [Configure DocuSign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgt-configure-docusign-pdf.md)
-   [Set up PDF document signers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgt-configure-pdf-document-signers.md)

</td><td>

sales\_operations\_specialists

</td></tr></tbody>
</table>## What to do next

After completing the configuration tasks, you can start using Quote Management to build and manage customer quotes. See [Using Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgmt-using.md).

Optionally, configure [Configuring Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-management.md) to build automated approval workflows for customer quotes and other Sales Customer Relationship Management entities.

**Related topics**  


[Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management.md)

[Using Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgmt-using.md)

[Approving or rejecting quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approving-or-rejecting-quotes.md)

[Using product offering recommendations in quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-prod-recommendations-quote.md)

[Sync quote and opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/synchronise_quote_and_opportunity.md)

