---
title: Quote Experience configuration for subscriptions
description: Subscription workflows provide the data that Quote Experience uses to process amendments and renewals. A system-provided blueprint defines the fields and rules that Quote Experience uses to populate, represent, and validate the data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sm-configuring-subscription-quote-experience.html
release: brazil
topic_type: concept
last_updated: "2026-09-20"
reading_time_minutes: 2
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote Experience configuration for subscriptions

Subscription workflows provide the data that Quote Experience uses to process amendments and renewals. A system-provided blueprint defines the fields and rules that Quote Experience uses to populate, represent, and validate the data.

The system-provided blueprint components work together to enable Quote Experience to process amendments and renewals accurately. Subscription workflows provide and assign the data, while Quote Experience uses the blueprint to populate the quote, apply business rules, and prevent invalid changes.

## Transaction fields

Transaction fields define the information that Quote Experience uses to represent a subscription amendment or renewal. The fields include transaction header-level and line-level information.

Subscription workflows process the subscription data and pass it to Quote Experience, which uses the system-provided blueprint to populate transaction fields.

Line type and line action data add context to the transaction fields, indicating how the quote represents the change.

## Line type and line action

Subscription workflows assign the line type and line action based on the amendment or renewal and pass these values to Quote Experience with the subscription data.

For configurable product offerings, the CPQ Configurator processes the changes by splitting lines and assigning line types and line actions. For more information about the CPQ Configurator, see [CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/explore-servicenowcpq.md).

For non-configurable product offerings, Quote Experience uses the line type and line action values to represent the change on the quote and to support downstream workflows. For example, an upsell requiring additional quantity creates a split line. The workflow sets the line type to **Amend** and the line action to **Add** for the additional quantity.

Line type and line action values identify the type of change and the action required for specific amendment and renewal use cases. The use cases include upsells, downsells, end date changes, product swaps, and standard and early renewals.

## Business rules

Business rules define how Quote Experience processes the data that subscription workflows provide. For example, a business rule clears the renewal adjustment type and value when the renewal basis is not set to Contracted Price.

Business rules work with the transaction fields, line type, and line action to support consistent and accurate quote processing and valid downstream workflows.

## Guardrails

Quote Experience applies guardrails to prevent changes that would make an amendment or renewal invalid. For example, a guardrail resets an upsell line quantity to `1` if it was set to less than `1`. It also resets the line end date if it is earlier than the start date.

Guardrails work with the transaction fields, line type, line action, and business rules to maintain the validity of the quote.

## Quote Experience and subscription workflow integration

Subscription workflows process amendments and renewals for non-configurable product offerings, package the data, and assign the line type and line action for Quote Experience.

Quote Experience uses the system-provided blueprint to populate the transaction fields, and the line type and line action to represent the change and support downstream workflows.

Quote Experience applies business rules and guardrails to process the quote and prevent changes that would make the amendment or renewal invalid.

Together, subscription workflows and the Quote Experience blueprint provide the data, processing rules, and controls required to process the quote accurately and support downstream workflows.

**Related topics**  


[Subscription Management in Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-quote-integration.md)

