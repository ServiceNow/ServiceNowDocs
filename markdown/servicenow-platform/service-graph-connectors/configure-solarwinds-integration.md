---
title: Configure Service Graph Connector for SolarWinds
description: Set up authentication credentials and scheduled jobs to import SolarWinds data into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for SolarWinds

Set up authentication credentials and scheduled jobs to import SolarWinds data into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-license-module.md), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Before you start the configuration, navigate to **System Definition** &gt; **Business Rules**, and deactivate the **ValidateServiceAccountID** business rule.

Air gap connections are available from version 2.5.0 of the Service Graph Connector for SolarWinds. You can set up either regular data sources or air gap data sources. Before you set up air gap data sources, you must configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure server and low-secure server. See [Configuring air gap connections for Service Graph Connector for SolarWinds](../concept/airgap-solarwinds.md).

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_ActivateTheDiscoveryPlugin.md).
-   SolarWinds Orion Platform.
-   SolarWinds Server &amp; Application Monitor and/or Network Performance Monitor.

Roles required:

-   To configure the ServiceNow platform: admin
-   To access SolarWinds data: User with SWIS \(SolarWinds Information Service\) access \(the same as through the Orion website, not database users\).

## About this task

**Note:** SolarWinds Integration can work with or without Service &amp; Application Monitor \(SAM\) and Network Performance Monitor \(NPM\) being installed.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **SolarWinds** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  Configure your authentication credentials used to connect to the SolarWinds SWIS API.

    1.  On the Service Graph Connector for SolarWinds page, in the Configure the connection section, select the **Configure the authentication credentials used to connect to SolarWinds SWIS API** task.

    2.  For the Configure the authentication credentials used to connect to SolarWinds SWIS API task, select **Configure**.

    3.  Fill in the fields on the Basic Auth Credentials form.

<table id="table_wr5_3fv_wlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Human-readable name for this credential. This field is automatically set. You can optionally change this setting.

</td></tr><tr><td>

User name

</td><td>

SolarWinds user name.**Note:** The SolarWinds user must have a role with read privileges to the SolarWinds Information Service API for all SolarWinds data sources that the integration can pull data.

</td></tr><tr><td>

Password

</td><td>

SolarWinds password that is stored in the database in encrypted form.

</td></tr><tr><td>

Active

</td><td>

Option to check whether this credential is active.

</td></tr><tr><td>

Credential alias

</td><td>

Advanced selection criteria for this credential.

</td></tr><tr><td>

Order

</td><td>

Order in which credentials are tried. Smaller numbers are tried first.

</td></tr></tbody>
</table>    4.  Select **Update** if required.

    5.  Set the Configure the authentication credentials used to connect to the SolarWinds SWIS API task to complete by selecting **Mark as Complete**.

4.  Configure the SolarWinds HTTP connection.

    1.  For the Configure SolarWinds HTTP connection task, select **Configure**.

    2.  Review the HTTP\(s\) Connection form, and fill in the fields as required.

        |Field|Description|
        |:----|:----------|
        |Name|Name of the connection. This field is automatically set. You can optionally change the name.|
        |Use MID server|Option to enable the connection to use a MID server.|
        |Host|Target host value used by the connection. This field is automatically set by the connection URL.|
        |Credential|Credential value used by the connection.|
        |Connection alias|Connection alias value with which the connection can be referred.|
        |URL builder|URL builder that is used to build the connection URL.|
        |Mutual authentication|Option to enable mutual authentication.|
        |Protocol|Underlying protocol used by the connection.|
        |Active|Option to activate the HTTP connection.|
        |Domain|Domain to which the connection belongs.|
        |Override default port|Target port value used by the connection.|
        |Base path|Base path for HTTP\(S\) connection that is required but should not be modified.|

    3.  Select **Update**, if required.

    4.  Set the Configure SolarWinds HTTP connection task to complete by selecting **Mark as Complete**.

5.  Configure the SolarWinds modules.

    1.  For the Configure SolarWinds Modules task, select **Configure**.

    2.  Update the **Value** for the **sn\_solarwinds\_inte.npm\_installed** and the **sn\_solarwinds\_inte.sam\_installed** properties in one of the following ways:

        -   If the respective module is installed on the SolarWinds instance, then set the fields to **true**.
        -   If the respective module is not installed on the SolarWinds instance, then set the fields to **false**.
        **Note:** This update changes the API class and the data that is returned from them.

    3.  Set the Configure SolarWinds Modules task to complete by selecting **Mark as Complete**.

