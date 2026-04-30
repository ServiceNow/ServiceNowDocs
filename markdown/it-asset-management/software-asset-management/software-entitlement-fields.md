---
title: Software entitlement fields
description: Software Entitlement form and related list field descriptions.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Software entitlement fields

Software Entitlement form and related list field descriptions.

## Software Entitlement form

**Note:** From the Zurich release, the Database option column no longer exists in the Software Entitlement \[alm\_license\] and the Override License Cost \[samp\_override\_license\_cost\] tables. If you customized your form view prior to the Zurich release to include the database option column, then you get to see the Database option in the software entitlement form.

The list view for software entitlements shows the total number of software entitlement records for your organization based on the value specified in the **SAM Workspace License operations list count limit** system property \(**sn\_sam\_workspace.sam\_license\_operations\_list\_count**\). The default value for the record count is set to **5000000**. However, the SAM administrator can set the value for the count in the system property as required. If there are less than five million records, then the exact count is shown. If there are more than five million records, then the count is shown as 5000000+. For more information on this system property, see [Software Asset Management properties](sam-properties.md).

<table id="table_zql_nkm_11b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_fzb_lss_mfb"><td>

Display name

</td><td>

Automatically generated name based on the software model display name.

</td></tr><tr id="row_h4t_kss_mfb"><td>

Asset tag

</td><td>

Serial number and the bar code used for tracking the asset.

</td></tr><tr><td>

Publisher part number

</td><td>

Publisher part number \(PPN\) from the Software Product Definitions lookup list of predefined software that may have already been purchased.

 You can edit this field in existing entitlements.

 When you select a publisher part number, you may encounter a message: `Many underlying software models are being created. These might be part of suite components, downgrade rights or next version. Please validate on completion`. The message appears only if there are greater than or equal to 50 suite components for the software model and if any of the following conditions are met:

-   A software model doesn’t exist for any suite component
-   A software model doesn’t exist for any downgrade right
-   A software model doesn’t exist for the next version

 **Note:** If a software model exists for the publisher part number, the **Software model** field is automatically populated. Otherwise, the software model is automatically created for you directly from this form. If there are multiple software models created with the same discovery map conditions, the software model must be selected manually.

</td></tr><tr id="row_p5g_kss_mfb"><td>

Software model

</td><td>

The software model to match the entitlement.

 **Note:** A warning message is shown if the publisher part number isn’t associated with the publisher and product for the software model. You can either change the software model, or save the entitlement as is.

 You can edit this field in existing entitlements.

</td></tr><tr id="row_af1_3ss_mfb"><td>

Agreement type

</td><td>

Based on the agreement type that you select, downgrade rights are automatically generated.

**Note:** If you select any of the following agreement types, the status of the entitlement is Compliant even if you have unlicensed installations:

-   **Enterprise Agreement**
-   **Enterprise Enrollment**
-   **Enterprise Subscription Agreement**
-   **Enterprise Subscription Enrollment**
-   **Enterprise License Agreement \(ELA\)**
-   **Enterprise Term License Agreement \(ETLA\)**
-   **Server and Cloud Enrollment \(SCE\)**
-   **Unlimited License Agreement \(ULA\)**

</td></tr><tr id="row_cdm_jss_mfb"><td>

License type

</td><td>

The type determines whether the rights grant full access to the software or if they’re being upgraded from a previous version of the software.

 The following are the various license types:

-   Perpetual
-   Perpetual + Software Assurance
-   Software Assurance
-   Subscription
-   Step-up
-   Subscription Step-up
-   Add-on
-   From SA

**Note:** After you upgrade to the Zurich release and a content update is performed, if the content update changes the license type of a specific PPN from Step-up to Subscription Step-up, all entitlements associated with that PPN will be updated to Subscription Step-up entitlements.

 The default value for SaaS entitlements is **Subscription**.

 For more information about the license types and their impact on software reconciliation, see [Impact of different license types on software reconciliation](license-types-impact-reconciliation.md).

</td></tr><tr><td>

Metric group

</td><td>

This field is automatically populated based on the **Software Model** field. Each metric group has a set of license metrics that are specific to the software publisher.**Note:** If this field is set to **Consumption** or **Subscription**, the **License type** field is automatically set to **Subscription**.

</td></tr><tr><td>

License metric

</td><td>

License metric for the license group that the software license is counted against when reconciliation is run. The options for license metric change based on the **Metric group** field.For more information, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).

 **Note:**

