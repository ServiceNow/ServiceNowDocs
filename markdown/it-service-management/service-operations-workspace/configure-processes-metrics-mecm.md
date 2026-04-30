---
title: Configure processes metrics
description: Configure the top processes by CPU and top processes by memory metrics for Microsoft Endpoint Configuration Manager for Investigation.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure processes metrics

Configure the top processes by CPU and top processes by memory metrics for Microsoft Endpoint Configuration Manager for Investigation.

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Create a MECM script with the name `GetProcess`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](create-mecm-script.md).

3.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$orderBy,
    [Parameter(Mandatory=$True)]
    [string]$top
    )
    
    $processes = get-process
    
    $Total = 0;
    ForEach ($process in $processes) {
        $Total += $process.cpu;
    }
    
    $processes | Sort-Object $orderBy -Descending | select processname,id,ws,cpu -First $top | select processname,id, @{l="mem"; e={$_.ws}}, @{l="cpu"; e={($_.cpu / $Total) * 100}};
    
    ```

4.  Retrieve and copy the script GUID.

5.  Open the MECM Adapter Configuration \[sn\_mecm\_adapter\_config\] table.

    The MECM Adapter Configuration table displays the list of adapter configurations.

6.  From the list of configurations, select and edit **Running processes - CPU%**.

7.  In the **Action input** field, add the script GUID.

    ![Edit running processes CPU](../image/edit-cpu-config.png)

8.  Click **Save**.

9.  From the list of configurations, select and edit **Running processes - MEM**.

10. In the **Action input** field, add the script GUID.

11. Click **Save**.


## Result

The top processes by CPU and top processes by memory metrics are displayed on the **Investigation** tab of the incident record in Service Operations Workspace.

**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

