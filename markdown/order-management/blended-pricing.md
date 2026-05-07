---
title: Blended pricing for contract consolidation of subscription renewals
description: When selected contract lines are consolidated into a renewal line for renewal purposes, the pricing engine uses blended pricing to calculate the renewal line pricing.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Blended pricing for contract consolidation of subscription renewals

When selected contract lines are consolidated into a renewal line for renewal purposes, the pricing engine uses blended pricing to calculate the renewal line pricing.

## Overview of renewal pricing in contract consolidation

Over the life of a subscription, contract quantities can change due to the following:

-   **Upsells**: Changes to a customer contract that increase its value by adding more quantity, licenses, or new products or services. These changes can result in  one or more new contract lines or an amendment, while the original contract remains in effect.
-   **Downsells**: Changes to a customer contract that reduce the quantity of a product or service and supersedes an earlier contract line.

In renewal pricing for contract consolidation, the pricing engine does the following:

-   Finds which contract lines are included in the renewal.
-   Aggregates the quantities for the contract lines in the renewal.
-   Blends prices and uplift increases to determine pricing for the single quote renewal line.

-   **How contract line changes are handled**

    Agents indicate which contract lines are to be consolidated by setting the **Renewable** option on a contract line. At renewal, active upsell lines and the latest downsell lines that represent the current base quantity are combined to calculate renewal pricing. The context variable **Consolidated From Contract Lines** identifies a consolidated quote renewal line. Within those consolidated lines, if the **Include quantity for renew** field is selected, the quantity is used in the price blending.

-   **How renewal quantity and prices are calculated**

    The pricing engine calculates prices on the quote renewal line using  weighted averages, based on the quantities of the contributing contract lines. The following values are blended:

    -   Base price
    -   Unit price
    -   List price \(after price increases, such as uplifts\)
-   **How contract lines with uplifts are calculated**

    An uplift is a price increase applied at contract renewal, typically expressed as a percentage, which raises the list price above the base price for a given term or period.

    If contributing contract lines have different uplift percentages:

    1.  Each contract line’s  uplifted price  is calculated first.
    2.  A  weighted average of the uplifted prices  is computed based on the current active contract lines.
    3.  The resulting value is set as the  list price  on the renewal line.
    Uplifts in contracts are handled as list price adjustments, where:

    -   During blending, the renewal base price is the weighted average of the unit price of the consolidated contract lines.
    -   The uplift is reflected in the list price.

## Controlling uplift values in contracts and renewals

You can configure the following uplift features:

-   Uplift amounts: To control uplift amounts that are applied, use the Price Increase Defaulting Matrix. For details, see [Create a price increase adjustment](../task/create-price-increase-adjustment.md).
-   Uplift renewal multiplier: To set the uplift renewal multiplier, use the **renewal\_uplift\_term ** system property. For more information, see [Set term multiplier for contract renewal uplift](../task/set-renewal-term-multiplier.md).

