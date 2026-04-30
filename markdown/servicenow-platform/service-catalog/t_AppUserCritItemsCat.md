---
title: Apply user criteria to items and categories
description: Apply a user criteria record to items and categories, either from the item or category form or from the user criteria form.Apply user criteria to an item to define which users can and cannot access that item.Apply user criteria to a category to define which users can and cannot access a category.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Set security for items and categories, Service Catalog security, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Apply user criteria to items and categories

Apply a user criteria record to items and categories, either from the item or category form or from the user criteria form.

## Before you begin

Role required: admin

## About this task

The user criteria restriction applies only within Service Catalog for the specific item that it’s applied for. However, the user criteria restriction isn’t applied outside the Service Catalog where the user has access to the item via the table.

To apply criteria directly to an item or category, use the Available For or Not Available For related lists in the Item or Category form.

**Note:**

-   Changes to the user's profile, such as location or department, apply immediately for standard user criteria. The catalog item visibility is updated without needing a new session. However, for the scripted user criteria, a session relaunch is needed for the changes to take effect.
-   The user criteria restrictions of a category don’t automatically apply to the catalog items within the category. If necessary, you should apply the user criteria restrictions to the individual catalog items.

To apply criteria directly from the User Criteria form, add items to the Available For Catalog Items and Not Available For Catalog Items related lists, and add categories to the Available For Categories and Not Available For Categories related lists. You can configure the User Criteria form to add these lists.

**Note:**

The **Not Available For** settings override **Available For** settings. A user on the **Not Available For** list for an item can’t access that item, even if that user is also on the **Available For** list for that item.

**Parent Topic:**[Set security for items and categories](../concept/c_ServiceCatalogAccessControls.md)

## Apply user criteria to items

Apply user criteria to an item to define which users can and cannot access that item.

### Before you begin

Role required: admin

### About this task

You can apply user criteria to all types of catalog item, including order guides, content items, and record producers.

**Note:** The user criteria restriction applies only within Service Catalog for the specific item it is applied for. However, the user criteria restriction is not applied outside the Service Catalog where the user has access to the item via the table.

### Procedure

1.  In an item record, navigate to the Available For or Not Available For related lists.

2.  Click **Edit** to add an existing user criteria record, or click **New** to create a new one.

3.  Save the record to associate the user criteria record with the item.

    **Note:** The **Not Available For** settings override **Available For** settings. A user on the **Not Available For** list for an item cannot access that item, even if that user is also on the **Available For** list for that item.


## Apply user criteria to categories

Apply user criteria to a category to define which users can and cannot access a category.

### Before you begin

Role required: admin

### Procedure

1.  In a category record, navigate to the Available For or Not Available For related lists.

2.  Click **Edit** to add an existing user criteria record, or click **New** to create a new one.

3.  Save the record to associate the user criteria record with the category.

    **Note:**

    -   The **Not Available For** settings override **Available For** settings. A user on the **Not Available For** list for a category cannot access that category, even if that user is also on the **Available For** list for that category.
    -   The user criteria restrictions of a category do not automatically apply to the catalog items within the category. If required, you should apply the user criteria restrictions to the individual catalog items.

