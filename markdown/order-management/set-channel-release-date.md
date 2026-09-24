---
title: Set a channel-specific release date for a product offering
description: Add a channel override to a product offering so it becomes available on a specific sales channel on the date you choose.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/set-channel-release-date.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Channel-specific availability, Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Set a channel-specific release date for a product offering

Add a channel override to a product offering so it becomes available on a specific sales channel on the date you choose.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Offerings** &gt; **Product Offerings**.

4.  Select a product offering that you want to make available on a specific channel.

    The product offering must be in the Draft state.

5.  From the **More** drop-down menu, select the **Product Offering Channel Overrides** option.

6.  Select **New**.

7.  On the Channel override form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Product offering|Product offering to which the channel-specific availability applies. The value is populated from the product offering where you create the override.|
    |Channel|Distribution channel where you want the product offering to become available on different dates.|
    |Start date|Date when the product offering becomes available in the selected channel. Until this date, the offering is hidden from the channel in catalog search and AI Search.|
    |End date|Date when the product offering stops being available in the selected channel. If no end date is specified, the channel override continues to apply.|

    **Note:** While the offering is in Draft, you can set both a start date and an end date. After the offering is published, you can only change the end date, and only to a future date.

8.  Select **Save**.


## Result

The product offering stays hidden from the selected channel in catalog search and AI Search until the release date arrives.

**Parent Topic:**[Releasing product offerings by distribution channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-specific-availability.md)

**Related topics**  


[Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)

