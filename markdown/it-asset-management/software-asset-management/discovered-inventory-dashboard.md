---
title: Discovered inventory dashboard
description: View your licensable discovered software and devices on the Discovered inventory dashboard in the Software asset analytics view of Software Asset Workspace.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software asset analytics view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Discovered inventory dashboard

View your licensable discovered software and devices on the Discovered inventory dashboard in the Software asset analytics view of Software Asset Workspace.

Discovered inventory dashboard enables you to view all your licensable discovered software and devices. This dashboard also provides an insight into software products with multiple and potentially older versions that can result in security and compliance risk.

You can filter the count of installations based on a publisher or product. Select any report to see more information on software installations.

You can access the Discovered inventory dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Discovered inventory**.

![Discovered inventory dashboard view](../image/discovered-inventory-workspace.png "Discovered inventory dashboard")

<table id="table_eqb_mjt_s1c"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software installation count

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Number of normalized and not normalized installs. For more information on normalized installations, see [Normalization statuses](../reference/normalization-status.md).

</td></tr><tr><td>

Software installations by discovery sources

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Total number of software installations grouped by discovery sources.

</td></tr><tr><td>

Highest number of software installations

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

The highest number of software installations for different products or publishers. You can view the count of installations by publisher or product.

</td></tr><tr><td>

Install deployment by environment type

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Number of software deployments grouped by the type of environment.

</td></tr><tr><td>

Installation across hybrid infrastructure

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Number of installations grouped by the type of infrastructure.

</td></tr><tr><td>

Cloud installations by license type

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Number of cloud installations grouped by license type.

</td></tr><tr><td>

Server count

</td><td>

Server \[cmdb\_ci\_server\]

</td><td>

Number of discovered servers.

</td></tr><tr><td>

Cluster count

</td><td>

Cluster \[cmdb\_ci\_cluster\]

 Windows Cluster \[cmdb\_ci\_win\_cluster\]

 UNIX Cluster \[cmdb\_ci\_unix\_cluster\]

 VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]

 Hyper-V Cluster \[cmdb\_ci\_hyper\_v\_cluster\]

 Nutanix Cluster \[cmdb\_ci\_nutanix\_cluster\]

</td><td>

Number of discovered clusters.

</td></tr><tr><td>

Client device count

</td><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Number of discovered computers.

</td></tr><tr><td>

Container count

</td><td>

Docker Container\[cmdb\_ci\_docker\_container\]

</td><td>

Number of discovered Docker containers.

</td></tr><tr><td>

Products with highest number of versions

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Software products with the highest number of versions in descending order.

</td></tr></tbody>
</table>