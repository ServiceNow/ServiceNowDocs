---
title: Create model categories
description: You can create model categories for the Enterprise Asset Management application.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise models, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Create model categories

You can create model categories for the Enterprise Asset Management application.

## Before you begin

Various base model categories are already available for you to choose from.

Keep the following in mind while creating model categories:

-   When you create a configuration item \(CI\) class in the Configuration Management Database \(CMDB\), you can also create a corresponding model category to associate that CI class with. By associating a CI class with a model category, you can then associate that CI class with the corresponding asset and product model classes.
-   If you associate a CI class with a model category that is already associated with an asset class, the asset and CI synchronization capability automatically triggers, creating assets for all CIs under the given CI class. If an asset is not created automatically, you can create it manually.
-   The **Allow pre-allocated**, **Allow in bundle**, and **Allow as main** options are available only if the model category is associated with an asset class.

    **Note:** These options are not applicable to enterprise model categories.


Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Model categories**.

2.  Select **New**.

    The Create New Model Category page appears.

3.  On the form, fill in the fields.

<table id="table_igx_4sp_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the model category in the Service Catalog.

</td></tr><tr><td>

Parent category

</td><td>

Parent model category that this model category falls under.

</td></tr><tr><td>

UNSPSC code

</td><td>

United Nations Standard Products and Services Code \(UNSPSC\) for all products under the model category.

</td></tr><tr><td>

Picture or icon

</td><td>

Visual representation of the model category in the Service Catalog.

</td></tr><tr><td>

CI class

</td><td>

CMDB CI class that you want to associate with the model category. **Important:** You can select a CI class only when you are creating the model category. You can't select one after you have created the model category.

</td></tr><tr><td>

Product model class

</td><td>

Product model class that you want to associate the model category with.

</td></tr><tr><td>

Asset class

</td><td>

Asset class that you want to associate the model category with. You can select a default asset class, such as **Enterprise Asset**, or any new asset class that you have created. If you select **Consumable** or **Software License**, the **CI class** field becomes read-only since consumables and software licenses do not create CIs. If you specify a CI class and then select **Consumable** or **Software License**, the**CI class** field automatically changes to **None**.

 **Important:** You can select an asset class after you have created the model category, but you can't change it after it has been selected.

 After you associate the model category with an asset class, the Enterprise Asset Management application can automatically create assets based on the given model category.

</td></tr><tr><td>

Allow pre-allocation

</td><td>

Option to allow items under this model category to be added and tracked as pre-allocated assets.

</td></tr><tr><td>

Allow in bundle

</td><td>

Option to allow items under this model category to be used in bundles.

</td></tr><tr><td>

Allow as main

</td><td>

Option to allow items under this model category to be used as the main component in a bundle.

</td></tr><tr><td>

Is product instance

</td><td>

Option that indicates if you are using a product instance to identify and synchronize the assets, CIs, and install base items \(IBIs\) under this model category.

</td></tr><tr><td>

Enforce CI verification

</td><td>

Option to prevent the Enterprise Asset Management application from automatically creating assets for a specific model category when CIs are added manually or found through Discovery. This option enables you to review and verify new CIs before adding them as assets.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The model category is created. You can perform additional configurations on the model category by entering details in the **Product Models** tab.

**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

