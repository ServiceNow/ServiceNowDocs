---
title: Create vaccine models
description: Create a vaccine model to track and manage different vaccines under Vaccine Administration Management.
locale: en-US
release: yokohama
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create vaccine models

Create a vaccine model to track and manage different vaccines under Vaccine Administration Management.

## Before you begin

Role required: sn\_vaccine\_sm.model\_manager

## About this task

Vaccine Administration Management includes vaccine models for the Moderna COVID-19 vaccine and the Pfizer-BioNTech COVID-19 vaccine. To track and manage any other vaccines, create vaccine models.

## Procedure

1.  Navigate to **All** &gt; **Vaccine Administration** &gt; **Administration** &gt; **Vaccine Models**, and click **New**.

2.  In the **Model categories** field, select **Vaccine**.

3.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

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

The manufacturer-assigned name of the model or abstract name specified by the model manager, such as **Field Agent Laptop**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Model categories

</td><td>

The categories that the model is assigned to. This field is a Glide list and can’t be used to create reports.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

The process by which the model can be tracked. Choose from the following:

-   **Leave to Category:** The model is transparent and the category defines the asset class.
-   **Create Consumable Asset:** The model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   **Don't create assets:** The model blocks asset instantiation, regardless of what the category defines as the asset class.


</td></tr><tr><td>

Asset tracking unit

</td><td>

The unit that is used to measure the asset.

</td></tr><tr><td>

Acquisition method

</td><td>

The method for purchasing the model. The options are **Both**, **Buy**, or **Lease**.

</td></tr><tr><td>

Cost

</td><td>

The cost of a single unit of the model.

</td></tr><tr><td>

Depreciation

</td><td>

The depreciation scheme for the model.

</td></tr><tr><td>

Salvage value

</td><td>

The estimated value that an asset realizes on its sale at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr><tr><td>

Model number

</td><td>

The model number assigned to the item by the manufacturer.

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

The status of the model. The options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr><td>

Expenditure type

</td><td>

The type of expenditure. Choose from the following:

-   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an ongoing expenditure. For example, toners for the photocopier.


</td></tr><tr><td>

Certified

</td><td>

The option that determines whether the model is approved for use.

</td></tr><tr><td>

Comments

</td><td>

Information about the model that would be helpful for others to know.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

