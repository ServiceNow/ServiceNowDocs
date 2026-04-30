---
title: Use Windows Remote Management for classification
description: You can configure the discovery of Windows hosts using the Windows Remote Management \(WinRM\) protocol.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
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

    ![MID Server configuration parameter](../image/MIDServerConfigParameter.png "MID Server configuration parameter")

7.  Click **Submit**.

    The system displays the MID Server record.

8.  Add other Windows Remote Management protocol parameters as needed.

    |Parameter|Description|Default|Requires MID Server restart|
    |---------|-----------|-------|---------------------------|
    |mid.powershell\_api.winrm.remote\_port|Specifies the communications port the MID Server uses to communicate with the WinRM protocol.|5985|No|
    |mid.powershell\_api.session\_pool.target.max\_size|Specifies the maximum number of sessions allowed in the pool per target host.|2|Yes|
    |mid.powershell\_api.session\_pool.max\_size|Specifies the maximum number of sessions allowed in the session pool.|25|Yes|
    |mid.powershell\_api.idle\_session\_timeout|Specifies the timeout value of idle Powershell sessions in seconds.|60|Yes|


## What to do next

Run a discovery from the [Discovery schedule](../../discovery/task/t_CreateADiscoverySchedule.md) to find Windows machines on your network.

