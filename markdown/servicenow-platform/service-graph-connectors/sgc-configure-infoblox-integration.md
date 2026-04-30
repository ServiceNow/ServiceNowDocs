---
title: Configure Service Graph Connector for Infoblox using the guided setup
description: Pull in data from Infoblox into your CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 9
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Infoblox using the guided setup

Pull in data from Infoblox into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** If you have an earlier version of the Service Graph Connector for Infoblox, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Infoblox application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Infoblox** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the authentication credentials and HTTP connection details for sending requests to the Infoblox API.

    1.  Configure your Infoblox authentication credentials.

        1.  In the Configure the connection section of the Service Graph Connector for Infoblox page, select **Get Started**.
        2.  For the Configure Infoblox authentication credentials task, select **Configure** to open the Basic Auth Credentials page opens in a new browser tab.
        3.  In the **Name** field, enter a name for the authentication.

            For example, `Infoblox Credential`.

        4.  In the **User name** field, enter the user name that is used to authenticate the HTTP request when this authentication profile is enabled.
        5.  In the **Password** field, enter the password for the user name that is used to authenticate the HTTP request.
        6.  Select **Update**to return to the guided setup page.
        7.  Set the Configure Infoblox authentication credentials task to complete by selecting **Mark as Complete**.
    2.  Configure the Infoblox connection settings.

        1.  For the Configure Infoblox HTTP connection task, select **Configure**to open the HTTP\(s\) Connection page in a new browser tab.
        2.  Review the fields and in the **Name** field and enter the Infoblox instance name.
        3.  Use the URL builder to build the connection string or in the **Connection URL** field, enter the Infoblox base URL in the following format: `https://*&lt;base-URL&gt;*`.
        4.  In the **api\_version** field of the Attributes section, enter the [version of WAPI](https://ipam.illinois.edu/wapidoc/) you’re using.
        5.  In the **network\_view** field of the Attributes section, enter the network views for which data is to be imported.

            For multiple views, separate the views with commas. For example: `view1,view2`. If you leave this field empty, the data sources import data from all the network views.

        6.  Select **Update**to return to the guided setup page.
        7.  Set the Configure Infoblox HTTP connection task to complete by selecting **Mark as Complete**.
        For more information about the Infoblox API, see the [Infoblox Developer documentation](https://www.infoblox.com/wp-content/uploads/infoblox-deployment-infoblox-rest-api.pdf).

    3.  Configure the connection properties.

        1.  For the Configure connection properties task, select **Configure** to open the Service Graph Connections page in a new browser tab.
        2.  To review and modify the property details, select a property from the **Property** column in the Service Graph Connection Properties related list.
        3.  Select **Update** on the Service Graph Connection Properties page.
        4.  Select **Update** on the Service Graph Connections page to return to the guided setup page.
        5.  Set the Configure connection properties task to complete by selecting **Mark as Complete**.
    4.  Test the Infoblox API connection to import data from the Infoblox application.

        1.  In the Configure the connection section of the Service Graph Connector for Infoblox page, select **Continue**.
        2.  For the Test the connection task, select **Configure**to open the Service Graph Connections page in a new browser tab.
        3.  Select **Test Connection**.
        4.  When the **Status** field is set to **Success**, select **Update** to close the Test the connection dialog box and return to the guided setup page.

            If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test the connection task to complete by selecting **Mark as Complete**.
5.  Add multiple instances.

    **Note:** If you don't need to add multiple instances, you can skip this step.

    1.  In the Add Multiple Instances section of the Service Graph Connector for Infoblox page, select **Get Started**.

    2.  For the Update Data Source Access task, select **Configure**.

    3.  Select the Data Source \[sys\_data\_source\] table.

    4.  Select the **Global** application scope by using the application picker.

    5.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    6.  Select **Update** to close the tab and return to the guided setup.

    7.  Modify the application scope again to **Service Graph Connector for Infoblox** by using the application picker.

    8.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.

    9.  For the Update Scheduled Data Import Access task, select **Configure**.

    10. Select the Scheduled data import \[scheduled\_import\_set\] table.

    11. Repeat steps [5.d](sgc-configure-infoblox-integration.md#substep_cyy_1hv_zfc) to [5.g](sgc-configure-infoblox-integration.md#substep_j1l_bhv_zfc).

    12. Set the Update Scheduled Data Import Access task to complete by selecting **Mark as Complete**.

    13. Clear the cache for the new connection.

        1.  For the Clear Cache for Data Source and Scheduled Data Imports tables task, select **Configure**.
        2.  Select the **Global** application scope by using the application picker.
        3.  In the **Run script** text box of the background script page, enter the following script:

            ```
            GlideTableManager.invalidateTable("sys_data_source");
            GlideCacheManager.flushTable("sys_data_source");
            
            GlideTableManager.invalidateTable("scheduled_import_set");
            GlideCacheManager.flushTable("scheduled_import_set");
            
            GlideTableManager.invalidateTable("sys_db_object");
            GlideCacheManager.flushTable("sys_db_object");
            ```

        4.  Select **Run Script** to run the background script.

            The script may take several minutes to execute.

        5.  After the script is executed, select **Close**.
        6.  Modify the application scope again to **Service Graph Connector for Infoblox** by using the application picker.
        7.  Set the Clear Cache for Data Source and Scheduled Data Imports tables task to complete by selecting **Mark as complete**.
    14. Add a basic authentication connection to the new Infoblox instance.

        1.  For the Add Another Basic Auth Connection task, select **Configure**.
        2.  To create a new connection, select **Add Connection**.
        3.  In the Connection Information section of the Create Connection window, fill in the fields.

<table id="table_x3l_r3v_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Infoblox connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Infoblox base URL in the following format: `*&lt;base-URL&gt;*`.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

MID Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID server** check box is selected.

</td></tr><tr><td>

MID Application

</td><td>

Name of the MID application used by the connector.This field appears only when the **Use MID server** check box is selected.

</td></tr></tbody>
</table>        4.  In the Credential Information section of the Create Connection window, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Username|Infoblox account user name that is used to authenticate the connection request.|
            |Password|Password that is used to authenticate the connection request.|

        5.  Select **Create Connection**.
        6.  Navigate back to the guided setup, and set the Add Another Basic Auth Connection task to complete by selecting **Mark as Complete**.
    15. Test the newly added connections.

        1.  For the Test connections task, select **Configure**.
        2.  From the **Name** column, select the new connection.
        3.  Select the **Test Connection** related link to start the testing process.
        4.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test connections task to complete by selecting **Mark as Complete**.
6.  Configure the IP address management tasks and user groups.

    1.  Enable properties to create an IP address management task when deleting or inserting a network.

        1.  In the Configure IP address management tasks section of the Service Graph Connector for Infoblox page, select **Get Started**.
        2.  For Enable creating a task, select **Configure**to open the Enable create Task page in a new browser tab.
        3.  Select the **Create a task when a network is deleted** and **Create a task when a network is inserted** check boxes to enable properties for creating IP address management tasks when deleting and inserting a network, respectively.
        4.  Select **Save**.
        5.  Close the Enable create Task page tab and return to the guided setup page.
        6.  Set Enable creating a task to complete by selecting **Mark as Complete**.
    2.  Configure the user group for IP address management tasks.

        1.  For the Configure the user group for IP address management tasks task, select **Configure**to open the SG Infoblox Connection page in a new browser tab.
        2.  In the **Connection alias** field, review and change the connection alias.
        3.  In the **Task user group** field, change the assignment group for the connection alias.

            **Note:** By default, the user group for the IP address management tasks is assigned to the IP Address Management user group. To change the default assignment group, change the task user group for the connection alias.

        4.  Select **Update**to return to the guided setup page.
        5.  Set the Configure the user group for IP address management tasks task to complete by selecting **Mark as Complete**.
7.  Configure the scheduled jobs to import data from the Infoblox application.

    1.  In the Set up scheduled import jobs section of the Service Graph Connector for Infoblox page, select **Get started**.

    2.  For the Configure the scheduled jobs task, select **Configure**to open the Scheduled Data Imports page in a new browser tab.

    3.  From the **Name** column, select the scheduled job that you want to activate.

    4.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Update**.

    6.  Repeat the steps [7.c](sgc-configure-infoblox-integration.md#select-job) to [7.e](sgc-configure-infoblox-integration.md#exe-job) for each scheduled job for data import.

    7.  Close the Scheduled Data Imports page tab and return to the guided setup page.

    8.  Set the Configure the scheduled jobs task to complete by selecting **Mark as Complete** in the guided setup.


