---
title: Sync quote and opportunity
description: Sync quote information from the quote record to an opportunity record. This keeps the quote data consistent and accurate across both the records and enables sales agents to track revenue from opportunities accurately.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Opportunity Management, Lead and opportunity apps, Use, Sales and Order Management]
---

# Sync quote and opportunity

Sync quote information from the quote record to an opportunity record. This keeps the quote data consistent and accurate across both the records and enables sales agents to track revenue from opportunities accurately.

## Establish a sync between quote and opportunity

As a sales agent, you can establish the sync between quote and opportunity records and ensure that a defined set of fields between opportunity-quote and opportunity line items-quote line items remain synchronized.

When a quote is created through an opportunity, the **Source Opportunity** field on the quote record is automatically populated with the details of the opportunity through which the quote is created. To create a quote through an opportunity, see [Create a quote](../task/create-new-quote.md).

When a quote is created with child line items, the revenue metrics and prices for the quote are automatically calculated. To learn more about the revenue metrics and how they’re calculated, see [Subscription revenue metrics](som-subscription-pricing.md).

When the quote record is synchronized with the opportunity record, the prices and revenue metrics are also synced and are consistent across both forms.

The **Synced** banner on the **Details** tab on the opportunity record displays whether the quote is in sync with its opportunity. To automatically sync the first quote with its source opportunity, set the autoEnableSyncFirstQuote system property to **true**.

To learn more about establishing a sync between quote and opportunity and automatically enable sync, see [Sync a quote with an opportunity](../task/som-sync-quote-with-opportunity.md).

You can create a new version of a quote from a quote record to establish a sync between the new revised quote with the initial opportunity.

**Note:** The new version of the quote is in sync with the opportunity only if the previous version was also in sync.

View the new quote revisions from the **Revisions** tab on the quote record.

On the quote record, mark the **State** as **Accepted** or **Completed** to move the synced opportunity to **Closed-won**.

## Map quote and opportunity header fields and line items

As a sales agent, you can only edit and make changes on the fields on an opportunity record that aren’t in sync with a quote.

The following is a list of default field mappings between opportunity line items with quote line items and opportunity header with quote header fields. To learn more about the fields and their descriptions, see [Subscription revenue metrics](som-subscription-pricing.md).

|Opportunity header|Quote header|
|------------------|------------|
|Term \(months\)|Term \(months\)|
|Total one-time price|Total one-time price|
|Total MRR|Total Monthly Recurring price|
|Total ARR|Total Annual Recurring price|
|Amount|Total Amount|
|Primary Quote|Quote id ref|
|Currency|Currency|
|Price list|Price list|

|Opportunity Line items|Quote Line items|
|----------------------|----------------|
|Term \(months\)|Term \(months\)|
|Cumulative one-time price|Cumulative one-time price|
|Cumulative MRR|Cumulative Monthly Recurring price|
|Cumulative ARR|Cumulative Annual Recurring price|
|Cumulative TCV|Cumulative Net price|
|Product offering|Product Offering|
|Price list|Price list|
|Unit of measure|Unit of measure|
|Unit list price|Unit list price|
|Quantity|Quantity|
|Periodicity|Periodicity|
|Unit net price|Unit net price|

**Note:** When an opportunity and quote header, and an opportunity line item and quote line item are in sync with each other, the addition and deletion of line items on the opportunity record is disabled. All the synced fields on the opportunity and opportunity line item record becomes read only.

**Parent Topic:**[Using Opportunity Management](opportunity-mgmt-using.md)

