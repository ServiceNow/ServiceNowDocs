---
title: Set up MID Servers to use PowerShell
description: Configure MID Servers in your organization to use PowerShell for horizontal and top-down discovery of Windows servers.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [PowerShell for Discovery and Service Mapping, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Set up MID Servers to use PowerShell

Configure MID Servers in your organization to use PowerShell for horizontal and top-down discovery of Windows servers.

## Before you begin

Role required: agent\_admin, discovery\_admin, or admin

**Note:** This is enabled by default.

PowerShell version 2.0 is not supported, therefore it is recommended to upgrade to a higher version. If the MID Server detects that it has version 2.0, it may work partially. The MID Server creates a record in the mid\_server issue table with the following message: PowerShell version 2 is deprecated. Upgrading PowerShell to version 5 is recommended.

## Procedure

1.  Download PowerShell and install it on each MID Server configured to discover Windows computers.

    If a compatible PowerShell is available on the Host, you don’t need to do anything else.

2.  Determine which credentials MID Servers use for PowerShell.

    -   To discover Windows computers using credentials from the credentials table, set the **mid.powershell.use\_credentials** parameter to **true**. Using credentials form the credentials table is the default behavior when PowerShell is enabled.
    -   To force Discovery and Service Mapping to use the credentials of the MID Server service user, set the **mid.powershell.use\_credentials** parameter to **false** on the MID Server. The MID Server service must have domain admin credentials to have access to the Windows machines in the domain.
3.  If necessary, configure advanced parameters for PowerShell and PowerShell Remoting on each MID Server separately.

    Although you can disable PowerShell by changing the **mid.use\_powershell** and **mid.sa.prefer\_powershell**, this method is deprecated and should not be used.


**Parent Topic:**[PowerShell for Discovery and Service Mapping](../reference/r_PowerShellForDiscovery.md)

