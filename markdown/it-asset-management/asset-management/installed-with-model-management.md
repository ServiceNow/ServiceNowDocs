---
title: Installed with Model Management
description: Several types of components are installed with Model Management.Model Management uses a number of business rules.Model Management includes a number of client scripts.Model Management includes the property glide.cmdb\_model.display\_name.shorten.Model Management includes script includes.Model Management includes numerous tables.Model Management includes UI policies.Model Management includes user roles.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Asset Management, IT Asset Management]
---

# Installed with Model Management

Several types of components are installed with Model Management.

Demo data is available with Model Management.

## Business rules installed with Model Management

Model Management uses a number of business rules.

|Name|Table|Description|
|----|-----|-----------|
|Abort action if no license type|\[cmdb\_software\_product\_model\]|Ensures that a license type \(not a license type group that cannot be handled by counters\) has been selected.|
|Calculate display\_name|Product Model \[cmdb\_model\]|Sets the **Display name** field when any of the following field values change: **Manufacturer**, **Name**, **Version**, **Edition**. The display name differs depending on whether the **glide.cmdb\_model.display\_name.shorten** property is set to **true** or **false**.|
|Date validation|\[cmdb\_m2m\_downgrade\_model\]|Ensures that the Start date is before the End date.|
|Enforce CI Rules|\[cmdb\_model\_category\]|Ensures that categories that track assets as consumables or software licenses do not have a CI class.|
|Flag parent as bundle on creation|\[cmdb\_m2m\_model\_component\]|Flags a model that has components as a bundle.|
|License Type - Fullname|\[cmdb\_sw\_license\_calculation\]|Computes the full name of the license type.|
|License validation|Software Upgrade and Downgrades \[cmdb\_m2m\_downgrade\_model\]|Prevents software upgrades and downgrades from being duplicated and prevents having duplicate upgrades and downgrades for the same license where duplication also involves having the same dates. Also ensures that both the **Upgrade parent** and **Downgrade child** fields are mandatory and that if the **License** field is not empty, either **Upgrade parent** or **Downgrade child** must be equal to the license.model.|
|Protect cmdb\_ci\_class|\[cmdb\_model\_category\]|Prevents CI class from being changed after creation.|
|Protect cmdb\_ci\_class on insert|\[cmdb\_model\_category\]|Prevents creation of a category if another category already exists for the chosen CI class.|
|Protect Contract|\[cmdb\_model\_category\]|Prevents changes to the Contract model category record.|
|Set parent's main component link|\[cmdb\_m2m\_model\_component\]|Populates a read-only reference from the bundle to the component when a bundle component is selected as the main component.|
|Unflag parent on last delete|\[cmdb\_m2m\_model\_component\]|Removes the bundle flag from a model when the last component is deleted from the bundle.|
|Update model category|\[cmdb\_ci\]|Updates the model categories for the associated model if the model is not already associated with the CI's model category.|
|Validate record before creation|\[cmdb\_m2m\_model\_component\]|Ensures that a component is not already in a bundle when an attempt is made to add the component to a bundle.|

## Client scripts installed with Model Management

Model Management includes a number of client scripts.

|Name|Table|Description|
|----|-----|-----------|
|Clear models not matching license|\[cmdb\_m2m\_downgrade\_model\]|Clears the **Upgrade parent** and **Downgrade child** fields when the **License** field is changed to a license and neither the upgrade or downgrade fields match the license model.|
|Constraints based on asset class|\[cmdb\_model\_category\]|Enables or disables bundling options based on the asset class of the category.|
|Hide sections when needed|\[cmdb\_model\]|Shows and hides sections according to what is relevant for a given model.|
|model\_category change|\[cmdb\_model\]|Ensures compatibility of classes between the several categories referenced by the same model \(client part\).|
|Populate downgrade from license|\[cmdb\_m2m\_downgrade\_model\]|Sets the downgrade child to the software model on the referenced license when an upgrade is selected. Only sets the downgrade to the license if the license is not empty.|
|Populate upgrade from license|\[cmdb\_m2m\_downgrade\_model\]|Sets the upgrade parent to the software model on the referenced license when a downgrade is selected. Only sets the upgrade to the license if the license is not empty.|

