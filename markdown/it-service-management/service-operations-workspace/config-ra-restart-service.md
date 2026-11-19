---
title: Configure remedial action - Restart Service
description: Configure the Restart Service remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-operations-workspace/config-ra-restart-service.html
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure remedial action - Restart Service

Configure the Restart Service remedial action for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin or sn\_reacf.sn\_remedial\_action\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Create a MECM script with the name `RestartService`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/create-mecm-script.md).

3.  Provide the following code in the script block.

    ```
    Param(
    [Parameter(Mandatory=$True)]
    [string]$service_name
    )
    Restart-Service -Force -Name $service_name -PassThru
    
    ```

4.  Retrieve and copy the script GUID.

5.  Open the MECM Action Configuration \[sn\_mecm\_action\_config\] table.

    The MECM Action Configuration table displays the list of action configurations.

6.  From the list of configurations, select and edit **Restart service using name**.

7.  In the **Action input** field, add the script GUID.

    \[Omitted image "mecm-restart-service.png"\] Alt text: MECM restart service

8.  Click **Save**.


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.md)

