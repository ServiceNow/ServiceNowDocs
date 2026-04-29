---
title: Configure Service Graph Connector for Microsoft SCCM using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft SCCM for pulling in Microsoft SCCM data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft SCCM using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft SCCM for pulling in Microsoft SCCM data into the CMDB.

## Before you begin

Install Service Graph Connector for Microsoft SCCM version 3.5.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To access Microsoft SCCM data, you must have appropriate access to the Microsoft SCCM database. You must have sufficient credentials to query the SQL Server that contains the Microsoft SCCM database. You must do the following:

1.  Create a SQL Server account to connect to the Microsoft SCCM database on the MID Server to use the data sources.
2.  Connect to your Microsoft SCCM SQL Server and configure the following:
    1.  Add a new login user name and password for SQL authentication.
    2.  Choose the Microsoft SCCM database that ServiceNow data sources will connect to.
    3.  Assign the db\_datareader role membership to the Microsoft SCCM user.

Air gap connections are available from version 3.7.0 of the Service Graph Connector for Microsoft SCCM. You can add either standard data sources or air gap data sources. Before you set up air gap data sources, you must configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your high-secure server and low-secure server. See [Configuring air gap connections for Microsoft SCCM](../../configuration-management/concept/sgc-sccm-airgap.md).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Microsoft SCCM connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Select an air gap template ora template that matches the credentials for establishing a Java Database Connectivity \(JDBC\) connection to the SCCM database.

    1.  In the **Setup** stage of the playbook, select the **Select alias template** activity.

    2.  Select one of the following templates.

        -   **SCCM JDBC Connection Credentials**: Select this option to use a user name and password to establish a JDBC connection to the SCCM database.

            **Note:** The new user must be assigned the db\_datareader role membership. For more information, see [Create a database user](https://learn.microsoft.com/en-us/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-ver15).

        -   **SCCM Air Gap**: Select this option to use an air gap connection if you're working with restricted environments that don't have direct internet access \(see [Configuring air gap connections for Microsoft SCCM](../../configuration-management/concept/sgc-sccm-airgap.md)\).
        -   **SCCM JDBC Conn Cred \(Integrated Auth\)**: Select this option to use Windows JDBC-integrated authentication, which uses domain credentials, for authenticating a JDBC connection to the SCCM database.

            **Note:** The account that runs the MID Server agent must have the db\_datareader role to access the SCCM DB.

    3.  Select **Continue**.

        -   If you selected **SCCM Air Gap** in step [5.b](sgcc-configure-sccm-integ.md#substep_tk2_qgs_4gc), proceed to step [6](sgcc-configure-sccm-integ.md#step_bzt_lbh_g3c).
        -   If you selected either **SCCM JDBC Connection Credentials** or **SCCM JDBC Conn Cred \(Integrated Auth\)** in step [5.b](sgcc-configure-sccm-integ.md#substep_tk2_qgs_4gc), proceed to step [7](sgcc-configure-sccm-integ.md#step_skd_3hs_4gc).
6.  Download and run the PowerShell scripts to set up an air gap connection.

    The **PowerShell Script Download** activity appears only when you select **SCCM Air Gap** as the template in step [5.b](sgcc-configure-sccm-integ.md#substep_tk2_qgs_4gc).

    **Note:** Before you add an air gap connection, you must configure the air gap solution for the Service Graph Connector for Microsoft SCCM in your high-secure and low-secure servers. See [Configuring air gap connections for Microsoft SCCM](../../configuration-management/concept/sgc-sccm-airgap.md).

    1.  In the **Setup** stage of the playbook, select the **PowerShell Script Download** activity.

    2.  Select **Download Airgap Scripts**.

    3.  Run the PowerShell scripts.

    4.  After configuring the air gap connection, select the **I have read the instructions and executed the scripts accordingly** check box.

    5.  Select **Continue**.

7.  Enter connection details and test the API connection for importing Microsoft SCCM data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields on the form depending on the template you selected in step [5.b](sgcc-configure-sccm-integ.md#substep_tk2_qgs_4gc): [SCCM JDBC Connection Credentials](sgcc-configure-sccm-integ.md#li_dqk_g2h_g3c), [SCCM JDBC Conn Cred \(Integrated Auth\)](sgcc-configure-sccm-integ.md#li_dqk_g2h_g3c), or [SCCM Air Gap](sgcc-configure-sccm-integ.md#li_ncv_g2h_g3c).

        -   For the SCCM JDBC Connection Credentials and SCCM JDBC Conn Cred \(Integrated Auth\) templates:

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Microsoft SCCM connection record.For example, `SG-SCCM connection`.

</td></tr><tr><td>

Query timeout

</td><td>

Number of seconds the JDBC driver waits for a query to complete.`0` indicates no timeout. If the timeout is exceeded, the integration considers the JDBC result inaccessible and marks the result as an error.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of seconds before the MID Server connection cache pool closes the connection and removes the connection.`0` indicates no timeout.

</td></tr><tr><td>

Host

</td><td>

Network address of the server where the Microsoft SQL Server database is located.

</td></tr><tr><td>

Database name

</td><td>

Name of the Microsoft SQL Server database that SCCM uses.

</td></tr><tr><td>

Override default port

</td><td>

Custom port of the Microsoft SQL Server instance.The default port for Microsoft SQL Server is 1433

</td></tr><tr><td>

Instance name

</td><td>

Microsoft SQL Server instance.

</td></tr><tr><td>

MID Server

</td><td>

MID Server for the connection. Mandatory for an Integrated Authentication connection; recommended for all JDBC connections.

</td></tr><tr><td colspan="2">

**Note:** The following fields appear only when you select the **SCCM JDBC Connection Credentials** template in step [5](sgcc-configure-sccm-integ.md#alias-template).

</td></tr><tr><td>

Format

</td><td>

JDBC driver used for connecting to the SCCM database.SCCM uses Microsoft SQL Server as its database backend. This field is automatically set to **com.microsoft.sqlserver.jdbc.SQLServerDriver**. Leave the field value as is.

</td></tr><tr><td>

Username

</td><td>

User name for connecting to the JDBC server.

</td></tr><tr><td>

Password

</td><td>

Password for the JDBC server.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use the MID Server for accessing the JDBC server.

</td></tr></tbody>
</table>        -   For the SCCM Air Gap template:

<table id="table_zxl_g3s_4gc"><thead><tr><th>

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

Path of the Microsoft SCCM directory where the data is stored in your low-secure server.

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

Name of the MID Server that you deployed in your low-secure server.See [Configure air gap solution for Microsoft SCCM in a low-secure server](../../configuration-management/task/sgc-sccm-airgap-low-secure.md).

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

8.  Configure the connection and connector properties to map attributes and manage data imports.

    **Note:** To skip this step, select **Continue** for the **Configure properties** activity.

    1.  In the **Setup** stage of the playbook, select the **Configure properties** activity.

    2.  To map the asset tags from Microsoft SCCM to the asset tag attribute in the Computer \[cmdb\_ci\_computer\] class, in the Connection properties section of the Configure properties page, select the **Map asset tags** check box.

    3.  To avoid creating duplicate records in the CMDB Disks \[cmdb\_ci\_disk\] table when the Discovery application is running, in the Connector properties section of the Configure properties page, select the **Avoid creating duplicate records** check box.

    4.  To set the import disk name to the format starting with Disk \#\[*disknumber*\], in the Connector properties section of the Configure properties page, select the **Transform disk name to disk number** check box.

        Where the *disknumber* is the number extracted from the disk name

    5.  Select **Continue**.

9.  Modify the SQL statement for a data source.

    **Note:** To skip this step, select **Skip** for the **Customize data source SQL statement** activity.

    1.  In the **Setup** stage of the playbook, select the **Customize data source SQL statement** activity.

    2.  Double-click \(or use the keyboard shortcut\) the **Custom SQL statement** column value for a data source and enter the custom SQL statement.

    3.  Repeat the step [9.b](sgcc-configure-sccm-integ.md#custom-sql) for each data source where you want to modify the SQL statement.

    4.  Select **Mark Complete**.

10. Configure the import schedules to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **_Connection Name_-SCCM Computer Identity** import schedule.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

11. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Microsoft SCCM](../../configuration-management/concept/cmdb-integration-sccm.md)

[CMDB classes targeted in Service Graph Connector for Microsoft SCCM](../../configuration-management/reference/cmdb-sccm-classes.md)

[Enable Software Editions in Service Graph Connector for Microsoft SCCM](../../configuration-management/task/enable-software-editions-sccm.md)

[Accessing the connection details of Service Graph Connector for Microsoft SCCM](../../configuration-management/concept/sgc-cmdb-sccm-conn.md#)

[Configuring air gap connections for Microsoft SCCM](../../configuration-management/concept/sgc-sccm-airgap.md)

