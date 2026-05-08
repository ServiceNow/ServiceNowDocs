---
title: Configure Service Graph Connector for Microsoft SCCM using the guided setup
description: Set up and validate data source connection credentials to import Microsoft SCCM data into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft SCCM using the guided setup

Set up and validate data source connection credentials to import Microsoft SCCM data into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

Confirm that you are in the Service Graph Connector for Microsoft SCCM application scope by using the application picker.

**Note:** If you’re currently using a version of the Microsoft SCCM plugin, see .

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   Integration - JDBC \(com.snc.integration.jdbc\)
-   Windows MID Server required for access to the SCCM environment.

To access Microsoft SCCM data, you must have appropriate access to the Microsoft SCCM database. You must have sufficient credentials to query the SQL Server that contains the Microsoft SCCM database. You must do the following:

1.  Create a SQL Server account to connect to the Microsoft SCCM database on the MID Server to use the data sources.
2.  Connect to your Microsoft SCCM SQL Server and configure the following:
    1.  Add a new login user name and password for SQL authentication.
    2.  Choose the Microsoft SCCM database that ServiceNow data sources will connect to.
    3.  Assign the db\_datareader role membership to the Microsoft SCCM user.

**Note:** If you have the Service Graph Connector for Microsoft SCCM version 2.1.6 or earlier versions installed in your production environment, contact Customer Service and Support for additional steps to remove the SCCM Discovery Source from being included when calculating the subscription unit consumption.

