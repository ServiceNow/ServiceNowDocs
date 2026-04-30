---
title: Software model results license metric results fields
description: Software model results License Metric Results form and related list field descriptions. You can access this form through the License Metric Results related list in your software model results.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software model results license metric results fields

Software model results License Metric Results form and related list field descriptions. You can access this form through the License Metric Results related list in your software model results.

## License Metric Results form

Two license metric results are generated if a software model has two entitlements, one with a perpetual SA license type and the other with a subscription license type. One license metric result where active maintenance is true and the other where the active maintenance is false. In such a scenario, two license position reports are generated, one with active maintenance true and the other one with active maintenance false.

<table id="table_hg1_gtq_gnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

License metric

</td><td>

Name of the license metric that the software license is counted against when reconciliation runs.

</td></tr><tr><td>

Software model result

</td><td>

Software model result associated with the license metric results.

</td></tr><tr><td>

Group

</td><td>

Group on which reconciliation was run.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup on which reconcliation was run.

</td></tr><tr><td>

Rights owned

</td><td>

Sum of all active rights from entitlements that share a license metric.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated + not allocated and installed\).

</td></tr><tr><td>

Rights available

</td><td>

Sum of rights not used during reconciliation \(rights owned — rights used\).

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

Number of rights that are used to license installations, but not allocated.

 When this value is greater than 0, two remediation options \(Create Allocations and Remove Unallocated Installs\) are automatically created for each unique license metric in the software model that meets this requirement, except User CAL and Device CAL.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights that are allocated but are not being used to license any installations.

 **Note:** **Allocated not in use** reflects rights that are wasted because the user or device for which these rights have been allocated do not have the software installed.

 When this value is greater than 0, a Remove Allocations remediation option is automatically created for each unique license metric in the software model that meets this requirement.

</td></tr><tr><td>

Not allocated

</td><td>

Number of rights that have not been allocated \(rights owned — allocated regardless of whether installed or not\).

</td></tr><tr><td>

Allocations needed

</td><td>

Number of allocations needed for compliance. Only used for Per Named User and Per Named Device license metrics.

</td></tr></tbody>
</table>## Rights Used By related list

<table id="table_ckc_5tq_gnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Used by

</td><td>

User or device that is using the rights.**Note:** If your rights are associated with client access records, the **Used by** field displays the name of each client access record that is using those rights. Select a client access record name to view the corresponding breakdown of users or devices that are using the associated rights. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for more information on client access records in the Software Asset Management classic application. See [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) for more information on client access records in the Software Asset Workspace.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated + not allocated and installed\).

</td></tr><tr><td>

Allocated in use

</td><td>

Rights that are allocated and are used to license installations.

</td></tr><tr><td>

Not allocated in use

</td><td>

Number of rights that are used to license installations, but not allocated.

 When this value is greater than 0, two remediation options \(Create Allocations and Remove Unallocated Installs\) are automatically created for each unique license metric in the software model that meets this requirement, except User CAL and Device CAL.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights that are allocated but are not being used to license any installations.

 **Note:** **Allocated not in use** reflects rights that are wasted because the user or device for which these rights have been allocated do not have the software installed.

 When this value is greater than 0, a Remove Allocations remediation option is automatically created for each unique license metric in the software model that meets this requirement.

</td></tr><tr><td>

Nontransferable rights

</td><td>

Remaining rights from a core pack that cannot be used to license any additional devices. Nontransferable rights are available only for Microsoft Per Core and Microsoft Per Core with \(CAL\).

</td></tr><tr><td>

Allocations needed

</td><td>

Number of allocations needed for compliance. Only used for Per Named User and Per Named Device license metrics.

</td></tr></tbody>
</table>## Rights Needed By related list

<table id="table_d2r_gr2_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rights needed by

</td><td>

Unlicensed user or device that requires rights.**Note:** If rights are needed to cover unlicensed users or devices in an associated client access record, the **Rights needed** field displays the name of the client access record that requires those additional rights. Select the client access record name to view the corresponding breakdown of unlicensed users or devices that require rights. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for more information on client access records in the Software Asset Management classic application. See [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) for more information on client access records in the Software Asset Workspace.

</td></tr><tr><td>

Rights needed

</td><td>

Number of rights that are required to cover the unlicensed user or device.

</td></tr></tbody>
</table>## Licensed Installs related list

**Note:** This related list is not available for SAP license metrics.

|Field|Description|
|-----|-----------|
|Display name|Name of the software installation.|
|Publisher|Publisher of the software.|
|Version|Version of the software.|
|Discovery model|Software discovery model for the installed software.|
|Installed on|Hardware on which the software is installed.|
|Assigned to|User or device to which the software is assigned.|

## Downgrades/Upgrades related list

**Note:** This related list is not available for SAP license metrics.

<table id="table_phw_ytq_gnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software model

</td><td>

Software model that is available for upgrade or downgrade.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated + not allocated and installed\).

</td></tr><tr><td>

Allocated in use

</td><td>

Rights that are allocated and are used to license installations.

</td></tr><tr><td>

Not allocated in use

</td><td>

Number of rights that are used to license installations, but not allocated.

 When this value is greater than 0, two remediation options \(Create Allocations and Remove Unallocated Installs\) are automatically created for each unique license metric in the software model that meets this requirement, except User CAL and Device CAL.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights that are allocated but are not being used to license any installations.

 **Note:** **Allocated not in use** reflects rights that are wasted because the user or device for which these rights have been allocated do not have the software installed.

 When this value is greater than 0, a Remove Allocations remediation option is automatically created for each unique license metric in the software model that meets this requirement.

</td></tr><tr><td>

Allocations needed

</td><td>

Number of allocations needed for compliance. Only used for Per Named User and Per Named Device license metrics.

</td></tr></tbody>
</table>## SAP System Users related list

**Note:** This related list is available only for SAP named user license metrics.

|Field|Description|
|-----|-----------|
|Display name|Identifier containing the SAP user ID and SAP client.|
|User|Full name of the SAP user.|
|SAP user id|Unique identifier for the SAP user.|
|Email|Email address of the SAP user.|
|First name|First name of the SAP user.|
|Last name|Last name of the SAP user.|
|User type|Type of SAP user.|
|License type|Named user type value assigned to the SAP user.|
|Named user type|Normalized named user type of the SAP user.|
|Optimized named user type|Optimized named user type of the SAP user.|
|SAP client|Organizational subunit to which the SAP user belongs.|

## Licensed Subscriptions related list

|Field|Description|
|-----|-----------|
|Display name|Identifier containing the publisher and product of the software subscription.|
|User|Name of the subscription user.|
|User principal name|Email address of the subscription user.|
|Software model|Software model for the subscription software.|
|Subscription profile|Direct integration profile for the subscription software.|
|Subscription type|Type of subscription.|

**Parent Topic:**[Software Asset Management references](references.md)

