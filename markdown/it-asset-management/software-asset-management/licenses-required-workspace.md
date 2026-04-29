---
title: View calculations for your licenses in workspace
description: Evaluate the license compliance of software applications by viewing the details for all required licenses through the Software Asset Workspace License usage view.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View calculations for your licenses in workspace

Evaluate the license compliance of software applications by viewing the details for all required licenses through the Software Asset Workspace License usage view.

## Before you begin

Role required: sam\_admin and sam\_user

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License usage**.

2.  View the summary of a software model by selecting a publisher from the left pane.

3.  View the number of licenses purchased and required by selecting the **License Metric Results** tab.

    For more information about the fields in the License Metric Results tab, see the License metric results table in [License usage publisher fields in workspace](../reference/workbench-publisherfields-workspace.md).

4.  View the details about the required licenses by selecting a value for a configuration item under the **License required** column.

    ![Details of a configuration item.](../image/licenses-required-by.png)

<table id="table_mcl_jpt_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required by \(Device\)

</td><td>

Name of the configuration item such as server, cluster, which consumes the licenses.The **Required by \(Device\)** field is replaced by the **Required by \(SAP Cloud use type\)** field when the publisher selected is SAP and the product is SAP S/4HANA.

</td></tr><tr><td>

Cluster

</td><td>

-   If the configuration item is part of any cluster, the cluster name displays.
-   If the configuration item is not part of any cluster, the value is empty.


</td></tr><tr><td>

Assigned to

</td><td>

Name of the user assigned to that particular configuration item.

</td></tr><tr><td>

Licenses required

</td><td>

Sum of rights that the configuration item \(allocated, not allocated, and installed\) uses.

</td></tr><tr><td>

Licensing status

</td><td>

Indicates whether the configuration item is licensed or not licensed.

</td></tr><tr><td>

Is Virtual

</td><td>

Indicates whether the configuration item is a virtual or physical host.

</td></tr></tbody>
</table>5.  View all the downgrades being used by the license.

    This related list only appears if the specified license is used by a downgrade version of the software. If a downgrade is not using any rights, that downgrade doesn't appear in this related list.

    |Field|Description|
    |-----|-----------|
    |Software model|Name of the software model.|
    |Rights used|Number of rights used by the license.|
    |Install count|The number of installations being used for the software model for the specified license.|

6.  In the Licenses Required By related list, view the details of required licenses by selecting the value for a device under the **License required** column.

    ![Licenses required](../image/license-consumption-explanation.png)

<table id="table_k2j_5tt_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Licenses required by

</td><td>

The cluster for which the calculations are shown.

</td></tr><tr><td>

Total \# of licenses required

</td><td>

The total number of licenses consumed or required.

</td></tr><tr><td>

Licensing status

</td><td>

Shows the status of licenses. **Licensed** implies that all rights were used. **Not Licensed** implies that rights are required.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights allocated on the cluster but are unused to license any installations. The value 0 implies that there are no allocations on the cluster. **Note:** **Allocated not in use** are the rights that are wasted because the user or device for which these rights have been allocated does not have the software installed.

</td></tr><tr><td>

Not allocated in use

</td><td>

Number of rights for license installations, but not allocated.

</td></tr><tr><td>

Level 1 Relationships

</td><td>

Relationship of hosts to the current configuration item. **Note:** Appears only for server-based calculators.

</td></tr><tr><td>

Dependency View

</td><td>

Graphically displays an infrastructure view for a configuration item.

</td></tr><tr><td>

License Metric

</td><td>

Detailed explanation of the license metric.

</td></tr><tr><td>

License Consumption Explanation

</td><td>

A detailed license consumption summary post reconciliation. The summary gives you a thorough understanding of how your license rights are used, the methodology behind license calculations, and the reasoning for the consumption process.

</td></tr></tbody>
</table>7.  View the infrastructure of a configuration item and the metric attributes applied by selecting the **License consumption breakdown** tab.

    For more information on the license calculation for CrowdStrike products, see [License usage breakdown for CrowdStrike products](../reference/license-usage-crowdstrike.md).

    ![License consumption breakdown of a configuration item.](../image/license-consumption-breakdown.png)

    |Fields|Description|
    |------|-----------|
    |Required by|Name of the configuration item that consumes the rights.|
    |Processors|Number of processors on this configuration item.|
    |Cores|Numbers of cores in this processor.|
    |Licensable cores|Number of core licenses required to license this configuration item.|
    |Licenses required|Number of licenses required to license this configuration item.|
    |Metric attributes applied|Software products from publishers such as Microsoft require a minimum number of licenses to be assigned. For example, Microsoft SQL Server requires a minimum of 4 core licenses for each processor on a server. Metric attributes auto-assign these licenses.|

8.  View the details of the installations covered by licensing related to the configuration item by selecting **Software installs licensing details**.

    ![Licensing details of configuration items.](../image/software-installs-licensing-details.png)

    |Field|Description|
    |-----|-----------|
    |Normalized display name|The normalized display name of a software product.|
    |Discovery model|Normalizes the software you own by analyzing and classifying models to reduce duplication.|
    |Installed on|Configuration item on which the software is installed.|
    |Assigned to|Name of the user assigned to this configuration item.|
    |Unlicensed install|Indicates whether the install is licensed or unlicensed.|

    1.  View the licensing status of an install on various hosts within a cluster by selecting a normalized display name for Per Core and Per Core \(with CAL\) license metrics.

        ![Licensing status of the software install on various hosts within a cluster.](../image/normalized-display-name.png)

9.  Check the accuracy of the license consumption and view the host affinity rules configured for a cluster by selecting the **Host affinity rules** tab.

    Host affinity rules can be configured for SQL Server and Windows Server Standard while determining license consumption. This helps to optimize the number of licenses required and significantly minimizes the number of licenses required resulting in cost savings.

    ![Host affinity rules configured for a cluster.](../image/Host-affinity-rules.png)

    |Field|Description|
    |-----|-----------|
    |Name|Name of the rule configured for the cluster.|
    |Active|Indicates whether the configured rule is active or inactive.|
    |Cluster|Name of the cluster where the host affinity rule is configured.|
    |VM Group|Name of the group of virtual machines.|
    |Host Group|Name of the group of hosts.|
    |Mandatory|Indicates whether the configured rule is required.|
    |Affinity|Indicates whether the virtual machines live on a host group.|

10. View the suite components for the software model.

    This tab appears only if the software model is a suite.

    |Field|Description|
    |-----|-----------|
    |Suite parent|The parent suites to which the software is assigned. For example, the parent suite for several common Microsoft products is a version of Microsoft Office.|
    |Suite child|The child product or products of the suite.For example, For example, Microsoft Word and Microsoft Excel are child products of Microsoft Office.|
    |Mandatory|Requirement of a suite component. A suite component can be Optional, Always Mandatory, or Mandatory Group.|


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

