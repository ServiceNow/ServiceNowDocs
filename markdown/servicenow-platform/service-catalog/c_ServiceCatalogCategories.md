---
title: Service catalog categories
description: Categories organize service catalog items into logical groups. Administrators and catalog administrators can create and configure categories, defining their characteristics and adding content such as catalog items to them.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service catalog categories

Categories organize service catalog items into logical groups. Administrators and catalog administrators can create and configure categories, defining their characteristics and adding content such as catalog items to them.

Categories can have a parent-child relationship, for example, **IT** and **Laptops**. A child category is a subcategory of its parent category. Each catalog item, order guide, record producer, content item, and subcategory appears as a single item within the category. A catalog item can exist in multiple categories, giving you the flexibility to offer the same service from multiple places within your catalog.

Certain system properties control the following Service Catalog category configuration.

-   How categories are displayed to users. For example, are subcategories displayed in a panel or as a list in the category view.
-   What content types and search and navigation elements are available on the homepage. For example, searching the service catalog can be enabled or disabled for all users.
-   How catalog items, item class names and item categories appear to users. For example, what number of catalog items or categories are previewed in a section.

Catalog managers and catalog editors can also configure categories, but only categories to which they are assigned.

**Note:**

-   If there are no active items in a category’s hierarchy, that category does not appear in the catalog, and cannot be added to the catalog.
-   Users with the admin or catalog\_admin roles can view categories only if there is an active item in the category and **Availability** is set to either **Desktop** or **Both**.
-   Configure the **glide.sc.category.canview.override** property to change the roles for this behaviour.

-   **[Create a category](../task/t_CreateACategory.md)**  
Administrators and catalog administrators can create or edit a category.
-   **[Configure dynamic categories](../task/t_ConfigureDynamicCategories.md)**  
Dynamic categories let you organize and display commonly requested items and knowledge articles. Dynamic categories appear on the right side of the service catalog homepage by default.

**Parent Topic:**[Configuring Service Catalog](configuring-service-catalog.md)

