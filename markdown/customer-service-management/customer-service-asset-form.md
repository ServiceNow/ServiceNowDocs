---
title: Asset form
description: The Asset Management application uses the Asset form to store asset information.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Asset form

The Asset Management application uses the Asset form to store asset information.

<table id="table_yd3_v2c_3p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the asset as it appears in the record lists. This field is automatically set when you create an asset, based on the **Asset Tag** and **Model** fields.

</td></tr><tr><td>

Model category

</td><td>

Model grouping of the asset. Based on the model category you select, the asset is linked to a configuration item.

</td></tr><tr><td>

Model

</td><td>

Specific product model of the asset.

</td></tr><tr><td>

Configuration Item

</td><td>

CI is automatically created when you create an asset. The name that appears in this field is based on the **Serial number** and **Model** field values. Point to the reference icon to view the configuration item details inherited from the asset record.

</td></tr><tr><td>

Quantity

</td><td>

Number of items this asset represents. An asset always has a quantity of one unless one or more of these points are true.-   If the asset is a consumable, the quantity is unrestricted because consumables are tracked in groups.
-   If the asset is pre-allocated, the quantity is unrestricted when the **Model category** and **Model** values are defined and **Substate** is set to **Pre-allocated**.

</td></tr><tr><td class="sub-head" colspan="2">

GeneralAll the fields aren't available for each type of asset.

</td></tr><tr><td>

Asset tag

</td><td>

Alphanumeric information assigned by your organization to help track the asset.

</td></tr><tr><td>

State

</td><td>

Current state of the asset, such as **On order** or **In use**.

</td></tr><tr><td>

Assigned to

</td><td>

Person using or primarily responsible for this item. This field appears when the asset state is **In Use**.

</td></tr><tr><td>

Stockroom

</td><td>

Name of the stockroom. This field appears only when the state of the asset is **In stock** or **Build**.

</td></tr><tr><td>

Aisle

</td><td>

Aisle details of the asset within the stockroom. This field appears only when the state of the asset is **In stock** or **Build**.**Note:** This field would appear only when the Hardware Asset Management Professional plugin \(com.sn\_hamp\) is installed.

</td></tr><tr><td>

Space

</td><td>

Space details of the asset within the aisle. This field appears only when the state of the asset is **In stock** or **Build**.**Note:** This field would appear only when the Hardware Asset Management Professional plugin \(com.sn\_hamp\) is installed.

</td></tr><tr><td>

Managed by

</td><td>

Person who maintains the asset. This field value can be different from the person in the **Owned by** field.

</td></tr><tr><td>

Owned by

</td><td>

Person who has financial ownership of the asset. This field value can be different from the person in the **Managed by** field.

</td></tr><tr><td>

Parent

</td><td>

Parent asset of the asset. For example, a monitor or peripheral can have a workstation as their parent asset. When a parent link is defined, the fields related to assignment and state of the child assets is set to read-only and are populated based on the parent assignment and state fields. For more information, see [Bundled models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/product-catalog/c_CreatingBundledModels.md).

</td></tr><tr><td>

Class

</td><td>

Asset group, for example, base, hardware, license, or consumable.

</td></tr><tr><td>

Comments

</td><td>

Information about the asset that would be helpful for others to know.

</td></tr><tr><td>

Serial number

</td><td>

Serial number of this asset.

</td></tr><tr><td>

Substate

</td><td>

Current substate of the asset. The available substate settings depend on the state selected. For example, the **Retired** state contains the **Substate** options **Disposed**, **Sold**, **Donated**, and **Vendor credit**.

</td></tr><tr><td>

Location

</td><td>

Current physical location of the asset.**Note:** You can set the location to a place, floor, building, or campus. When you set the location to any of the options except the campus, the Location hierarchy section is shown on the asset form. The location hierarchy shows the hierarchical relationship between the specified location and its parent locations.

Also, when you set the Location field to a place and then set the **sn\_itam\_common.sn\_enable\_indoormap\_for\_assets** system parameter to **true** on your ServiceNow instance, a real-time location map of the asset is shown on the asset form. The Location map doesn’t appear by default. To view the map, select the Location map \(![asset indoor location con](../image/asset-indoor-location-icon.png)\) icon on the contextual sidebar of the asset record.

Location map doesn’t appear for excluded assets.

You can also track your asset location using the Asset Indoor map in the Asset estate view of the Hardware Asset Workspace. For more information, see [Track asset location using indoor maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/track-asset-location-using-indoor-maps.md).

</td></tr><tr><td>

Department

</td><td>

Department to which the asset belongs.

</td></tr><tr><td>

Company

</td><td>

Company or organization to which this asset belongs.

</td></tr><tr><td>

Assigned

</td><td>

Date on which the asset was assigned to a user.

</td></tr><tr><td>

Installed

</td><td>

