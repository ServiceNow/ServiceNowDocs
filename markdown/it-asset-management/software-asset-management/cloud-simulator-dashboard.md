---
title: Cloud simulator dashboard
description: Compare and evaluate the estimated costs of migrating your on-premises resources to the cloud for each cloud environment.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software asset analytics view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Cloud simulator dashboard

Compare and evaluate the estimated costs of migrating your on-premises resources to the cloud for each cloud environment.

Access the Cloud cost simulator dashboard by navigating to **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Cloud cost simulator**.

![Cloud cost simulator dashboard.](../image/cloud-cost-dboard.png "Cloud cost simulator dashboard")

Use filters on your on-premises resources to specify a criteria for receiving cost recommendations for cloud migration.

-   Software
-   Cluster
-   Hardware EOL
-   Software EOL
-   Low utilization
-   Show all matched VMs

**Note:** You can also use the Optimization and savings dashboard to view recommendations without a filter.

The recommendations are listed based on the criteria you specified. Virtual machine records that meet the criteria you specified are listed. In addition to the on-premises cost listed for each virtual machine, the Software Asset Management application automatically lists the most optimal price match for the corresponding virtual machines on cloud: AWS and Microsoft Azure.

You can view the total cost of all the on-premises records as well as compare the individual cost for AWS and Microsoft Azure in the Compare cost estimates section.

Once you decide on the cloud environment that you want to migrate to, click **Change Request** to initiate your cloud migration request.

<table id="table_lyc_fvs_gtb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Capex cost

</td><td>

Calculated hardware cost after including depreciation

</td></tr><tr><td>

Opex cost per month

</td><td>

Calculated from software entitlements: Windows Server, SQL Server, software assurance, and extended security updates costs. Also calculated from configuration item \(CI\) rate cards that are created by the user.

</td></tr><tr><td>

Without BYOL benefits per month

</td><td>

Cost of the instance \(compute cost, OS cost, and software cost\) plus storage cost​.

</td></tr><tr><td>

With BYOL benefits per month

</td><td>

Cost of the instance cost \(compute Cost\) plus storage cost.​

</td></tr><tr><td>

Potential savings

</td><td>

Total savings if all recommendations are applied.

</td></tr><tr><td>

Matched

</td><td>

Number of virtual machines on the cloud that match the on-premises virtual machines.

</td></tr><tr><td>

Unmatched

</td><td>

Number of virtual machines on the cloud that don't match the on-premises virtual machines.

</td></tr></tbody>
</table>