---
title: Configure system overview - msinfo32 metrics
description: Configure the system overview - msinfo32 metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure system overview - msinfo32 metrics

Configure the system overview - msinfo32 metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Create a MECM script with the name `createMSInfo32File`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](create-mecm-script.md).

3.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$scriptName
    )
     
    $filePath = ".\" + $scriptName + ".txt";
     
    #invoke msinfo32 and save data into file
    msinfo32 /report $filePath;
    
    ```

4.  Create a MECM script with the name `checkMsInfo32FileExist`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](create-mecm-script.md).

5.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$scriptName
    )
     
    $filePath = ".\" + $scriptName + ".txt";
     
    #check if file exist
    $fileExist = Test-Path -Path $filePath;
     
    #read msinfo32 data
    if($fileExist) {
        Write-Host "True"
    }else {
        Write-Host "False";
    }
    
    ```

6.  Create a MECM script with the name `fetchMsInfo32File`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](create-mecm-script.md).

7.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$scriptName
    )
     
    $filePath = ".\" + $scriptName + ".txt";
     
    #check if file exist
    $fileExist = Test-Path -Path $filePath;
     
    #read msinfo32 data
    if($fileExist) {
        Get-Content $filePath;
        Remove-Item $filePath
    }else {
        Write-Host "File doesn't exist";
    }
    
    ```

8.  Retrieve and copy the script GUID.

9.  Open the MECM Adapter Configuration \[sn\_mecm\_adapter\_config\] table.

    The MECM Adapter Configuration table displays the list of adapter configurations.

10. From the list of configurations, select and edit **System information \(msinfo32\)**.

11. In the **Action input** field, add the script GUID.

    ![System overview - msinfo32](../image/mecm-msinfo32-edit.png)

12. Click **Update**.


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

