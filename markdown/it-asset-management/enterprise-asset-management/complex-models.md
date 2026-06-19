---
title: Multi-component models and assets in Enterprise Asset Management
description: Multi-component models and multi-components assets help you track the maintenance of your enterprise assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/complex-models.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Model types, Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Multi-component models and assets in Enterprise Asset Management

Multi-component models and multi-components assets help you track the maintenance of your enterprise assets.

## Multi-component model

An enterprise model that is associated with one or more model components is defined as a multi-component model. Each model component can be a consumable or enterprise model. The same model can be listed more than once as a model component.

Every model component has three mutually-exclusive properties that define its relationship with the parent multi-component model.

|Property|Description|
|--------|-----------|
|Required|If this property is set to **true**, the model component is essential for the multi-component model to function and cannot be removed permanently.|
|Hot swappable|If this property is set to **true**, the model component can be replaced while the multi-component model is operational.|
|Repairable|If this property is set to **true**, the model component can be repaired when it fails.|

The Enterprise Asset Management application supports two types of multi-component models: pre-assembled and user-assembled. You can convert a pre-assembled or user-assembled model to a simple model by removing all of its associated model components while it is in the Build state.

## Multi-component asset

Multi-component assets are created from a multi-component model.

The Enterprise Asset Management application supports two types of multi-component assets: serialized assets and consumable assets. Serialized child assets are created for model components. Consumable model components that are listed more than once are merged into a single consumable child asset with the combined component quantity.

\[Omitted image "eammodel-asset.png"\] Alt text: Multi-component model and multi-component asset

## Pre-assembled and user-assembled assets

Assets that are associated with pre-assembled and user-assembled multi-component models are referred to as pre-assembled and user-assembled multi-components assets, respectively.

-   Pre-assembled asset: Child assets are automatically created when a parent asset is created. These child assets are created and placed in the same stockroom that the parent asset was created in. Each child asset inherits various properties from the parent asset, including the asset stockroom, state, and sub status.

    If you want to add additional child assets to an existing parent asset, you can use add-on assets. These assets do not have to be defined through the original model components. If you use an add-on asset, the Asset type of the parent asset is automatically updated to Pre-assembled with add-on.

-   User-assembled asset: Assets that are assembled using components from the parent asset stockroom. You can assemble these assets using either of the following methods:
    -   Manual assembly: Manually select the required components and assemble the asset by using the **Assemble** button in the asset record. For details, see [Select assets for user-assembled asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/assemble-assets-eam.md).
    -   Automatic assembly: Automatically select the required components and assemble the asset by using the **Auto-assemble** button in the asset record. If the required quantity of components is unavailable in your stockrooms, an error appears. You must then assemble the asset manually.

If a parent asset is in one of the following states, you can swap its child assets with any other assets that are created for the same model component:

-   In Use
-   In Maintenance
-   In Stock Defective
-   In Stock Pending Repair

**Note:** For more details on swapping assets, see [Swap assets for parent multi-component asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/swap-assets-eam.md).

## Multiple components for an enterprise model

You can simultaneously add multiple components to an enterprise model by specifying the component quantity in the **Quantity** field of the Add model components dialog box.

-   For serialized components, each row in the dialog box splits into multiple model components based on the quantity that you specify in the **Quantity** field. For example, if you set the **Quantity** field to `10` for a given row, 10 model component records are created for that row.
-   For consumable components, one model component record is created per row. Each record indicates the quantity that you specify in the **Quantity** field. For example, if you set the **Quantity** field to `10` for a given row, only one model component record is created with a quantity of 10.

## Component number usage for consumable components

Since consumable assets don't have asset tags or serial numbers, the **Component number** field in your model component records can help you identify and track your consumable child assets. This component number is propagated to the display name of the child asset as a prefix.

## Component number usage for serialized components

Since serialized assets can have asset tags, component numbers are optional for serialized child assets. You can specify a component number only if you set the **Quantity** field of the Add model components dialog box to `1`. If you set this field to a value greater than one, the component number is generated automatically. If a serialized child asset does not have an asset tag, the component number is propagated as the asset tag. Any asset tag that you later add overrides the component number.

**Parent Topic:**[Model types in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-model-types.md)

