---
title: Model fields for Enterprise Asset Management
description: A detailed description of all model fields in the Enterprise Asset Management application.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Model fields for Enterprise Asset Management

A detailed description of all model fields in the Enterprise Asset Management application.

## Model Details

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

The manufacturer-assigned name of the model or abstract name specified by the model manager, such as **Field Agent Laptop**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Model categories

</td><td>

The category to which the model belongs to. This is a read-only field.

</td></tr><tr><td>

Model type**Note:** This field doesn’t appear if you’re creating a pallet model.

</td><td>

Type of multi-component model. The following are the options to choose from:

-   Simple
-   Consumable
-   Pre-assembled
-   User-assembled

</td></tr><tr><td>

Asset tracking strategy**Note:** This field doesn’t appear if you’re creating a pallet model.

</td><td>

Process that is used to track the asset. Options are **Leave to category**, **Create consumable asset**, **Don't create assets**.

</td></tr><tr><td>

Asset tracking unit

</td><td>

Unit that is used to measure the asset. Options are **Individual Unit**and **Fixed Fee**.

</td></tr><tr><td>

Acquisition method

</td><td>

The method for purchasing the model. Options are **Both**, **Buy**, or **Lease**.

</td></tr><tr><td>

Model number

</td><td>

The specific model number assigned to the item by the manufacturer.

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

The status of the model. By default, the newly created model is in **Build** status. Once you define the model and its components, you can change the status of the model. The other status options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr><td>

Picture

</td><td>

An image that represents the model. Select the **Attach image** link to choose and attach an image. Once you attach the image, the link changes to **View image**.

</td></tr><tr><td>

Certified

</td><td>

The option that determines whether the model is approved for use.

</td></tr><tr><td>

Comments

</td><td>

Information about the model that would be helpful for others to know.

</td></tr><tr><td>

Calculated lifecycle template

</td><td>

Lifecycle template to calculate lifecycle dates. This template can be assigned to models

</td></tr><tr><td>

Calculated lifecycle start date

</td><td>

Start date from which the Phase start date and Phase end date are calculated for each lifecycle phase defined in the Calculated lifecycle template that you selected.

</td></tr></tbody>
</table>## Financials

<table id="table_cnz_pff_3zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost

</td><td>

The cost of a single unit of the model.

</td></tr><tr><td>

TCO benchmark cost

</td><td>

Specify a TCO benchmark cost for the model.

</td></tr><tr><td>

TCO benchmark threshold

</td><td>

The TCO benchmark threshold is a percentage of the TCO benchmark cost where you want to be alerted that the cost is approaching the benchmark. By default the percentage is 75%. For example, if the TCO benchmark cost is $100 then the TCO benchmark threshold is $75.

 If you set the TCO benchmark cost, this field is automatically calculated.

 You can change the percentage in the **asset\_tco\_benchmark\_threshold\_percentage** system property.

</td></tr><tr><td>

Average assets TCO

</td><td>

Indicates the average Asset TCO value for all assets in the report source. For example, if you have 10 assets in a report source, and adding up all of the Asset TCO values for all assets totals 100,000, then the average asset TCO is 10,000.

</td></tr><tr><td>

Expenditure type

</td><td>

The type of expenditure. Choose from the following: -   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an ongoing expenditure. For example, toners for the photocopier.

</td></tr><tr><td>

Useful life \(months\)

</td><td>

The number of months that the model can be used for.

</td></tr><tr><td>

Depreciation

</td><td>

The depreciation scheme for the model.

</td></tr><tr><td>

Salvage value

</td><td>

The estimated value that an asset realizes upon its sale at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr></tbody>
</table>## Failure Risk

Values in the **Likelihood** and **Impact** fields appear only if the configuration records for risk likelihood and risk impact are frozen.

<table id="table_ixk_mpm_stb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Failure likelihood

</td><td>

The likelihood values for the risk score.

 The configuration values that you created for risk likelihood appear as options in this field. The options appear in the format of `value-label`. For example, `1-Low` where 1 is the value and Low is the label. For details, see [Create configuration values for risk likelihood](../task/risk-likelihood-config.md).

