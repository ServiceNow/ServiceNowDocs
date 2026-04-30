---
title: Define item quantity choices
description: In the Service Catalog, the default quantity choices are 1–10. You can configure the quantity selector with additional choices. This configuration is also applicable in Service Portal.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define item quantity choices

In the Service Catalog, the default quantity choices are 1–10. You can configure the quantity selector with additional choices. This configuration is also applicable in Service Portal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Choice Lists**.

2.  Search for the table **sc\_cart\_item** and the element **quantity**.

    The existing quantity choices appear.

3.  Add quantity choices, modeling them after the existing ones.

    To reduce the quantities available for catalog items, delete the relevant quantity records. For example, to reduce the quantity range to 1-3, delete the records for 4 and 5.

    To restrict the roles allowed to change quantities, edit the **List of roles \(comma-separated\) that can use the quantity selector in the shopping cart** \(**glide.sc.allow.quantity**\) service catalog property. For example, you can limit this ability to the admin and catalog\_admin roles.


**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

**Related topics**  


[Service Catalog administration](t_ServiceCatalogAdministration.md)

