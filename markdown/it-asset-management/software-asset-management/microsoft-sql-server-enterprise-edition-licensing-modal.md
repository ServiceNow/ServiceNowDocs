---
title: Licensing support for Microsoft SQL Server enterprise on Server+ CAL
description: Leverage the enhanced licensing rule to optimize licensing for legacy  Microsoft SQL Server Enterprise edition licenses under the Server + CAL licensing model with Software Assurance \(SA\).
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Licensing support for Microsoft SQL Server enterprise on Server+ CAL

Leverage the enhanced licensing rule to optimize licensing for legacy  Microsoft SQL Server Enterprise edition licenses under the Server + CAL licensing model with Software Assurance \(SA\).

Microsoft no longer sells new SQL Server Enterprise Server + CAL licenses, but existing customers with active software assurance can continue to use this licensing. The  Software Asset Management Professional application enables you to license SQL Server based on a combination of server licenses and client access licenses \(CALs\).

## Licensing rules for SQL Server enterprise on Server + CAL Model

The following types of licensing support are available for SQL Server Enterprise on Server/CAL licensing support:

-   On Physical Servers: For customers deploying SQL Server Enterprise Edition using the server/CAL model in a physical environment, each Operating System Environment \(OSE\) can only utilize up to twenty physical cores. This technical limitation is enforced by Microsoft, so no additional action is required from administrators.
-   On Virtual Machines: For customers using SQL Server Enterprise Edition server licenses in virtualized environments, each group of virtual machines tied to a single server license \(up to four VMs per server license\) is allowed access to a combined maximum of twenty hardware threads at any time. This limitation will be managed and enforced by ServiceNow SAM Pro.

The following formula is used to determine the number of licenses required when using the Server + CAL licensing model:

```
Max ( (Sum of number of VM) / 4, (Sum of total VM cores) / 20 )
```

To determine the number of licenses needed, divide the total number of virtual machines \(VMs\) by 4 \(as one server license covers up to 4 VMs\) and divide the total number of cores \(threads\) across all VMs by 20 \(as each license allows up to 20 threads\). The higher of this two result is the required number of licenses.

For example, the cluster ABC consists of three hosts. Each host can run up to 13 virtual machines \(VMs\), and each VM may have a distinct number of processor cores assigned. The licensing entitlement is SQL Server 2019 Enterprise edition with Software Assurance \(SA\), which utilizes the Server Core Licensing model. The following table demonstrates the calculation process for determining the required number of licenses, ensuring proper compliance based on the potential number of VMs and processor cores.

|Host name|Number of VMs|Number of potential VMs|Number of potential cores|Server licenses required|
|---------|-------------|-----------------------|-------------------------|------------------------|
|Host A|4|13|72|Maximum \( \(Number of potential VMs\) / 4, \(Total VM cores\) / 20\) = Max \(13/4, 72/20\) = Max \(3.25, 3.6\) = 4 licenses|
|Host B|4|13|72|Maximum \( \(Number of potential VMs\) / 4, \(Total VM cores\) / 20\) = Max \(13/4, 72/20\) = Max \(3.25, 3.6\) = 4 licenses|
|Host C|5|13|72|Maximum \( \(Number of potential VMs\) / 4, \(Total VM cores\) / 20\) = Max \(13/4, 72/20\) = Max \(3.25, 3.6\) = 4 licenses|

When calculating the required licenses, the maximum number of potential VMs per host is crucial because licensing is based on potential, not actual, usage. In this example, each host can run up to 13 VMs, so this number is used for the calculation. For the cluster, the total number of server licenses required is 12. Client Access Licenses \(CALs\) must be calculated separately and aren’t included in this formula. This approach ensures compliance with Microsoft’s licensing requirements and provides clarity on the number of server licenses to be procured.

**Note:** For detailed information about Client Access Licenses or CAL licensing, see [Microsoft server software CAL setup on ServiceNow® Software Asset Management Professional](https://www.servicenow.com/community/sam-blog/microsoft-server-software-cal-setup-on-servicenow-sam-pro/ba-p/3186310).

## Configuring Microsoft SQL server enterprise when you have multiple licensing models

For configuring the Microsoft SQL Server Enterprise on Software Asset Management Professional, see Microsoft SQL server enterprise, see [https://support.servicenow.com/kb?sys\_kb\_id=6ec3c13d93da3610080af35d6cba106e&amp;id=kb\_article\_view](https://support.servicenow.com/kb?sys_kb_id=6ec3c13d93da3610080af35d6cba106e&id=kb_article_view).

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

