---
title: Hardware model details
description: Find the hardware model details and related list field descriptions.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Hardware model details

Find the hardware model details and related list field descriptions.

## Details

<table id="table_vfl_q5r_cjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Display name of the model. The display name is generated from the **Manufacturer** and **Name** field.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the model manufacturer.

</td></tr><tr><td>

Short description

</td><td>

Description of the model.

</td></tr><tr><td>

Model categories

</td><td>

Model categories that the model can be associated with. Model categories are used to create configuration items \(CIs\) and assets.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

Asset tracking for the model.

</td></tr><tr><td>

Useful life \(months\)

</td><td>

Number of months that the hardware model can be used for.

</td></tr><tr><td>

Asset tracking unit

</td><td>

Unit that is used to measure the asset.

</td></tr><tr><td>

Acquisition method

</td><td>

Method the assets or CIs were procured.

</td></tr><tr><td>

Cost

</td><td>

Cost of the an individual model.

</td></tr><tr><td>

Depreciation

</td><td>

Depreciation scheme of the model.

</td></tr><tr><td>

Salvage value

</td><td>

An estimate of the residual value of the model.

</td></tr><tr><td>

Name

</td><td>

Name of the model.

</td></tr><tr><td>

Model number

</td><td>

The number that identifies the model. This number can be defined internally or by the manufacturer of the model.

</td></tr><tr><td>

Barcode

</td><td>

Bar code that identifies the model.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

Status of the hardware model, which is being inherited from the product model.This field is hidden when you’ve opted in for the Common Service Data Model \(CSDM\).

</td></tr><tr><td>

Life Cycle Stage

</td><td>

Stage in the overall life cycle of hardware assets and CIs as related to their products.This field appears only when you’ve opted in for the Common Service Data Model \(CSDM\).

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Status in the overall life cycle of hardware assets and CIs as related to their products.This field appears only when you’ve opted in for Common Service Data Model \(CSDM\).

</td></tr><tr><td>

Expenditure type

</td><td>

Type of expenditure.

</td></tr><tr><td>

Certified

</td><td>

Option that indicates if a model is certified for use.

</td></tr><tr><td>

Calculated lifecycle template

</td><td>

Applied template to calculate life cycle dates.

</td></tr><tr><td>

Calculated lifecycle start date

</td><td>

Date to apply the template and derive the final dates for each phase defined in the template.

</td></tr><tr><td>

TCO benchmark cost

</td><td>

Benchmark cost of the asset model.**Note:** Amount displayed in the currency specified on the model record.

</td></tr><tr><td>

TCO benchmark threshold

</td><td>

The threshold value of your asset model cost identifying that the asset is reaching the TCO benchmark cost value. The benchmark threshold is set to 75% of the TCO benchmark cost by default.

For example, if you set the TCO benchmark cost of an asset model as $1000, the TCO benchmark threshold is set to $750 automatically.

Use the system property **sn\_itam\_common.asset\_tco\_benchmark\_threshold\_percentage** to update the threshold percentage.

**Note:** Amount displayed in the currency specified on the model record.

</td></tr><tr><td>

Hazardous materials

</td><td>

Option to indicate if your asset model contains hazardous materials.

</td></tr><tr><td>

Comments

</td><td>

Comments about the model.

</td></tr><tr class="sub-head"><td>

Normalization

</td><td>

 

</td></tr><tr><td>

Normalized manufacturer

</td><td>

Normalized name of the model manufacturer.

</td></tr><tr><td>

Product

</td><td>

Normalized name of the product.

</td></tr><tr><td>

Model

</td><td>

Normalized name of the model.

</td></tr><tr><td>

Normalization status

</td><td>

Normalization status of the model.

</td></tr><tr><td>

Device type

</td><td>

Type of device.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option indicating whether the normalization information is excluded from the content service.

</td></tr><tr><td colspan="2">

**Dimensions**

</td></tr><tr><td>

Height

</td><td>

Height of the model populated from the content service.

</td></tr><tr><td>

Width

</td><td>

Width of the model populated from the content service.

</td></tr><tr><td>

Depth

</td><td>

Depth of the model populated from the content service.

</td></tr><tr><td>

Electrical Specifications

</td><td>

Electrical specifications of the model \(such as voltages and frequencies\) populated from the content service.

</td></tr><tr><td>

Weight

</td><td>

Weight of the model populated from the content service.

</td></tr><tr><td colspan="2">

**Environmental Social Governance \(ESG\)**

</td></tr><tr><td>

Energy star

</td><td>

Energy Star certified status of the model populated from content service.

</td></tr><tr><td>

EPEAT compliant

</td><td>

Electronic Product Environmental Assessment \(EPEAT\) compliant status of the model populated from the content service.

</td></tr><tr><td>

EPEAT level

</td><td>

EPEAT level \(Gold, Silver, or Bronze\) of the model populated from the content service.

</td></tr><tr class="sub-head"><td colspan="2">

**Additional Details**

</td></tr><tr><td>

Manufacturer warranty

</td><td>

Manufacturer warranty terms of the model populated from content service.

</td></tr><tr><td>

Features

</td><td>

Product overview, specifications, or attributes of the model populated by the content service.

</td></tr><tr class="sub-head"><td>

Information

</td><td>

 

</td></tr><tr><td>

