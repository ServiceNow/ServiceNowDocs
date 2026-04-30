---
title: Windows Server cluster license optimization
description: Optimize rights used for Windows Server clustering based on costs and compliance criteria.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Software Asset Management, Software Asset Management, IT Asset Management]
---

# Windows Server cluster license optimization

Optimize rights used for Windows Server clustering based on costs and compliance criteria.

Windows Server installations are categorized into two editions - Standard and Datacenter. Windows Server Standard and Datacenter editions are licensed by physical cores. The licenses are available in packs of 2 and packs of 16. The minimum license requirements for Windows Server clustering is:

-   All physical cores must be licensed
-   8 core licenses per processor
-   16 core licenses per server

A cluster is licensed by calculating the maximum number of virtual machines \(VMs\) that can run on one physical host.

The Windows Server Standard edition is licensed for 2 operating system environments \(OSEs\) or Hyper-V containers. Additional OSEs require additional licenses \( physical server is licensed for every 2 OSEs, minimum of 16 rights\). Windows Server Datacenter edition is licensed for unlimited OSEs.

The cluster or host density is determined by dividing the active operating systems by 2. The system property **com.snc.samp.windowserver.license.threshold** with a default value of 4.59 is used for marking the host or cluster density. This property is a ratio of the cost of Datacenter and non Datacenter licenses and identifies the optimal cluster size for Datacenter licenses. You can modify the value of this property based on the purchase costs for these licenses. Low density clusters are licensed by non Datacenter licenses starting from low to high density. High density clusters are licensed by Datacenter licenses starting from high to low density. Optimal license and potential savings are generated for host or cluster using non optimal licenses.

The Windows Standard rights are used first for the Standard list by using them from the smallest to the largest within this list. After using Standard rights for low density host or cluster, the remaining low density host or cluster are licensed by the remaining Datacenter rights from high to low density. After using Datacenter rights for high density host or cluster, the remaining high density host or cluster are licensed by the remaining Standard rights from low to high density. Clusters that do not have enough Datacenter or Standard rights to consume are marked as unlicensed.

A new table, Potential savings by optimizing licenses, \[samp\_license\_optimization\_summary\] is created to store information about licensing Windows Server software installed on each device.

**Parent Topic:**[Setting up Software Asset Management](setup-sam.md)

