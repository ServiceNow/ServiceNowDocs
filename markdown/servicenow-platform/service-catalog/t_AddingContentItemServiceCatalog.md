---
title: Define a content item
description: A content item is a service catalog item that provides information instead of goods or services.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a content item

A content item is a service catalog item that provides information instead of goods or services.

## Before you begin

Role required: admin

## About this task

Content items can reference knowledge articles, static blocks of text, or external web-based content.

To define content items:

## Procedure

1.  Navigate to **All** &gt; **Service Catalog &gt; Catalog Definition &gt; Content Items**.

2.  Click **New**.

3.  Fill in the form to define the item.

<table id="table_hkx_rkd_fcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name, Category, Icon, Roles, Active,

</td><td>

As for standard catalog items.

</td></tr><tr><td>

Content type

</td><td>

The type of information to display when a user selects the item. -   **KB Article**: a ServiceNow knowledge article available to users with the specified roles.
-   **Catalog Content**: a static block of text, formatted with HTML.
-   **External Content**: documents or web pages stored outside the base system instance.


</td></tr><tr><td>

Target

</td><td>

Location where the content appears. -   **Within Catalog**: displays the content within the catalog iframe window \(which may not render some external websites properly\).
-   **New Window/Tab**: displays the content in a new browser window or tab. Choose this option if the content does not display properly within the catalog.


</td></tr><tr><td>

URL

</td><td>

The full URL \(including the prefix http:// or https://\) for external content to display when a user selects the item. This field is available only if the **Content type** is **External Content**. **Note:** Since base system instances are accessed via HTTPS, links to HTTP sites could result in a mixed mode content error or warning, depending on browser security settings.

</td></tr><tr><td>

KB article

</td><td>

The knowledge article to display when a user selects the item. This field is available only if the **Content type** is **KB Article**.

</td></tr><tr><td>

Short description, Description, Picture

</td><td>

As for standard catalog items. These fields are only available if the **Content type** is **Catalog Content**.

</td></tr><tr><td>

Meta

</td><td>

Comma-separated list of tags used to search for the content item. See [Configure keyword search for catalog items](search-catalog-item.md).

</td></tr><tr><td>

Hide on Service Portal

</td><td>

If selected, the content item is not available on Service Portal.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