-   The default value for SaaS entitlements is **User Subscription**.
-   For SaaS Consumption, the spend in the License Metric Results \(samp\_license\_metric\_result\) gets calculated for the current subscription period only, which isn't the total cost of the entitlement. For example, if the Purchased rights are 100, the Unit cost is $1, the License type is Subscription, the Subscription period is Monthly, and the Start date and End date are set to a period of 2 months, then the Total cost would be $200. But since the consumption is reconciled for the current subscription period, the spend in the License Metric Results shows as $100.

</td></tr><tr><td>

Unlimited license

</td><td>

Indicates that the entitlement being created is an unlimited license.

</td></tr><tr><td>

Subscription period

</td><td>

Billing frequency for your software subscription. The options are **Monthly**, **Quarterly**, **Annually**, and **Entire Subscription Period**. The **Entire Subscription period** option indicates that you’re required to pay only after throughout the entire duration of your subscription.If you select **Monthly**, **Quarterly**, or **Annually**, you must specify the time period during which the subscription is valid in the **Start date** and **End date** fields. If you select **Entire Subscription Period**, only the **Start date** field is required.

 This field appears only if you select **Subscription**, **Subscription Step-up**, **Add-on**, or **From SA** from the License type list.

</td></tr><tr><td>

Start date

</td><td>

Start date of your subscription, maintenance entitlement, SA service, add-on capability, or From SA service.This field appears only if you select **Subscription**, **Perpetual + Maintenance**, **Maintenance**, **Perpetual + Software Assurance**,**Software Assurance**, **Step-up**, **Subscription Step-up**, **Add-on**, or **From SA** from the License type list.

</td></tr><tr><td>

End date

</td><td>

End date of your subscription, maintenance entitlement, SA service, add-on capability, or From SA service.After the end date is reached, the maintenance flag is cleared and the state is retired if **Software Assurance** was specified as the **License type**.

 This field appears only if you select **Subscription**, **Perpetual + Maintenance**, **Maintenance**, **Perpetual + Software Assurance**,**Software Assurance**, **Step-up**, **Subscription Step-up**, **Add-on**, or **From SA** from the License type list.

</td></tr><tr><td>

Rights per license pack

</td><td>

Number of rights associated with each pack that is purchased for Microsoft products that use Per Core or Per Core with CAL licenses.For Microsoft products, the licenses are available in packs. For example, SQL server core licenses are available in packs of two.

</td></tr><tr><td>

Number of packs

</td><td>

Number of packs for Microsoft products that use Per Core or Per Core with CAL licenses.

 You can edit this field in an existing entitlement. If you change the value in this field, the **Purchased rights** field is automatically updated.

</td></tr><tr id="row_xnb_hss_mfb"><td>

Purchased rights

</td><td>

Number of rights that you’re purchasing.

 You can edit this field in an existing entitlement. If you change the value in the this field, the expense line item is automatically updated.

 **Note:** If you have specified a Microsoft Per Core or Microsoft Per Core with CAL license type, this field is automatically populated. This value is based on the value entered in the **Rights per license pack** field multiplied by the value in the **Number of packs** field.

From the Zurich release, revenue-based licensing support is enabled for this field for SAP Engine products. This support enables using higher value revenue-based SAP Engine products.

</td></tr><tr id="row_gj5_gss_mfb"><td>

Active rights

</td><td>

Number of rights to be granted for this entitlement. **Note:** If an enterprise contract is attached to the license, the **Active rights** field isn’t shown.

</td></tr><tr id="row_ktm_gss_mfb"><td>

Allocations available

</td><td>

Number of user or device allocations that haven’t been created for an entitlement.Allocations available = \(number of active rights\) - \(sum of all allocation quantities\).

</td></tr><tr><td>

Unit cost

</td><td>

Unit cost of the software. **Note:** Required for total cost and savings calculations on the [Software Asset Management dashboard.](../concept/c_SAMDashboard.md)

From the Zurich release, revenue-based licensing support is enabled for this field for SAP Engine products. This support enables using higher value revenue-based SAP Engine products.

</td></tr><tr><td>

Total cost

</td><td>

Total cost of the entitlement calculated from the unit cost.

</td></tr><tr><td>

Total units

</td><td>

Total number of software units that you’ve purchased for this entitlement.This field appears only if the **Metric group** field is set to **Consumption**.

</td></tr><tr><td>

Unrestricted consumption

</td><td>

If selected, license consumption isn't limited to the entities listed in the consumption rule. Any entity can consume rights, but the entities in the consumption rules have rights reserved for them. The reserved rights come from the license pool column.**Note:** This check box can only be selected if all existing consumption rules have a license pool. Any new consumption rule must define a pool as well.

</td></tr></tbody>
</table>## General tab

<table id="table_gy4_qpz_4hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Serial number

