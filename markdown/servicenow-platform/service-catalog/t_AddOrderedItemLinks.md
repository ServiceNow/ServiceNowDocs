---
title: Add an ordered item link to an item
description: Use ordered item links to provide a link on the ordered item screen that provides more information about an item.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add an ordered item link to an item

Use ordered item links to provide a link on the ordered item screen that provides more information about an item.

## Before you begin

Role required: Catalog administrator

## About this task

After you order the catalog item, you can click the link to see relevant information about the item ordered, for example, for standard delivery terms and conditions. The URL text and link can be defined once and reused across multiple items.

Links are rendered with an added parameter providing the sys\_id of the requested item. For example, if the link is mylink.com, it is rendered as mylink.com?req\_item=abcde12345. This added parameter can be useful for virtual provisioning situations.

**Note:** Ordered item links cannot be configured for Classic Mobile devices.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Ordered Item Links**.

2.  Click **New**.

3.  Enter a **Name** for the ordered item link.

4.  Enter **Link text** to display as the link.

    For example, `Click here to see more information about the iPhone`.

5.  Enter the exact **Link URL**.

    For example, http://www.mylink.com.

6.  Select the **Target**.

    You can choose to open the link in a new window or tab, or within the catalog. If Within Catalog is chosen, the link must be within the same site. An HTTP site cannot be called from within HTTPS.

7.  Click **Submit**.

8.  Navigate to **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

9.  Click an item **Name**.

10. In the **Ordered Item Link** field, click the reference lookup icon.

11. Click an ordered item link **Name**.

12. Click **Update**.


**Parent Topic:**[Service Catalog items](../concept/c_IntroductionToCatalogItems.md)

