---
title: Mandatory fields in the bulk import spreadsheets
description: A list of the mandatory fields in the model, asset, and model and asset templates for bulk import in the Enterprise Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/enterprise-asset-management/mandatory-bulk-fields.html
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [References, Enterprise Asset Management, IT Asset Management]
---

# Mandatory fields in the bulk import spreadsheets

A list of the mandatory fields in the model, asset, and model and asset templates for bulk import in the Enterprise Asset Workspace.

## Mandatory fields for model template

<table id="table_eh1_gx2_3xb"><thead><tr><th>

Field/column

</th><th>

Mandatory for creating models

</th><th>

Mandatory for updating models

</th></tr></thead><tbody><tr><td>

Index**Note:** Representing the row number can be used to identify a specific row. However, you need to fill this in manually.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Manufacturer

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Name

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Number

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model category

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model type

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Parent model manufacturer

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Parent model name

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Parent model number

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Component number

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Component quantity

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Required

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Hot swappable

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr><tr><td>

Repairable

</td><td>

Yes**Note:** Not applicable for single models.

</td><td>

No

</td></tr></tbody>
</table>## Mandatory fields for asset template

<table id="table_bqz_psg_3xb"><thead><tr><th>

Field/column

</th><th>

Mandatory for creating assets

</th><th>

Mandatory for updating assets

</th></tr></thead><tbody><tr><td>

Index**Note:** Representing the row number can be used to identify a specific row. However, you need to fill this in manually.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Manufacturer

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Name

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Number

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Parent model manufacturer

</td><td>

Yes**Note:** Not applicable for single assets.

</td><td>

Yes

</td></tr><tr><td>

Parent model name

</td><td>

Yes**Note:** Not applicable for single assets.

</td><td>

Yes

</td></tr><tr><td>

Parent model number

</td><td>

Yes**Note:** Not applicable for single assets.

</td><td>

Yes

</td></tr><tr><td>

Component number

</td><td>

Yes**Note:** Not applicable for single assets.

</td><td>

Yes

</td></tr><tr><td>

Asset Tag

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

Serial Number

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

MAC Address

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

Parent asset

</td><td>

Conditional**Note:** Required for child assets when parent model information is provided.

</td><td>

Conditional**Note:** Required for child assets when parent model information is provided.

</td></tr><tr><td>

Quantity

</td><td>

Conditional**Note:** Required for consumable assets \(positive number\).

</td><td>

No**Note:** Consumable assets cannot be updated.

</td></tr><tr><td>

State

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Sub state

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Stockroom

</td><td>

Conditional**Note:** Required for In stock and Build states.

</td><td>

Conditional**Note:** Required for In stock and Build states.

</td></tr><tr><td>

Location

</td><td>

Conditional**Note:** Required for In stock, In use, and Build states.

</td><td>

Conditional**Note:** Required for In stock, In use, and Build states.

</td></tr><tr><td>

Install status

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Substatus

</td><td>

Conditional**Note:** Required for In stock state only.

</td><td>

Conditional**Note:** Required for In stock state only.

</td></tr><tr><td>

Component ID

</td><td>

Conditional**Note:** Required for child assets when applicable.

</td><td>

No

</td></tr><tr><td>

OT entity

</td><td>

Conditional**Note:** Required as **true** for hardware models when the OT Asset Management application is activated.

</td><td>

Conditional**Note:** Required as **true** for hardware models when the OT Asset Management application is activated.

</td></tr></tbody>
</table>## Mandatory fields for model and asset template

<table id="table_ukz_yyj_3xb"><thead><tr><th>

Field/column

</th><th>

Mandatory for creating models and assets

</th><th>

Mandatory for updating models and assets

</th></tr></thead><tbody><tr><td>

Index**Note:** Representing the row number can be used to identify a specific row. However, you need to fill this in manually.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Manufacturer

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Name

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model Number

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model category

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Model type

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Parent model manufacturer

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

Yes

</td></tr><tr><td>

Parent model name

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

Yes

</td></tr><tr><td>

Parent model number

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

Yes

</td></tr><tr><td>

Component number

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Component quantity

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Required

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Hot swappable

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Repairable

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Asset Tag

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

Serial Number

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

MAC Address

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td><td>

Conditional**Note:** At least one unique identifier is required for non-consumables based on model category.

</td></tr><tr><td>

Parent asset

</td><td>

Yes**Note:** Not applicable for single models and single assets.

</td><td>

No

</td></tr><tr><td>

Quantity

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

State

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Sub state

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Stockroom

</td><td>

Conditional**Note:** Required for In stock and Build states.

</td><td>

Conditional**Note:** Required for In stock and Build states.

</td></tr><tr><td>

Location

</td><td>

Conditional**Note:** Required for In stock, In use, and Build states.

</td><td>

Conditional**Note:** Required for In stock, In use, and Build states.

</td></tr></tbody>
</table>## Unit of measurement fields

<table id="table_ult_2sm_ngc"><thead><tr><th>

Field/column

</th><th>

Mandatory for creating models

</th><th>

Mandatory for updating models

</th></tr></thead><tbody><tr><td>

Dimensions Unit

</td><td>

Conditional**Note:** Required if length, width, height, or depth is provided.

</td><td>

Conditional**Note:** Required if length, width, height, or depth is provided.

</td></tr><tr><td>

Weight Unit

</td><td>

Conditional**Note:** Required if the weight\_decimal value is provided.

</td><td>

Conditional**Note:** Required if the weight\_decimal value is provided.

</td></tr><tr><td>

Volume Unit

</td><td>

Conditional**Note:** Required if the volume is provided.

</td><td>

Conditional**Note:** Required if the volume is provided.

</td></tr><tr><td>

Current Unit

</td><td>

Conditional**Note:** Required if the value is provided for Current.

</td><td>

Conditional**Note:** Required if the value is provided for Current.

</td></tr><tr><td>

Power Unit

</td><td>

Conditional**Note:** Required if the rated\_power value is provided.

</td><td>

Conditional**Note:** Required if rated\_power is provided.

</td></tr><tr><td>

Voltage Unit

</td><td>

Conditional**Note:** Required if the voltage value is provided.

</td><td>

Conditional**Note:** Required if voltage is provided.

</td></tr><tr><td>

Cooling Unit

</td><td>

Conditional**Note:** Required if the cooling value is provided \(Enterprise models only\).

</td><td>

Conditional**Note:** Required if the cooling value is provided \(Enterprise models only\).

</td></tr><tr><td>

Pressure Unit

</td><td>

Conditional**Note:** Required if the pressure value is provided \(Enterprise models only\).

</td><td>

Conditional**Note:** Required if the pressure value is provided \(Enterprise models only\).

</td></tr><tr><td>

Temperature Unit

</td><td>

Conditional**Note:** Required if the temperature value is provided \(Enterprise models only\).

</td><td>

Conditional**Note:** Required if the temperature value is provided \(Enterprise models only\).

</td></tr></tbody>
</table>## Reference fields validation

The values entered in the following columns should exist in the database:

-   PO Number
-   Assigned To
-   Department
-   Company
-   Cost Center
-   Asset Depreciation
-   Aisle Space Location

**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management]()

[Enterprise Asset Management roles]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance plan fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Enterprise asset disposal order stages]()

[Terminology for linear assets]()

[Installed with Enterprise Asset Management for Healthcare]()

[Installed with OT Asset Management]()

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)]()

[Components installed with Enterprise Asset Management for Providers]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

