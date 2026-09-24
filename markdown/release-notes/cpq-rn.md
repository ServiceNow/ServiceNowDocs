---
title: ServiceNow Quote Experience release notes
description: The ServiceNow Quote Experience application is enhanced to manage complete lifecycle of Subscription Management workflows, and productized pricing across contract, sales product, and purchase item scenarios. See the following sections for release notes by version.This release adds subscription amendments and renewals for simple products, guardrails for amendment and renewal, and a pricing integration for calculating and adjusting transaction pricing from a quote.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/cpq-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Quote Experience release notes

The ServiceNow Quote Experience application is enhanced to manage complete lifecycle of Subscription Management workflows, and productized pricing across contract, sales product, and purchase item scenarios. See the following sections for release notes by version.

## About ServiceNow Quote Experience

The ServiceNow Quote Experience is enhanced to integrate with Subscription Management and supports the complete lifecycle of Subscription Management workflows. Using ServiceNow Quote Experience, you can:

-   Amend a contract by adding or removing products mid-term, including upsells and downsells. The Pricing Service automatically calculates deltas and adjusts pricing changes accordingly.
-   Swap one product offering with another. Initiate a full or partial swap, while maintaining contract continuity.
-   Create an auto-renewal automatically, enabling a renewal pipeline before expiration.
-   Initiate an early or late renewal and add or remove products during the renewal process, providing greater flexibility to accommodate changing needs.

See [ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quoting-experiences-overview.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install the Pricing Management application \(`sn_csm_pricing`\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/install-price-management.md).


## Accessibility and localization

-   **Accessibility information**
    -   ServiceNow Quote Experience is now fully accessible when using dark themes, so you can view and interact with all interface elements clearly in a dark-themed environment.
-   **Localization information**

    Enhanced localization in CPQ: Translation and localization support is enhanced to include product offering labels, definitions, and field text in CPQ. Content is translated at compile time, enabling multilingual configuration workflows and a more consistent localized experience.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Brazil Early Availability

This release adds subscription amendments and renewals for simple products, guardrails for amendment and renewal, and a pricing integration for calculating and adjusting transaction pricing from a quote.

### What's new

-   **ServiceNow Quote Experience Experience integration with Contracts**

    Amend simple and configurable products that originate from a contract, directly within a quote. Amend the products from a contract to complete upsell, downsell, and end-date changes, including early termination and extension. You can also renew the products from a contract using standard renewal, early renewal, or automatic renewal operations.

-   **ServiceNow Quote Experience Integration with Subscription Management**

    Subscription Management integrates with ServiceNow Quote Experience, CPQ Configurator, and the Pricing Management to provide a unified experience throughout the Subscription Management lifecycle.

-   **ServiceNow Quote Experience integration with Pricing Management**

    Calculate and adjust transaction pricing directly from a quote.

    -   Enable Pricing setup without manual field mappings. Set the pricing integration type to **productized**, and the application loads context-variable mappings from blueprint metadata and connects to the pricing service automatically when the blueprint is deployed.
    -   Reprice on demand or automatically. Recalculate transaction pricing with the Reprice action, or let it recalculate when a configuration is added to a quote. Administrators can turn off the default triggers for each event.
    -   Set automatic pricing behavior by stage. For example, enable automatic reprice in **Draft** stage, but disable for **Order Submitted** stage.
    -   Adjust prices manually. Apply a fixed-amount or percentage discount or uplift to a line or the header total. Each adjustment is preserved as a distinct input and tracked for audit.
    -   Apply automatic price adjustments. Use rules such as volume tiers, promotions, and contracted discounts during a pricing call. A manual adjustment always takes precedence over an automatic one on the same line or header.

