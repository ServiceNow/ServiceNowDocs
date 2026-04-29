---
title: Create assets manually
description: The ServiceNow AI Platform does not create an asset automatically under certain conditions. You can create an asset manually as needed.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Model categories, Product Catalog, Asset Management, IT Service Management]
---

# Create assets manually

The ServiceNow AI Platform does not create an asset automatically under certain conditions. You can create an asset manually as needed.

## Before you begin

Role required: model\_manager

## About this task

The conditions under which an asset is not automatically created include the following.

-   Forced CI verification: If you select the **Enforce CI verification** check box in the **Model Category** form, the system does not create an asset automatically when a CI is created or discovered. When **Enforce CI verification** is enabled, newly created CIs do not trigger an automatic creation of an asset. Instead, these newly created CIs have their **Requires verification** field automatically set to true, which displays the following UI actions for the CI:
    -   **Create Asset**: Creates an asset and sets **Requires verification** to false.
    -   **Merge CI**: Merges duplicates of a CI. This action is useful if an asset for the CI was created in a separate process, which created an associated CI. Then a second CI was created either manually or via the discovery source - and the duplicate CIs did not properly coalesce.
-   Configuration errors: In rare cases, the system can fail to create the asset automatically. This failure can occur if you assign the model and model category to the CI in the wrong sequence.

Follow these steps to create an asset manually.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Model** &gt; **Model Categories**.

2.  Open a model category that has no assigned CI class.

3.  Click **Create Assets**.

    This action creates assets from all CIs deferred for verification in this model category. This option is only available for users with the admin role.


**Parent Topic:**[Model categories](../concept/c_ModelCategories.md)

**Related topics**  


[View model categories](t_ViewingModelCategories.md)

[Create model categories](t_CreatingModelCategories.md)

[Edit model categories](t_EditingModelCategories.md)

[Delete model categories](t_DeletingModelCategories.md)

