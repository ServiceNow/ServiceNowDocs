---
title: Inventory Model form - General
description: The General section in the Inventory Model form enables you to create, review, and modify the details of a model.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Inventory Model forms, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Inventory Model form - General

The General section in the Inventory Model form enables you to create, review, and modify the details of a model.

<table id="table_f3c_dmd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Description of the equipment holder model that you’re defining.

</td></tr><tr><td>

Model categories

</td><td>

List of model categories that maps to a CI class. The model categories are part of the Product Catalog application.**Note:**

-   The instance is created in the mapped CI class of the selected model category.
-   To achieve the Telecommunications Network Inventory functionalities, choose one of the following options:
    -   Equipment rack
    -   Cabinet
    -   Slot
    -   Subslot
-   On selecting the **Equipment rack** as the category, the **RU naming pattern** and **Post Type** fields appear under the information section.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

Process to track the model. Select one of the following options:

-   **Leave to Category**: The model is transparent and the category defines the asset class.
-   **Create Consumable Asset**: The model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   **Don't create assets**: The model blocks the asset instantiation, regardless of what the category defines as the asset class.

</td></tr><tr><td>

Useful life \(months\)

</td><td>

Number of months that the model can be used for.

</td></tr><tr><td>

Asset tracking unit

</td><td>

Number of equipment holder units that are available for use in this network asset.

</td></tr><tr><td>

Acquisition method

</td><td>

Acquisition method for the model:

-   **Buy**

The model was purchased.

-   **Leased**

The model was leased.

-   **Both**

The model was bought and leased.


</td></tr><tr><td>

Cost

</td><td>

Cost of a single unit of the model.

</td></tr><tr><td>

Depreciation

</td><td>

Depreciation schedule of the equipment model.

</td></tr><tr><td>

Salvage value

</td><td>

The estimated value that an asset realizes when sold at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr><tr><td>

Comments

</td><td>

Any additional information on the model that would be useful.

</td></tr><tr><td>

Model number

</td><td>

The model number that is assigned to the model by the manufacturer.

</td></tr><tr><td>

Barcode

</td><td>

Bar code number that is assigned to the model by the manufacturer.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

Production status of the model:

-   **Build**

The model must be built.

-   **In Production**

The model is in production.

-   **Sold**

The model was sold.

-   **Retired**

The model has been retired.


</td></tr><tr><td>

Expenditure type

</td><td>

Type of expenditure. Select one of the following options:

-   **Capex**

Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.

-   **Opex**

Operational expenditure is an ongoing expenditure. For example, toners for the photocopier.


</td></tr><tr><td>

Certified

</td><td>

Option that designates if this network asset is certified.

</td></tr></tbody>
</table>**Parent Topic:**[Inventory Model forms](tni-model-forms.md)

**Related topics**  


[Creating your inventory models](../concept/creating-your-inventory-models.md)

