---
title: Now Assist: Location, catalog, category, and topic functions
description: When creating or editing a catalog item, you can use plain language to assign values for catalog, category, or topic. If the value you provide matches an existing entry, Now Assist automatically applies it to the item. This streamlines the process and reduces manual data entry.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Now Assist: Location, catalog, category, and topic functions

When creating or editing a catalog item, you can use plain language to assign values for catalog, category, or topic. If the value you provide matches an existing entry, Now Assist automatically applies it to the item. This streamlines the process and reduces manual data entry.

Content generation by Now Assist within Catalog Builder is limited to Topic, Catalog, and Category fields. It does not generate values for Location or other fields outside this set. Users can only select a Catalog, Category, or Topic from the list that already exists.

When you enter a value, Now Assist searches for an exact match. The system handles the different scenarios as follows:

-   Exactly one match found: The value is applied automatically, and no further action is needed.
-   Multiple matches or no match found: Now Assist does not guess. Instead, it notifies you and displays available options in the chat, allowing you to select the correct value yourself.

**Note:** While you resolve any ambiguity in the chat, the rest of your conversation with Now Assist remains active. You can continue making other changes or asking questions at the same time.

Categories are always associated with a catalog, creating a close relationship between the two. Now Assist manages different input scenarios as follows:

## Providing both catalog and category together

If you specify both a catalog and a category, Now Assist checks whether the category belongs to the selected catalog.

-   Valid combination: Both values are applied.
-   Invalid combination: You are notified and prompted to select the correct and available values from the list.

## Providing only a category

When only a category is provided, Now Assist searches under any catalogs already assigned to the item for a matching category.

-   Exactly one match found: The category is applied automatically.
-   Multiple matches found: Now Assist asks to select the correct and available value from the list.

## If no catalog has been assigned yet

If no catalog is assigned when you specify a category, Now Assist asks you to add a catalog first since a category must always be linked to a parent catalog.

## Assigning topics

You can assign topics to a catalog item simply by mentioning them in your prompt. After Now Assist recognizes valid topics, it adds them to the item automatically. Also, when a user tries to add a topic, Now Assist searches in the attached taxonomies. If there is no taxonomy attached to the item, then user would be prompted to add a taxonomy first and then a topic.

## Assigning multiple values

A catalog item can belong to more than one catalog, category, or topic. Now Assist supports assigning multiple values for these fields in a single interaction, making it efficient to update or create complex catalog items.

-   When a template controls values:

    In cases where a catalog item is based on a template with pre-set values for catalog, category, or topic, those template values take priority and cannot be changed. If you attempt to modify a locked field, Now Assist informs you that the value is controlled by the template and cannot be edited.

-   When some fields are locked and others are not:

    If you request updates to multiple fields at once, and some of those fields are locked by a template while others are not, Now Assist will:

    -   Apply the changes to any fields that are allowed to be updated.
    -   Notify you about which fields could not be changed due to template control.

**Parent Topic:**[Catalog item generation reference](catalog-item-generation-reference.md)

