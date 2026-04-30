---
title: Create a Software Asset Management Foundation plugin entitlement in classic
description: Software entitlements enable you to define license details that are matched to software models.
locale: en-US
release: xanadu
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Configuring Software Asset Management Foundation plugin classic, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a Software Asset Management Foundation plugin entitlement in classic

Software entitlements enable you to define license details that are matched to software models.

## Before you begin

Role required: sam\_user

## About this task

Software entitlements are stored in the Software Entitlement \[alm\_license\] table.

**Note:** Entitlements are assigned to [Create a Software Asset Management Foundation plugin software model in classic](t_AddASoftwareModelSAMF.md), which are different than software discovery models.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Software Entitlements** and create a new record \(see table for field descriptions\).

<table id="table_zql_nkm_11b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Automatically generated name based on asset tag and model.

</td></tr><tr><td>

Asset tag

</td><td>

Specify the serial number and the bar code for tracking the asset.

</td></tr><tr><td>

Software model

</td><td>

Select the software model to match the entitlement.

</td></tr><tr><td>

License type

</td><td>

Specify the license type. Whether the rights grant full access to the software or if they are being upgraded from a previous version of the software.-   Full: The rights grant full access to the software.
-   Upgrade: The rights are being upgraded from a previous version of the software.

When upgrade is selected, the Upgraded Entitlements related list is shown, which is used to specify the entitlements you are upgrading from.

 This field becomes read-only after the form has been submitted.

</td></tr><tr><td>

License duration

</td><td>

Length of time the license is valid. Default value is Perpetual.-   Perpetual: Duration is continuous.
-   Subscription: Duration is for a specified length of time.

Duration dates:

    -   Start date: Required.
    -   End date: If empty, subscription does not expire.
State is automatically set to In Use when current date is between start and end dates.

State is automatically set to Retired when current date is past the end date and active rights is 0.

State is automatically set to On Order when the start date is in the future and active rights is 0.

</td></tr><tr><td>

Metric group

</td><td>

Select the metric group for the software. Each metric group has a set of license metrics that are specific to the publisher. -   Common
-   [Add a custom license metric](https://www.servicenow.com/docs/access?context=add-custom-license-metric&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)


</td></tr><tr><td>

License metric

</td><td>

Select the license metric for the license group that the software license is counted against when reconciliation is run. Point to the reference field icon to view the license calculation.

 -   Common:
    -   Per Device: Licenses a device for a number of installations of software.
    -   Per Named Device: Licenses a specific device for a number of installations of software.
    -   Per Named User: Licenses a specific user for a number of installations of software.
    -   Per User: Licenses a user for a number of installations of software.
-   Custom:

[Custom license metrics](add-custom-license-metric-samf.md) configured, if any.

</td></tr><tr><td>

Agreement type

</td><td>

Select the agreement type.-   Generic
-   Enterprise Level Agreement \(ELA\)


</td></tr><tr><td>

Purchased rights

</td><td>

Specify the number of rights that you are purchasing.The number of purchased rights for the new entitlement gets set in the **Active rights** field.

</td></tr><tr><td>

Active rights

</td><td>

\[Read-only\] Specifies the number of entitlements to be granted for this license. **Note:** If an enterprise contract is attached to the license, the **Active rights** field is not shown.

</td></tr><tr><td>

Allocations available

</td><td>

\[Read-only\] Specifies the number of user or device allocations that have not been created for an entitlement.Allocations available = \(number of active rights\) - \(sum of all allocation quantities\)

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Serial number

</td><td>

Unique number assigned for identification of the asset.

</td></tr><tr><td>

Owned by

</td><td>

User or department with financial ownership of the asset. Can be different than the manager.

</td></tr><tr><td>

State

</td><td>

Current state of the asset. Values include On order, In stock, In transit, In use, Consumed, In maintenance, Retired, and Missing.If the state is Retired, the **Active rights** field is set to 0.

</td></tr><tr><td>

Substate

</td><td>

More details about the software license stage. The available substate settings depend on the **State** selected. For example, if you select the **Retired** state, the substate options available are **Disposed**, **Sold**, **Donated**, and **Vendor credit**.

</td></tr><tr><td>

Company

</td><td>

Company to which this asset belongs.

</td></tr><tr><td>

Location

</td><td>

Where the license is used. For example, a specific site, country, or region.

</td></tr><tr><td>

Department

</td><td>

Department of the person **Assigned to** this software license.

</td></tr><tr><td class="sub-head" colspan="2">

Financial

</td></tr><tr><td>

Cost

</td><td>

Cost of the software. **Note:** Required for total cost and savings calculations on the [Software Asset Management Foundation dashboard](../concept/c_SAMDashboardSAMF.md).

</td></tr><tr><td class="sub-head" colspan="2">

Upgraded Entitlements

</td></tr><tr><td>

From Entitlement

</td><td>

The entitlement from which rights are upgrading. Multiple upgrade entitlements are supported. You can upgrade previously owned rights for a particular version of software to a newer version \(for example, Office Professional Plus 2013 to Office Professional Plus 2016\).

 **Note:** This field is shown only when the License type is Upgrade.

The rights from entitlements that you are upgrading from get deactivated when you upgrade because they are moved to the new entitlement.

</td></tr><tr><td>

Number of rights

</td><td>

Number of rights to upgrade.

</td></tr></tbody>
</table>    The Contracts related list contains contract details.

    The User or Device Allocations related list contains entitlement [allocations](t_AddAnEntitlementAllocationSAMF.md).

    **Note:** This related list is only shown when the **License Metric** field is Per User or Per Device.

    The Activities related list contains work notes for the asset.

2.  To perform additional configuration, select the new software entitlement record in the Software Entitlements list.

    1.  To set upgrade and downgrade entitlements, in the Downgrades/Upgrades related list, create a new record to specify which software models to which you have upgrade or downgrade rights \(see table for field descriptions\).

        This allows you to set entitlement to previous or future versions of software \(for example, the purchase of Office Professional Plus 2016 rights entitles you to Office Professional Plus 2013 as well\).

        |Field|Description|
        |-----|-----------|
        |Software entitlement|Software entitlement with which the upgrade/downgrade is associated.|
        |Software model|Software model of the entitlement.|
        |Order|Order of the upgrade/downgrade.|
        |Start date|Start date of the upgrade/downgrade.|
        |End date|End date of the upgrade/downgrade.|

    2.  To set up cost-tracking details, configure [Expense Lines](../../asset-and-configuration/concept/c_ExpenseLine.md).

    3.  To manage license keys, in the License Keys related list, create a new record to specify the licenses keys allocated to entitlements \(see table for field descriptions\).

        |Field|Description|
        |-----|-----------|
        |Is allocated|Check box indicating that the license key has been allocated.|
        |License key|License key value. Must be unique per entitlement.|
        |Software entitlement|Software entitlement associated with the license key.|


-   **[Create a Software Asset Management Foundation plugin entitlement allocation in classic](t_AddAnEntitlementAllocationSAMF.md)**  
A user or device allocation can be added to a software entitlement to specify a user or device to which rights have been allocated.

**Parent Topic:**[Configuring Software Asset Management Foundation plugin classic](../concept/samf-plugin-configuration.md)

