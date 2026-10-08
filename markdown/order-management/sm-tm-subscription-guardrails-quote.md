---
title: Guardrail rules for subscriptions
description: Subscription guardrail rules are system-provided rules in Quote Experience that prevent invalid changes to non-configurable transaction lines during amendments and renewals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sm-tm-subscription-guardrails-quote.html
release: brazil
topic_type: reference
last_updated: "2026-09-21"
reading_time_minutes: 1
breadcrumb: [Quote Experience configuration for subscriptions, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Guardrail rules for subscriptions

Subscription guardrail rules are system-provided rules in Quote Experience that prevent invalid changes to non-configurable transaction lines during amendments and renewals.

## Guardrail rules

Subscription guardrails are available through the Quote Experience administration interface. Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Rule Groupings** and select `txnSubscriptionsGuardrails`.

Guardrails are part of the business rules for subscriptions and are included in the transaction blueprint.

The following table summarizes the system-provided rules for subscription guardrails.

|Variable name|Description|
|-------------|-----------|
|`subscriptionsUpsellStartDateLock`|Set upsell line start date to read-only|
|`subscriptionsUpsellEndDateReset`|Reset upsell line end date if less than its start date|
|`subscriptionsUpsellQuantityReset`|Reset upsell line quantity to `1` if less than `1`|
|`subscriptionsDownsellStartDateReset`|Reset downsell line start date if less than original line start date|
|`subscriptionsDownsellEndDateLock`|Set downsell line end date to read-only|
|`subscriptionsDownsellQuantityReset`|Reset downsell line quantity if it is less than or equal to `1` or greater than or equal to the original line quantity|
|`subscriptionsStandardRenewalStartDateLock`|Set renewal line start date to read-only|
|`subscriptionsStandardRenewalEndDateReset`|Reset renewal line end date if less than its start date|
|`subscriptionsStandardRenewalQuantityReset`|Reset renewal line quantity to `1` if less than `1`|
|`subscriptionsEarlyRenewalStartDateLock`|Set renewal line start date to read-only|
|`subscriptionsEarlyRenewalEndDateReset`|Reset renewal line end date if less than its start date|
|`subscriptionsEarlyRenewalQuantityReset`|Reset renewal line quantity to `1` if less than `1`|
|`subscriptionsGeneralEndDateSet`|Set the original line end date to one day before the amendment line start date on change|

