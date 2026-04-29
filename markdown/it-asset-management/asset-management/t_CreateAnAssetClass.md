---
title: Create an asset class
description: Creating an asset class requires defining a new table and creating a corresponding application and module, then adding the new asset class to new or existing model categories. The default asset classes are Hardware, Software License, and Consumable. These general classes can be used to manage various assets.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage various assets through asset classes, Using Asset Management, Asset Management, IT Asset Management]
---

# Create an asset class

Creating an asset class requires defining a new table and creating a corresponding application and module, then adding the new asset class to new or existing model categories. The default asset classes are Hardware, Software License, and Consumable. These general classes can be used to manage various assets.

## Before you begin

Role required: asset or category\_manager

## About this task

If the general classes aren’t appropriate for a specific group of assets, consider creating an asset class. For example, a fleet of cars could be tracked in a custom asset class named Vehicle. Before creating asset classes, analyze business needs to see if the general classes can be used. A large number of asset classes can be difficult to maintain.

Built-in functionality allows you to use asset classes for financial tracking, in a model bundle, and as a pre-allocated asset.

Ensure that the model categories contain models. Use the Table form to extend an existing table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables &amp; Columns** &gt; **Create Table** and fill out the Table form fields with information on the new table.

<table id="table_gsy_h5g_ms"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Display name of table that can be localized.For example, a custom asset class to track a fleet of cars can be labeled as Vehicle.

</td></tr><tr><td>

Name

</td><td>

Internal name of table that can’t be changed later.For example, the Vehicle asset class can be named alm\_u\_vehicle.

</td></tr><tr><td>

Extends table

</td><td>

Table that new table inherits fields from.The Asset \(alm\_asset\) table can be extended to create a custom asset class.

</td></tr><tr><td>

Application

</td><td>

Application that uses the record.

</td></tr><tr><td>

Create module

</td><td>

Check box for creating a module.

</td></tr><tr><td>

Create mobile module

</td><td>

Check box for creating a mobile module.

</td></tr><tr><td>

Add module to menu

</td><td>

Menu that module displays.

</td></tr><tr><td>

New menu name

</td><td>

New menu name.

</td></tr></tbody>
</table>2.  Click **Submit**.

3.  Navigate to the new application \(for example, **Asset** &gt; **Vehicle**\) and click **New**.

4.  Configure the form to include **Model**, **Model Category**, and **Quantity**.

5.  Create a model category and add the asset class you created to the **Asset class** field.

6.  Create models and add them to the model category.


## What to do next

Now that the model category \(associated with the new asset class\) and the models are created, manage the models as assets. For example, use the model in a bundle.

**Parent Topic:**[Manage various assets through asset classes](../concept/c_AssetClasses.md)

**Related topics**  


[Create license assets](t_CreatingLicenseAssets.md)

[Set asset states and substates](t_SettingAssetStatesAndSubstates.md)

[Add depreciation to an asset](t_AddingDepreciationToAnAsset.md)

