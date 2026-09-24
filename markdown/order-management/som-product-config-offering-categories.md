---
title: Add product catalog categories
description: Use the Product Offering Categories tab to organize your products in groups in Sales Customer Relationship Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/som-product-config-offering-categories.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Create product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Add product catalog categories

Use the Product Offering Categories tab to organize your products in groups in Sales Customer Relationship Management.

## Before you begin

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## About this task

Product catalog categories help organize products into groups, which makes it easier for order agents to find products while creating orders or building quotes. Catalog categories are associated with a catalog. For more information about catalogs, see [Create a product offering catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-create-product-catalog.md).

Product offering catalog categories must be published before products can be added.

This procedure explains the Product Offering Category tab. To set up categories before adding products, see [Create a product offering category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-create-product-offering-category.md).

**Note:** Creating a product offering category and associating it to the product offering is required for validating product offerings before publishing them using the In Test and Staged intermediate life cycle states. For more information on the life cycle states, see [Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md).

## Procedure

1.  In the CRM Workspace, select the **List** icon \[Omitted image "list-outline-24.svg"\] Alt text:.

2.  Navigate to **Offerings** &gt; **Product Offerings** and select the product offering you are working with.

3.  Select the **Product Offering Categories** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Category|Select an existing published category.|
    |Product offering|Name of the product offering you are working with.|

6.  Select **Save**.

7.  Review the category information and select one of the following options.

    -   Ready for Test
    -   Publish
    The category is available to add product offerings or create child categories.


## What to do next

-   [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md)
-   [Add product visuals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-visuals.md)
-   [Add related contracts to product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-related-contracts.md)
-   [Add a unit of measure to a product offering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-unit-of-measure.md)
-   [Create a product offering version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-create-new-version.md)
-   [Create product offering relationship groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-relationship-groups.md)

**Related topics**  


[Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)

