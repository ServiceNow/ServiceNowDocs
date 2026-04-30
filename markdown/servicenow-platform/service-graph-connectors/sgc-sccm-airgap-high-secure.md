---
title: Configure air gap solution for Microsoft SCCM in a high-secure server
description: Configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your high-secure server.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-09-05"
reading_time_minutes: 2
breadcrumb: [Configuring air gap connections, Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure air gap solution for Microsoft SCCM in a high-secure server

Configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your high-secure server.

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

    3.  Download the `SgSCCMHighSecureSetup.ps1` and `GetSCCMData.ps1` PowerShell scripts from the link provided in the Download Airgap Scripts section.

4.  Log on to your high-secure server.

5.  Create a Microsoft SCCM directory.

    All the configurations required for the air gap solution are created in the Microsoft SCCM directory.

6.  Copy the `GetSCCMData.ps1` and `SgSCCMHighSecureSetup.ps1` PowerShell scripts that you downloaded in step [3.c](sgc-sccm-airgap-high-secure.md#substep_rj5_lbw_4gc) to the Microsoft SCCM directory.

7.  Start a PowerShell session, and run the `SgSCCMHighSecureSetup.ps1` script to generate the JSON configuration file that is used by the `GetSCCMData.ps1` script.

    1.  At the prompt, enter the path for the Microsoft SCCM data directory that you created in step [5](sgc-sccm-airgap-high-secure.md#step_e1p_mbw_4gc).

    2.  Enter a name for the configuration file, or press the Return key to accept the default value.

    3.  Enter the values for the global properties, or press the Return key to accept the default values.

        -   **logDirectory**: Specify the location to store the log file from the `GetSCCMData.ps1` script.
        -   **host**: Specify the host name for your Microsoft SCCM instance.
        -   **dbname**: Specify the SCCM database name.
        -   **port**: Specify the port on which the Microsoft SCCM instance allows API calls.
        -   **pageSize**: Specify the number of records to be fetched in a Microsoft SCCM API call.
        -   **credentialsPath**: Specify the location to store the Microsoft SCCM credentials XML file.
    4.  Specify names for the data source data directories, or press the Return key to accept the default values.

        The directories are created if they don’t already exist.

    5.  Enter the Microsoft SCCM credentials in the **Windows PowerShell credential request** pop-up window.

    6.  Exit the PowerShell session.

8.  Provide write and delete permissions for the Microsoft SCCM data directory and the child directories \(created in step [5](sgc-sccm-airgap-high-secure.md#step_e1p_mbw_4gc)\) to the account that will run the `GetSCCMData.ps1` script.

    Delete permissions are required for old records to be cleaned up.


**Related topics**  


[Configure air gap solution for Microsoft SCCM in a low-secure server](sgc-sccm-airgap-low-secure.md)

