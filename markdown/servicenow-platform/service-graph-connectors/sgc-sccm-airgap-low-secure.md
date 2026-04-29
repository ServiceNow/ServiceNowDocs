---
title: Configure air gap solution for Microsoft SCCM in a low-secure server
description: Configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your low-secure server after you finish the configuration in your high-secure server.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring air gap connections, Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure air gap solution for Microsoft SCCM in a low-secure server

Configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your low-secure server after you finish the configuration in your high-secure server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central** &gt; **Create connection**.

2.  Select the air gap template.

    1.  In the **Setup** stage of the playbook, select the **Select alias template** activity.

    2.  Select **SCCM Air Gap**.

    3.  Select **Continue**.

3.  Download and run the PowerShell scripts to set up an air gap connection.

    1.  In the **Setup** stage of the playbook, select the **PowerShell Script Download** activity.

    2.  Select **Download Airgap Scripts**.

    3.  Download the `SgSCCMLowSecureSetup.ps1` PowerShell script from the link provided in the Download Airgap Scripts section.

4.  Log on to your low-secure server.

5.  Create a Microsoft SCCM directory.

    All the configurations required for the air gap solution are created in the Microsoft SCCM directory.

6.  Copy the `SgSCCMLowSecureSetup.ps1` PowerShell script that you downloaded in step [3.c](sgc-sccm-airgap-low-secure.md#substep_tjm_wbw_4gc) to the Microsoft SCCM directory.

7.  Start a PowerShell session, and run the `SgSCCMLowSecureSetup.ps1` script.

    1.  At the prompt, enter the path for the Microsoft SCCM directory that you created in step [5](sgc-sccm-airgap-low-secure.md#step_fk2_xbw_4gc).

    2.  Specify names for the data source data directories, or press the Return key to accept the default values.

        The directories are created if they don’t already exist.

    3.  Exit the PowerShell session.

8.  Provide read and delete permissions for the Microsoft SCCM directory.


**Related topics**  


[Configure air gap solution for Microsoft SCCM in a ServiceNow instance](sgc-sccm-airgap-sn-instance.md)

