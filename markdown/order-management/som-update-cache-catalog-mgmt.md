---
title: Update a cache in Product Catalog Management
description: Regenerate the cache associated with product offerings or product offering catalogs after changing the Unit of Measure in a product offering or category-related hierarchies in a product offering catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/som-update-cache-catalog-mgmt.html
release: brazil
topic_type: task
last_updated: "2026-11-17"
reading_time_minutes: 1
breadcrumb: [Caching in Product Catalog Management, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Update a cache in Product Catalog Management

Regenerate the cache associated with product offerings or product offering catalogs after changing the Unit of Measure in a product offering or category-related hierarchies in a product offering catalog.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin, sn\_prd\_pm.product\_catalog\_manager

## Procedure

1.  Navigate to the record that you updated.

<table id="choicetable_tty_nql_p1c"><thead><tr><th align="left" id="d123653e58">

Feature change

</th><th align="left" id="d123653e61">

Navigate to

</th></tr></thead><tbody><tr><td id="d123653e67">

**Unit of Measure \(UOM\) for a product offering**

</td><td>

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.
2.  Select the **List** view.
3.  Navigate to **Offerings** &gt; **Product Offerings**.
4.  Select the product offering record that you just updated.


</td></tr><tr><td id="d123653e113">

**Product offering catalog changes-   Catalog to category
-   Category to sub-category
**

</td><td>

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.
2.  Select the **List** view.
3.  Navigate to **Offerings** &gt; **Product Offering Catalogs**.
4.  Select the product offering catalog record that you just updated.


</td></tr></tbody>
</table>2.  Select the **More Actions** menu in the record header and select an option for the record type.

    -   **Regenerate Product Offering Cache** for a product offering
    -   **Regenerate Catalog Hierarchy Cache** for a product offering catalog
    The system immediately updates the associated cache for the product offering or product offering catalog. You can then view the changes that you made to the **Unit of Measure** in a product offering or the product offering catalog.


**Related topics**  


[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md)

