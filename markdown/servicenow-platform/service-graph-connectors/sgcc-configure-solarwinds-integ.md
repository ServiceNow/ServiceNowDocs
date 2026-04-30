---
title: Configure Service Graph Connector for SolarWinds using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for SolarWinds for pulling in SolarWinds data into the CMDB.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for SolarWinds using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for SolarWinds for pulling in SolarWinds data into the CMDB.

## Before you begin

Install Service Graph Connector for SolarWinds version 2.6.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Air gap connections are available from version 2.5.0 of the Service Graph Connector for SolarWinds. You can set up either standard data sources or air gap data sources. Before you set up air gap data sources, you must configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure server and low-secure server. See [Configuring air gap connections for Service Graph Connector for SolarWinds](../../configuration-management/concept/airgap-solarwinds.md).

Role required: admin

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../../configuration-management/image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Dashboard page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the SolarWinds connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Complete the setup for configuring the connector for importing data.

    1.  Select the data source type.

        1.  In the **Setup** stage of the playbook, select the **Select data source type** activity.
            -   Select **Standard data sources** if you're working with environments that have direct internet access.

                Proceed to step [5.c](sgcc-configure-solarwinds-integ.md#substep_j4h_31n_xfc).

            -   Select **Air gap data sources** if you're working with restricted environments that don't have direct internet access.
        2.  Select **Continue**.
    2.  Download and run the PowerShell scripts to set up an air gap connection.

        **Note:** Before you add an air gap connection, you must configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure and low-secure servers. See [Configuring air gap connections for Service Graph Connector for SolarWinds](../../configuration-management/concept/airgap-solarwinds.md).

        1.  In the **Setup** stage of the playbook, select the **Download PowerShell scripts** activity.

            The **Download PowerShell scripts** activity appears only when you select **Air gap data sources** as the data source type in step [5.a](sgcc-configure-solarwinds-integ.md#substep_flm_l2n_xfc).

        2.  Select **Download PowerShell scripts**.
        3.  Run the PowerShell scripts.

            For more information on configuring an air gap connection, see [Configuring air gap connections for Service Graph Connector for SolarWinds](../../configuration-management/concept/airgap-solarwinds.md).

        4.  After configuring the air gap connection, select **Continue**.
    3.  Create and test a connection.

        1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.
        2.  On the form, fill in the fields.
            -   For standard data sources:

<table id="table_dcb_bbn_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Display name for the connection.

</td></tr><tr><td>

Connection URL

</td><td>

Connection host name for SolarWinds.

</td></tr><tr><td>

User name

</td><td>

User name for SolarWinds authentication.

</td></tr><tr><td>

Password

</td><td>

Password for SolarWinds authentication.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. Select this check box.

</td></tr><tr><td>

MID selection

</td><td>

Select a MID Server from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr><tr><td>

MID application

</td><td>

Select a MID Server application from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>            -   For air gap data sources:

<table id="table_ht3_bbn_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Display name for the connection.

</td></tr><tr><td>

Parent directory

</td><td>

Path of the SolarWinds directory where the data is stored in your low-secure server.

</td></tr><tr><td>

Archive data after retrieval

</td><td>

Option to archive data after retrieval.

</td></tr><tr><td>

Archive path \[Optional\]

</td><td>

Folder where the data is to be archived if the **Archive data after retrieval** check box is selected.

</td></tr><tr><td>

MID server

</td><td>

Name of the MID Server that you deployed in your low-secure server.See [Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server](../../configuration-management/task/sgc-cmdb-solarwinds-airgap-low-secure.md).

</td></tr></tbody>
</table>        3.  Select **Create and test connection**.
        4.  Once the connection test is complete, select **Continue**.
    4.  Configure the properties of the connector to access resources.

        1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.
            -   Select **SAM installed** if a Service &amp; Application Monitor \(SAM\) module is installed on the SolarWinds instance.
            -   Select **NPM installed** if a Network Performance Monitor \(NPM\) module is installed on the SolarWinds instance.
        2.  Select **Continue**.
    5.  Configure the import schedule to import data at regular intervals.

        1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.
        2.  Expand the Parent scheduled data import within the Import schedules list, and select the SG-Solarwinds Hardware import schedule.
        3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Save**.

            Alternatively, select **Execute Now** to execute the import schedule immediately.

        5.  Select **Continue**.
    6.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for SolarWinds](../../configuration-management/concept/cmdb-integration-solarwinds.md)

[CMDB classes targeted in Service Graph Connector for SolarWinds](../../configuration-management/reference/cmdb-solarwinds-classes.md)

[Accessing the connection details of Service Graph Connector for SolarWinds](../../configuration-management/concept/sgc-cmdb-solarwinds-conn.md#)

[Configuring air gap connections for Service Graph Connector for SolarWinds](../../configuration-management/concept/airgap-solarwinds.md)

