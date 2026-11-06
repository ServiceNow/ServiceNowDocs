---
title: Discovery behaviors
description: Discovery behaviors determine the probes that Shazzam launches and from which MID Servers these probes are launched.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/c\_DiscoveryBehaviors.html
release: brazil
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-10-20"
reading_time_minutes: 4
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery behaviors

Discovery behaviors determine the probes that Shazzam launches and from which MID Servers these probes are launched.

A scan performed by a single MID Server targets a designated IP address range. A behavior can assign different tasks to multiple MID Servers on the same IP address segment or on different network segments. Behaviors are available in [Discovery schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md) for discoveries that update configuration items \(CIs\) in the Configuration Management Database \(CMDB\).

You can use behaviors in the following scenarios:

-   Load balancing: A behavior enables load balancing in systems that use multiple MID Servers deployed across one or more domains.
-   Multiple protocols in multiple domains: A behavior can configure one MID Server to scan for all protocols on one domain and another MID Server to perform a WMI scan on a second domain.
-   Access control lists \(ACLs\): Discovery can scan SNMP devices protected by an ACL if the MID Server host machine is granted access by that ACL. A behavior can configure a MID Server to scan devices protected by an ACL.
-   Devices running two protocols: Some devices run two protocols at the same time, most commonly SSH and SNMP. A behavior can control which of the two protocols is explored for certain devices. The behavior then excludes the other protocol from exploration.

Behaviors enable Discovery of SSH and SNMP devices and WMI devices running on multiple Windows domains by using multiple MID Servers.

For example, an organization has two Windows domains in its network and a variety of UNIX computers and SNMP devices. The challenge is to discover all the devices efficiently, without duplicating effort. Each domain contains a Windows MID Server, which is used to scan the IP addresses from the two domains specified in the Discovery schedule, and the SSH and SNMP devices. Use a behavior to divide the work so that no device is scanned twice. In this example, both domains are in the same geographical location, and a single schedule is sufficient.

**Note:** To run Discovery over multiple Windows domains, use [PowerShell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/r_PowerShellForDiscovery.md), which enables a single MID Server to authenticate on machines on different domains using credentials stored on the instance.

## Discovery functionalities

Each behavior contains one or more Discovery functionality records. A Discovery functionality defines what each MID Server in this behavior must do, specifically which protocols to detect.

A functionality record links the following items:

-   Functionality definition: The protocol or list of protocols that the MID Servers in the functionality scan. Several definitions are available by default, and you can also create custom definitions.
-   MID Servers: The MID Servers that perform the functionality. When you select multiple MID Servers, Discovery balances the load across them.
-   Phase: An integer that groups functionalities. Functionalities in the same phase run together in one Shazzam probe, and phases run in numerical order.
-   Functionality criteria: Conditions that determine which MID Server processes the Shazzam results, based on the MID Server name \(`mid_server`\), the target domain \(`win_domain`\), or the MID Server domain \(`mid_win_domain`\). Criteria are required only for Windows MID Servers, and only when the behavior controls Discovery across multiple domains.

The following table lists some common functionality definitions. For the full list, view the records in the Functionality Definition \[discovery\_function\_def\] table by navigating to **All** &gt; **Discovery** &gt; **Discovery Definition** &gt; **Functionality Definitions**.

|Functionality|Description|
|-------------|-----------|
|Windows only \(WMI\)|Scans for Windows devices using the WMI protocol. Requires a Windows MID Server and functionality criteria to specify the domain.|
|Windows, DNS, and WINS|Scans for Windows devices using the WMI protocol and resolves the domain using DNS and WINS. Requires a Windows MID Server and functionality criteria.|
|SNMP only|Scans for SNMP devices only. Use this when scanning devices protected by an ACL that restricts SNMP access to specific MID Server hosts. Does not require functionality criteria.|
|All except SNMP|Scans for all protocols except SNMP, including WMI and SSH. Use this in combination with SNMP only functionality when you need separate MID Servers for SNMP and other protocols.|
|All except Windows \(no WMI\)|Scans for all protocols except WMI, including SSH and SNMP. Use this in combination with Windows only functionality when scanning multiple domains or when non-Windows devices require a different MID Server.|

-   **[Create a Discovery behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/create-disco-behavior.md)**  
Create a Discovery behavior to determine which probes Shazzam launches and which MID Server is used.
-   **[Set up a load balancing behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/t_SetUpLoadBalDiscoBehavr.md)**  
When multiple MID Servers are configured to scan the same protocol, you can set up load balancing behavior to automatically balance the work between MID Servers.
-   **[Examples of Discovery behavior functionalities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/r_DefineTheFunctionalities.md)**  
This example of a Discovery behavior requires three functionalities for the behavior.
-   **[Access an ACL-protected SNMP device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/t_AccessAnACLProtectedSNMPDevice.md)**  
Access an SNMP device protected by an ACL using a Discovery behavior.

**Parent Topic:**[Advanced Discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/c_DiscoveryExtendedCapabilities.md)

