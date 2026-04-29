---
title: Citrix License Server and Delivery Controller discovery
description: Discovery can find Citrix License Server instances and Delivery Controller components that run on Windows machines.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Citrix License Server and Delivery Controller discovery

Discovery can find Citrix License Server instances and Delivery Controller components that run on Windows machines.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Requirements

-   Configure [Windows administrative credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) to access the host machine.
-   Make sure that [PowerShell for Discovery](../reference/r_PowerShellForDiscovery.md) is installed on your MID Servers. The patterns used for Citrix discovery require the ability to run PowerShell commands.
-   For OS users, make sure you can execute “Get-XDSite.” The Citrix Studio Admin should provide permissions.
-   \(Optional\) For top-down discovery with Service Mapping, on Citrix Delivery Controller, install the Citrix.Broker module.
-   \(Optional\) For top-down discovery with Service Mapping, a user with permission to run PowerShell commands.
-   \(Optional\) \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Patterns

Discovery uses these patterns to perform horizontal discovery:

|Pattern|Process detected|
|-------|----------------|
|Citrix License Server|lmadmin.exe|
|Delivery Controller|BrokerService|

## Data collected and relationships

<table id="table_hlf_wsv_ndb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Citrix License Server \[cmdb\_ci\_appl\_license\_server\]

</td><td>

Name \[name\]

 TCP ports \[tcp\_port\]

 Operational status \[operational\_status\]

</td></tr><tr><td>

Citrix Delivery Controller \[cmdb\_ci\_appl\_delivery\_controler\]

</td><td>

Name \[name\]

 Version \[version\]

 Operational status \[operational\_status\]

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|Citrix License Server \[cmdb\_ci\_appl\_license\_server\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\]|
|Citrix Delivery Controller \[cmdb\_ci\_appl\_delivery\_controler\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\]|

**Parent Topic:**[Software discovery](c_Software.md)

