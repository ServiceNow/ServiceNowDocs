---
title: Releasing product offerings by distribution channel
description: Channel-specific availability lets you release a published product offering to different distribution channels on different dates. Use channel overrides to coordinate phased rollouts instead of launching everywhere at once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/channel-specific-availability.html
release: brazil
topic_type: concept
last_updated: "2026-09-16"
reading_time_minutes: 4
breadcrumb: [Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Releasing product offerings by distribution channel

Channel-specific availability lets you release a published product offering to different distribution channels on different dates. Use channel overrides to coordinate phased rollouts instead of launching everywhere at once.

Set a channel-specific release date to make a published product offering available in selected channels at different times. This flexibility helps you coordinate training, regional launches, partner readiness, and other rollout dependencies without delaying availability in channels that are ready.

By default, the start date on a product offering applies to every distribution channel. Agent assist is the default channel. Add a channel override when a channel requires a different release date.

## How effective dates affect catalog visibility

Every product offering has a Start date and an optional End date. When you open the catalog from a quote or an order, the catalog uses these dates to decide whether an offering appears. The offering appears only when the entity's transaction date falls within its effective period.

An offering's effective period follows these rules:

-   An offering whose start date hasn't arrived doesn't appear.
-   An offering whose end date has passed doesn't appear.
-   Both dates are inclusive, so an offering is available on its start date and on its end date.
-   An offering with no end date remains available indefinitely.

Effective dates filter the catalog listing, the result totals shown alongside it, and AI Search results.

For a quote or order dated in the future, the catalog evaluates effective dates against that transaction date instead of today's date. This lets you build a quote for a future date and see the offerings that will be effective on that date.

Effective date filtering doesn't apply when you open the catalog from an opportunity. Offerings outside their effective period still appear in that context.

An optional child product offering also carries its own effective date on the relationship to its parent offering. You can add an optional child offering to a published parent without creating a new version of the parent. The child offering appears in the CPQ Configurator product picker only after its effective date is reached.

## How channel-specific availability works

Use channel overrides to control when a product offering becomes available in each distribution channel.

-   Add channel overrides while the product offering is in Draft. After publication, you can adjust only the end date on an existing override, and only to a future date.
-   Control visibility until the release date. The offering remains hidden from the specified channel in catalog search and AI Search until the override date.
-   Adjust a published offering safely. After publication, you can change the date on an existing override only to a future date.
-   Keep availability current automatically. A nightly scheduled job applies channel availability as release dates arrive. You don't need to refresh the catalog manually.

For more information, see [6b5fdcd25ab225319356670c436121273b57b6e4.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/set-channel-release-date.md).

## Distribution channels

Each distribution channel includes a Value field. This field stores the canonical token that the system uses to match the channel at runtime, such as when a quote or order provides a channel through a context variable or header of the entity.

When you create a distribution channel, the system populates the Value field automatically. It reuses a matching order channel value when one exists. Otherwise, it derives the value from the channel name. Runtime matching uses the Value field, not the Name field. As a result, you can rename a distribution channel without interrupting channel-based filtering.

Predefined distribution channels include Web, Mobile, Service Exchange, and Agent assist.

## Example: Stagger a launch across channels

A product catalog admin plans to release a new mobile plan on the website two weeks before it becomes available in Agent assist. This approach gives support agents time to complete training before they can use the plan.

The admin adds a channel override for Web and sets its release date two weeks earlier than the offering’s default start date. As a result, the plan becomes available on the website on the override date. It becomes available in Agent assist and all other channels on the default start date.

You can use the same approach for a regional or partner rollout. For example, set an earlier override date for Service Exchange and continue to use the default dates for other channels.

-   **[Set a channel-specific release date for a product offering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/set-channel-release-date.md)**  
Add a channel override to a product offering so it becomes available on a specific sales channel on the date you choose.

**Parent Topic:**[Setting up specifications and product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-product-catalog.md)

**Related topics**  


[6b5fdcd25ab225319356670c436121273b57b6e4.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/set-channel-release-date.md)

[Components installed with Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/components-installed-catalog-mgmt.md)

[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

