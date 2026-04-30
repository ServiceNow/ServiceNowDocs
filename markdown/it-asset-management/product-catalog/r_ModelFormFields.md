---
title: Model form fields
description: There are fields on the Model form that apply to all types of models.
locale: en-US
release: yokohama
product: Product Catalog
classification: product-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Models, Product Catalog, IT Asset Management]
---

# Model form fields

There are fields on the Model form that apply to all types of models.

<table id="table_ijg_fpj_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the model. A system property called **glide.cmdb\_model.display\_name.shorten** controls how software model display names are generated.

</td></tr><tr><td>

Manufacturer

</td><td>

The company that built the model.

</td></tr><tr><td>

Name

</td><td>

Field that Discovery uses to create a model with the value discovered. Model managers can specify a name of their choice when creating a model and can also edit the name of an existing model.

</td></tr><tr><td>

Edition

</td><td>

The edition of the software model, such as **Professional**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Model categories

</td><td>

The categories to which the model is assigned. This field is a glide list and cannot be used to create reports.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

The process by which the model can be tracked. Choose from the following:-   **Leave to Category:** model is transparent and the category defines the asset class.
-   **Create Consumable Asset:** model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   **Don't create assets:** model blocks asset instantiation, regardless of what the category defines as the asset class.

</td></tr><tr><td>

Acquisition method

</td><td>

The method for purchasing the model. Options are **Both**, **Buy**, or **Lease**.

</td></tr><tr><td>

Cost

</td><td>

The cost of a single unit of the model.

</td></tr><tr><td>

Depreciation

</td><td>

The [Use depreciation with fixed assets](../../asset-management/concept/c_CreatingFixedAssets.md#) for the model.

</td></tr><tr><td>

Salvage value

</td><td>

The estimated value that an asset realizes upon its sale at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr><tr><td>

Model number

</td><td>

The specific model number assigned to the item by the manufacturer. Setting the system property **glide.cmdb.makeandmodel.use\_model\_number\_lookup** to true enables you to lookup the model number of hardware models through the MakeAndModelJS script.

</td></tr><tr><td>

Barcode

</td><td>

The barcode number assigned to the model. Barcodes are assigned by the manufacturer.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

The status of the model. Options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr><td>

Expenditure type

</td><td>

The type of expenditure. Choose from the following: -   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an on-going expenditure. For example, toners for the photocopier.

</td></tr><tr><td>

Certified

</td><td>

The option that determines whether the model is approved for use.

</td></tr><tr><td>

Comments

</td><td>

Information about the model that would be helpful for others to know.

</td></tr><tr><td>

Assets

</td><td>

The assets created from this model. This creation can have any combination of assets and configuration items. For example, with a single hardware model you can have assets and no configuration items, configuration items and no assets, or have both.

</td></tr><tr><td>

Configuration Items

</td><td>

The configuration items created from this model. Can have any combination of assets and configuration items.

</td></tr><tr><td>

Product Catalog

</td><td>

The information about the model as it appears in the product catalog and service catalog. Information only appears if the model has been published to the product catalog.

</td></tr></tbody>
</table>**Parent Topic:**[Models](../concept/c_Models.md)

