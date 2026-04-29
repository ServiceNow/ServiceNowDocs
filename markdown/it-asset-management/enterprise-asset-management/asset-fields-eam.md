---
title: Asset fields for enterprise assets
description: A detailed description of all asset fields in the Enterprise Asset Management application.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Asset fields for enterprise assets

A detailed description of all asset fields in the Enterprise Asset Management application.

<table id="table_njq_yfh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the asset as it appears in record lists. Automatically set when asset is created, based on **Asset Tag** and **Model** fields.

</td></tr><tr><td>

Model

</td><td>

Specific product model of the asset.**Note:** If you are creating a consumable asset, you can select any product model that meets the following criteria:

-   The Model type is set to Consumable.
-   The product model falls under the Enterprise good model \[sn\_ent\_model\] class or any of its child classes.

</td></tr><tr><td>

Model category

</td><td>

Model grouping of the asset. Based on the model category selected, the asset can be linked to a configuration item.

</td></tr><tr><td>

Parent

</td><td>

Parent asset of the asset. When a parent link is defined, the fields related to assignment and state of the child assets is set to read-only and are populated based on the parent assignment and state fields.

</td></tr><tr><td>

Asset type

</td><td>

Type of multi-component asset. The following are the types of multi-component assets:-   Pre-assembled
-   User-assembled
-   Simple
-   Simple with add-on
-   Pre-assembled with add-on
-   User-assembled with add-on

</td></tr><tr><td>

Asset tag

</td><td>

Alphanumeric information assigned by your organization to help track the asset.

</td></tr><tr><td>

Configuration item

</td><td>

CI automatically created when this asset is created. The name that appears in this field is based on **Serial number** and **Model**. Point to the reference icon to see the configuration item details inherited from the asset record.

</td></tr><tr><td>

Serial number

</td><td>

Serial number of this asset.

</td></tr><tr><td>

State

</td><td>

The current state of the asset. By default, the newly created asset is in **Build** state. Once you configure the asset and its components, you can change the status of the model. The other state options are:

-   **On order**
-   **In stock**
-   **In transit**
-   **In use**
-   **In maintenance**
-   **Retired**
-   **Missing**

</td></tr><tr><td>

Substate

</td><td>

Current substate of the asset, such as **Available** or **Reserved**. The values in the Substate list change based what you select from the **State** list.

</td></tr><tr><td>

Asset function

</td><td>

Function as which the asset is used such as Primary, Secondary, Shared, or Loaner.

</td></tr><tr><td>

Stockroom**Note:** This field appears only if you set the **State** field to **In stock**.

</td><td>

Stockroom that the asset is located in.

</td></tr><tr><td>

Aisle and space

</td><td>

Aisle and space details of the asset within the stockroom. This field appears only when the state of the asset is **In stock** or **Build**.

</td></tr><tr><td>

Reserved for**Note:** This field appears only if you set the **State** field to **In stock** or **In transit**.

</td><td>

User who the asset is reserved for.

</td></tr><tr><td>

Quantity

</td><td>

Number of items this asset represents. An asset always has a quantity of one unless one or more of these points are true.-   It is a consumable. Quantity is unrestricted because consumables are tracked in groups.
-   It is pre-allocated. Quantity is unrestricted when **Model category** and **Model** are defined and **Substate** is set to **Pre-allocated**.

</td></tr><tr><td>

Eligible for refresh

</td><td>

Indicates whether or not the asset is eligible for a refresh. If the date in the **Installed** field is in the past, this check box is shown. This check box is selected automatically two months before the number specified in the model's **Useful life \(months\)** field.

 When the `EAM- Calculate Asset Refresh Eligibility` weekly scheduled job runs, it calculates all of the assets that are eligible for refresh.

</td></tr><tr><td>

Location

</td><td>

Current physical location of the asset.

 **Note:**

If you set the location to a specific building, floor, or place, and then set the **sn\_itam\_common.sn\_enable\_indoormap\_for\_assets** system parameter to **true** on your ServiceNow instance, the Enterprise Asset Management application automatically populates a corresponding location hierarchy of up to three levels, including the campus, building or structure, and floor that the asset is currently located in. The location hierarchy depicts the hierarchical relationship between the specified location and the corresponding parent locations. You can view the location hierarchy in the Location Hierarchy section of the asset record, which is generated after you fill in all fields and save the form.

 **Note:**

If you set the location to a specific place and then set the **sn\_itam\_common.sn\_enable\_indoormap\_for\_assets** system parameter to **true** on your ServiceNow instance, the asset record, which is generated after you fill in all fields and save the form, includes an interactive map that shows the real-time location of the asset. This map is still included in the asset record when you open the record from an associated work order task or stockroom record.

