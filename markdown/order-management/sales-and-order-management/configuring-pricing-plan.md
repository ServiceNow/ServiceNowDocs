---
title: Configurable pricing plans
description: Pricing Management provides a default pricing plan that defines the sequence of steps in which pricing calculations and adjustments are applied to determine final product prices.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Configurable pricing plans

Pricing Management provides a default pricing plan that defines the sequence of steps in which pricing calculations and adjustments are applied to determine final product prices.

## How the pricing plan works

The default pricing plan is an active, published plan that is automatically implemented with Pricing Management. You can use the default plan, or you can copy the default plan and customize it by adding or changing the pricing steps to tailor it for your organization. You can have only one active pricing plan per domain.

**Note:** The Pricing Management v16.0.1 release provides a default pricing plan that includes a new step. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade to the v16.0.1 release. Determine whether you want to publish the default plan or customize the default pricing plan and then publish the custom plan to be used.

![Pricing steps that apply certain actions and calculations to determine product offering prices in Pricing Management](../image/default-pricing-plan-q1-2026.png "Default Pricing Plan steps")

The default plan consists of basic pricing steps in which certain actions are run to calculate product offering prices.

<table id="table_nrc_vpm_ddc"><thead><tr><th>

Step

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Initialize Pricing Context

</td><td>

Starts the pricing engine context. The system gathers basic data required for subsequent calculation steps. For example, the system resolves context variable values, initializes the pricing cache, and performs basic validation of request payloads.

</td></tr><tr><td>

Analyze Line Changes

</td><td>

Reviews price line changes to determine whether adjustments to sold products and contracts require new pricing, as defined in the Delta Price Treatment Matrix.

</td></tr><tr><td>

Fetch Base Cost

</td><td>

Get costs from a [cost book](../task/create-cost-books.md), if your organization is using cost books in Quote Management.

</td></tr><tr><td>

Apply Attribute based Cost Adjustments

</td><td>

Apply adjustments to the cost based on product offering characteristics.

</td></tr><tr><td>

Fetch Base List Price

</td><td>

Get the list price for all requested products based on the [price list](../task/som-create-price-list.md), unit of measurement, and data provided to the pricing API.

</td></tr><tr><td>

Apply Attribute Adjustments

</td><td>

Apply attribute adjustments based on product characteristics selected.

</td></tr><tr><td>

Apply Renewal Adjustment

</td><td>

Apply a renewal adjustment for contracts. This step determines whether a markup or markdown value, either a percentage or specific amount, such as a pricing uplift for contract renewals, is to be calculated and applied. **Note:**

-   Subsequent pricing adjustment steps in the pricing plan are not applied after this renewal adjustment step.
-   You can change or remove this step in a custom pricing plan. You can also change the conditions for running subsequent steps after the renewal adjustment step. For details on changing conditions for a particular step, see [Add or change a pricing plan step](../task/add-pricing-step.md).

</td></tr><tr><td>

Annual Price Increase Adjustments for Ramps

</td><td>

Applies the percentage Annual Price Increase to the list price of products that have price ramps. Sales agents specify the percentage increase when they create price ramps for quote line items.

</td></tr><tr><td>

Apply configuration component adjustments

</td><td>

Apply adjustments as defined in the Configuration Component Price Adjustment Matrix for child product offerings that are bundled under a parent product offering.

</td></tr><tr><td>

Apply contextual adjustments

</td><td>

Apply adjustments as defined in the Standard Price Adjustment Matrix for product offerings based on non-product characteristics, such as billing state or shipping zip code.

</td></tr><tr><td>

Custom adjustments

</td><td>

Apply custom adjustments if implemented using the PricingAdjustmentExtensionPoint to fetch adjustments from another system or for adjustments that can't be supported via a pricing matrix.

</td></tr><tr><td>

Floor and Ceiling Calculation

</td><td>

Calculates the price floor, using the minimum price allowed for a product, and the price ceiling, using the maximum price allowed for a product.

</td></tr><tr><td>

Net Price Calculation

</td><td>

Calculates the net price for products using any automatic and manual adjustments made in quotes or orders.

</td></tr><tr><td>

Line Rollup

</td><td>

Calculates the cumulative pricing fields in quote and order lines that are rolled up to the parent line of bundled products.

</td></tr><tr><td>

Derived Price Calculation

</td><td>

Calculates the line prices using the Derived Pricing Matrix, which defines the pricing source and the unit base list price for the price list line.

</td></tr><tr><td>

Calculate Delta Prices

</td><td>

Calculates the difference in net pricing for sold products and contracts after adjustments are made.

</td></tr><tr><td>

Header Rollup

</td><td>

Calculates total pricing values, such as total annual or total monthly amounts, displayed at the header level

</td></tr></tbody>
</table>For the configuration component adjustments, contextual adjustments, and custom adjustments, the **Price point** and **Calculation type** values in a step determine how multiple pricing adjustments are calculated:

-   **Price point**: The price for a product or service that is calculated after the step is run, either the List Price or Net Price.
-   **Calculation type**: Method for evaluating the impact of the adjustment at each step. The adjustment is applied to either the Previous Price Point or the Rolling Price.
    -   When the Calculation Type is Previous Price Point and the price point is Net Price, the previous price point is List Price. The adjustment is applied to the List Price.
    -   When the Calculation Type is Rolling, the adjustment calculated is based on the output of the previous step.

## Customizing a pricing plan

The default pricing plan is fixed, to preserve the default pricing logic. You can copy the default plan, and add or change steps as needed for your organization. When you finish your changes, you publish the copy so that it becomes the active plan. If needed, you can revert to the default plan at any time by publishing the default plan.

As a pricing admin or manager, follow these steps to define a custom pricing plan:

-   [Create a configurable pricing plan](../task/create-custom-pricing-plan.md) \(copy the default plan\).
-   [Add or change a pricing plan step](../task/add-pricing-step.md). In your configurable pricing plan, you can add one or more pricing steps for pricing adjustments, including any conditions for running the step. You can also change the sequence of the adjustment steps, if needed.
-   [Delete a pricing plan step](../task/delete-pricing-plan-step.md), if needed.

As you add or change pricing steps, the system validates your entries, such as the sequence number, price point, and calculation type. When you finish adding or changing steps, publish the configurable pricing plan to make it active. The former active plan is retired.

