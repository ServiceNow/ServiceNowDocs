---
title: Software license usage
description: Review reconciliation results in a simplified workbench view.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Software license usage

Review reconciliation results in a simplified workbench view.

The License Workbench lets you forecast the needs of your organization by trending the number of rights consumed against the number of active rights purchased. You can stay in compliance by purchasing additional rights before software consumption surpasses the number of rights owned.

Workbench features include:

-   Color-coded compliance banner
-   Financial calculations on card
-   Publisher pinning functionality \(user specific, saved\)
-   Sort card functionality
-   Active filtering
-   Card drill down to Product Results list
-   Keyboard control
-   Group and subgroup reconciliation information, if applicable

![License Workbench showing all publishers, publishers out of compliance, and pinned publishers in different tabs.](../image/license-workbench.png "License workbench")

Pinned publishers are listed in the **Pinned Publishers** tab. The list of pinned publishers is saved on a per-user basis.![Pin Publisher icon pins a publisher that appears in the Pinned Publishers tab.](../image/sam-pin-publisher.png)

|Tab|Description|
|---|-----------|
|All Publishers|List of all publishers.|
|Publishers Out of Compliance|List of all publishers where status is not compliant.|
|Pinned Publishers|User-specific saved list of publishers that have been grouped.|

## Publisher workbench navigation tree

Drill down on a specific publisher, product, software model, or license metric in the workbench navigation tree to view the calculation and compliance information from the latest reconciliation results.

The navigation tree features are:

-   Filter products \(active filtering, including collapsed items\)
-   Compliance toggle switch
-   Expand and collapse tree links
-   Software model compliance icons

![Publisher Workbench navigation tree showing publishers and their product results](../image/software-model-results.png)

By default, the navigation tree on the publisher license overview page is collapsed. When expanded, it's grouped by publisher.

Publisher: Product Results related lists:

-   [Software Model Results](../task/t_ViewSWModelResults.md)
-   Licensed Installs
-   Unlicensed Installs \(SAP: Unlicensed Users or Unlicensed Engines\)
-   Unlicensed Subscriptions \(Subscription-based software\)
-   Removal Candidates

Software Model Results related lists:

-   License Metric Results
-   Remediation Options: The **Rights Needed By** tab is not visible for the Resource Value Unit \(RVU\) IBM license metric. Rights are not used by individual devices, as the Resource Value Unit \(RVU\) license metric is licensed at the product level.

    **Note:** For more details on the remediation options, see [View software model results](../task/t_ViewSWModelResults.md).

-   Licensed Installs
-   Unlicensed Installs \(SAP: Unlicensed Users\)
-   Unlicensed Subscriptions \(Subscription-based software\)
-   Unlicensed Consumptions \(Consumption-based software models\)
-   Unlicensed Options \(Oracle only\)
-   Removal Candidates
-   Purchase Orders \(only when the Procurement \(com.snc.procurement\) plugin is active\)

License Metric Results related list:

-   Rights Used By: Not visible for the Resource Value Unit \(RVU\) IBM license metric. The Resource Value Unit \(RVU\) license metric is licensed at the product level; it is calculated based on the total consumption of the product in your enterprise.

    **Note:** Four additional fields are visible in the Rights Used By related list if you have cloud installations.

-   Licensed Installs
-   Installs Used \(SAP: System Users\)
-   Downgrades/Upgrades
-   Licensed Subscriptions
-   Cloud Special Rights: This tab is available only if you have cloud installations on cloud platforms such as AWS or Azure. This tab is a subset of the Rights Used By tab and displays fields pertaining to cloud installations. For detailed descriptions on the Cloud Special Rights fields, refer to the Rights Used By tab.

<table id="table_ghv_rwz_rfb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Publisher, product, software model

</td></tr><tr><td>

Total Spend

</td><td>

Total cost of rights owned.

</td></tr><tr><td>

True-up Cost

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed \(rights needed multiplied by average price per right from entitlements\).The lowest cost from Purchase Rights remediation options.

</td></tr><tr><td>

Over-licensed Amount

</td><td>

Estimated cost of rights not being used. The sum of the Over Licensed amount from the True-up value costs.

</td></tr><tr><td>

Potential Savings

</td><td>

