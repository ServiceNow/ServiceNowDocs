---
title: Configurable pricing plans
description: Pricing Management provides a default pricing plan that defines the sequence of steps in which pricing calculations and adjustments are applied to determine final product prices.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-09-11"
reading_time_minutes: 4
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configurable pricing plans

Pricing Management provides a default pricing plan that defines the sequence of steps in which pricing calculations and adjustments are applied to determine final product prices.

## How the pricing plan works

The default pricing plan is an active, published plan that is automatically implemented with the November 2024 release. You can use the default plan, or you can copy the default plan and customize it by adding or changing the pricing steps to tailor it for your organization. You can have only one active pricing plan per domain.

**Note:** If you upgraded to the November 2024 release, there is no change in pricing calculations or pricing logic with the pricing plan. If you don't change anything with the pricing plan, the pricing calculations occur exactly as before the upgrade.

![Sequence of steps in the default pricing plan, described in the following table](../image/default-pp-steps.png "Default Pricing Plan steps")

The default plan consists of basic pricing steps in which certain actions are run to calculate product offering prices.

|Step|Action|
|----|------|
|Initialize Pricing Context|Starts the pricing engine context. The system gathers basic data required for subsequent calculation steps. For example, the system resolves context variable values, initializes the pricing cache, and performs basic validation of request payloads.|
|Fetch Cost|Get costs from a [cost book](../task/create-cost-books.md), if your organization is using cost books in Quote Management.|
|Fetch Price List Price|Get the list price for all requested products based on the [price list](../task/som-create-price-list.md), unit of measurement, and data provided to the pricing API.|
|Apply Attribute Adjustments|Apply attribute adjustments based on product characteristics selected.|
|Apply configuration component adjustment|Apply adjustments as defined in the Configuration Component Price Adjustment Matrix for child product offerings that are bundled under a parent product offering.|
|Apply contextual adjustments|Apply adjustments as defined in the Standard Price Adjustment Matrix for product offerings based on non-product characteristics, such as billing state or shipping zip code.|
|Custom adjustments|Apply custom adjustments if implemented using the PricingAdjustmentExtensionPoint to fetch adjustments from another system or for adjustments that can't be supported via a pricing matrix.|

For the configuration component adjustments, contextual adjustments, and custom adjustments, the **Price point** and **Calculation type** values in a step determine how multiple pricing adjustments are calculated:

-   **Price point**: The price for a product or service that is calculated after the step is run, either the List Price or Net Price.
-   **Calculation type**: Method for evaluating the impact of the adjustment at each step. The adjustment is applied to either the Previous Price Point or the Rolling Price.
    -   When the Calculation Type is Previous Price Point and the price point is Net Price, the previous price point is List Price. The adjustment is applied to the List Price.
    -   When the Calculation Type is Rolling, the adjustment calculated is based on the output of the previous step.

## Example pricing plan calculations

The following example shows how multiple pricing adjustments in a pricing plan are calculated and applied to a door sensor product. The door sensor is part of the Home Automation bundled product, which is being sold to Boxeo, a customer in California. The price of the door sensor is based on the price list for Boxeo.

![Table that shows how pricing adjustments are calculated for a door sensor product, using the list price and previous price point and rolling calculations.](../image/pricing-plan-example.png "Pricing plan calculations for a product")

## Customizing a pricing plan

The default pricing plan is fixed, to preserve the default pricing logic. You can copy the default plan, and add or change steps as needed for your organization. When you finish your changes, you publish the copy so that it becomes the active plan. If needed, you can revert to the default plan at any time by publishing the default plan.

As a pricing admin or manager, follow these steps to define a custom pricing plan:

-   [Create a configurable pricing plan](../task/create-custom-pricing-plan.md) \(copy the default plan\).
-   [Add or change a pricing plan step](../task/add-pricing-step.md). In your configurable pricing plan, you can add one or more pricing steps for pricing adjustments, including any conditions for running the step. You can also change the sequence of the adjustment steps, if needed.
-   [Delete a pricing plan step](../task/delete-pricing-plan-step.md).

As you add or change pricing steps, the system validates your entries, such as the sequence number, price point, and calculation type. When you finish adding or changing steps, publish the configurable pricing plan to make it active. The former active plan is retired.

