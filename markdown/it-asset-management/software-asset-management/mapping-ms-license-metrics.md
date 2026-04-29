---
title: License metrics for Microsoft products
description: A detailed description of the license metrics that can be used with Microsoft products.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# License metrics for Microsoft products

A detailed description of the license metrics that can be used with Microsoft products.

## Microsoft products and Software Asset Management license metrics

**Note:** The support for Per Processor license metric for Windows Server is applicable for Zurich patch 4 and Software Asset Management \(sn\_itam\_samp\) 3.2.0 version onwards. If you have already upgraded to Zurich, you can install the Software Asset Management manually.

<table id="table_olj_hhx_rqb"><thead><tr><th>

Product

</th><th>

Edition

</th><th>

Licensing model provided by Microsoft

</th><th>

Software Asset Management license metrics to be used on ServiceNow Software Asset Management

</th></tr></thead><tbody><tr><td>

Windows Server**Note:** For legacy versions of Windows Server, refer to the Windows Server legacy versions table.

</td><td>

Data Center/Standard

</td><td>

-   Per Core
-   Per Processor
-   CAL licensing

</td><td>

-   Per Core \(with CAL\)
-   Per Processor
-   User/Device CAL for CAL licensing

</td></tr><tr><td>

Microsoft System Center

</td><td>

Data Center/Standard

</td><td>

-   Server - use core based licensing \(Server Management Licenses\)
-   Client - Use Client Management Licenses

</td><td>

-   Server MLs- Per Core \(with CAL\)
-   Client MLs- User/Device

</td></tr><tr><td>

Microsoft Exchange Server

</td><td>

Standard/Enterprise

</td><td>

-   Server licenses
-   CAL licenses

</td><td>

-   Server \(Per Instance\) for Server licensing
-   User/Device CAL for CAL licensing

</td></tr><tr><td>

Microsoft Project Server

</td><td>

Standard/Enterprise

</td><td>

-   Server licenses
-   CAL licenses

</td><td>

-   Server \(Per Instance\) for Server licensing
-   User/Device CAL for CAL licensing

</td></tr><tr><td>

Microsoft SharePoint Server

</td><td>

Standard/Enterprise

</td><td>

-   Server licenses
-   CAL licenses

</td><td>

-   Server \(Per Instance\) for Server licensing
-   User/Device CAL for CAL licensing

</td></tr><tr><td>

Microsoft SQL Server**Note:** For legacy versions of SQL Server, refer to the SQL Server legacy versions table.

</td><td>

Standard/Enterprise

</td><td>

-   Per Core
-   Server/CAL

</td><td>

-   For Core licensing: Per Core
-   For Server/CAL:
    -   Server \(Per Instance\) for Server licensing

        -   Use Server \(Per Instance\) for server licensing for Standard, Web, Business Intelligence Editions
        -   Use Server \(Per Server\) for Enterprise Edition legacy versions 1
**Note:** SQL Server Enterprise is licensed usually using the Per Core licensing model only. However if you have software assurance, you might follow Legacy Server/CAL licensing models. ServiceNow recommends using the Server \(Per Server\) license metric on ServiceNow Software Asset Management.

    -   User/Device CAL for CAL licensing

</td></tr><tr><td>

Microsoft Office 365

</td><td>

Enterprise E3/E5/E1

</td><td>

User Subscription

</td><td>

User Subscription

</td></tr><tr><td>

Microsoft Office

</td><td>

Professional/Standard

</td><td>

Per Device

</td><td>

Per Device

</td></tr><tr><td>

Windows 10

</td><td>

Enterprise Professional

</td><td>

Per Device

</td><td>

Per Device

</td></tr><tr><td>

Microsoft Dynamics CRM 365 Server \(On Premise\)

</td><td>

 

</td><td>

Server/CAL

</td><td>

Only requires User/Device CALs to be created. No Server license required.

</td></tr><tr><td>

Microsoft Dynamics 365 Operations Server \(On Premise\) ERP

</td><td>

 

</td><td>

Server/CAL

</td><td>

-   Requires User/Device CALs to be created.
-   Server \(Per Instance\) for Server licenses

</td></tr><tr><td>

Microsoft 365

</td><td>

Enterprise E3/E5/F3

</td><td>

User Subscription

</td><td>

User Subscription

</td></tr><tr><td>

Core Infrastructure Suite

</td><td>

Data Center/Standard

</td><td>

Per Core

</td><td>

Per Core \(with CAL\)

</td></tr></tbody>
</table>## Windows Server legacy versions

<table id="table_upn_w3d_sqb"><thead><tr><th>

Version

</th><th>

Edition

</th><th>

Licensing model provided by Microsoft

</th><th>

Software Asset Management license metrics to be used on ServiceNow Software Asset Management

</th><th>

Licensing rules

</th></tr></thead><tbody><tr><td rowspan="2">

2003-2008 R2

</td><td>

Standard

</td><td>

Server

</td><td>

Server \(Per Instance\) + add User/Device CALs

</td><td>

Min: NA

 Virtualization: 1 VM per license.

 A single Standard Edition license server permits you to run one instance of the software in a physical or virtual OSE on the server. You need to assign a Standard Edition license for each running instance.

</td></tr><tr><td>

Datacenter

</td><td>

Processor

</td><td>

Per Processor + add User/Device CALs

</td><td>

Minimum: 2 processor

 Virtualization: Unlimited

 When DataCenter Edition is licensed for every physical processor in a server, the server may run both in the physical OSE and in an unlimited number of Windows Server instances in virtual OSEs.

</td></tr><tr><td rowspan="2">

2012-2012R2

</td><td>

Standard

</td><td>

Processor

</td><td>

Per Processor + add User/Device CALs