6.  Test the connection.

    1.  For the Test the connection task, select **Configure**.

    2.  Review the fields on the Data Source form, which are automatically set.

        |Field|Description|
        |:----|:----------|
        |Name|Unique name for this data source.|
        |Import set table label|Label of the table that will be created for this data source.|
        |Import set table name|Name of the table that will be created for this data source.|
        |Type|Data storage type of the data to be imported.|
        |Data in single column|Data in single column.|
        |Application|Application containing this record.|
        |Data stream action|The Data Source request action that will be invoked to get data.|

    3.  Test the connection by selecting the **Test Load 20 Records** related link.

        Testing the connection takes a few moments, after which the page refreshes to show the test results.

        This step tests the SG-Solarwinds Hardware data source, and verifies that data is loaded into the staging table. A successful connection for the SG-Solarwinds Hardware data source means that all SolarWinds data sources connect successfully, so you do not need to individually test all data sources.

        The connection is successful if the **HTTP Status** is **200**. If there is an **Error Code** and **Error Message**, the connection failed and further troubleshooting is required.

    4.  Navigate back to the guided setup, and set the Test the connection task to complete by selecting **Mark as Complete**.

7.  Add multiple instances.

    **Note:** If you do not need to add multiple instances, you can skip this step.

    1.  On the Service Graph Connector for SolarWinds page, in the Add Multiple Instances section, select the **Update Data Source Access** task.

    2.  For the Update Data Source Access task, select **Configure**.

    3.  Select the Data Source \[sys\_data\_source\] table.

    4.  Select the **Global** application scope by using the application picker.

    5.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    6.  Select **Update** to close the tab and return to the guided setup.

    7.  Modify the application scope again to **Service Graph Connector for SolarWinds** by using the application picker.

    8.  Set the **Update Data Source Access** task to complete by selecting **Mark as Complete**.

    9.  Repeat the steps [7.d](configure-solarwinds-integration.md#global) to [7.g](configure-solarwinds-integration.md#app) for the Update Scheduled Data Import Access task with the Scheduled data import \[scheduled\_data\_set\] table and for the Update Value Access task with the Value \[sys\_variable\_table\] table, and set the tasks to complete by selecting **Mark as Complete**.

8.  Clear the cache for the new connection.

    1.  Select the **Clear Cache for Datasource and Import set** task, and then select **Configure**.

    2.  Clear the cache by selecting **Global** from the Scope menu.

    3.  Enter the following script.

        ```
        
              GlideTableManager.invalidateTable("sys_data_source");
              GlideCacheManager.flushTable("sys_data_source");
        
              GlideTableManager.invalidateTable("scheduled_import_set");
              GlideCacheManager.flushTable("scheduled_import_set");
        
              GlideTableManager.invalidateTable("sys_variable_value");
              GlideCacheManager.flushTable("sys_variable_value");
        
              GlideTableManager.invalidateTable("sys_db_object");
              GlideCacheManager.flushTable("sys_db_object");
        ```

    4.  Select **Run Script**.

    5.  From the Scope menu, select **Service Graph Connector for SolarWinds**.

    6.  Set the Clear Cache for Datasource and Import set task to complete by selecting **Mark as Complete**.

9.  Add a connection to another SolarWinds instance.

    **Note:** Confirm that the current scope is **Service Graph Connector for SolarWinds**.

    1.  Select the **Add Another Connection** task, and then select **Configure**.

    2.  In the Select Data Source Type section, select either regular data sources or air gap data sources.

        -   To add or edit regular data sources, select **Regular Data Sources**.
        -   To add or edit air gap data sources, select **Airgap Data Sources**.

            **Note:** Before you add an air gap data source, you must configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure and low-secure servers. See [Configuring air gap connections for Service Graph Connector for SolarWinds](../concept/airgap-solarwinds.md).

    3.  Either create or edit a connection.

        -   To create a new connection, select **Add Connection**.
        -   To edit an existing connection, select **Edit**.
    4.  Fill in or edit the fields on the form, as required.

        -   For regular data sources:

            |Field|Description|
            |-----|-----------|
            |Connection Name|Display name for the connection.|
            |Connection URL|Connection host name for SolarWinds.|
            |User name|User name for SolarWinds authentication.|
            |Password|Password for SolarWinds authentication.|

        -   For air gap data sources:

<table id="table_rkf_3jb_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Display name for the connection.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID server that you deployed in your low-secure server.See [Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server](sgc-cmdb-solarwinds-airgap-low-secure.md).

</td></tr><tr><td>

Parent Directory

</td><td>

Path of the SolarWinds directory where the data is stored in your low-secure server.

</td></tr><tr><td>

Archive Data After Retrieval

</td><td>

Option to archive data after retrieval.

</td></tr><tr><td>

Archive Path \[Optional\]

</td><td>

Folder where the data is to be archived if the **Archive Data After Retrieval** check box is selected.

</td></tr></tbody>
</table>    5.  Either add or save the connection.

        -   To add a new connection, select **Create Connection**.
        -   To save the edits for the existing connection, select **Edit Connection**.
    6.  Navigate back to the guided setup, and select **Mark as Complete** to set the Add Another Connection task to complete.

    7.  If required, set up the MID Server for the connection you created.

        1.  For the Configure Mid Servers task, select **Configure**.
        2.  Select the name of the connection you created.
        3.  Select the **Use MID server** check box.
        4.  Select **Update**.
        5.  Set the Configure Mid Servers task to complete by selecting **Mark as Complete**.
    8.  If required, configure the connections in the Configure SolarWinds Modules section by selecting **Configure**.

    9.  When you're finished, close the window, and navigate back to the guided setup.

    10. Set the Configure SolarWinds Modules task to complete by selecting **Mark as Complete**.

    11. For the Test New Connections task, select **Configure**.

        1.  Select the name of the data source associated with the newly created connection.
        2.  Select the **Test Load 20 Records** related link.

            **Note:** If the displayed completion code is `Success`, then the sources are validated. But if the displayed completion code is `Error`, then there is an error that you must fix.

        3.  Navigate back to the guided setup, and set the Test New Connections task to complete by selecting **Mark as Complete**.
10. Set up scheduled import jobs.

    1.  On the Service Graph Connector for SolarWinds page, in the Set up scheduled import jobs section, select the **Configure the scheduled import jobs** task.

    2.  For the Configure the scheduled import jobs task, select **Configure**.

    3.  Review the fields on the Scheduled Data Import form, which are automatically set.

        |Field|Description|
        |:----|:----------|
        |Name|Name of the scheduled job.|
        |Data source|Data source record that defines the data to import.|
        |Run as|Option to run the scheduled job with the credentials of the specified user.|
        |Active|Option to activate the scheduled job. Select this option.|
        |Concurrent Import|Function that loads the data from multiple import sets. The function then processes and transforms the data concurrently.|
        |Partition Method|Partition method for the concurrent import set.|
        |Partition Size|Import set size for early scheduling.|
        |Execute pre-import script|Option to run a pre-import script before the import is performed.|
        |Execute post-import script|Option to run a post-import script after the import is performed.|
        |Application|Application containing this record.|
        |Run|Frequency of running the import.|
        |Conditional|Conditions under which this job is executed.|

        **Note:** All active SolarWinds scheduled jobs will run in their specified order after the SG-Solarwinds Hardware scheduled job runs. You can modify the **Active** setting for each SolarWinds scheduled job as appropriate for your integration.

    4.  Select **Update** if required, and then select **Mark as Complete** to set the Set up scheduled import jobs task to complete.


**Related topics**  


[Service Graph Connector for SolarWinds](../concept/cmdb-integration-solarwinds.md)

[CMDB classes targeted in Service Graph Connector for SolarWinds](../reference/cmdb-solarwinds-classes.md)

[Configure Service Graph Connector for SolarWinds using SGC Central](../../sgc-central/task/sgcc-configure-solarwinds-integ.md)

[Accessing the connection details of Service Graph Connector for SolarWinds](../concept/sgc-cmdb-solarwinds-conn.md#)

[Configuring air gap connections for Service Graph Connector for SolarWinds](../concept/airgap-solarwinds.md)

