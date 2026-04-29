---
title: Configure remedial actions - End Process
description: Configure the End Process remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Investigation using Microsoft Endpoint Configuration Manager, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure remedial actions - End Process

Configure the End Process remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Create a MECM script with the name `EndProcess`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](create-mecm-script.md).

3.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$process_id
    )
    Get-Process -Id $process_id | Stop-Process -Force -PassThru
    
    ```

4.  Retrieve and copy the script GUID.

5.  Open the MECM Action Configuration \[sn\_mecm\_action\_config\] table.

    The MECM Action Configuration table displays the list of action configurations.

6.  From the list of configurations, select and edit **End Process**.

7.  In the **Action input** field, add the script GUID.

    ![MECM End Process](../image/mecm-end-process.png)

8.  Click **Save**.


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