## Properties installed with Model Management

Model Management includes the property **glide.cmdb\_model.display\_name.shorten**.

<table id="table_nch_ns2_cp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.cmdb\_model.display\_name.shorten**

</td><td>

When set to **true**, generates shorter display names for models by eliminating duplication of the manufacturer name. Consider the following model, for which **Manufacturer** is set to **Spotify** and **Name** is set to **Spotify Premium**.The **Display name** field is set as follows, based on the property setting.

-   false: Display name is Spotify Spotify Premium
-   true: Display name is Spotify Premium

 For software models, the edition and version are also included in the name, if they are specified.

-   Type: true \| false
-   Default value: false
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>## Script includes installed with Model Management

Model Management includes script includes.

|Name|Description|
|----|-----------|
|ModelAndCategoryFilters|Refines reference qualifiers for models and model categories based on class.|
|ModelCategoryCheck|Ensures compatibility of classes between the several categories referenced by the same model.|

## Tables installed with Model Management

Model Management includes numerous tables.

|Table|Description|
|-----|-----------|
|Application Model \[cmdb\_application\_product\_model\]|Stores models used to describe software application products.|
|Consumable Model \[cmdb\_consumable\_product\_model\]|Describes consumable product models.|
|Contract Model \[cmdb\_contract\_product\_model\]|Stores all contract models.|
|Depreciation \[cmdb\_depreciation\]|Stores asset depreciation patterns.|
|Hardware Model \[cmdb\_hardware\_product\_model\]|Describes hardware product models.|
|Model Category \[cmdb\_model\_category\]|Defines groups of assets, consumables, product bundles, and configuration items.|
|Model Compatibility \[cmdb\_m2m\_model\_compatibility\]|Stores many-to-many relationship between two models signifying their compatibility with one another.|
|Model Component \[cmdb\_m2m\_model\_component\]|Stores many-to-many relationship between two models signifying that they form a bundle.|
|Product model \[cmdb\_model\]|Describes all kinds of product models.|
|Software License Calculation \[cmdb\_sw\_license\_calculation\]|Defines commonly used software licensing patterns.|
|Software Model \[cmdb\_software\_product\_model\]|Describes software product models.|
|Software Suite \[cmdb\_m2m\_suite\_model|Stores many-to-many relationship between two models that defines elements of a software suite.|
|Software Upgrade and Downgrades \[cmdb\_m2m\_downgrade\_model\]|Stores many-to-many relationship between two models signifying that being licensed for one model grants rights to the other as well.|

## UI policies installed with Model Management

Model Management includes UI policies.

<table id="table_mpc_vt2_cp"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide unverified

</td><td>

Model Category \[cmdb\_model\_category\]

</td><td>

Shows the **Enforce CI verification** field if the **Asset class** and **CI class** fields are not empty.

</td></tr><tr><td>

Lock fields for Contract and Work

 Lock fields for Contract

</td><td>

Model Category \[cmdb\_model\_category\]

</td><td>

Sets all fields on the Model Category form to read-only if the **Name** is **Contract** or, **Work Order** or **Work Task**.

</td></tr><tr><td>

Protect model category

</td><td>

Product Model \[cmdb\_model\]

</td><td>

Makes the **Model categories** field mandatory and read-only if it contains any of the following values: **Software License**, **Contract**, **Work Order**, **Work Task**.

</td></tr><tr><td>

Show is an option if Oracle

</td><td>

Software Model \[cmdb\_software\_product\_model\]

</td><td>

Shows the **Is an option** field if the selected **Manufacturer** name starts with **Oracle**.

</td></tr></tbody>
</table>## User roles installed with Model Management

Model Management includes user roles.

|Role|Contains Roles|Description|
|----|--------------|-----------|
|category\_manager|model manager|Can create, edit, and delete model categories.|
|model\_manager|none|Can create new CMDB models. The model manager role can control the base models and any model extensions that are not hardware, software, or consumables. Hardware and consumable models are controlled by the asset manager \(asset\) role. Software models are controlled by the software asset manager \(sam\) role.|

