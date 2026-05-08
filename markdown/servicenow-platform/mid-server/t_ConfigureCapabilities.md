---
title: Configure MID Server capabilities
description: MID Server capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Configure capabilities on MID Servers for applications like Orchestration, Cloud Management, and Service Mapping.MID Server capabilities define the specific functions of a MID Server within an IP address range.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure MID Server capabilities

MID Server capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Configure capabilities on MID Servers for applications like Orchestration, Cloud Management, and Service Mapping.

## Before you begin

Role required: admin or sm\_admin

<table id="table_u1g_ts4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

Several applications use capabilities, IP ranges, and [MID Server selection](../concept/c_MIDServerSelector.md) to narrow the pool of MID Servers the applications need.

**Note:** At least one capability is required for each MID Server used by Orchestration. See [MID Servers for Orchestration](../../orchestration/concept/c_OrchestrationMID.md) for more information.

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


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)

## MID Server capabilities

MID Server capabilities define the specific functions of a MID Server within an IP address range.

### Nmap capability

The **Nmap** capability is only assigned to MID Servers for which the Network Mapper \(Nmap\) scanner has been installed for [credential-less Discovery](https://www.servicenow.com/docs/access?context=nmap-credential-less-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US). This capability cannot be added to or removed from any MID Server manually. For instructions on installing or uninstalling Nmap, see [Install and uninstall Nmap on a MID Server](install-nmap-on-mid-server.md#)

### MID Server capability values

Capabilities provided in the base system do not have a defined value string. The capability value can be blank, a single value, or a \* \(wildcard\). A MID Server configured to use a capability that has no value can locate any device using that capability's protocol. If a capability has a defined value, the MID Server using that capability finds only those devices using that protocol that match the value string exactly. The exception to this is the Resolve DNS capability, which is configured to resolve any DNS name into an IP address using a partial string match. The \* \(wildcard\) will match a request capability specifying any non-blank value.

Starting with the Madrid release, the **\[capability name\]:\[value\]** combination appears in the slushbucket when you add a capability to a MID Server. This combination allows you to see all the capabilities that have different values, even if the capability name is the same. For example, if you are using the Cloud Management capability, and you use the value field to specify the us-west logical datacenter on one of the capability records, you can see the combination in the **Collection** list.

![Capability name and value combination](../image/capability-value-combo.png)

### MID Server selection

The MID Server is selected using an algorithm based on the capabilities available. The selector produces a list of suitable MIDs using filters in the following order: **server status** &gt; **applications** &gt; **IP range** &gt; **capabilities**. The algorithm searches the capabilities in the following sequence and, if a step finds at least one MID server, the remaining steps are skipped:

1.  **Exact value match:** Find each MID Server containing capabilities with name/value pairs with an exact match to all requested capability name/value pairs. Blank is a valid value. \* \(wildcard\) values are ignored.
2.  **Wildcard value match:** The same as an exact value match, but also allows a non-blank request value to match MID server capability records containing value \*.
3.  **Special capability name ALL:** Find each MID Server containing the special capability name ALL, ignoring capability's value field.

**Note:** If the requested capability name does not exist in the ecc\_agent\_capability table, **BadArgumentException** is thrown rather than falling back to the ALL capability.

### Scripted MID Server capability value matching

You can use value tests to create capabilities that find devices using values without requiring exact string matching. Action on these values is controlled by a user-defined script.

The Resolve DNS capability is provided in the base system and is configured to resolve DNS names into IP addresses for devices whose names end with a specified domain name. The capability **Value** entered is automatically prefaced with a dot during processing to match domain syntax. This value can contain one or more sub-domains, but must include the end of the domain string. Matching devices must end with the identical syntax. The script for the Resolve DNS capability determines if a device name matches the criteria defined by **Value**. If a match exists, the platform performs the address resolution automatically. For example, if the value for the Resolve DNS capability is `service-now.com`, the MID Server with this capability finds `lnxlab01.sandiego.service-now.com` and `dbsrv101.sanjose.service-now.com`. If the value is changed to `sandiego.service-now.com`, then the MID Server finds only `lnxlab01`.

**Note:** If **Value** in the Resolve DNS capability is blank, then all domains match.

To view the script for evaluating this capability, navigate to **MID Server** &gt; **Capability Value Tests** and select **Resolve DNS** from the list.

![MID capabilities](../image/MIDServerResolveDNS.png)