</td><td>

Unique number assigned for identification of the asset.

</td></tr><tr><td>

Owned by

</td><td>

User or department with financial ownership of the asset. The asset owner can be different than the manager.

</td></tr><tr><td>

State

</td><td>

Current state of the asset. Values include **On order**, **In stock**, **In transit**, **In use**, **Consumed**, **In maintenance**, **Retired**, **Missing**, and **Build**. **Note:** When you start creating an entitlement, its initial status is **Build**. After you publish the entitlement, the status changes to **In use**.

 If the state is **Retired**, the **Active rights** field is set to **0**.

 For entitlements with a **Subscription** license duration, the **State** field is automatically updated based on the **Start date** and **End date** fields.

</td></tr><tr><td>

Substate

</td><td>

More details about the software license stage. The available substate settings depend on the state selected in the **State** field. For example, if you select the Retired state, the substate options available are Disposed, Sold, Donate, and Vendor credit.

</td></tr><tr><td>

Active maintenance

</td><td>

Indicates if Subscription, SA, or maintenance is activated on the entitlement. If the entitlement has an active SA, subscription, or maintenance associated with it, the check box is automatically selected. If an entitlement initially had subscription, SA or maintenance activated on it and subscription, SA or maintenance is no longer active, the check box is automatically cleared.If you upgrade from a previous release to the Zurich release, this check box is automatically selected for your existing entitlements that have an active SA, subscription, or maintenance associated with them.

</td></tr><tr><td>

Company

</td><td>

Company that this asset belongs to.

</td></tr><tr><td>

Location

</td><td>

Where the license is used. For example, you can specify a site, country, or region.

</td></tr><tr><td>

Department

</td><td>

Department of the person **Assigned to** this software license.

</td></tr></tbody>
</table>## Financial tab

<table id="table_ic2_2qz_4hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor

</td><td>

Company that the asset was purchased from.

</td></tr><tr><td>

Invoice number

</td><td>

Invoice that the asset was billed under.

</td></tr><tr><td>

Request line

</td><td>

Request line linked to the asset.

</td></tr><tr><td>

Purchased

</td><td>

The date the entitlement was purchased. This date is considered when reconciliation runs as Microsoft has updated its licensing rules for dedicated hosts on AWS and Microsoft Azure.**Note:** The purchased date is also visible when importing entitlements.

</td></tr><tr><td>

Opened

</td><td>

Date that the request was opened.

</td></tr><tr><td>

GL account

</td><td>

General ledger account number associated with the asset.

</td></tr><tr><td>

Cost center

</td><td>

Cost center financially responsible for the asset.

</td></tr></tbody>
</table>## Contracts tab

When [importing software entitlements](../task/view-entitlement-import-errors.md), use the **Contract number** column on the downloadable template to link the contracts to the entitlements. Since the **Contract number** is a reference field, the system first searches for matches to existing contracts, so enter existing contract numbers. If no matching contract number is found, entitlement import errors are generated.

You should be able to create the contract from the error, enabling for the creation of the entitlement and the appearance of the contract on the entitlement form in the Contracts related list. You can also skip the contract creation process and still create the entitlement, but without a contract.

|Field|Description|
|-----|-----------|
|Lease contract|Contract that applies to the asset.|
|Warranty expiration|Expiration date of the warranty.|
|Support group|Group that supports incidents related to the asset.|
|Supported by|Individual that supports incidents related to the asset.|

## User Allocations tab

**Note:** This tab appears only if you’re using a user-based license metric, such as Per User or User CAL.

<table id="table_cq2_5hp_drb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned condition

</td><td>

Condition to account for only user allocations during reconciliation. Only user allocations that meet the specified conditions are included in the reconciliation.

</td></tr><tr><td>

Assigned to

</td><td>

User that the associated rights are allocated to.**Note:** If you’re using a client access record to track and manage the users that are accessing your server software, this field displays the name of each user that you assigned the associated client access licenses \(CALs\) to. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for detailed instructions on how to assign CALs to users in the Software Asset Management classic application. See [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) for detailed instructions on how to assign CALs to users in the Software Asset Workspace.

</td></tr><tr><td>

Quantity

</td><td>

Number of rights that are allocated to the user.

</td></tr><tr><td>

License key

</td><td>

Unique license key that is allocated to the user.

</td></tr><tr><td>

Group

</td><td>

Indicates the assignment group name when a user allocation is created from a group user allocation to the software entitlement. When a user allocation isn't created from a group user allocation to the software entitlement, this column value is empty.

</td></tr></tbody>
</table>## Device Allocations tab

