---
title: Multi-component models and assets in Enterprise Asset Management
description: Multi-component models and multi-components assets help you track the maintenance of your enterprise assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Multi-component models and assets in Enterprise Asset Management

Multi-component models and multi-components assets help you track the maintenance of your enterprise assets.

## Multi-component model

An Enterprise Asset Management model associated with one or more model components is defined as a multi-component model.

A model component can be a consumable or an enterprise model. The same model can be listed more than once as a model component of a multi-component model. For example, consumable model component A can be repeated thrice for the multi-component model.

Every model component has the following three relationships with a multi-component model each with a true or false value:

-   Required: If the value is true, then the model component is essential for the multi-component model to work and can't be permanently removed.
-   Hot Swappable: If the value is true, then the model component can be swapped while the multi-component model is operational
-   Repairable: If the value is true, then the model component can be repaired.

A model component's relationship to a multi-component model is mutually exclusive. For example if a multi-component model comprises of two model component A's, each model component A can have its own relationship with the multi-component model.

There are two types of multi-component models: Pre-assembled and user-assembled models.

You can change a pre-assembled or a user-assembled multi-component model to a simple model by disassociating all its model components, while the model is still in the **Build** state. Once you save the model record, the multi-component model is changed to a simple model and all associations to model components are removed.

## Multi-component asset

Multi-component assets are created from a multi-component model.

If a consumable model component is listed more than once in a multi-component model, they are merged into a single record regardless of whether the **Required**, **Hot Swappable**, or **Repairable** fields are the same or not.

There are two kinds of assets: consumable assets and serialized assets.

For enterprise model components, serialized child assets are created that are based on the model component. For example, Child Asset B is the child asset created for Model Component B.

The model component relationship defined with the multi-component model is extended and visible in the child asset records. Swapping of child assets can only be performed with the same model component. A child asset can't be swapped with a different model component.

![Multi-component model and multi-component asset](../image/eammodel-asset.png "Relationship between multi-component model and multi-component asset")

## Pre-assembled and user-assembled assets

Assets associated with pre-assembled and user-assembled multi-component models are referred to as pre-assembled and user-assembled multi-components assets, respectively.

-   Pre-assembled asset: when the parent asset is created, the child assets are automatically created. Child assets are created in the same stockroom where the parent asset is created. The child assets inherit the parent asset's properties such as stockroom, state, sub status. No asset tag or serial tag is attached to the child asset when it's created. You can add additional child assets, add-ons, even if it's not defined in the model component. When an add-on asset is added, the **Asset type** field displays the value **Pre-assembled with add-on**.
-   User-assembled asset: assemble assets using assets present in the parent asset stockroom.
    -   Assemble the assets yourself by using the **Assemble** button in the asset record. For details, see [Select assets for user-assembled asset](../task/assemble-assets-eam.md).
    -   Automatically assemble assets via the **Auto-assemble** button to trigger a process to automatically select assets from a stockroom and associate the assets to a parent asset. If the required quantity of assets isn’t available in the stockroom, an error appears and you can't automatically assemble assets. Use the **Assemble** button to assemble the assets on your own.
    -   Release all child and add-on assets from the parent asset. For details on releasing assets, see [Release assets from the parent asset](../task/release-assets-eam.md).

You can swap child assets for any multi-component asset that is in one of the following states:

-   In-Use
-   In-Maintenance
-   In Stock Defective
-   In Stock Pending Repair

**Note:** For more details on swapping assets, see [Swap assets for parent multi-component asset](../task/swap-assets-eam.md).

## Multiple model components for an enterprise model

You can add multiple model components to an enterprise model at one go by specifying the quantity. The **Quantity** field in the Add model components dialog lets you create multiple serialized components and consumable components for a single enterprise model.

-   For serialized components: each row in the Add model components dialog box is split into multiple model components based on the quantity. For example, if the Quantity field has a value of 10 for a row, then 10 model component records are created.
-   For consumable components: one model component is created per row. For example, if the quantity field has a value of 10 for a row, then only one model component record is created with the quantity as 10.

For consumable child models, one child asset is created per component, with a quantity equal to the quantity of the component. For serialized child models, assets are created per component.

When you create assets, the consumable assets do not merge. Consumable assets are individual assets with a quantity. For example, model component A record has a quantity value of two and the model component B record has a quantity value of three. So two assets are created. One asset record with quantity two and the other asset record one with quantity three.

The add on assets of consumables are however merged as they are not linked to a model component. For example, model A has two components of consumable model C. When you create a complex asset from that model, two child assets get created of that same model C.

## Component number usage for consumable components

Since consumables don't have an asset tag or serial numbers, the **Component number** field in the model component form helps you to identify and keep track of child consumables. While creating a consumable component record, ensure to enter a value in the **Component number** field.

For consumable components, the component number gets propagated to the display name of the child asset as a prefix.

## Component number usage for serialized components

For serialized components, it's optional to enter a component number. You can specify a component number if the value you enter in the **Quantity** field is 1. If you enter a value of more than one in the **Quantity** field, then the **Component number** field is disabled. However, the component numbers are automatically generated by the system. You can go to the model component form and change the component number if you want.

For serialized components, if an asset tag isn't mentioned, then the component number is propagated as the asset tag. If you later decide to add an asset tag, the component number gets overridden by the asset tag.

