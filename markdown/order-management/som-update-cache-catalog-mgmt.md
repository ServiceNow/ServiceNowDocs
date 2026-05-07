---
title: Update a cache in Product Catalog Management
description: Regenerate the cache associated with product offerings or product offering catalogs after changing the Unit of Measure in a product offering or category-related hierarchies in a product offering catalog.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Caching in Product Catalog Management, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Update a cache in Product Catalog Management

Regenerate the cache associated with product offerings or product offering catalogs after changing the **Unit of Measure** in a product offering or category-related hierarchies in a product offering catalog.

## Before you begin

Role required: sn\_prd\_pm.product-catalog\_admin, sn\_prd\_pm.product-catalog\_manager, or admin

## Procedure

1.  Navigate to the record that you updated.

<table id="choicetable_tty_nql_p1c"><thead><tr><th align="left" id="d105232e59">

Feature change

</th><th align="left" id="d105232e62">

Navigate to

</th></tr></thead><tbody><tr><td id="d105232e68">

**Unit of Measure \(UOM\) for a product offering**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Product Offering**.
2.  Select the product offering record that you just updated.


</td></tr><tr><td id="d105232e98">

**Product offering catalog changes-   Catalog to category
-   Category to sub-category
**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Product Offering Catalogs**.
2.  Select the product offering catalog record that you just updated.


</td></tr></tbody>
</table>2.  Right-click the **Additional actions** menu in the record header and select **Regenerate Configuration JSON**.

    The system immediately updates the associated cache for the product offering or product offering catalog. You can then view the changes that you made to the **Unit of Measure** in a product offering or the product offering catalog.