The map does not display by default. To display the map, select the Location map icon \(![Location map icon.](../image/asset-indoor-location-icon.png)\) on the sidebar of the asset record.

</td></tr><tr><td>

Assigned to

</td><td>

Person using or primarily responsible for this item. This field is visible when the asset state is **In Use**.

</td></tr><tr><td>

Assigned

</td><td>

Date on which the asset was assigned to a user.

</td></tr><tr><td>

Managed by

</td><td>

Person who maintains the asset. This can be different from the person in the **Owned by** field.

</td></tr><tr><td>

Installed

</td><td>

Date on which the asset was assigned to the person mentioned in the **Assigned to** field.

</td></tr><tr><td>

Owned by

</td><td>

Person who has financial ownership of the asset. This can be different from the person in the **Managed by** field.

</td></tr><tr><td>

Warranty expiration

</td><td>

The date the warranty expires.

</td></tr><tr><td>

Company

</td><td>

Company or organization to which this asset belongs.

</td></tr><tr><td>

Department

</td><td>

Department to which the asset belongs.

</td></tr><tr><td>

RFID tag

</td><td>

Real-time radio-frequency identification \(RFID\) tag that is associated with the asset. See [Zebra MotionWorks RFID integration for Enterprise Asset Management](../concept/eam-zebra-rfid-integration.md) for more information on RFID tags.**Note:** If this asset is a child of another asset and does not contain its own RFID tag, the **RFID tag** field populates with the RFID tag of the parent asset. If you remove the parent asset, the **RFID tag** field is cleared for this asset.

</td></tr><tr><td>

MAC address

</td><td>

MAC address of the asset.**Important:** From the Yokohama release onward, the value in this field is populated based on the **MAC address** \[mac\_addr\] field in the Asset \[alm\_asset\] table. The **MAC address** \[mac\_address\] field in the Hardware \[alm\_hardware\] table is deprecated.

This field isn't shown on the asset form for consumables and pallets.

</td></tr><tr><td>

Support group

</td><td>

Group responsible for maintaining and managing the asset. The support group can belong to any of the following group types:

-   Asset managers
-   Asset techs

</td></tr><tr><td>

Supported by

</td><td>

Specific individual from the support group who is assigned to support the asset.

</td></tr><tr><td>

Comments

</td><td>

Message to add if any.

</td></tr></tbody>
</table><table id="table_ocl_1gh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor

</td><td>

Vendor from which the asset was purchased. For assets automatically created from purchase orders in Procurement, the default value of the **Vendor** field is the vendor specified on the purchase order.

</td></tr><tr><td>

Opened

</td><td>

Date on which the requested item record was opened. The system automatically populates the field when a request line is specified.

</td></tr><tr><td>

Invoice number

</td><td>

Number of the invoice.

</td></tr><tr><td>

GL account

</td><td>

General ledger account number with which the asset is associated.

</td></tr><tr><td>

Request line

</td><td>

Requested item to which the asset is linked.

</td></tr><tr><td>

Cost

</td><td>

Price at which the asset was purchased.

</td></tr><tr><td>

Cost center

</td><td>

Cost center under which the asset was billed.

</td></tr><tr><td>

Acquisition method

</td><td>

How the asset was acquired. Base system choices are **Purchase**, **Lease**, **Rental**, **Loan**, and **RMA Replacement**.For assets automatically created from purchase orders in Procurement, the default value is **Purchase**

</td></tr><tr><td>

PO number

</td><td>

Purchase Order under which the asset was billed.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Depreciation|Depreciation method that is applied. Base system choices are **Declining Balance** and **Straight Line**. The depreciation value is defaulted from the associated Model.|
|Residual date|Number of days that have passed since the **Depreciation effective date**.|
|Depreciation effective date|Date on which the specified depreciation method begins.|
|Residual value|Value in the Cost field with the depreciation method applied.|
|Salvage value|Estimated value of an asset at the end of its useful life. This value must be less than or equal to the Cost of the asset.|
|Depreciated amount|Amount the asset has depreciated.|

<table id="table_l2k_fgh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lease contract

</td><td>

Name of the lease contract that applies to the asset.

</td></tr><tr><td>

Lease expiration date

</td><td>

Date on which the lease contract expires

</td></tr><tr><td>

Lease term \(months\)

</td><td>

Length of the lease contract, in months.

</td></tr><tr><td>

Monthly lease payment

</td><td>

Amount that you must pay monthly for the lease contract.**Note:** You can set this field to any currency of your choice.

</td></tr></tbody>
</table><table id="table_ygh_cgh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disposal order number

</td><td>

A unique number assigned to the asset disposal order.

