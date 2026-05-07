---
title: Transaction Manager: Advanced product filtering
description: In Transaction Manager, you can dynamically filter products based on any number of factors, with real-time data synchronization from managed tables and fast search speeds even in very large catalogs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Advanced product filtering

In Transaction Manager, you can dynamically filter products based on any number of factors, with real-time data synchronization from managed tables and fast search speeds even in very large catalogs.

CPQ Advanced Product Filtering feature enables dynamic product catalog filtering using Admin-defined business rules. This includes support for real-time data synchronization from managed tables and sub-second search speeds, even with product catalogs over millions of SKUs.

This article explains how to use and manage this feature, and outlines performance benefits, configuration steps, and common use cases.

## Use case

As your catalog grows and your business logic becomes more dependent on regions or rules, it becomes essential to dynamically filter products based on:

-   Country, region, or compliance constraints
-   Available pricing or configuration status
-   Transaction-specific input fields

## Key features

<table id="table_o2g_pvs_hhc"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced filter rule search

</td><td>

Contextual product filtering with sub-second results

</td></tr><tr><td>

Real-time data sync

</td><td>

Managed Table and rule changes take effect immediately \(no redeploy needed\)

</td></tr><tr><td>

Rule-based filtering engine

</td><td>

Include and exclude products using dynamic logic

</td></tr><tr><td>

No-code admin experience

</td><td>

UI-based rule builder with mapping and conditions

</td></tr><tr><td>

Scales with catalog size

</td><td>

Performance maintained even with more than a million products

</td></tr></tbody>
</table>## Prerequisites for product rule filtering

The tenant setting `enableCatalogFilter` must be turned ON. This setting activates the filtering logic during catalog interactions. To enable this, submit a request to DevOps.

Additionally, The Transaction Manager module must be enabled. This ensures that Add Lines operation uses the defined Product Rule Filters to dynamically include/exclude products during configuration.

## Configuration steps

First, define a managed table. Follow these steps:

1.  Navigate to the `Tables` tab in Logik Admin.
2.  Create or upload a table that contains your business logic \(for example, region-to-product mapping, availability flags, and so on\).
3.  Ensure column mapping. The table must include at least one column that can be mapped to the product catalog, such as `Region`, `SKU`, or `Product Family`.
4.  Deploy the table once to make it available for use in filter rules.

    **Note:** Updates made to the managed table data are automatically synced with the product filter engine. A tenant setting must be enabled on a 15-minute interval.

    The Product Filter Rule does not have to be redeployed when only table data changes. This behavior is enabled when `filterrules.scheduler.enable = true`.

    The system syncs the updated data every 15 minutes, making the latest information available during product filtering.


![Tables list](../images/cpq-txn-mgr-adv-product-filtering-1.png)

Next, create a product filter rule.

1.  Navigate to `Products` &gt; `Product Filter Rules`.
2.  Click `Create New Rule`.
3.  Enter the following details:
    -   Rule Name: A descriptive name for your rule
    -   Variable Name: A unique identifier used internally
    -   Description: A brief summary of the rule's purpose
4.  Select a reference table: Choose the managed table that contains the reference data for filtering \(such as region availability, pricing eligibility, and so on\).
5.  Define the filter conditions. Use fields from the managed table and transaction data to define when the rule should apply.
6.  Map columns. Match the reference table columns to corresponding product table columns \(for example, `Region` in the managed table to `Region` in the product catalog\).
7.  Set the rule behavior by choosing one of the following:
    -   Include: Only products that match the condition are shown
    -   Exclude: Products that match the condition are removed
8.  Save and deploy.
    -   Click **Save** to store the rule.
    -   Toggle the Active button to mark the rule as ready for deployment.
    -   Click **Deploy** to apply the rule and enforce it in the product catalog.

**Note:** Any change made to an existing rule must be redeployed for it to take effect.

![Product filter rules](../images/cpq-txn-mgr-adv-product-filtering-2.png)

![Product pricing screen](../images/cpq-txn-mgr-adv-product-filtering-3.png)

To test the filter in a transaction, start a transaction in the Transaction Manager, and the proceed to the product selection stage.

Only products that match the filter logic will be displayed.