Starting with Service Graph Connector for Microsoft SCCM version 3.0.4, support for multi-instance is introduced, enabling Service Graph Connector for Microsoft SCCM to connect to and import data from multiple Microsoft SCCM instances. This feature involves dynamically creating data sources and scheduled imports, requiring the granting of additional permissions. For more information about how to complete these steps, see [Service Graph Connector for Microsoft 3.0 Setup Guidelines \[KB1001248\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1001248) in Now Support.

Air gap connections are available from version 3.7.0 of the Service Graph Connector for Microsoft SCCM. You can add either standard data sources or air gap data sources by using SGC Central. See [Configure Service Graph Connector for Microsoft SCCM using SGC Central](../../sgc-central/task/sgcc-configure-sccm-integ.md).

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **SCCM** &gt; **Setup**.

2.  On the Getting Started page, select **Get Started**.

3.  On the Service Graph Connector for Microsoft SCCM page, in the Configure Data source and Scheduled data import access section, select the task **Configure Data source access**.

4.  Update the data source access to enable creating data sources and scheduled data imports for a new connection in the Service Graph Connector for Microsoft SCCM.

    1.  For the Configure Data source access task, select **Configure**.

    2.  Select the **Global** application scope by using the application picker.

    3.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    4.  Select **Update** to close the tab and return to the guided setup.

    5.  Modify the application scope again to **Service Graph Connector for Microsoft SCCM** by using the application picker.

    6.  Set the **Update Data Source Access** task to complete by selecting **Mark as Complete**.

    7.  Repeat the steps [4.b](configure-sccm-integration.md#global) to [4.e](configure-sccm-integration.md#app) for the Update Scheduled data import access task with the Scheduled data import \[scheduled\_data\_set\] table and set the task to complete by selecting **Mark as Complete**.

5.  Configure the authentication credentials and configuration used for connecting to the Microsoft SCCM database.

    -   To establish a JDBC connection to the SCCM database, proceed to step [5.a](configure-sccm-integration.md#substep_lsz_jdh_g3c).
    -   To use Windows JDBC-integrated authentication, proceed to step [5.b](configure-sccm-integration.md#substep_tnj_mdh_g3c).
    1.  Use a user name and password to establish a JDBC connection to the SCCM database.

        **Note:** Perform this step only when you want to use a user name and password to establish a JDBC connection. Otherwise, select **Skip** to skip the step.

        1.  For the Configure connection task in the Configure the connection section, select **Configure**.
        2.  Configure the connection.
            -   To configure the connection available by default, select **Configure** for the SCCM JDBC Connection Credentials connection.
            -   To create another connection, select **Add Connection**.

                **Note:** You can create multiple connections by selecting **Add Connection**. If not redirected to the connection setup, on the Workflow Studio Integrations page search for SCCM JDBC Connection Credentials to modify the default connection or add another connection.

        3.  On the form, fill in the fields.

<table id="table_u3c_zqg_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Information

</td></tr><tr><td>

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

Format

</td><td>

JDBC driver used for connecting to the Microsoft SCCM database.Microsoft SCCM uses Microsoft SQL Server as its database backend. This field is automatically set to **com.microsoft.sqlserver.jdbc.SQLServerDriver**. Leave the field value as is.

</td></tr><tr><td>

Host

</td><td>

Network address of the server where the Microsoft SQL Server database is located.

</td></tr><tr><td>

Database name

</td><td>

Name of the Microsoft SQL Server database that Microsoft SCCM uses.

</td></tr><tr><td>

Override default port

</td><td>

Custom port of the Microsoft SQL Server instance.The default port for Microsoft SQL Server is 1433

</td></tr><tr><td>

Instance name

</td><td>

Microsoft SQL Server instance.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use the MID Server for accessing the JDBC server.

</td></tr><tr><td>

MID Server

</td><td>

MID Server for the connection.**Note:** It’s required to select a MID Server for an Integrated Authentication connection.

For the **SCCM JDBC Connection Credentials** option.

</td></tr><tr><td class="sub-head" colspan="2">

Credential Information

</td></tr><tr><td>

Username

</td><td>

User name for connecting to the JDBC server.

</td></tr><tr><td>

Password

</td><td>

Password for the JDBC server.

</td></tr></tbody>
</table>            **Note:** The new user must be assigned the db\_datareader role membership. For more information, see [Create a database user](https://learn.microsoft.com/en-us/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-ver15).

        4.  Save your changes.
            -   For the default connection, select **Configure Connection**.
            -   For a new connection, select **Create Connection**.
        5.  Navigate back to the guided setup and set the Configure connection task to complete by selecting **Mark as Complete**.
    2.  Use Windows JDBC-integrated authentication, which uses domain credentials, for authenticating a JDBC connection to the SCCM database.

        **Note:** Perform this step if you need the JDBC connection with integrated authentication. Otherwise, select **Skip** to skip the step.

        1.  For the Configure connection \(Integrated authentication\) task in the Configure the connection section, select **Configure**.
        2.  Configure the connection.
            -   To configure the connection available by default, select **Configure** for the SCCM JDBC Conn Cred \(Integrated Auth\) connection.
            -   To create another connection, select **Add Connection**.

                **Note:** You can create multiple connections by selecting **Add Connection**. If not redirected to the connection setup, on the Workflow Studio Integrations page section search for SCCM JDBC Conn Cred \(Integrated Auth\) to modify the default connection or add another connection.

        3.  On the form, fill in the fields.

<table id="table_ggr_htg_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Microsoft SCCM connection record.

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

Name of the Microsoft SQL Server database that Microsoft SCCM uses.

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

MID Server for the connection.

</td></tr></tbody>
</table>            **Note:** The account that runs the MID Server agent must have the db\_datareader role to access the SCCM DB.

        4.  Save your changes.
            -   For the default connection, select **Configure Connection**.
            -   For a new connection, select **Create Connection**.
        5.  Navigate back to the guided setup and set the Configure connection \(Integrated authentication\) task to complete by selecting **Mark as Complete**.
6.  Configure the connection and connector properties to map attributes and manage data imports.

    1.  Enable mapping asset tags from Microsoft SCCM to the asset tag attribute in the Computer \[cmdb\_ci\_computer\] class.

        1.  For the Configure Connection Properties task in the Configure Data Source and Scheduled Data Import section, select **Configure**.
        2.  In the Name column, select the connection.
        3.  In the Service Graph Connection Properties related list, select **asset\_tag** in the Property column.
        4.  In the **Value** field, enter `true` to enable mapping asset tags.
        5.  Select **Update**.
        6.  Navigate back to guided setup and set the Configure Connection Properties task to complete by selecting **Mark as Complete**.
    2.  Test the Computer Identity data source to verify that all data sources are properly connected.

        1.  For the Validate Data Sources task in the Configure Data Source and Scheduled Data Import section, select **Configure**.
        2.  In the Name column, select the Computer Identity data source associated with the connection.
        3.  Select **Test Load 20 Records**.
        4.  When the **State** field is set to **Complete** and the **Completion code** field is set to **Success**, select the **Return to data source** link.
        5.  Navigate back to guided setup and set the Validate Data Sources task to complete by selecting **Mark as Complete**.
    3.  Ensure that all data from the Computer Identity source is imported without the date time filtering during the next test load.

        1.  For the Reset 'Last run datetime' in test load data source task in the Configure Data Source and Scheduled Data Import section, select **Configure**.
        2.  In the Name column, select the Computer Identity data source associated with the connection.
        3.  Clear the **Use last run datetime** check box.
        4.  Select **Update**.
        5.  Navigate back to guided setup and set the Reset 'Last run datetime' in test load data source task to complete by selecting **Mark as Complete**.
7.  Configure the process for importing disk data when the Discovery application is running.

    1.  Avoid creating duplicate records in the CMDB Disks \[cmdb\_ci\_disk\] table.

        **Note:** You can avoid creating duplicate records in the CMDB Disks \[cmdb\_ci\_disk\] table when the Discovery application is running by configuring the **sn\_sccm\_integrate.sccm\_disks\_managed** property and setting its value to `true`. By default, the property value is set to `false`.

        1.  For the Configure Disk Data Imports task in the Configure Disk Data Imports section, select **Configure**.
        2.  On the System Property page, set the value of the **sn\_sccm\_integrate.sccm\_disks\_managed** property to `true`.
        3.  Select **Update**.
        4.  Set the Configure Disk Data Imports task to complete by selecting **Mark as Complete**.
        **Note:** Any existing disk records are updated only after the next hardware scan is executed in the Microsoft SCCM instance.

    2.  Transform imported disk name to disk number format.

        **Note:** You can set the imported disk name to the format `Disk #*&lt;disknumber&gt;*`. Where *&lt;disknumber&gt;* is the number extracted from the imported disk name.

        1.  Select the **Integration Commons for CMDB** application scope from the application picker.
        2.  For the Configure Disk Name Transformation task in the Configure Disk Data Imports section, select **Configure**.
        3.  On the System Property page, set the value of the **sn\_cmdb\_int\_util.transform\_disk\_name\_to\_discovery\_format** property to `true`.
        4.  Select **Update**.
        5.  From the application picker, select the Service Graph Connector for Microsoft SCCM application scope.
        6.  Set the Configure Disk Name Transformation task to complete by selecting **Mark as Complete**.
8.  Configure the scheduled data imports.

    **Note:** If the **Use Integrated Authentication** check box is selected for the data source, the run as user for the scheduled data import job must have the import\_admin role. For more information, see the ["Use Integrated Authentication" is being unchecked when you run the scheduled import related to SG-SCCM or SG-SCCM Computer Identity Data Source \[KB1312810\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1312810) article in the Now Support Knowledge Base.

    1.  For the Configure scheduled jobs task in the Configure scheduled jobs task section, select **Configure**.

    2.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see Schedule a data import.

        All other Service Graph Connector for Microsoft SCCM scheduled jobs that are active will run in their specified order after the Computer Identity scheduled job is finished running. Select the **Active** check box for a scheduled job to activate the job.

        **Important:** If you are upgrading to the Service Graph Connector for Microsoft SCCM, deactivate the existing 'SG-SCCM Computer Identity scheduled data import'. Additionally, you cannot use the baseline scheduled data import or data sources that have a name starting with 'SG-SCCM' because they are used as templates for creating an instance of data sources and scheduled data imports.

    3.  Select **Update**.

    4.  Set the Configure Scheduled data imports task to complete by selecting **Mark as Complete**.

    5.  When upgrading the Service Graph Connector for Microsoft SCCM, deactivate the existing SG-SCCM Computer Identity scheduled data import.

        For the Deactivate Legacy Scheduled Data Imports task, select **Configure**.

    6.  In the Name column, select the SG-SCCM Computer Identity scheduled data import and clear the **Active** check box.

    7.  Set the Deactivate Legacy Scheduled Data Imports task to complete by selecting **Mark as Complete**.

9.  Customize the Instance Data source SQL statement.

    1.  For the Customizing Data source SQL statement task in the Customize Instance Data source SQL statement section, select **Configure**.

    2.  Select the name of the instance in which you want to customize the SQL statement.

    3.  Select **Update**.

    4.  Set the Customizing Data source SQL statement task to complete by selecting **Mark as Complete**.


To resolve issues when configuring the connector, you can view the following additional resources:

-   [How to identify and delete duplicate CMDB CI Relationship records or ones that have orphan or missing parent/child relationships \[KB0780988\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0780988) in the Now Support Knowledge Base
-   [How to delete sys\_object\_source records \[KB0746309 \]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0746309) in the Now Support Knowledge Base
-   [Duplicate software installs with different Discovery Source \[KB0958768\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0958768) in the Now Support Knowledge Base
-   [Assigned To Field Doesn't Get Updated For Computer CIs in Service Graph Connector for SCCM \[KB1277555\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1277555) in the Now Support Knowledge Base
-   [Service Graph connector for Microsoft SCCM software usages data import](https://www.servicenow.com/community/cmdb-blog/service-graph-connector-for-microsoft-sccm-software-usages-data/ba-p/2274907) blog post on the ServiceNow Community site

**Related topics**  


[Service Graph Connector for Microsoft SCCM](../concept/cmdb-integration-sccm.md)

[CMDB classes targeted in Service Graph Connector for Microsoft SCCM](../reference/cmdb-sccm-classes.md)

[Configure Service Graph Connector for Microsoft SCCM using SGC Central](../../sgc-central/task/sgcc-configure-sccm-integ.md)

[Enable Software Editions in Service Graph Connector for Microsoft SCCM](enable-software-editions-sccm.md)

[Accessing the connection details of Service Graph Connector for Microsoft SCCM](../concept/sgc-cmdb-sccm-conn.md#)

[Configuring air gap connections for Microsoft SCCM](../concept/sgc-sccm-airgap.md)

