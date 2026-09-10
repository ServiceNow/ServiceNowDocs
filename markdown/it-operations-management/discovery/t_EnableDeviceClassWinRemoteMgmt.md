---
title: Use Windows Remote Management for classification
description: You can configure the discovery of Windows hosts using the Windows Remote Management \(WinRM\) protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/t\_EnableDeviceClassWinRemoteMgmt.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Use Windows Remote Management for classification

You can configure the discovery of Windows hosts using the Windows Remote Management \(WinRM\) protocol.

## Before you begin

-   Install and configure a Windows MID Server on the local network.
-   WinRM service must be enabled on all discoverable Windows hosts.

Roles required: discovery\_admin, agent\_admin, admin

## About this task

By default, the system uses the WMI protocol for device classification of Windows hosts. Administrators can instead use the WinRM protocol for more efficient lightweight data transfer and remote command execution.

## Procedure

1.  Enable the WinRM service on all Windows hosts you want to discover.

2.  Navigate to **Discovery** &gt; **MID Servers**.

3.  Select the MID Server you will use for discovery of Windows hosts.

    The system displays the MID Server record.

4.  From the Configuration Parameters related list click **New**.

    The system displays a MID Server Configuration Parameter record.

5.  In the **Parameter name** field, select the **mid.windows.management\_protocol** parameter from the choice list.

6.  Enter a value of **WinRM**.

    \[Omitted image "MIDServerConfigParameter.png"\] Alt text: MID Server configuration parameter

7.  Click **Submit**.

    The system displays the MID Server record.

8.  Add other Windows Remote Management protocol parameters as needed.

    |Parameter|Description|Default|Requires MID Server restart|
    |---------|-----------|-------|---------------------------|
    |mid.powershell\_api.winrm.remote\_port|Specifies the communications port the MID Server uses to communicate with the WinRM protocol.|5985|No|
    |mid.powershell\_api.session\_pool.target.max\_size|Specifies the maximum number of sessions allowed in the pool per target host.|2|Yes|
    |mid.powershell\_api.session\_pool.max\_size|Specifies the maximum number of sessions allowed in the session pool.|25|Yes|
    |mid.powershell\_api.idle\_session\_timeout|Specifies the timeout value of idle Powershell sessions in seconds.|60|Yes|
    |mid.powershell\_api.winrm.additional\_pssesion\_options|Specifies additional WinRM PSSession options the MID Server applies when creating a session.|None| |
    |mid.powershell\_api.winrm.always\_taskkill|Specifies whether the MID Server always sends a TaskKill command to close the PowerShell process. Enable only when unexpected PowerShell processes remain when used with WinRM.|false| |
    |mid.powershell\_api.winrm.remote\_https\_port|Specifies the HTTPS port that WinRM uses to connect to remote hosts.|5986| |
    |mid.powershell\_api.winrm.skip\_ssl\_cert\_check|Specifies whether the MID Server skips the SSL certificate check with WinRM.|false| |
    |mid.powershell\_api.winrm.skip\_ssl\_cert\_check\_options|Specifies the options used to skip the SSL certificate check with WinRM.|`-SkipCACheck -SkipCNCheck -SkipRevocationCheck`| |
    |mid.powershell\_api.winrm.use\_reverse\_dns\_lookup|Specifies whether the MID Server uses the FQDN when the IP address is not in the list of TrustedHosts for WinRM.|true| |
    |mid.powershell\_api.winrm.use\_ssl|Specifies whether the MID Server uses SSL with WinRM.|false| |
    |mid.powershell\_api.winrm.working\_mode|Specifies the WinRM working mode. Possible values: http, https.|http| |


## What to do next

Run a discovery from the [Discovery schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md) to find Windows machines on your network.