</td></tr><tr><td>

Failure impact

</td><td>

The impact values for the risk score.

 The configuration values that you create for risk impact appear as options in this field. The options appear in the format of `value-label`. For example, `2-Medium` where 2 is the value and Medium is the label. For details, see [Create configuration values for risk impact](../task/risk-impact-config.md).

</td></tr><tr><td>

Failure risk score

</td><td>

The risk score is automatically populated based on the likelihood and impact values.

</td></tr></tbody>
</table>## Normalization

|Field|Description|
|-----|-----------|
|Normalized manufacturer|Normalized name of the manufacturer.|
|Normalized model name|Normalized name of the model.|
|Normalized model number|Normalized number of the model.|
|Normalization status|Current normalization status of the model.|
|Normalized model type|Normalized type of the model.|
|Exclude from sharing with content service|Option that excludes specific content from being shared with the Enterprise Asset Management Content Service. This option is applicable only if you have opted in to the Enterprise Asset Management Content Service.|

## Product Catalog

**Note:** The Product Catalog fields only appear for consumable models.

|Field|Description|
|-----|-----------|
|Catalog Item|Name of the catalog item.|
|Description|Description of the catalog item.|
|Picture|Picture depicting the product model.|

## Model Components tab

Use this tab to create model components. One or more than one model components is required to create a multi-component model.

**Note:** The Model components tab is visible only if the model is a multi-component model. If the **Multi-component** field on the Model page has either of the two values: **Pre-assembled** or **User-assembled**, the Model Components tab is visible. If the **Multi-component** field has the value **Not Applicable**, the Model Components tab is not visible.

|Field|Description|
|-----|-----------|
|Model category of component|Model category of the component.|
|Component|Component of the model. Only model components that belong to the model category you selected appear in this list.|
|Required|If the check box is selected, the model component is required for the complex model to work and can't be permanently removed.|
|Hot swappable|By default, this check box is selected. Indicates that the model component can be swapped while the multi-component model is operational. This check box is selected by default.|
|Repairable|Indicates that the model component can be repaired. This check box is selected by default.|

## Enterprise Model Lifecycles tab

Use this tab to specify life cycle information for the enterprise model.

<table id="table_lmg_d1y_cjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Name of the model.

</td></tr><tr><td>

Lifecycle type

</td><td>

Type of lifecycle.-   **Internal**
-   **Publisher**

</td></tr><tr><td>

Lifecycle phase

</td><td>

Phase of the lifecycle.-   **General Availability**
-   **End of Sale**
-   **End of Support**
-   **End of Extended support**
-   **End of Life**

</td></tr><tr><td>

Source

</td><td>

Source of the lifecycle of the model.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle.

</td></tr><tr><td>

Phase start date

</td><td>

Date the lifecycle phase starts.

</td></tr><tr><td>

Phase end date

</td><td>

Date the lifecycle phase ends.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the lifecycle.-   Very High
-   High
-   Moderate
-   Low
-   None

</td></tr><tr><td>

Active

</td><td>

Indicates that the lifecycle of the model is active.

</td></tr></tbody>
</table>## Vendor Catalog Items tab

**Note:** The Vendor Catalog Items tab appears only for consumable models.

|Field|Description|
|-----|-----------|
|Name|Display name of the vendor catalog item.|
|Vendor|Name of the product vendor.|
|Product Model|Product model associated with the vendor catalog item.|
|Out of Stock|Option that indicates if the product is out of stock.|
|Application|Application that contains the product record.|
|Product ID|Manufacturer product ID.|
|List Price|List price of the product before any discounts are applied.|
|Vendor Price|Vendor price of the product.|
|Rank tier|Vendor rank tier.|
|Short Description|Description of the product.|
|General|
|Product Catalog Item|Product catalog item that was created when the item was published.|
|UPC|Universal Product Code \(UPC\) of the product.|
|Description|Description of the product.|
|Picture|Picture of the product.|
|Active|Option that indicates if the product is active or not.|
|Information|
|Specifications|Product specifications that come from the vendor.|
|Features|Product features that come from the vendor.|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Asset put away task fields](put-away-task-form-eam.md)

