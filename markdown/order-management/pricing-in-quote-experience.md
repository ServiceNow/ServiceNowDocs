---
title: Pricing in the ServiceNow Quote Experience
description: ServiceNow Quote Experience integrates natively with CPQ Price Management, enabling your organization to set, manage, and optimize pricing strategies for Quotes. These pricing strategies enable your sales team to generate quotes with accurate and competitive pricing quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/pricing-in-quote-experience.html
release: brazil
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 5
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Pricing in the ServiceNow Quote Experience

ServiceNow Quote Experience integrates natively with CPQ Price Management, enabling your organization to set, manage, and optimize pricing strategies for Quotes. These pricing strategies enable your sales team to generate quotes with accurate and competitive pricing quickly.

Price evaluations can be triggered manually by a user or automatically when a price affecting field value changes. Price strategies support both user-entered and rule-driven price adjustments. For more information, see [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-management.md).

## Enable pricing for the Quote Experience

To enable pricing for the Quote Experience, complete the following steps:

1.  Complete CPQ setup for Quote Experience. For more information, see [Setting up CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/setup-cpq-integrator.md).
2.  Install the required [Price Management plugins](https://www.servicenow.com/docs/r/australia/order-management/quoting-experiences-overview.html).
3.  Submit a support ticket requesting the required tenant setting configurations for your instance:
    1.  transaction.oneQuoting.pricing.enabled to 'TRUE'
    2.  transaction.oneQuoting.pricing.integration.type to 'productized'
4.  Export and import the quote blueprint in CPQ Administration.

## Pricing states

The Quote Experience records a state for the quote header \(`txn.pricing.state`\) and for each quote line \(`txn.line.pricing.state`\) that indicates whether price values are up-to-date or need a reprice.

-   **Up-to-date**

    The prices reflect the most recent pricing call. No pricing-affecting change has occurred since the last successful reprice.

-   **Needs reprice**

    A pricing-affecting field has changed since the last successful pricing call, so the current prices might be out of date. The quote or line stays in this state until a pricing call completes successfully.


Pricing-affecting fields are the inputs that determine price, such as quantity, price list, discount, or product configuration. Changing a field that does not affect price, such as a description, does not change the pricing state.

## Last priced

The timestamp of the most recent successful pricing call is stored in the Last Priced \(`txn.pricing.lastPriced`\) field.

## Automatic and manual repricing

Price updates can be configured to run automatically or explicitly through an event \(user- or API-triggered\). Manual repricing allows sales representatives to request an updated price at any time. Automatic repricing ensures prices are recalculated when pricing-affecting fields change.

-   To configure the Reprice event action, see [Transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-events.md).
-   To configure automatic repricing per stage, see [Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-stages.md).

## Context variables

Context variables bring information beyond the product itself into pricing decisions — such as customer, channel, geography, term, transaction type, or usage. A single pricing rule can condition on that context instead of requiring a separate rule for every permutation. CPQ Pricing uses context variables to execute price rules, matrices, and calculations. A set of system-defined context variables is provided, and administrators can create custom variables.

**Important:** Pricing in the ServiceNow Quote Experience uses field-mapped context variables. Variable mappings using dot-walked fields or scripted values are not supported.

To implement a custom context variable to pricing:

1.  Define custom context variables in the Context Rule Management section of the CRM Workspace.
2.  Set **Entity** to **Quote Advanced**.
3.  Set **Table** to either Quote \(`sn_quote_mgmt_core_quote`\) or Quote Line Item \(`sn_quote_mgmt_core_quote_line_item`\)
4.  Sync it to CPQ.

For more information on creating and managing context variables, see the following resources:

-   [Create a custom context variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-create-context-variable.md)
-   [Map a custom context variable to a transaction entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-map-variable.md)
-   [Sync context variables to CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sync-variable-to-cpq.md)

## Field mapping

Custom transaction fields used by pricing must be mapped to columns on the Quote or Quote Lines tables. This mapping ensures that pricing data syncs between the transaction and the quote record. For the procedure, see [Configure transaction-to-quote field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configure-opportunity-quote-mapping.md).

## Manual price adjustments

A sales representative can apply a manual adjustment — a fixed-amount or percentage discount or uplift, or a price override — to a line or to the header total. A manual adjustment is preserved as a distinct, rep-supplied input and is not overwritten by the next pricing call. The key fields for manual adjustments are:

-   Discount Adjustment Type \(txn.line.pricing.adjustment.type\)
-   Discount Adjustment Value \(txn.line.pricing.adjustment.value\)
-   Discount Reason \(txn.line.pricing.discountReason\)

For additional field information, see [Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-line-level-system-fields.md).

**Related topics**  


[Enable pricing in the ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-pricing-quote-experience.md)

[Set up an external connection in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/set-up-external-connection-logik.md)

[Transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-events.md)

[Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-stages.md)

[Map a custom context variable to a transaction entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-map-variable.md)

[Sync context variables to CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sync-variable-to-cpq.md)

[Configure transaction-to-quote field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configure-opportunity-quote-mapping.md)

[Transaction-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-header-level-system-fields.md)

[Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-line-level-system-fields.md)

