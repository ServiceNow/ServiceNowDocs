---
title: Microsoft cost-based licensing optimization example
description: This example demonstrates how a software asset manager can optimize Microsoft SQL Server licensing in a cluster deployment.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cost-based licensing optimization for Microsoft, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft cost-based licensing optimization example

This example demonstrates how a software asset manager can optimize Microsoft SQL Server licensing in a cluster deployment.

In this example, a software asset manager is managing the following Microsoft SQL Server entitlements:

|Entitlement Name|License Type|Number of Purchased Rights|Cost Per Core|
|----------------|------------|--------------------------|-------------|
|SQL Server Enterprise Licenses|SQL Server 2019 Enterprise Core with Software Assurance|1800|$5000|
|SQL Server Standard Licenses|SQL Server 2019 Standard Core with Software Assurance|600|$1300|

The following infrastructure is a VMware cluster that consists of three physical hosts. Each physical host contains virtual machines \(VMs\) that are running various versions and editions of Microsoft SQL Server. These VMs may potentially be moving across all physical hosts within the cluster.

![Microsoft SQL Server cluster infrastructure](../image/mmasset0021885-microsoft-sql-server-cluster-example.svg)

Based on the available entitlements and the cluster infrastructure, the software asset manager can license the cluster using one of the following options:

<table id="table_lk1_x5v_zbc"><thead><tr><th>

Option Number

</th><th>

License Type

</th><th>

Licensing Layer

</th><th>

Number of Rights Required on Each Host or VM

</th><th>

Total Number of Required Rights

</th><th>

Total Approximated Cost

</th></tr></thead><tbody><tr><td>

1

</td><td>

SQL Server 2019 Enterprise Core with Software Assurance

</td><td>

Physical host layer

</td><td>

-   Host 1: 12 rights
-   Host 2: 16 rights
-   Host 3: 24 rights

</td><td>

12 rights \(Host 1\) + 16 rights \(Host 2\) + 24 rights \(Host 3\) = 52 rights total

</td><td>

52 rights X $5000 = $260,000

</td></tr><tr><td>

2

</td><td>

SQL Server 2019 Enterprise Core with Software Assurance

</td><td>

Virtual layer

</td><td>

-   VM-1: 4 rights
-   VM-2: 4 rights
-   VM-3: 4 rights
-   VM-4: 4 rights
-   VM-5: 4 rights
-   VM-6: 4 rights
-   VM-7: 4 rights
-   VM-8: 4 rights
-   VM-9: 4 rights
-   VM-10: 8 rights
-   VM-11: 8 rights

</td><td>

4 rights \(VM-1\) + 4 rights \(VM-2\) + 4 rights \(VM-3\) + 4 rights \(VM-4\) + 4 rights \(VM-5\) + 4 rights \(VM-6\) + 4 rights \(VM-7\) + 4 rights \(VM-8\) + 4 rights \(VM-9\) + 8 rights \(VM-10\) + 8 rights \(VM-11\) = 52 rights total

</td><td>

52 rights X $5000 = $260,000

</td></tr><tr><td>

3

</td><td>

Both SQL Server 2019 Enterprise Core with Software Assurance and SQL Server 2019 Standard Core with Software Assurance

</td><td>

Virtual layer

</td><td>

-   SQL Server 2019 Enterprise Core with Software Assurance:
    -   VM-1: 4 rights
    -   VM-9: 4 rights
    -   VM-10: 8 rights
    -   VM-11: 8 rights
-   SQL Server 2019 Standard Core with Software Assurance:
    -   VM-2: 4 rights
    -   VM-3: 4 rights
    -   VM-4: 4 rights
    -   VM-5: 4 rights
    -   VM-6: 4 rights
    -   VM-7: 4 rights
    -   VM-8: 4 rights

</td><td>

-   SQL Server 2019 Enterprise Core with Software Assurance:

4 rights \(VM-1\) + 4 rights \(VM-9\) + 8 rights \(VM-10\) + 8 rights \(VM-11\) = 24 rights total

-   SQL Server 2019 Standard Core with Software Assurance:

4 rights \(VM-2\) + 4 rights \(VM-3\) + 4 rights \(VM-4\) + 4 rights \(VM-5\) + 4 rights \(VM-6\) + 4 rights \(VM-7\) + 4 rights \(VM-8\) = 28 rights total


</td><td>

\(24 rights X $5000\) + \(28 rights X $1300\) = $156,400

</td></tr></tbody>
</table>The software asset manager determines that option number 3 is the most cost-effective licensing solution for the cluster. By using this licensing option, the software asset manager can achieve a total cost savings of approximately $103,600.

**Parent Topic:**[Cost-based licensing optimization for Microsoft](../concept/cost-based-microsoft-cluster-licensing.md)