**Note:** This tab appears only if you’re using a device-based license metric, such as Per Device or Device CAL.

<table id="table_apb_q32_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocated condition

</td><td>

Condition to account for only device allocations during reconciliation. Only device allocations that meet the specified conditions are included in reconciliation.

</td></tr><tr><td>

Assigned to

</td><td>

Device that the associated rights are allocated to.**Note:** If you’re using a client access record to track and manage the devices that are accessing your server software, this field displays the name of each device that you assigned the associated client access licenses \(CALs\) to. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for detailed instructions on how to assign CALs to devices in the Software Asset Management classic application. See [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) for detailed instructions on how to assign CALs to devices in the Software Asset Workspace.

</td></tr><tr><td>

Quantity

</td><td>

Number of rights that are allocated to the device.

</td></tr><tr><td>

License key

</td><td>

Unique license key that is allocated to the device.

</td></tr></tbody>
</table>## Related Entitlements tab

**Note:** This tab appears only if your software entitlement is linked to a related entitlement.

<table id="table_pzq_r54_4rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related Entitlement

</td><td>

Related entitlement that you want to link to your software entitlement.

</td></tr><tr><td>

License type

</td><td>

License type that is associated with the related entitlement.

</td></tr><tr><td>

Active rights

</td><td>

Number of rights that you want to grant to the related entitlement.

</td></tr><tr><td>

Software Entitlement**Note:** This field appears only in the Software Asset Workspace. This field doesn’t appear in the Software Asset Management classic application.

</td><td>

Software entitlement that you’re linking the related entitlement to.

</td></tr></tbody>
</table>## Upgraded Entitlements tab

<table id="table_ahn_xpz_4hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From Entitlement

</td><td>

The entitlement from which rights are upgrading. Multiple upgrade entitlements are supported. You can upgrade previously owned rights for a particular version of software to a newer version \(for example, Microsoft Office Professional Plus 2013 to Microsoft Office Professional Plus 2016\).

 **Note:** This field is available when **Upgrade** is selected from the **License type** field.

The rights from entitlements that you’re upgrading from get deactivated when you upgrade because they’re moved to the new entitlement.

</td></tr><tr><td>

Number of rights

</td><td>

Number of rights to upgrade.

</td></tr></tbody>
</table>## Activities tab

|Field|Description|
|-----|-----------|
|Work notes|Work notes for the asset.|

## Downgrade Rights related list

<table id="table_o1h_4cm_43b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software entitlement

</td><td>

Software entitlement with which the downgrade is associated.

</td></tr><tr><td>

Software model

</td><td>

Software model corresponding to the downgrade right.

</td></tr><tr><td>

Active

</td><td>

Indicates if the downgrade rights on the software entitlement are active or not. If needed, you can deactivate the downgrade rights. Only the active downgrade rights appear in the list. To see all the downgrade rights, remove the Active condition from the filter.If you deactivate a downgrade right on a software model, the change is propagated to the related software entitlement downgrade rights; irrespective of the source of the downgrade right.

 To deactivate a downgrade right, double-click the field to display the toggle button. Select false and select the Save icon \(![Save icon](../image/save-icon.png)\).

-   false: Deactivates the downgrade right on the software model and on the related software entitlements.
-   true: Deactivates the downgrade right on the software model and on the related software entitlements.

</td></tr><tr><td>

Order

</td><td>

Order of the downgrade. If necessary, you can edit this field.

</td></tr><tr><td>

Start date

</td><td>

Start date of the downgrade.

</td></tr><tr><td>

End date

</td><td>

End date of the downgrade.

</td></tr></tbody>
</table>## Entitlement Consumption Rules

**Note:** This tab appears for all publishers except Workday. Additionally, the tab appears for all license metrics except the following:

-   Resource Value Unit \(RVU\)
-   Resource Value Unit \(RVU\) Full Capacity
-   Resource Value Unit \(RVU\) Sub-capacity
-   Authorized User Value Unit
-   Employee User Value Unit
-   External User Value Unit
-   Employee

|Field|Description|
|-----|-----------|
|Software entitlement|The software entitlement that the consumption is linked to.|
|Consumption rule|The consumption rule linked to the entitlement.|
|License pool|License pool associated with the consumption rule. For details on license pools, see [Reconciliation of licenses across global entities](../concept/reconcile-licenses-global-entities.md).|

## License Key related list

|Field|Description|
|-----|-----------|
|Is allocated|Option that indicates that the license key has been allocated.|
|License key|License key value. Must be unique for an entitlement.|
|Software entitlement|Software entitlement associated with the license key.|

**Parent Topic:**[Software Asset Management references](references.md)