</td></tr><tr><td>

Disposal vendor

</td><td>

The vendor assigned to carry out the asset disposal order.

</td></tr><tr><td>

Scheduled retirement

</td><td>

Scheduled date on which the asset is retired.

</td></tr><tr><td>

Retired date

</td><td>

Actual date on which the asset was retired.

</td></tr><tr><td>

Vendor disposal order ID

</td><td>

Order number assigned by the vendor assigned to carry out the asset disposal order.

</td></tr><tr><td>

Resale price

</td><td>

Value of the asset when it is retired. For example, if the asset is donated, the value used when reporting taxes.

</td></tr><tr><td>

Disposal date

</td><td>

The date when the asset disposal order process is completed.

</td></tr><tr><td>

Beneficiary

</td><td>

Organization that receives the asset when it is retired.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Audit number|Audit number of the asset.|
|Audit type|Type of audit that was carried out on the asset.|
|Last audit date|Date on which the last audit was done.|
|Last audit state|State of the last audit.|
|Audited by|Person who performed the last audit.|

<table id="table_mfy_gmn_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RFID tag

</td><td>

Real-time radio-frequency identification \(RFID\) tag that is associated with the asset. For more information on RFID tags, see [Zebra MotionWorks RFID integration for Enterprise Asset Management](../concept/eam-zebra-rfid-integration.md).

</td></tr><tr><td>

Type

</td><td>

Type of RFID tag that is associated with the asset.

</td></tr><tr><td>

Tag source

</td><td>

Source of the asset's RFID location data that is stored and transferred through the RFID tag.

</td></tr><tr><td>

Serial number

</td><td>

Serial number of the asset.

</td></tr><tr><td>

Last blink time

</td><td>

Time at which the RFID tag was last scanned.

</td></tr><tr><td>

Last blink elapsed time

</td><td>

Amount of time that has passed since the RFID tag was last scanned.

</td></tr><tr><td>

Latitude

</td><td>

Latitudinal value of the asset.

</td></tr><tr><td>

Longitude

</td><td>

Longitudinal value of the asset.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the RFID tag is active. RFID location data can be mapped to the asset only if you select this option.

</td></tr><tr><td>

Site name

</td><td>

Name of the site that the asset is located in.

</td></tr><tr><td>

Zone group

</td><td>

Interrogation zone group that the asset belongs to.

</td></tr><tr><td>

Zone group dwell

</td><td>

Amount of time for which the asset belongs to the specified interrogation zone group.

</td></tr><tr><td>

Zone

</td><td>

Interrogation zone that the asset is located in.

</td></tr><tr><td>

Zone dwell

</td><td>

Amount of time for which the asset is located in the specified interrogation zone.

</td></tr><tr><td>

Grid-x

</td><td>

X coordinate of the asset within the designated RFID grid. The RFID system uses the XYZ coordinates to pinpoint the location of the asset.

</td></tr><tr><td>

Grid-y

</td><td>

Y coordinate of the asset within the designated RFID grid. The RFID system uses the XYZ coordinates to pinpoint the location of the asset.

</td></tr><tr><td>

Grid-z

</td><td>

Z coordinate of the asset within the designated RFID grid. The RFID system uses the XYZ coordinates to pinpoint the location of the asset.

</td></tr><tr><td>

Status

</td><td>

Status of mapping RFID location data to the asset. If the data is successfully mapped to the asset, this field is set to **Matched**. If the data is not mapped to the asset, this field is set to **Unmatched**.**Important:** RFID location data can be mapped to the asset only if you select the **Active** option in the RFID form section.

 **Tip:** You can view and take action on the asset records that have an RFID **Status** of **Unmatched** by using the **Unmatched RFID tags** important action that appears on the **Overview** tab of the Enterprise asset estate view. For more information on the Enterprise asset estate view, see [Enterprise asset estate overview for Enterprise Asset Workspace](../concept/asset-estate-overview-eam.md).

</td></tr></tbody>
</table><table id="table_ydm_ggh_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work notes

</td><td>

Work notes are updated for the following cases: -   Updates to **Assigned To**, **Managed To** **State**, **Substate**, and **Reserved** fields of asset. The columns for these fields are audited by default and any update is recorded in the work notes.
-   Work notes are updated when asset is received by a purchase order and transfer order. These work notes help in tracking life cycle of the asset.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|DaaS asset|Option that indicates if the given asset is a Device as a Service \(DaaS\) asset.|
|DaaS account|DaaS account that the asset is leased to.|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[OT Asset Workspace roles](ot-workspace-roles.md)

[Asset audit fields for enterprise assets](asset-audit-record-fields-eam.md)

[Audit results](audit-results-eam.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

