---
title: Limit description sizes in the Classic Mobile UI
description: By default, item descriptions in the smartphone interface are truncated to a maximum of two lines.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Classic Mobile devices, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Limit description sizes in the Classic Mobile UI

By default, item descriptions in the smartphone interface are truncated to a maximum of two lines.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  Set the **Limit descriptions in category and item listings to two rows in the Mobile UI** property \(glide.sc.mobile.limit.description\) to **No**.

<table id="table_wvc_glq_lq"><tbody><tr><td>

If set to **Yes**, descriptions are limited to two lines

</td><td>

If set to **No**, the full descriptions are given

</td></tr><tr><td>



 ![Screenshot for setting the property to Yes](../image/ServiceCatalog2LineLimitMobileUIYes.png)

</td><td>



 ![Screenshot for setting the property to No](../image/ServiceCatalog2LineLimitMobileUINo.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Configure Classic Mobile devices](t_ServiceCatalogOnMobileDevices.md)

**Related topics**  


[Define the mobile layout](t_DefiningMobileLayout.md)

