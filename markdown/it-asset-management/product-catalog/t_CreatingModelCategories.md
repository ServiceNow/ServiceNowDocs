---
title: Create model categories
description: You can add custom model categories for your instance.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Model categories, Product Catalog, IT Asset Management]
---

# Create model categories

You can add custom model categories for your instance.

## Before you begin

Role required: model\_manager

## About this task

When you create model categories, keep the following in mind:

-   The base system provides a model category for each CI class in the CMDB. As you create cmdb\_ci classes, create a corresponding row in the model category table for the model table to be used.
-   If you select an **Asset class** on any existing model category, the system automatically creates assets for all configuration items associated with the model category, if configured to do so. If an asset is not created automatically, you can create the asset manually. After an asset class is selected for a model category, the asset class cannot be changed.
-   The **Allow pre-allocated**, **Allow in bundle**, and **Allow as main** options are only available if an asset class is specified for the model category.
-   If you select **Consumable** or **Software License** for the asset class, the **Allow in bundle** option is available, but not **Allow pre-allocation** or **Allow as main**.
-   When a CI is created from a model category that requires asset tracking, the system automatically creates an asset record for the asset class specified in the model category. It then links that asset record to the CI. If a model is specified, the model category of the CI is determined by a combination of the CI class and the list of categories supported by the model. Asset tracking is specified on the model record.
-   When an asset is created from a model category that requires CI tracking, the system automatically creates a CI record of the class specified by the category and links it to the asset.
-   The Model Categories list \(**Product Catalog** &gt; **Product Model** &gt; **Model Categories**\) shows all the CI classes and what asset class is generated on the asset side.

## Procedure

1.  Navigate to **Product Catalog** &gt; **Product Model** &gt; **Model Categories** and select **New**.

2.  On the form, fill in the fields.

<table id="table_igx_4sp_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name for this category.

</td></tr><tr><td>

CI class

</td><td>

If a CI class is needed, it must be specified when you create the model category. You can't add the CI class the model category later.

</td></tr><tr><td>

Asset class

</td><td>

Default options and any new asset classes you’ve created. Setting the asset class triggers the creation of assets depending on the model category selected. You can add an asset class to the model category later, but can't be changed after it’s added. If you select **Consumable** or **Software License**, the **CI class** field becomes read-only because consumables and software licenses don’t create CIs. If you specify a CI class and then select **Consumable** or **Software License**, the**CI class** field is changed to **None** automatically.-   Asset: An item that can be tracked individually.
-   Consumable: An asset not tracked individually, such as keyboards.
-   Hardware: A physical piece of computer equipment, such as a laptop or server.
-   Software License: A legal statement defining the uses of software, such as the number of installations allowed or the terms of distribution.


</td></tr><tr><td>

Install base item class

</td><td>

Class to track the asset as an Install base item.**Note:** This field is available only when the Customer Service Install Base Management \[com.snc.install\_base\] plugin is installed. Also, currently, only the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] is available when the Healthcare and Life Sciences Service Management Core application is installed.

</td></tr><tr><td>

Product model class

</td><td>

Class table where the models are stored. The default values are:-   Application
-   Consumable
-   Contract
-   Facility
-   Hardware
-   Service
-   Software
After you select a value, the table content, form views, and overall functionality of the models created in the model category gets impacted.

</td></tr><tr><td>

Is product instance

</td><td>

Identifies whether the model category is associated with Product Instance, which is a logical grouping of asset, CI, and IBI class.**Note:** This check box is read-only and is supported only for Medical device model category. After you select this option, Product Instance Identifier \(PID\), a unique identifier for asset, CI, and IBI class is generated whenever you create an asset of that model category. However, for the existing assets, the PID is generated only when any of the asset fields such as Serial number, Model component ID, or Parent is updated.

</td></tr><tr><td>

Allow pre-allocation

</td><td>

Add and track items in this category as[Create pre-allocated assets](../../asset-management/task/t_CreatingPreAllocatedAssets.md#).

</td></tr><tr><td>

Allow in bundle

</td><td>

Use items in this category in [bundles](../concept/c_CreatingBundledModels.md).

</td></tr><tr><td>

Allow as main

</td><td>

Use items in this category as the main component in a bundle.

</td></tr><tr><td>

Enforce CI verification

</td><td>

Prevents the system from automatically creating assets in a specific model category when CIs are added manually or found with Discovery. This option enables an administrator to review and verify new CIs before adding them as assets.

</td></tr></tbody>
</table>3.  Select **Submit**.


**Parent Topic:**[Model categories](../concept/c_ModelCategories.md)

**Related topics**  


[View model categories](t_ViewingModelCategories.md)

[Create assets manually](t_CreatingAssetsManually.md)

[Edit model categories](t_EditingModelCategories.md)

[Delete model categories](t_DeletingModelCategories.md)

[Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r-discovery.md)