Date on which the asset was installed.

</td></tr><tr><td class="sub-head" colspan="2">

Location HierarchyThe Location Hierarchy section is available only for hardware, consumables,bundle, and pallet assets. This section appears only under the following conditions:

-   When the ** sn\_itam\_common.sn\_enable\_indoormap\_for\_assets** system parameter is set to **true** on your ServiceNow instance
-   When you select any location except the campus

</td></tr><tr><td>

Floor

</td><td>

Floor where the place specified in the Location field is located. **Note:** This field appears only when you select a place in the Location field and is populated automatically based on the location.

</td></tr><tr><td>

Building/Structure

</td><td>

Building to which the floor belongs.**Note:** This field appears only when you select a place or floor in the Location field and is populated automatically based on the location.

</td></tr><tr><td>

Campus

</td><td>

Campus where the building is located.**Note:** This field appears only when you select a place, floor, or building in the Location field and is populated automatically based on the location.

</td></tr><tr><td class="sub-head" colspan="2">

FinancialThe Financial section is available only for hardware, software entitlement, and facility assets.

</td></tr><tr><td>

Request line

</td><td>

Requested item to which the asset is linked.

</td></tr><tr><td>

Invoice number

</td><td>

Invoice under which the asset was billed.

</td></tr><tr><td>

Cost

</td><td>

Price at which the asset was purchased.

</td></tr><tr><td>

Vendor

</td><td>

Vendor from which the asset was purchased. The assets that are automatically created from purchase orders in Procurement, the default value of the **Vendor** field is the vendor specified on the purchase order.

</td></tr><tr><td>

Opened

</td><td>

Date on which the requested item record was opened. The system automatically populates the field when a request line is specified.

</td></tr><tr><td>

GL account

</td><td>

General ledger account number with which the asset is associated.

</td></tr><tr><td>

Cost center

</td><td>

Group financially responsible for the asset.

</td></tr><tr><td>

Acquisition method

</td><td>

The way of acquiring the asset. Base system choices are **Purchase**, **Lease**, **Rental**, and **Loan**.The assets that are automatically created from purchase orders in Procurement, the default value is **Purchase**

</td></tr><tr><td>

Expenditure type

</td><td>

The type of expenditure. -   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an on-going expenditure. For example, toners for the photocopier.

</td></tr><tr><td class="sub-head" colspan="2">

Disposal

</td></tr><tr><td>

Disposal order number

</td><td>

A unique number assigned to the asset disposal order.

 **Note:** This field appears only if you’ve installed Hardware Asset Management from ServiceNow Store.

</td></tr><tr><td>

Disposal vendor

</td><td>

The vendor assigned to carry out the asset disposal order.

 **Note:** This field appears only if you’ve installed Hardware Asset Management from ServiceNow Store.

</td></tr><tr><td>

Vendor disposal order ID

</td><td>

Order number assigned by the vendor to carry out the asset disposal order.

 **Note:** This field appears only if you’ve installed Hardware Asset Management from ServiceNow Store.

</td></tr><tr><td>

Disposal date

</td><td>

The date when the asset disposal order process is completed.

 **Note:** This field appears only if you’ve installed Hardware Asset Management from ServiceNow Store.

</td></tr><tr><td>

Disposal reason

</td><td>

Text explaining why the asset is being retired.

</td></tr><tr><td>

Beneficiary

</td><td>

Organization that receives the asset when it’s retired.

</td></tr><tr><td>

Resale price

</td><td>

Value of the asset when it’s retired. For example, if the asset is donated, the value used when reporting taxes.

</td></tr><tr><td>

Scheduled retirement

</td><td>

Scheduled date on which the asset is retired.

</td></tr><tr><td>

Retired date

</td><td>

Actual date on which the asset was retired.

</td></tr><tr><td class="sub-head" colspan="2">

DepreciationThe Depreciation section is available only for hardware and facility assets.

</td></tr><tr><td>

Depreciation

</td><td>

Depreciation method that is applied. Base system choices are **Declining Balance** and **Straight Line**. The depreciation value is defaulted from the associated Model.

</td></tr><tr><td>

Depreciation effective date

</td><td>

Date on which the specified depreciation method begins.

</td></tr><tr><td>

Salvage value

</td><td>

Estimated value of an asset at the end of its useful life. This value must be less than or equal to the Cost of the asset.

</td></tr><tr><td>

Residual date

</td><td>

Number of days that have passed since the **Depreciation effective date**.

</td></tr><tr><td>

Residual value

</td><td>

Value in the Cost field with the depreciation method applied.

</td></tr><tr><td>

Depreciated amount

</td><td>

Amount the asset has depreciated.

</td></tr><tr><td class="sub-head" colspan="2">

ContractsThe Contract section is available only for hardware, software entitlement, or facility assets.

</td></tr><tr><td>

