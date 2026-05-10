---
title: Modifications in the delivery screen
description: In the final checkout step, a summary screen provides a list of all items and services ordered.After you enable the two-step checkout process, the Requested for field appears on the Request form.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy flexible checkout and delivery forms, Cart layout, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modifications in the delivery screen

In the final checkout step, a summary screen provides a list of all items and services ordered.

**Warning:** Modifying the Order Status or Summary screen requires advanced scripting and a knowledge of [Jelly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/r_JellyTags.md). Also, the upgrade process skips updates to the summary screen after a customization. With these constraints in mind, you can modify the summary screen by editing the **com.glideapp.servicecatalog\_checkout\_view** UI page.

![Summary of ordered items and link to the request](../image/CatalogOrderSummaryStatus.png "Catalog order summary status")

**Parent Topic:**[Legacy flexible checkout and delivery forms](c_FlexibleCheckoutAndDeliveryForms.md)

## Requester search results

After you enable the two-step checkout process, the Requested for field appears on the Request form.

The Requested for field references the User `[sys_user]` table and has an auto-complete feature. Two service catalog properties \(**Service Catalog** &gt; **Catalog Administration** &gt; **Properties**\) enable an administrator to add columns to the search results for this field and to order the list by one of the columns.

<table id="table_zhc_4c2_zp"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional columns for the "request for" Service Catalog widget.\(glide.sc.request\_for.columns\)

</td><td>

Choose fields from the User `[sys_user]` table. Must be semicolon separated.

</td></tr><tr><td>

Ordering of matches for the "request for" Service Catalog widget.\(glide.sc.request\_for.order\_by\)

</td><td>

Choose fields from the User `[sys_user]` table.

</td></tr></tbody>
</table>