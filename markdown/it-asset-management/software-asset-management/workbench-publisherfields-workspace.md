---
title: License usage publisher fields in workspace
description: Field descriptions for the related lists for publishers in the Publishers page in the License usage view.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [License usage view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# License usage publisher fields in workspace

Field descriptions for the related lists for publishers in the Publishers page in the License usage view.

## Product Results

<table id="table_hbb_p24_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique product result number that is generated during the reconciliation process.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software.

</td></tr><tr><td>

Product

</td><td>

Name of software product.

</td></tr><tr><td>

Group

</td><td>

Group to which the product result belongs.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup to which the product result belongs.

</td></tr><tr><td>

Latest

</td><td>

Indicates whether this product result is from the most recent reconciliation run.

</td></tr><tr><td>

Reconciliation result

</td><td>

Unique reconciliation result number that is generated during the reconciliation process.

</td></tr><tr><td>

Status

</td><td>

Status of the product.-   Compliant
-   Not Compliant

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the lowest number of rights needed.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used. The sum of all Over Licensed amount values from every software model result.

</td></tr><tr><td>

Potential savings

</td><td>

Estimated cost of savings if software installations are reclaimed. The sum of all potential savings from all removal candidates.

</td></tr><tr><td>

Licensed installs

</td><td>

Total number of installations that are licensed for the product.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Total number of installations that are unlicensed for the product.

</td></tr></tbody>
</table>## Software Model Results

|Field|Description|
|-----|-----------|
|Software model result|Name of the software model.|
|Status|Status of the software model.|
|Unlicensed installs|Total number of installations that are unlicensed for the associated software product.|
|True-up cost|Estimated cost of remediating non-compliance based on the lowest number of rights needed.|
|Over-licensed amount|Estimated cost of rights not being used.|
|Potential savings|Estimated cost saved if reclamation candidates are reclaimed.|

## License metric Results

|Field|Description|
|-----|-----------|
|Software model|Name of the software model|
|License metric|Name of the license metric that the software license is counted against when reconciliation runs.|
|Licenses owned|Sum of all active rights from entitlements that share a license metric.|
|Licenses required|Sum of rights that are used during reconciliation \(allocated plus not allocated and installed\).|
|Licenses available|Sum of rights that are not used during reconciliation \(rights owned minus rights used\).|
|True-up cost|Estimated cost of remediating unlicensed installations that are based on the lowest number of rights needed.|

## Entitlements

<table id="table_ddr_3j4_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the publisher.

</td></tr><tr><td>

Metric group

</td><td>

The metric group specific to the publisher.

</td></tr><tr><td>

License metric

</td><td>

The license metric for the metric group that the software license is counted against when reconciliation is run.

</td></tr><tr><td>

License type

</td><td>

The type determines whether the rights grant full access to the software or if they are being upgraded from a previous version of the software.

</td></tr><tr><td>

Active rights

</td><td>

Number of rights to be granted for this entitlement.**Note:** If an enterprise contract is attached to the license, the **Active rights** field is not shown

</td></tr><tr><td>

Purchased rights

</td><td>

Number of rights you purchased.

</td></tr><tr><td>

Total cost

</td><td>

 

</td></tr></tbody>
</table>## Removal candidates

<table id="table_zs2_lj4_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Removal candidate number.

</td></tr><tr><td>

Name

</td><td>

Name of the removal candidate.

</td></tr><tr><td>

Publisher

</td><td>

Name of the publisher.

</td></tr><tr><td>

Product

</td><td>

Name of the product.

</td></tr><tr><td>

Potential savings

</td><td>

Savings to be gained from reclaiming unused software installations.

</td></tr><tr><td>

State

</td><td>

State of the removal candidate.-   Attention Required
-   Ready
-   Awaiting User
-   Awaiting Approval
-   Approval
-   Awaiting Revocation
-   Closed Complete
-   Closed Skipped

</td></tr><tr><td>

Justification

</td><td>

Reason for becoming a removal candidate.-   Low Usage \(default\)
-   Unallocated
-   Unlicensed
-   Restricted Software

</td></tr></tbody>
</table>## Remediation options

<table id="table_lqs_cfv_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remediation action

</td><td>

Action to take for compliance.-   Purchase Rights
-   Remove Allocations
-   Create Allocations
-   Remove Unallocated Installs \(Not available for Oracle database options\)
-   Remove Unlicensed Installs \(Not available for Oracle database options\)
-   Remove Unlicensed Installs - Cloud \(available only if you have cloud installations\)

</td></tr><tr><td>

Status

</td><td>

Status of the remediation option.-   New \(blue\)
-   Complete \(green\)
-   Void \(red\)
-   In Progress \(yellow\)

In Progress state indicates that removal candidates were created for the installs.


</td></tr><tr><td>

Affects compliance

</td><td>

Specifies whether the remediation options affect compliance.

</td></tr><tr><td>

Display Name

</td><td>

Specific license metric of the software model result.

</td></tr><tr><td>

Actionable rights

</td><td>

Total rights affected by the action.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed.

</td></tr></tbody>
</table>