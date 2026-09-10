---
title: Pricing in the ServiceNow Quote Experience
description: The Quote Experience prices quotes through an integrated pricing service. Pricing runs when you reprice a quote or when a change affects pricing, and it applies both rep-entered and rule-driven adjustments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/pricing-in-quote-experience.html
release: australia
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 3
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Explore, Sales Customer Relationship Management]
---

# Pricing in the ServiceNow Quote Experience

The Quote Experience prices quotes through an integrated pricing service. Pricing runs when you reprice a quote or when a change affects pricing, and it applies both rep-entered and rule-driven adjustments.

When pricing is enabled for a deployment, the Quote Experience connects to a pricing service that calculates quote and line prices. Pricing fields on the quote header and lines are populated automatically, so sales representatives see current prices, margins, and totals as they build a quote.

## Pricing integration model

You enable pricing by connecting the ServiceNow Quote Experience to the pricing service and turning on the productized pricing integration tenant setting. With the productized integration, field-to-context mappings load automatically from the quote blueprint when you deploy it, so you do not hand-configure request and response transformations.

If a pricing input has no matching quote field during deployment, the deployment records a warning and continues. It does not fail. Administrators set up the pricing connection and integration during configuration. For more information, see [Configuring ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-crm-tm-quoting-configure.md).

## Pricing states

The Quote Experience records a pricing state for the quote header and for each quote line. The state shows whether the current prices reflect the latest changes, so a representative can tell when a reprice is needed before sharing or submitting a quote.

-   **Up-to-date**

    The prices reflect the most recent pricing call. No pricing-affecting change has occurred since the last successful reprice.

-   **Needs reprice**

    A pricing-affecting field has changed since the last successful pricing call, so the current prices might be out of date. The quote or line stays in this state until a pricing call completes successfully.


The header shows a **Last Priced** timestamp that records when the most recent successful pricing call completed. Each line shows its own pricing state so that representatives can identify exactly which lines need attention.

A quote or line is marked as needing a reprice when a pricing-affecting field changes. Pricing-affecting fields are the inputs that determine price, such as quantity, price list, discount, or product configuration. Changing a field that does not affect price, such as a description, does not change the pricing state. The needs-reprice state persists on the quote across other processing, such as rules evaluation, until a successful pricing call clears it. A successful pricing call returns the affected quote or line to the up-to-date state.

## Manual and automatic repricing

You can reprice a quote in the following ways:

-   **Manual repricing**

    Reprice a quote or line explicitly with the **Reprice** action when you are ready to recalculate pricing.

-   **Event-driven repricing**

    Certain actions, such as adding or reconfiguring a product, carry a reprice action and trigger a pricing call automatically. Additionally, you can add reprice actions to the custom events.

-   **Automatic repricing**

    The ServiceNow Quote Experience can reprice quotes that need a reprice without a representative selecting **Reprice**, so a quote that is left idle does not stay out of date.


Administrators tune which events trigger repricing and how automatic repricing behaves per lifecycle stage during configuration.

## Manual and automatic adjustments

The Quote Experience supports two kinds of price adjustments:

-   **Manual adjustments**

    A sales representative applies a discount, markdown, or price override to a line or to the quote total. The Quote Experience preserves a manual adjustment as a distinct, rep-supplied input, so the next pricing call does not overwrite it. Manual adjustments are auditable.

-   **Automatic adjustments**

    The pricing service applies rule-driven adjustments, such as volume tiers, promotions, and contracted discounts, during a pricing call. Automatic adjustments recalculate on each call as inputs change.


Where both apply to the same line or header, a manual adjustment takes precedence over an automatic adjustment.

