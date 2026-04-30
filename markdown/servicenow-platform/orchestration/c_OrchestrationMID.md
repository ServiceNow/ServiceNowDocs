---
title: MID Servers for Orchestration
description: Orchestration automatically selects an appropriate MID Server based on the capabilities that you configure in activities, the IP addresses of target devices, and the application that the MID Server is allowed to use.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# MID Servers for Orchestration

Orchestration automatically selects an appropriate MID Server based on the capabilities that you configure in activities, the IP addresses of target devices, and the application that the MID Server is allowed to use.

To allow a MID Server to work with Orchestration, it must have the **Orchestration** application or the **ALL** application assigned to it. See [Configure a default MID Server for each application](../../mid-server/task/t_SpecifyMIDServerApplications.md#) for instructions.

You can have MID Servers focus on different capabilities and separate sections of your network. See:

-   [MID Server capabilities](../../mid-server/reference/r_MIDServerCapabilities.md)
-   [Map an IP address to a DNS name](../../mid-server/task/t_MapIPAddressToDNSName.md)

You can also specify a default MID Server to use if no MID Servers meet the capability and IP range criteria for an activity. See[Select the default MID Server for Orchestration](../../mid-server/concept/c_MIDServerSelectionCriteria.md).

-   **[MID Server capabilities](../../mid-server/reference/r_MIDServerCapabilities.md)**  
MID Server capabilities define the specific functions of a MID Server within an IP address range.
-   **[Select the default MID Server for Orchestration](../../mid-server/concept/c_MIDServerSelectionCriteria.md)**  
Orchestration uses the default MID Server if it cannot find a MID Server with the correct IP range and capability.
-   **[PowerShell probe version 2 system property](../../mid-server/reference/powershell-probe-v2.md)**  
View detailed PowerShell credential information and view extended logging information.
-   **[PowerShell log property](../../mid-server/concept/powershell-log-property.md)**  
Enable debug messages to display from PowerShell.

**Parent Topic:**[Classic Orchestration](../reference/r-orchestration.md)

**Related topics**  


[MID Server capabilities](../../mid-server/reference/r_MIDServerCapabilities.md)