Power \(watts\)

</td><td>

Power requirement of the model in watts.

</td></tr><tr><td>

Height \(U\)

</td><td>

Height of the model in rack units.

</td></tr><tr><td>

Flow Rate \(cfm\)

</td><td>

Flow rate of the model in cubic feet per minute.

</td></tr><tr><td>

Sound Power \(bels\)

</td><td>

Sound power of the model in bels.

</td></tr><tr><td>

Weight \(lbs\)

</td><td>

Weight of the model in lbs.

</td></tr><tr><td>

Expected lifetime CO2e

</td><td>

Consumed Carbon dioxide equivalent \(CO2e\) over the life of the model.

</td></tr><tr><td>

Energy use

</td><td>

Energy consumed by this model.

</td></tr><tr><td>

Energy Star

</td><td>

Requirements to be Energy Star certified by the Environmental Protection Agency \(EPA\).

</td></tr><tr class="sub-head"><td>

Product Catalog

</td><td>

 

</td></tr><tr><td>

Catalog Item

</td><td>

Name of the catalog item.

</td></tr><tr><td>

Description

</td><td>

Description of the catalog item.

</td></tr></tbody>
</table>## Compatibles

|Field|Description|
|-----|-----------|
|Model|Name of the hardware model.|
|Model|Name of the hardware model that is compatible with the hardware model record.|

## Substitutes

|Field|Description|
|-----|-----------|
|Model|Name of the hardware model.|
|Substitute|Name of the hardware model that can be substituted for the hardware model.|
|Domain|Domain of the hardware model record.|

## Assets

For information about the fields on the Assets tab, see [Create assets](../../asset-management/task/t_CreatingAssets.md).

## Configuration Items

|Field|Description|
|-----|-----------|
|Name|Name of the CI. This name is often the Domain Name System \(DNS\) or computer host name.|
|Manufacturer|Name of the manufacturer.|
|Location|Location of the manufacturer.|
|Description|Description of the CI.|
|Class|Type of asset class.|

## Model Components

<table id="table_b3y_y3c_2jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is main component

</td><td>

Option for indicating if this component is the one that other components are attached to.

</td></tr><tr><td>

Component

</td><td>

Model that the child component will be instantiated as when the asset is created.

</td></tr><tr><td>

Model category of component

</td><td>

Model category that the child component will be instantiated as when the asset is created.

</td></tr><tr><td>

Component parameter

</td><td>

Component parameter requirement.-   **Mandatory**
-   **Optional**

</td></tr><tr><td>

Main component

</td><td>

Name of the bundle if the model is an abstract model.**Note:** This field is only used if an abstract model has been defined.

</td></tr></tbody>
</table>## Vendor Catalog Items

<table id="table_jgb_mzw_pxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the vendor catalog item.

</td></tr><tr><td>

Product ID

</td><td>

The item identification number assigned by your organization.

</td></tr><tr><td>

Short Description

</td><td>

A brief description of the item.

</td></tr><tr><td>

Vendor Price

</td><td>

The price at which the item is available in the vendor catalog. If the vendor offers a discount, the vendor price reflects the discounted price.

</td></tr><tr><td>

Rank Tier

</td><td>

Displays the overall ranking for products and services of this vendor, such as Valued Partner or Tactical Supplier. Rank tier expresses the opinion of your organization of the vendor performance. It can be used to decide if the vendor's products should be promoted or discontinued. Users with the vendor\_manager role can edit this field.

</td></tr></tbody>
</table>## Hardware Model Lifecycles

<table id="table_ckb_jm4_gjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Name of the hardware model.

</td></tr><tr><td>

Lifecycle type

</td><td>

Type of life cycle.

</td></tr><tr><td>

Lifecycle phase

</td><td>

Phase of the life cycle for a hardware model.-   **General Availability:** The date when the hardware becomes generally available through the manufacturer’s sales channels, including its worldwide subsidiaries, affiliates, and country distributors. The hardware is considered current/active and receiving support from the manufacturer.
-   **End of Sale:**The last date to order the hardware through the manufacturer’s sales channels, including its worldwide subsidiaries, affiliates, and country distributors. After end of sale date, the hardware is no longer available for sale.
-   **End of Support**: The last date upon which the manufacturer provides standard/regular support for the hardware as entitled by active service contracts. After this date, the manufacturer may continue to provide active support for certain issues in a limited capacity, the scope of which may vary across different manufacturers according to their lifecycle and/or support policies.
-   **End of Extended Support:** Up until this date, the manufacturer extends limited support for the hardware \(after standard/regular support expires\), for a defined period according to manufacturer policy.
-   **End of Life:**The date which indicates the hardware is at the end of its useful life \(from the manufacturer’s point of view\). The manufacturer stops marketing, selling, or sustaining the hardware.

</td></tr><tr><td>

Source

</td><td>

Source of the hardware model.

</td></tr><tr><td>

Phase start date

</td><td>

Start date of the life cycle phase.

</td></tr><tr><td>

Phase end date

</td><td>

End date of the life cycle phase.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the life cycle.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the hardware model life cycle is active.

</td></tr><tr><td>

Description

</td><td>

Description of the hardware model.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

**Related topics**  


[Create a hardware or consumable model](../task/create-hardware-consumable-model.md)

