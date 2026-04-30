---
title: View Software Asset Management Foundation plugin software model results in classic
description: View compliance information for software model results from the Product Results list after reconciliation is run.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Software Asset Management Foundation plugin classic, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View Software Asset Management Foundation plugin software model results in classic

View compliance information for software model results from the Product Results list after reconciliation is run.

## Before you begin

Role required: sam\_user

## About this task

You can view License Metric Results, Remediation Options, and Unlicensed Installs related lists for a software model result from a Product Result record.

For example, if the status of a product result shows that it is not compliant, you can drill down on the product result to view software model details, such as the number of unlicensed installs and the true-up cost to become compliant. Further, you can drill down on the software model result to view the license metric result, which is based on the entitlements for the product.

License metric result information includes rights owned and rights used as well as the license allocation breakdown so you can determine your options to become compliant. The Remediation Options related list shows the number of rights needed and calculates the cost of those rights for you, based on the license metric.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Product Results** and open a record to view product results details.

2.  In the Software Model Results related list, open a record to view the details \(see table for field descriptions\).

<table id="table_bnb_zqv_pz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software model

</td><td>

Software model associated with the product. Drill down on the software model to see the software model result.

</td></tr><tr><td>

Product result

</td><td>

Unique product result number generated during the reconciliation process.

</td></tr><tr><td>

Latest

</td><td>

Indicates whether this software model result is from the most recent reconciliation run.

</td></tr><tr><td>

Status

</td><td>

Status of the software model.-   Compliant
-   Not Compliant


</td></tr><tr><td>

Agreement type

</td><td>

Common: Generic, Enterprise License Agreement \(ELA\)**Note:** If the agreement type is Enterprise Level Agreement, the **Status** is Compliant even if there are unlicensed installations.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Number of unlicensed software installations that are not covered by any entitlements.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the least number of rights needed \(rights needed \* average price per right from entitlements\). The lowest cost from Purchase Rights remediation options.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used. The sum of the Over Licensed amount from the True-up value costs.

</td></tr><tr><td class="sub-head" colspan="2">

License Metric Results

</td></tr><tr><td>

License metric

</td><td>

License metric that the software license is counted against when reconciliation is run.

</td></tr><tr><td>

Software model result

</td><td>

Software model with which the result is associated.

</td></tr><tr><td>

Rights owned

</td><td>

Sum of all active rights from entitlements that share a license metric.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated + not allocated and installed\).

</td></tr><tr><td>

Unused rights

</td><td>

Sum of rights not used during reconciliation \(rights owned - rights used\).

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of unused rights.

</td></tr><tr><td class="sub-head" colspan="2">

Right Allocations

</td></tr><tr><td>

Allocated in use

</td><td>

Rights that are allocated and are used to license installations.

</td></tr><tr><td>

Not allocated in use

</td><td>

Number of rights that are used to license installations, but not allocated.When this value is greater than 0, two remediation options \(Create Allocations and Remove Unallocated Installs\) are automatically created for each unique license metric in the software model that meets this requirement, except User CAL and Device CAL.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights that are allocated but are not being used to license any installations. **Note:** **Allocated not in use** reflects rights that are wasted because the user or device for which these rights have been allocated do not have the software installed.

 When this value is greater than 0, a Remove Allocations remediation option is automatically created for each unique license metric in the software model that meets this requirement.

</td></tr><tr><td>

Not allocated

</td><td>

Number of rights that have not been allocated \(rights owned - allocated regardless of whether installed or not\).

</td></tr><tr><td>

Allocations needed

</td><td>

Number of allocations needed for compliance. Only used for Per Named User and Per Named Device license metrics.

</td></tr><tr><td class="sub-head" colspan="2">

Remediation Options

</td></tr><tr><td>

Remediation action

</td><td>

Action to take to for compliance of Purchase Rights.

</td></tr><tr><td>

Affects compliance

</td><td>

Specifies whether compliance is affected by the remediation option.

</td></tr><tr><td>

License metric

</td><td>

Specific license metric of the software model result.

</td></tr><tr><td>

Software model result

</td><td>

Specific software model result pertaining to the remediation option.

</td></tr><tr><td>

Status

</td><td>

Status of the remediation option.-   New \(blue\)
-   Complete \(green\)
-   Void \(red\)
-   In Progress \(yellow\)

In Progress state indicates that removal candidates were created for the installs.

</td></tr><tr><td>

Rights needed

</td><td>

**Purchase Rights** shows Rights needed.

</td></tr><tr><td>

Actionable rights

</td><td>

Total rights affected by the action.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the least number of rights needed.

</td></tr></tbody>
</table>    The Unlicensed Installs related list contains the [software installations](../concept/c_DiscoveryModelsSAMF.md) that are unlicensed.


**Parent Topic:**[Using Software Asset Management Foundation plugin classic](../concept/using-samf-classic.md)