Lease contract

</td><td>

Name of the lease contract that applies to the asset.

</td></tr><tr><td>

Warranty expiration

</td><td>

Expiration date of the asset warranty.

</td></tr><tr><td>

Lease expiration date

</td><td>

Date on which the contract gets expired.**Note:** This field would appear only when Hardware Asset Management \(sn\_hamp\) is installed.

</td></tr><tr><td>

Lease term \(months\)

</td><td>

The period in months the lease contract is active for.**Note:** This field would appear only when Hardware Asset Management \(sn\_hamp\) is installed.

</td></tr><tr><td>

Monthly lease payment

</td><td>

Amount that you pay monthly for the contract.**Note:** This field would appear only when Hardware Asset Management \(sn\_hamp\) is installed.

</td></tr><tr><td>

Support group

</td><td>

Group managing the contract covering the asset.

</td></tr><tr><td>

Like-kind exchange

</td><td>

A similar asset that you want to return to the contract vendor instead of the asset that you brought in lease.**Note:** This field would appear only when Hardware Asset Management \(sn\_hamp\) is installed.

</td></tr><tr><td>

Supported by

</td><td>

Person managing the contract covering the asset.

</td></tr><tr><td class="sub-head" colspan="2">

Activities

</td></tr><tr><td>

Work notes

</td><td>

Work notes are updated for the following cases: -   Updates to **Assigned To**, **Managed To** **State**, **Substate**, and **Reserved** fields of asset. The columns for these fields are audited by default and any update is recorded in the work notes.
-   Work notes for hardware and software assets are updated when the asset is received by a purchase order and transfer order. These work notes help in tracking the life cycle of the asset.

</td></tr><tr><td class="sub-head" colspan="2">

Audit

</td></tr><tr><td>

Audit number

</td><td>

Audit number of the asset.

</td></tr><tr><td>

Audit type

</td><td>

Type of audit that was carried out on the asset.

</td></tr><tr><td>

Last audit date

</td><td>

Date on which the last audit was done.

</td></tr><tr><td>

Last audit state

</td><td>

State of the last audit.

</td></tr><tr><td>

Audited by

</td><td>

Person who performed the last audit.

</td></tr><tr><td class="sub-head" colspan="2">

MobileThe Mobile section is available only for the Mobile Device model category.

**Note:** This section appears only when Hardware Asset Management \(sn\_hamp\) is installed.

</td></tr><tr><td>

Carrier

</td><td>

Name of the carrier company.

</td></tr><tr><td>

Ownership

</td><td>

Ownership of the asset. The available values are:-   Employee
-   Corporate

</td></tr><tr><td>

IMEI

</td><td>

Unique number for tracking the mobile device.

</td></tr><tr><td>

Pre-enrollment ID

</td><td>

User who conducted the last audit.

</td></tr><tr><td>

MAC Address

</td><td>

MAC address of the mobile device.

</td></tr><tr><td>

Enrollment ID

</td><td>

User conducting the current audit.

</td></tr><tr><td>

Phone number

</td><td>

Phone number associated with the mobile device.

</td></tr><tr><td>

Enrollment name

</td><td>

Name of the mobile device enrollment.

</td></tr><tr><td>

Platform

</td><td>

Platform of the mobile device. The available options are:-   Android
-   iOS
-   Windows
-   ChromeOS
-   Other

</td></tr><tr><td>

Enrollment state

</td><td>

Current enrollment state of the device. The available options are:-   Enrolled
-   Unenrolled
-   Expired
-   Pending enrollment
-   Pending unenrollment

</td></tr><tr><td>

Purchased

</td><td>

Date on which the mobile device was purchased.

</td></tr><tr><td>

Enrollment date

</td><td>

Initial enrollment date.

</td></tr><tr><td>

Upgrade eligible date

</td><td>

Date on which the mobile device is eligible for an upgrade.

</td></tr><tr><td>

Last enrolled

</td><td>

Date of last enrollment.

</td></tr><tr><td>

Service contract

</td><td>

Contract number associated with the mobile device.

</td></tr><tr><td>

Device activated

</td><td>

Activation status of the mobile device. The available options are:-   Yes- The mobile device is activated.
-   No- The mobile device isn't activated.

</td></tr><tr><td class="sub-head" colspan="2">

Related links

</td></tr><tr><td>

Calculate Depreciation

</td><td>

Select to calculate the depreciation amount and residual value.

</td></tr><tr><td>

Delete Assets Only

</td><td>

Select to delete the assets and not the associated CI.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Assets

</td><td>

Assets that 's related to the asset you created.

</td></tr><tr><td>

Expense lines

</td><td>

Expense line associated with the asset.

</td></tr><tr><td>

RMA

</td><td>

Return Merchandise Authorization associated with the asset.

</td></tr></tbody>
</table>