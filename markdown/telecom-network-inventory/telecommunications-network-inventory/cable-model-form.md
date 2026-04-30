---
title: Cable model form
description: The Cable Model form enables you to describe the details for an optical fiber cable model record.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Cable model form

The Cable Model form enables you to describe the details for an optical fiber cable model record.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](../task/add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the cable model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr><tr><td>

Short description

</td><td>

Description of the cable model that you’re defining.

</td></tr><tr><td>

Model categories

</td><td>

List of model categories that maps to a CI class. The model categories are part of the Product Catalog application.

</td></tr><tr><td>

Model number

</td><td>

The model number that is assigned to the model by the manufacturer.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

Number of equipment holder units that are available for use in this network asset.

</td></tr><tr><td>

Barcode

</td><td>

A bar code number that is assigned to the model by the manufacturer.

</td></tr><tr><td>

Useful life \(months\)

</td><td>

Number of months that the model can be used for.

</td></tr><tr><td>

Asset tracking unit

</td><td>

Number of equipment holder units that are available for use in this network asset.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

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

Cost

</td><td>

Cost of a single unit of the model.

</td></tr><tr><td>

Expenditure type

</td><td>

Type of expenditure. Select one of the following options:

-   **Capex**

Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.

-   **Opex**

Operational expenditure is an ongoing expenditure. For example, toners for the photocopier.


</td></tr><tr><td>

Depreciation

</td><td>

Depreciation schedule of the cable model.

</td></tr><tr><td>

Certified

</td><td>

Option that designates if this network asset is certified.

</td></tr><tr><td>

Salvage value

</td><td>

The estimated value that an asset realizes when sold at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr><tr><td>

Comments

</td><td>

Any additional information on the model that would be useful.

</td></tr><tr><td>

Power \(watts\)

</td><td>

Electrical power of the network asset in watts.

</td></tr><tr><td>

Dimensions Unit

</td><td>

Unit of measure in which you’re expressing dimensions. Select one of the following options:-   **--None--**

No distance measurement is expressed for the connection route length.

-   **Inches**

Distance is expressed in inch.

-   **Feet**

Distance is expressed in feet.

-   **Miles**

Distance is expressed in miles.


</td></tr><tr><td>

Sound Power \(bels\)

</td><td>

The rate at which the energy of the network asset is emitted in bels.

</td></tr><tr><td>

Length

</td><td>

Length of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `12` if the asset is one foot, or enter `60` if the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within the designated network site.

</td></tr><tr><td>

Characteristic

</td><td>

Type of the cable. Select one from the following.-   **Optical**

Transmits signals using light pulses.

-   **Electrical**

Transmits signals using electrical currents.


</td></tr><tr><td>

Width

</td><td>

Length of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `12` if the asset is one foot, or enter `60` if the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within the designated network site.

</td></tr><tr><td>

Height

</td><td>

Height of the network asset, expressed in the unit of measure that you designate in the **Units** field.

-   For example, enter `60` if the height of the asset is 60 inches and you've selected `Inches` as the unit of measure in the **Units** field.
-   The ServiceNow AI Platform uses this information to calculate the cubic dimensions of the asset to determine its physical placement within its designated network site.

</td></tr><tr><td>

Depth

</td><td>

Depth of the network asset that is expressed in the unit of measure that you designate in the **Units** field.**Note:** This field is applicable for the equipment models and equipment holder models.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create a cable model](../task/create-a-cable-model.md)

