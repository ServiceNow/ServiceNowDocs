---
title: ServiceNow Quote Experience release notes
description: The ServiceNow Quote Experience application is enhanced to manage complete lifecycle of Subscription Management workflows, and productized pricing across contract, sales product, and purchase item scenarios. See the following sections for release notes by version.A system-provided blueprint defines the fields and rules for populating, representing, and validating quote data so ServiceNow Quote Experience can process subscription amendments and renewals accurately and consistently.This release adds subscription amendments and renewals for simple products, guardrails for amendment and renewal, and a pricing integration for calculating and adjusting transaction pricing from a quote.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/cpq-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
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

See [Subscription Management in Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-integration.md).

## Activation and other requirements

-   **Activation information**

    Install the Pricing Management application \(`sn_csm_pricing`\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/install-price-management.md).


## Accessibility and localization

-   **Accessibility information**

    Color contrast in ServiceNow Quote Experience was updated to display all interface elements clearly in dark-themed environments. This update helps users view and interact with all interface elements clearly in a dark-themed environment.

-   **Localization information**

    Enhanced localization in CPQ: Translation and localization support is enhanced to include product offering labels, definitions, and field text in CPQ. Content is translated at compile time, enabling multilingual configuration workflows and a more consistent localized experience.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## October 2026

A system-provided blueprint defines the fields and rules for populating, representing, and validating quote data so ServiceNow Quote Experience can process subscription amendments and renewals accurately and consistently.

### What's new

-   **[Quote Experience configuration for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-configuring-subscription-quote-experience.md)**

    Import the system-provided blueprint to define the fields and rules for populating, representing, and validating quote data. The blueprint includes transaction header-level fields, transaction line-level fields, line type and line action fields, business rules, and guardrails that enable ServiceNow Quote Experience to process subscription amendments and renewals.

-   **[Transaction header-level system fields for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-tm-system-fields.md)**

    Reference the transaction header-level fields that ServiceNow Quote Experience uses to process subscription amendments and renewals.

-   **[Transaction line-level system fields for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-tm-system-line-fields.md)**

    Reference the transaction line-level fields that ServiceNow Quote Experience uses to process subscription amendments and renewals.

-   **[Line type and line action fields for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-tm-line-type-action-fields.md)**

    Reference the line type and line action fields that ServiceNow Quote Experience uses to process subscription amendments and renewals. These values add context to transaction fields and identify the type of change and action required for upsells, downsells, end date changes, product swaps, and standard and early renewals.

-   **[Header-level and line-level business rules for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-tm-header-level-business-rules.md)**

    Reference the business rules that ServiceNow Quote Experience uses to process data from subscription workflows. Business rules work with transaction fields, line type, and line action to support accurate quote processing and downstream workflows.

-   **[Guardrail rules for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-tm-subscription-guardrails-quote.md)**

    Reference the guardrails that ServiceNow Quote Experience uses to help prevent invalid changes during amendment and renewal processing. Guardrails work with transaction fields, line type, line action, and business rules to maintain quote validity.


## Brazil Early Availability

This release adds subscription amendments and renewals for simple products, guardrails for amendment and renewal, and a pricing integration for calculating and adjusting transaction pricing from a quote.

### What's new

-   **ServiceNow Quote Experience Experience integration with Contracts**

    Amend simple and configurable products that originate from a contract, directly within a quote. Amend the products from a contract to complete upsell, downsell, and end-date changes, including early termination and extension. You can also renew the products from a contract using standard renewal, early renewal, or automatic renewal operations.

-   **ServiceNow Quote Experience Integration with Subscription Management**

    Subscription Management integrates with ServiceNow Quote Experience, CPQ Configurator, and the Pricing Management to provide a unified experience throughout the Subscription Management lifecycle.

-   **[Pricing in the ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-in-quote-experience.md)**

    Calculate and adjust transaction pricing directly from a quote.

    -   Enable Pricing setup without manual field mappings. Set the pricing integration type to **productized**, and the application loads context-variable mappings from blueprint metadata and connects to the pricing service automatically when the blueprint is deployed.
    -   Reprice on demand or automatically. Recalculate transaction pricing with the Reprice action, or let it recalculate when a configuration is added to a quote. Administrators can turn off the default triggers for each event.
    -   Set automatic pricing behavior by stage. For example, enable automatic reprice in **Draft** stage, but disable for **Order Submitted** stage.
    -   Adjust prices manually. Apply a fixed-amount or percentage discount or uplift to a line or the header total. Each adjustment is preserved as a distinct input and tracked for audit.
    -   Apply automatic price adjustments. Use rules such as volume tiers, promotions, and contracted discounts during a pricing call. A manual adjustment always takes precedence over an automatic one on the same line or header.
-   **Configure ServiceNow Quote Experience through Guided Setup**

    Set up ServiceNow Quote Experience directly from the Guided Setup for CPQ Integration. Configure it alongside the rest of your CPQ integration in a single guided flow, instead of configuring components separately.