Cost saved if removal candidates are reclaimed.

</td></tr><tr><td>

Agreement Type

</td><td>

Software license type.

</td></tr><tr><td class="sub-head" colspan="2">

License Metric results

</td></tr><tr><td>

Display name

</td><td>

Name of the license metric that the software license is counted against when reconciliation runs.

</td></tr><tr><td>

Rights owned

</td><td>

Sum of all active rights from entitlements that share a license metric.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights that are used during reconciliation \(allocated plus not allocated and installed\).

</td></tr><tr><td>

Rights available

</td><td>

Sum of rights that are not used during reconciliation \(rights owned minus rights used\).

</td></tr><tr><td>

Legacy license**Note:** This field appears only if your environment has dedicated hosts on AWS or on Azure.

</td><td>

Indicates licenses purchased before 1 Oct 2019.​ **Note:** Microsoft has updated licensing rules for dedicated hosts based on the purchase date.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of unused rights.

</td></tr><tr><td>

Right allocations

</td><td>

-   Allocated in use
-   Not allocated in use
-   Allocated not in use
-   Not allocated
-   Allocations needed

 **Note:** For Microsoft Per Core and Microsoft Per Core with \(CAL\), you can have non-transferable rights. Non-transferable rights are any remaining rights from a core pack that cannot be used to license any additional devices.

</td></tr><tr><td>

Rights needed**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Number of rights that are required to cover unlicensed installations.

</td></tr><tr><td>

Unlicensed installs**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed software installations that are not covered by any entitlements.

</td></tr><tr><td>

Unlicensed SAP users \(SAP only\)**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed SAP users that are not covered by any entitlements.

</td></tr><tr><td>

Unlicensed options \(Oracle only\)**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed Oracle database options that are not covered by any entitlements.

</td></tr><tr><td>

Unlicensed subscriptions**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed software subscriptions that are not covered by any entitlements.

</td></tr><tr><td>

True-up cost**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list icon.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Estimated cost of remediating unlicensed installations that are based on the lowest number of rights needed.

</td></tr><tr><td>

Potential savings**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list.](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Estimated cost saved by reclaiming removal candidates.

</td></tr><tr><td>

Downgrade rights**Note:** This field is hidden by default. Select the personalize list icon \(![Personalize list](../image/gear-icon.png)\) to modify the fields that appear in the License Metric Results.

</td><td>

Previous software versions that you can license using software entitlements for the latest software version.

</td></tr></tbody>
</table>## Rights Used By

<table id="table_ckc_5tq_gnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Used by

</td><td>

User or device using the rights.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated + not allocated and installed\).

</td></tr><tr><td>

Cloud Provider

</td><td>

Name of the cloud provider.**Note:** This field appears only if you have cloud installations on AWS or Azure.

</td></tr><tr><td>

Dual Use Rights Applied

</td><td>

Indicates if the concurrent rights provided by Microsoft Azure that allows simultaneous usage of rights on-premise and on cloud is applied or not. **Note:** This field appears only if you have cloud installations on AWS or Azure.

</td></tr><tr><td>

Host Type

</td><td>

Type of host on the cloud: shared or dedicated. **Note:** This field appears only if you have cloud installations on AWS or Azure.

</td></tr><tr><td>

Edition Flexibility Applied

</td><td>

Indicates if the edition flexibility benefits provided by Microsoft Azure for Windows Server and SQL Server is applied or not.

**Note:** For details on the edition flexibility benefits, refer to [Licensing rules for BYOL and BYOS](../reference/byol-license-rules.md).

 This field appears only if you have cloud installations on AWS or Azure.

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
</table>-   **[Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md)**  
Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in your environment on demand.
-   **[View software model results](../task/t_ViewSWModelResults.md)**  
View compliance information for software model results from the Product Results list after reconciliation is run.
-   **[Add a software removal candidate in Software Asset Management classic](../task/t_AddAReclCandidate.md)**  
Removal candidates reclaim software resources in your environment. They are created from reclamation rules, or can be created manually.
-   **[Reconciliation and product results](../reference/Recon-swmodelresults-classic.md)**  
Field descriptions for the reconciliation results, product results, and software product results.

**Parent Topic:**[Using Software Asset Management classic](using-sam-classic.md)

