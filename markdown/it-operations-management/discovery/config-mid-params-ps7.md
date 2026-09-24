---
title: Configure MID Server parameters for PowerShell 7
description: Configure two MID Server parameters to run File-based Discovery and Windows ADME on target hosts that use PowerShell 7.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/config-mid-params-ps7.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [File-based Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure MID Server parameters for PowerShell 7

Configure two MID Server parameters to run File-based Discovery and Windows ADME on target hosts that use PowerShell 7.

## Before you begin

Confirm the following:

-   The instance is on the Brazil version of the ServiceNow AI Platform.
-   PowerShell 7 is installed on the MID Server.
-   PowerShell 7 is installed on target hosts.
-   On each target host that runs PowerShell 7, **DisableImplicitWinCompat** is set to `true` in the PowerShell configuration file. By default, PowerShell 7 loads certain modules through a background Windows PowerShell 5.1 session, which blocks Discovery scripts from running on PowerShell 7. For more information, see the "About Windows PowerShell Compatibility" article on the [Microsoft PowerShell](https://learn.microsoft.com/en-us/powershell/) documentation site.
-   File-based Discovery or Windows ADME is active on the instance.

Role required: agent\_admin or admin

## About this task

By default, File-based Discovery and Windows ADME use PowerShell 5 on target hosts. To run these features on hosts that use PowerShell 7, create two parameters on the MID Server. Setting **mid.powershell.prefer\_7\_plus** controls the MID Server itself. Setting **mid.powershell.prefer\_7\_plus\_remote** controls the target host. Each parameter defaults to `false` if not set, so any host where the parameter is not configured runs on PowerShell 5.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Select the MID Server.

3.  In the **Configuration Parameters** tab, select **New**.

4.  Create the required parameters in the following table.

    |Parameter name|Value|Description|
    |--------------|-----|-----------|
    |**mid.powershell.prefer\_7\_plus\_remote**|`true`|Prefer PowerShell 7 or later, if available, on remote target hosts. Default: `false`.|
    |**mid.powershell.prefer\_7\_plus**|`true`|Prefer PowerShell 7 or later, if available. Default: `false`.|

5.  Select **Submit** after each.


## Result

File-based Discovery and Windows ADME run using PowerShell 7 on the configured target hosts.

**Related topics**  


[File-based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/file-based-discovery.md)

