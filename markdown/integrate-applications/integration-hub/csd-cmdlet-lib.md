---
title: Update the SCCM cmdlet libraries
description: Ensure that the System Center Configuration Manager SCCM Cmdlet Library is up-to-date.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Update the SCCM cmdlet libraries

Ensure that the System Center Configuration Manager SCCM Cmdlet Library is up-to-date.

## Before you begin

Role required: Either current user or system administrator, depending on settings.

## About this task

The System Center Configuration Manager SCCM Cmdlet Library installs and updates the Windows PowerShell module for SCCM. SCCM checks for library updates on a daily basis. Out-of-date libraries can cause Discovery of the SCCM server to fail, because the system cannot parse the SCCM activity output. This warning message appears in the ECC queue input records for the SCCM GET activities:

```
WARNING: An update to the System Center 2012 Configuration Manager Cmdlet
Library is available. Please go to
'http://go.microsoft.com/fwlink/?LinkId=528947' to download the latest version.
Running cmdlet version: 5.0.8231.1004 Latest cmdlet version: 5.0.8328.1155
```

Download the latest version of the cmdlet library from [http://go.microsoft.com/fwlink/?LinkId=528947](http://go.microsoft.com/fwlink/?LinkId=528947). For installation instructions, see [https://technet.microsoft.com/en-us/library/dn958404\(v=sc.20\).aspx](https://technet.microsoft.com/en-us/library/dn958404(v=sc.20).aspx).

If you elect to use an earlier version library, use this procedure to disable the CM update check, which allows Discovery to proceed without issues.

## Procedure

1.  Log into the SCCM console as an administrator.

2.  Open the menu from the upper left corner of the console.

3.  Select **Connect via Windows PowerShell**.

4.  Run one of these commands to disable the update check:

    -   **Per-user**: `Set-CMCmdletUpdateCheck -CurrentUser -IsUpdateCheckEnabled 0`
    -   **Per-system**: `Set-CMCmdletUpdateCheck -System -IsUpdateCheckEnabled 0`
    **Important:** The per-system cmdlet must run in an elevated Windows PowerShell session.

5.  Run the `Get-CMCmdletUpdateCheck` command to refresh the console and check the settings.

6.  Ensure that the value of the *IsEnabled* configuration variable has changed to **False**.

    This indicates that the warning for an out of date cmdlet library is disabled for the users specified.

7.  To re-enable the update check, run the `-IsUpdateCheckEnabled 1` command for either the current user or for the system.


**Parent Topic:**[Configuring SCCM](../concept/configure-sccm-ihub.md)

