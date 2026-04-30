---
title: Show item details in sections or pop-ups
description: By default, a service catalog category displays the first two items with the preview section expanded to show item details. You can change the number of items that are previewed, or change the preview to appear in a pop-up window.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service catalog home page configuration, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Show item details in sections or pop-ups

By default, a service catalog category displays the first two items with the preview section expanded to show item details. You can change the number of items that are previewed, or change the preview to appear in a pop-up window.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  To change the number of items previewed, set the **Number of Catalog Items to expand in browsing and search when not using pop-up icons to view details** \(**glide.sc.auto\_expand**\) property to the desired number.

<table id="table_wvc_glq_lq"><tbody><tr><td>

Expanded to 2 items.

</td><td>

Expanded to 1 item.

</td></tr><tr><td>



 ![](../image/SC_ShowItemDetailsCol-1.png)

</td><td>



 ![](../image/SC_ShowItemDetailsCol-2.png)

</td></tr></tbody>
</table>3.  To use the preview icon, set the **When browsing a category use the pop-up icon to show item details** \(**glide.sc.cat\_view\_use\_popup\_for\_details**\) property to **Yes**.

<table id="table_wvc_glq_lr"><tbody><tr><td>

When set to **No**, the item details appear when you click **Preview**.

</td><td>

When set to **Yes**, the item details appear as a pop-up when the cursor hovers over the item icon.

</td></tr><tr><td>



 ![](../image/SC_ShowItemDetailsPopup-1.png)

</td><td>



 ![](../image/SC_ShowItemDetailsPopup-2.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Service catalog home page configuration](../concept/c_ManagingTheHomepageForACatalog.md)

