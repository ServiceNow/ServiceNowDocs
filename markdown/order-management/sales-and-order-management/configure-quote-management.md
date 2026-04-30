---
title: Install and configure Quote Management
description: Learn how to set up Quote Management so that your sales agents can create and manage customer quotes.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Install and configure Quote Management

Learn how to set up Quote Management so that your sales agents can create and manage customer quotes.

Admins and Quote Management administrators complete the following configuration tasks to set up Quote Management.

<table id="table_b23_thc_zzb"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

[Install Quote Management](../task/installing-quote-management.md)

</td><td>

Install Quote Management from the ServiceNow® Store Store. It provides these key features for your agents:-   Build quotes with products and pricing, then present them to customers.
-   Use the product configurator to select simple and configurable product offerings.
-   Add pricing adjustments to products.
-   Convert quotes to product orders once customers have approved.

</td><td>

Admin

</td></tr><tr><td>

[Assign user roles in Sales Customer Relationship Management applications](configure-SOM-roles.md)

</td><td>

Set the roles for Quote Management users and your product catalog and pricing administrators.

</td><td>

Admin

</td></tr><tr><td>

[Configuring product offerings and catalogs](som-managing-product-catalogs.md)

</td><td>

Create the product offerings and catalogs, unless they've been previously defined.

</td><td>

Product catalog admin

</td></tr><tr><td>

[Configuring product pricing](../task/som-create-price-list-line.md)

</td><td>

Define the price lists, pricing strategies, and other pricing features that you want to use, unless they've been previously defined.-   Set the [price lists](../task/som-create-price-list.md) and pricing strategies that control how pricing is applied to quotes.
-   If you're using cost books, create the [cost books](../task/create-cost-books.md) that define the unit costs for product offerings.

</td><td>

Pricing admin

</td></tr><tr><td>

Activate cost books and cost margins

</td><td>

Use the **sn\_quote\_mgmt\_core.enable\_cost\_margin\_calculation** system property to activate the cost book and cost margin features in Quote Management. These features enable sales agents to view product unit costs and cost margins when creating sales quotes.

</td><td>

Quote Management admin

</td></tr><tr><td>

[Activate location-based transactions](../task/som-activate-location-filter.md)

</td><td>

Use the **sn\_sales\_common.enable\_location\_based\_transactions** system property to activate location-based transactions in Quote Management.

</td><td>

Admin

</td></tr><tr><td>

[Configuring quote PDF documents](quote-management-configure-pdf-documents.md)

</td><td>

Set up PDF template, signers, and Docusign.-   [Create PDF templates](../task/quote-mgt-setup-pdf-document-templates.md)
-   [Configure DocuSign](../task/quote-mgt-configure-docusign-pdf.md)
-   [Set up PDF document signers](../task/quote-mgt-configure-pdf-document-signers.md)

</td><td>

sales\_operations\_specialists

</td></tr></tbody>
</table>