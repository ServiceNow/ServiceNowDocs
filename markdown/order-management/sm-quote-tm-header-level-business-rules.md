---
title: Header-level and line-level business rules for subscriptions
description: Business rules for subscriptions are system-provided rules in Quote Experience that enforce the integrity and validity of subscription-related transaction fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sm-quote-tm-header-level-business-rules.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Quote Experience configuration for subscriptions, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Header-level and line-level business rules for subscriptions

Business rules for subscriptions are system-provided rules in Quote Experience that enforce the integrity and validity of subscription-related transaction fields.

## Business rules for subscriptions

Business rules are available through the Quote Experience administration interface. Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Rule Groupings** and select `txnSubscriptionsBRs`.

Business rules validate subscription dates, term, line type, and renewal adjustment transaction fields and provide defaults, where applicable. They are included in the transaction blueprint.

The following table summarizes the system-provided business rules for subscriptions.

|Variable name|Description|
|-------------|-----------|
|Header-level business rules|
|`resetAdjustmentValuesWhenBasisChangesFromContractedPrice`|Clears the renewal adjustment type and value when the adjusted basis changes away from Contracted Price. Avoids stale adjustment settings from being applied to a new basis.|
|`contractStartDateBeforeEndDate`|Validates the contract start date does not fall after the contract end date. Blocks saves with invalid date ranges to avoid downstream term calculation errors.|
|`contractEndDateBeforeToday`|Helps prevent users from saving a contract end date earlier than the current date during interactive sessions.|
|`nonNegativeRenewalAdjustmentValue`|Blocks negative renewal adjustment values, which would invert pricing logic and create discounts instead of increases.|
|`defaultValuesContractedPrice`|Populates the default renewal adjustment type \(percentage\) and value \(0\) when the basis is Contracted Price and either field is missing. Avoids missing required inputs for Price Management.|
|`setTermAndContractEndDateHeader`|Auto-derives the contract end date from the start date and term, or derives the term from the date range. Keeps the three fields in sync and avoids quote lines inheriting invalid or inconsistent data.|
|Line-level business rules|
|`backCalculateContractStartDate`|Back-calculates the contract start date from the contract end date and term when the start date is missing. Helps prevent date range errors that would corrupt the renewal quote term.|
|`clearAutoRenewContractFlag`|Clears the auto-renew flag when the contract dates are incomplete on a top-level quote line. Helps prevent silent renewal failures due to missing trigger dates.|
|`clearRenewalAdjustmentTypeAndValue`|Clears the renewal adjustment type and value when the basis changes from Contracted Price on a quote line. Helps prevent stale adjustments from corrupting child line renewal pricing.|
|`renewalAdjustValueCannotBeNegative`|Blocks negative renewal adjustment values on quote lines. Helps prevent negative values from inverting pricing logic and creating unintended discounts.|
|`setDefaultValuesForContractedPriceQLI`|Populates default renewal type \(percentage\) and value \(0\) on quote lines when the basis is Contracted Price and fields are missing. Enables renewal pricing to be calculated.|
|`setHeaderInfoOnLineItemOnInsert`|Copies quote header information \(account, dates, renewal settings\) to new quote line items on insert.|
|`setQuoteLineTypeWhenEmpty`|Sets the line type to New or Upsell based on the header Quote Type when a new line is added from the Catalog.|
|`setTermAndContractEndDate`|Auto-derives the term and the contract end date based on supplied fields, keeping dates and terms in sync.|
|`dateValidationsMessageBR`|Validates contract date ranges on quote lines: Start date before end date, end date not in the past, child dates within parent bounds, line dates within header bounds. Helps prevent date hierarchy violations and expired contracts.|
|`validateStartDateNotRetroactive`|Helps prevent setting a past contract start date on amendment-type quotes during interactive sessions. Blocks retroactive amendments that could corrupt billing and audit trails.|

