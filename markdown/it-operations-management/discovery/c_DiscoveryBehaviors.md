---
title: Discovery behaviors
description: Discovery behaviors determine the probes that Shazzam launches, and from which MID Servers these probes are launched.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery behaviors

Discovery behaviors determine the probes that Shazzam launches, and from which MID Servers these probes are launched.

Unlike a scan performed by a single MID Server on a designated IP address range, a behavior can assign different tasks to multiple MID Servers on the same IP address segment or on different network segments. Behaviors are available in [Discovery schedules](../task/t_CreateADiscoverySchedule.md#) for discoveries in which configuration items \(CI\) are updated in the CMDB.

Behaviors can be used in the following scenarios:

-   Load balancing: A behavior enables load balancing in systems that use multiple MID Servers deployed across one or more domains.
-   Multiple protocols in multiple domains: Configure one MID Server to scan for all protocols on one domain and another MID Server to perform a WMI scan on a second domain.
-   Access Control Lists \(ACL\): Discovery can scan SNMP devices protected by an ACL if the MID Server host machine is granted access by that ACL. Use a behavior to configure a MID Server to scan devices protected by an ACL.
-   Devices running two protocols: Some devices might have two protocols running at the same time. Examples of this are the SSH and SNMP protocols running concurrently on one device \(most common\). A behavior can control which of the two protocols is explored for certain devices. The behavior then prevents the other protocol from being explored.

Behaviors also enable the efficient Discovery of SSH and SNMP devices and WMI devices running on multiple Windows domains, using multiple MID Servers.

For example, an organization has two Windows domains in its network and a variety of UNIX computers and SNMP devices. The challenge is to discover all the devices efficiently, without duplicating effort. Each domain contains a Windows MID Server which is used to scan the IP addresses from the two domains specified in the Discovery Schedule, as well as the SSH and SNMP devices. We need a Behavior that divides the work appropriately to avoid scanning anything twice. In this example, we assume that both domains are in the same geographical location, and that a single schedule is sufficient.

**Note:** The preferred method for running Discovery over multiple Windows domains is to use [PowerShell](../reference/r_PowerShellForDiscovery.md), which allows a single MID Server to authenticate on machines on different domains using credentials stored on the instance.

## Available functionality definitions

When creating a behavior, you select a functionality definition that determines which protocols Shazzam scans. The following table lists the available options.

|Functionality|Description|
|-------------|-----------|
|Windows only \(WMI\)|Scans for Windows devices using WMI protocol. Requires a Windows MID Server and functionality criteria to specify the domain.|
|Windows, DNS, and WINS|Scans for Windows devices using WMI protocol and resolves the domain using DNS and WINS. Requires a Windows MID Server and functionality criteria.|
|SNMP only|Scans for SNMP devices only. Use this when scanning devices protected by an ACL that restricts SNMP access to specific MID Server hosts. Does not require functionality criteria.|
|All except SNMP|Scans for all protocols except SNMP, including WMI and SSH. Use this in combination with SNMP only functionality when you need separate MID Servers for SNMP and other protocols.|
|All except Windows \(no WMI\)|Scans for all protocols except WMI, including SSH and SNMP. Use this in combination with Windows only functionality when scanning multiple domains or when non-Windows devices require a different MID Server.|

-   **[Create a Discovery behavior](../task/create-disco-behavior.md)**  
Create a Discovery behavior to determine which probes Shazzam launches and which MID Server is used.
-   **[Set up a load balancing behavior](../task/t_SetUpLoadBalDiscoBehavr.md)**  
When multiple MID Servers are configured to scan the same protocol, you can set up load balancing behavior to automatically balance the work between MID Servers.
-   **[Examples of Discovery behavior functionalities](../reference/r_DefineTheFunctionalities.md)**  
This example of a Discovery behavior requires three functionalities for the behavior.
-   **[Discovery behavior example: access an ACL protected SNMP device](../task/t_AccessAnACLProtectedSNMPDevice.md)**  
Access an SNMP device protected by an ACL using a Discovery behavior.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

