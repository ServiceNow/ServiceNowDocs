---
title: Create assets manually
description: The ServiceNow AI Platform does not create an asset automatically under certain conditions. You can create an asset manually as needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/product-catalog/t\_CreatingAssetsManually.html
release: zurich
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Model categories, Product Catalog, Asset Management, IT Service Management]
---

# Create assets manually

The ServiceNow AI Platform does not create an asset automatically under certain conditions. You can create an asset manually as needed.

## Before you begin

Role required: model\_manager, asset\_system\_admin

## About this task

The system does not create an asset automatically under the following conditions:

-   Enforce CI verification is selected: If the **Enforce CI verification** check box is selected in the **Model Category** form, the system doesn'tcreate an asset when a CI is created or discovered. Instead, the system sets the **Requires verification** field to true for the new CI and displays the following UI actions on the CI:
    -   **Create Asset**: Creates an asset and sets **Requires verification** to false.
    -   **Merge CI**: Merges duplicates of a CI. This action is useful if an asset for the CI was created in a separate process, which created an associated CI. Then a second CI was created either manually or via the discovery source - and the duplicate CIs did not properly coalesce.
-   Configuration errors: In rare cases, the system can fail to create the asset automatically. This failure can occur if you assign the model and model category to the CI in the wrong sequence.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Model** &gt; **Model Categories**.

2.  Open a model category that has a CI class and an asset class assigned, and in which the **Enforce CI verification** check box isn't selected.

3.  Select **Create Assets**.

    **Note:** This option is available only for users with the asset\_system\_admin role.

    The system submits a job that creates assets for CIs of the category’s CI class that don't have an asset yet.

    **Note:** To create an asset for a CI held for verification, select the **Create Asset** option on that CI.


**Parent Topic:**[Model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/product-catalog/c_ModelCategories.md)

**Related topics**  


[View model categories]()

[Create model categories]()

[Edit model categories]()

[Delete model categories]()

