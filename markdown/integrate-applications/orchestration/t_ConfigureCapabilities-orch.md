---
title: Configure MID Server capabilities
description: MID Server capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Configure capabilities on MID Servers for applications like Orchestration, , and .
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MID Server capabilities, MID Servers for Orchestration, Classic Orchestration, Creating integrations with applications]
---

# Configure MID Server capabilities

MID Server capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Configure capabilities on MID Servers for applications like Orchestration, , and .

## Before you begin

Role required: admin or sm\_admin

<table id="table_u1g_ts4_nhb"><tbody><tr><td>

 

</td></tr></tbody>
</table>## About this task

Several applications use capabilities, IP ranges, and  to narrow the pool of MID Servers the applications need.

**Note:** At least one capability is required for each MID Server used by Orchestration. See  for more information.

The following capabilities are available by default with Discovery:

<table id="table_mqg_wkg_f3b"><tbody><tr><td>

All

</td><td>

IBM

</td><td>

Resolve DNS

</td></tr><tr><td>

Ansible

</td><td>

JDBC

</td><td>

REST

</td></tr><tr><td>

AWS

</td><td>

NetApp

</td><td>

SNMP

</td></tr><tr><td>

Azure

</td><td>

Nmap

</td><td>

SOAP

</td></tr><tr><td>

Chef

</td><td>

OpenStack

</td><td>

SSH

</td></tr><tr><td>

Cloud Management

</td><td>

PowerShell

</td><td>

VMware

</td></tr><tr><td>

Google

</td><td>

RCA

</td><td>

WMI

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Capabilities**.

2.  Select an existing capability or select **ALL** to include all capabilities.

    **Note:** Ensure that each IP address range has MID Servers with the necessary capabilities to complete the Orchestration activities on that network segment.

3.  Create a new capability:

    1.  Select **New**.

    2.  Configure the value for a custom capability.

        An example is a capability for **DOMAIN**, with a value of **service-now**.

    3.  Select **Submit**.

4.  Select **Edit** in the MID Servers related list to add MID Servers to the capability.

5.  Select one or more MID Servers for this capability from the **Available** list.

6.  Select **Save**.

    The capability defined here also appears in the primary record for this MID Server.


**Parent Topic:**[MID Server capabilities](product/mid-server/reference/r_MIDServerCapabilities.md)

