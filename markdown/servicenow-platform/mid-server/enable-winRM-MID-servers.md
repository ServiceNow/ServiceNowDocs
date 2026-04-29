---
title: Configure MID Server as WinRM trusted host
description: In environments using Windows Remote Management \(WinRM\), Discovery or Service Mapping can discover servers using the WinRM protocol. Add servers, which are part of WinRM, as trusted hosts on all MID Servers that Discovery or Service Mapping use for discovery.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure MID Server as WinRM trusted host

In environments using Windows Remote Management \(WinRM\), Discovery or Service Mapping can discover servers using the WinRM protocol. Add servers, which are part of WinRM, as trusted hosts on all MID Servers that Discovery or Service Mapping use for discovery.

## Before you begin

Role required: mid\_admin

<table id="table_wyl_ys4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

MID Server cannot access servers using the WinRM protocol unless these servers are configured as trusted hosts for this MID Server.

Perform this procedure on each MID Server used by Service Mapping or Discovery.

## Procedure

1.  On the MID Server, open the command-line shell.

2.  To add all servers to the TrustedHosts lists, run the following command:

    `winrm s winrm/config/client '@{TrustedHosts="*"}'`

    The command requires different syntax depending on the shell: use single quotation marks around `@{TrustedHosts="*"}` in Windows PowerShell, and do not use quotation marks in Command Prompt.

3.  To add specific servers to the TrustedHosts list, run the command with the comma-separated hosts instead of the asterisk \(\*\), for example:

    `winrm s winrm/config/client '@{TrustedHosts="serverA,serverB,serverC"}'`


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)