</td><td>

Minimum: 2 processors.

 Virtualization: 2 VMs for each fully licensed server.

</td></tr><tr><td>

Datacenter

</td><td>

Processor

</td><td>

Per Processor + add User/Device CALs

</td><td>

Minimum: 2 processors.

 Virtualization: Unlimited.

</td></tr><tr><td rowspan="2">

2016-2019

</td><td>

Standard

</td><td>

Per Core/CAL

</td><td>

Per Core \(with CAL\) + add User/Device CALs

</td><td>

Minimum: 16 cores per server or 8 Per Processor.

 Virtualization: 2 VMs for each fully licensed server.

</td></tr><tr><td>

Datacenter

</td><td>

Per Core/CAL

</td><td>

Per Core \(with CAL\) + add User/Device CALs

</td><td>

Minimum: 16 cores per server or 8 Per Processor.

 Virtualization: Unlimited.

</td></tr></tbody>
</table>## SQL Server legacy versions

<table id="table_prs_2hk_sqb"><thead><tr><th>

Version

</th><th>

Edition

</th><th>

Licensing model provided by Microsoft

</th><th>

Software Asset Management license metrics to be used on ServiceNow Software Asset Management

</th><th>

Licensing rules

</th></tr></thead><tbody><tr><td rowspan="2">

2005

</td><td>

Standard

</td><td>

-   Server/CAL
-   Processor

</td><td>

-   For Server/CAL use: Server\(Per Instance\) for Server licensing and User/Device CAL for CAL licensing.
-   Per Processor

</td><td>

A server licensing rule \(for Workgroup, Standard, or Enterprise editions\) is required for every operating system environment on which that edition pf SQL Server software or any of its components, such as Analysis Services, is running.

 A Processor license is required for each processor installed on each operating system environment running SQL Server or any of its components, such as Analysis Services.

</td></tr><tr><td>

Enterprise

</td><td>

-   Server/CAL
-   Processor

</td><td>

-   For Server/CAL use: Server\(Per Instance\) for Server licensing and User/Device CAL for CAL licensing.
-   Per Processor

</td><td>

Only for Enterprise edition: If all processors in a machine are licensed, you may run unlimited instances of SQL Server 2002 on an unlimited number of virtual operating environments on the same machine.

</td></tr><tr><td rowspan="3">

2008-2008 R2

</td><td>

Standard

</td><td>

-   Server/CAL
-   Processor

</td><td>

-   For Server/CAL use: Server\(Per Instance\) for Server licensing and User/Device CAL for CAL licensing.
-   Per Processor

</td><td>

-   Server/CAL: Each server license for these editions permits you to run unlimited instances of the software in one OSE or virtual machine \(VM\). To run the software in additional OSEs or VMs, you require additional server licenses.
-   Processor license: Number of OSEs on which you can run SQL Server. Only Physical OSEs.

</td></tr><tr><td>

Enterprise

</td><td>

-   Server/CAL
-   Processor

</td><td>

-   Use Server \(per Server\) for Server Licensing and User/Device CAL for CAL licensing.
-   Per Processor

</td><td>

-   Server/CAL: Each server license for the Enterprise edition permits you to run unlimited instances of the software in up to four OSEs or VMs.
-   Processor license: Number of OSEs on which you can run SQL Server. Up to four OSEs per license.

</td></tr><tr><td>

Datacenter

</td><td>

Processor

</td><td>

Per Processor

</td><td>

Processor license: Number of OSEs on which you can run the SQL Server: Unlimited. The Datacenter edition requires that all the physical processors on the server are licensed and at least two processor licenses are assigned to the server.

</td></tr><tr><td rowspan="2">

2012-2014

</td><td>

Standard

</td><td>

-   Server/CAL
-   Per Core

</td><td>

-   For Server/CAL: Use Server \(Per Instance\) for server licensing and User/Device CAL for CAL licensing
-   Per Core

</td><td>

Core based licensing:

1.  Count the total number of physical cores in the server. Multiple the number of cores by the appropriate core factor to determine the total number of licenses required for the server.

**Note:** The core factor used depends on the processor type deployed and a minimum of four core licenses is required for each physical processor on a physical server.

2.  To license individual VMs using the Per Core model, you must purchase a core license for each v-core \(or virtual processor, virtual CPU, virtual thread\) allocated to the VM, subject to a four core license minimum per VM.

For licensing purposes, a v-core maps to a hardware thread. When licensing individual VMs, core factors do not apply.


</td></tr><tr><td>

Enterprise

</td><td>

Per Core1

</td><td>

Per Core

</td><td>

Same as above.

</td></tr><tr><td rowspan="2">

2016-2019

</td><td>

Standard

</td><td>

-   Server/CAL
-   Per Core

</td><td>

-   For Server/CAL: Server \(Per Instance\) for server licensing and User/Device CAL for CAL licensing
-   For Core licensing: Per Core

</td><td>

-   Server/CAL: Each server running SQL Server software requires a server license.
-   Per Core: A minimum of four core licenses are required for each physical processor on the server.

</td></tr><tr><td>

Enterprise

</td><td>

Per Core1

</td><td>

Per Core

</td><td>

Same as above.**Note:** If you are already using SQL Server Enterprise edition with \(Server/CAL\) server licenses with software assurance, continue to use the Server+CAL licensing model. Use license metric as Server \(per Server\) for Server Licensing and User/Device CAL for CAL licensing. The new purchases for SQL Server Enterprise will be based only on the Per Core licensing model.

For more information about licenses required for Server + CAL licensing model, see [Licensing support for Microsoft SQL Server enterprise on Server+ CAL](../concept/microsoft-sql-server-enterprise-edition-licensing-modal.md).

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

