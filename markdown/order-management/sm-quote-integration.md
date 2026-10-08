---
title: Subscription Management in Quote Experience
description: Quote Experience integrates with existing subscription workflows to support the Subscription Management lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sm-quote-integration.html
release: brazil
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Subscription Management in Quote Experience

Quote Experience integrates with existing subscription workflows to support the Subscription Management lifecycle.

## Integration overview

A system-provided blueprint defines the transaction fields, line type and line action fields, business rules, and guardrails that Quote Experience uses to populate and validate subscription quotes.

Sales agents use Quote Experience to create quotes and orders for subscription product offerings. When an agent completes the order, the system creates a contract that serves as the system of record for subscriptions. Subscription workflows manage the subscription lifecycle.

## Amendments and renewals

Sales agents can update a contract through amendments and renewals. For example, an amendment can increase or decrease the quantity of an existing subscription product offering. A renewal can change the renewal date.

Subscription workflows process amendments and renewals, assigning the line type and line action based on the change.

The workflows pass the data to Quote Experience, which uses the system-provided blueprint to populate the transaction fields.

Quote Experience uses the line type and line action fields to represent the change and support downstream processing. For example, an upsell requiring additional quantity splits the line. The workflow sets the line type to **Amend** and the line action to **Add** for the additional quantity. Quote Experience uses these values to represent the change on the quote.

Quote Experience also applies business rules and guardrails when it processes a quote. Business rules and guardrails support amendment and renewal processing and prevent changes that would invalidate the quote.

Together, the transaction fields, line types and line actions, business rules, and guardrails in the system-provided blueprint control how Quote Experience represents and processes subscription amendments and renewals.

**Related topics**  


[Quote Experience configuration for subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sm-configuring-subscription-quote-experience.md)

