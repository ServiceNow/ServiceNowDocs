---
title: Create a product filter rule
description: Create a product filter rule in CPQ to dynamically include or exclude products from the quote catalog based on managed table data and transaction context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-product-filter-rule.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Advanced filters, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a product filter rule

Create a product filter rule in CPQ to dynamically include or exclude products from the quote catalog based on managed table data and transaction context.

## Before you begin

The `enableCatalogFilter` tenant setting must be enabled. Submit a request to DevOps to enable this setting.

A managed table containing the reference data for filtering must exist. For more information, see the managed table configuration steps in [Advanced product filtering for quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-advanced-product-filtering.md).

Role required: admin

## Procedure

1.  Navigate to **Products** &gt; **Product Filter Rules**.

2.  Before creating a filter rule, define or verify the managed table that contains the reference data for filtering.

    1.  Navigate to the **Tables** tab in CPQ Admin.

    2.  Create or upload a table containing the business logic, such as region-to-product mapping or availability flags.

    3.  Verify that the table includes at least one column that can be mapped to the product catalog, such as Region, SKU, or Product Family.

    4.  Deploy the table to make it available for use in filter rules.

3.  Select **Create New Rule**.

4.  Enter a **Rule Name**, a **Variable Name**, and a **Description** for the rule.

5.  In the **Reference Table** field, select the managed table that contains the filtering reference data.

6.  Define the filter conditions using fields from the managed table and transaction data to specify when the rule applies.

7.  Map the columns by matching the reference table columns to the corresponding product catalog columns.

    For example, map the `Region` column in the managed table to the `Region` column in the product catalog.

8.  Set the rule behavior.

    -   Select **Include** to show only products that match the filter condition.
    -   Select **Exclude** to hide products that match the filter condition.
9.  Select **Save** to store the rule.

10. Toggle the **Active** button to mark the rule as ready for deployment.

11. Select **Deploy** to apply the rule.

    The rule is active. Only products matching the filter logic are displayed when users open the catalog from within a quote.


