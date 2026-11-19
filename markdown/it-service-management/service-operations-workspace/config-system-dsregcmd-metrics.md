---
title: Configure system overview - dsregcmd metrics
description: Configure the system overview - dsregcmd metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-operations-workspace/config-system-dsregcmd-metrics.html
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure system overview - dsregcmd metrics

Configure the system overview - dsregcmd metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Create a MECM script with the name `dsregcmd`.

    For more information, see [Create a script in Microsoft Endpoint Configuration Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/create-mecm-script.md).

3.  Provide the following code in the script block.

    ```
    dsregcmd /status
    ```

4.  Retrieve and copy the script GUID.

5.  Open the MECM Adapter Configuration \[sn\_mecm\_adapter\_config\] table.

    The MECM Adapter Configuration table displays the list of adapter configurations.

6.  From the list of configurations, select and edit **System information**.

7.  In the **Action input** field, add the script GUID.

    \[Omitted image "mecm-dsregcmd-edit.png"\] Alt text: System Overview dsregcmd

8.  Click **Update**.


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.md)

