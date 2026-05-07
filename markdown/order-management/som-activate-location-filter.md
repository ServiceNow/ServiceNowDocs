---
title: Activate location-based transactions
description: Turn on location-based transactions for opportunities, quotes, and orders by using the sn\_sales\_common.enable\_location\_based\_transactions system property.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Location-based product transactions, Configuring agent tools in Sales CRM, Configure, Sales Customer Relationship Management]
---

# Activate location-based transactions

Turn on location-based transactions for opportunities, quotes, and orders by using the **sn\_sales\_common.enable\_location\_based\_transactions** system property.

## Before you begin

Role required: admin

## About this task

The **sn\_sales\_common.enable\_location\_based\_transactions** system property enables your agents to select a customer location and view only the eligible products for that customer location when adding product lines to an opportunity, quote, or order. This feature also enables agents to copy line items to another location within the same transaction \(opportunity, quote, or order\).

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **sn\_sales\_common.enable\_location\_based\_transactions** system property.

3.  In the **Value** field, enter `true`.

4.  Select **Update**.

    The location filter is displayed in the product catalog interface. Agents can use the filter to select a location when adding product lines to an opportunity, quote, or order. The catalog displays the eligible product offerings for the location. After adding products from the catalog, agents can then copy selected products \(line items\) to another location within the same transaction, without having to create another opportunity, quote, or order for a different customer location.


## What to do next

Define the [product eligibility rule filters](som-create-rule-entity-filter.md) and [matrices](som-define-eligibility-rules.md) that control the product offerings displayed by location.

**Parent Topic:**[Configuring location-based product transactions](../concept/config-location-transaction.md)

