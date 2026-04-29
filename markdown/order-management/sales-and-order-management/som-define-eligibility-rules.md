---
title: Define product eligibility rules in a product eligibility matrix
description: Define product eligibility rules by using the Product Offering Catalog Eligibility, Product Offering Category Eligibility, or Product Offering Eligibility Matrix.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring product offer eligibility, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Define product eligibility rules in a product eligibility matrix

Define product eligibility rules by using the Product Offering Catalog Eligibility, Product Offering Category Eligibility, or Product Offering Eligibility Matrix.

## Before you begin

[Create the rule entity filters](som-create-rule-entity-filter.md) and define any new [custom context variables](som-create-context-variable.md) needed to define the eligibility rules.

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## About this task

When you define eligibility rules, consider the two modes for determining eligibility:

-   Ineligible: Determine all the catalogs, categories, and product offers that are considered ineligible by default, then set your eligibility rules as needed.
-   Eligible: Determine all the catalogs, categories, and product offers that are considered eligible by default, then set your ineligibility rules as needed.

Use the **Default result** field in the decision table for the product eligibility matrix to control the default mode.

The November 2024 release provides Version 2 of the product eligibility matrices, which now support eligibility rules based on transaction line attributes. You can also use service location context variables to set product eligibility rules for service locations: Service City, Service State, Service Country, and Service Zip.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Context Rule Management** &gt; **Rule Matrices**.

3.  Select the product eligibility matrix for the rule to be defined.

    -   To set the eligibility rules for a product catalog, select the Product Catalog Eligibility Matrix.
    -   To set the eligibility rules for a product category, select the Product Category Eligibility Matrix.
    -   To set the eligibility rules for a product offering, select the Product Offering Eligibility Matrix.
4.  Select **Edit Rule**.

    The Decision Table for the selected eligibility matrix opens in Workflow Studio and shows the inputs and the decision table for setting the conditions that control the eligibility.

5.  In the decision table, set the rule to control the eligibility.

    1.  In the **Default result** field of the Condition section, review the eligibility mode being used and update it if needed.

    2.  Select **Add new decision row**.

    3.  In the row, select the column for the input \(context variable\) to be applied, such as the Billing State or Account.

    4.  In the **Active** column, set the value to true.

    5.  In the Results section, under the **Eligibility Rules** column, select the eligibility state to be applied, for example Ineligible or Eligible.

    6.  Under the **Rule Entity Filter** column, select the filter to be applied.

6.  Select **Save**.

    Review the **Validation Status** and **Validation Messages** columns to see if you're missing mandatory inputs, outputs or other information. If so, enter the appropriate information and select **Save**.

    The filtered product entity \(product catalog, category, or offering\) is displayed or hidden to sales and order agents, depending on the filter.


