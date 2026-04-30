---
title: Configure Service Graph Connector for Observability - Dynatrace using guided setup
description: Use the Service Graph Connector for Observability - Dynatrace to ingest Configuration Management Database \(CMDB\) data from Dynatrace using REST APIs. This connector is the second generation of the Service Graph Connector for Observability - Dynatrace application developed by ServiceNow.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 16
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - Dynatrace using guided setup

Use the Service Graph Connector for Observability - Dynatrace to ingest Configuration Management Database \(CMDB\) data from Dynatrace using REST APIs. This connector is the second generation of the Service Graph Connector for Observability - Dynatrace application developed by ServiceNow.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   The Observability Commons for CMDB \(sn\_observability\) plugin, which is only required for event ingestion and must be installed before installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** To access the Dynatrace API, you need an access token with Read entities \(entities.read\) scope.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Dynatrace Observability** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  Set impact values for clusters and have the connector get access to the SNC.ImpactManager API.

    **Note:** This step appears when Observability Commons is installed.

    1.  On the Setup page, in the Enable Access To SNC.Impact Manager section, select the **Copy Script to Global Scope** task.

    2.  In the Copy Script to Global Scope section, copy the script.

        1.  Select **Configure**.
        2.  Switch to the global scope.
        3.  Select the Additional actions icon \(![Additional actions icon](../image/menu-icon.png)\).
        4.  Select **Insert and Stay**.
        5.  Select **Mark as Complete**.
    3.  In the Verify script is copied properly section, verify the script.

        1.  Select **Configure**.
        2.  Select the **EvtMgmtImpactManagerMediator** script and verify it was copied to the global scope.
        3.  In the **Accessible from** field, ensure it is set to **All application scopes**.
        4.  Select **Mark as Complete**.
4.  Configure the basic setup.

    1.  On the Setup page, in the Basic section, select the **Configure Auth Token for Dynatrace** task.

    2.  On the next page, in the Configure Auth Token for Dynatrace section, configure the authentication token.

        1.  Select **Configure**.
        2.  In the **API Key** field, enter `api-token <your api token>`.

            For example, `api-token mytokenid`.

        3.  Select **Mark as Complete**.
    3.  In the Configure HTTP Connection for Dynatrace section, configure the HTTP connection.

        1.  Select **Configure**.
        2.  Update the **Host** field with a fully qualified hostname for your Dynatrace instance.

            For example, `abc123.live.dynatrace.com`.

            The hostname is automatically filled in the **Connection URL** field.

        3.  Enable the use of a MID Server, select the **Use MID Server** check box.

            **Note:** The HTTP connection will be pre-configured to use the API key that was configured during the previous setup task.

        4.  Select **Mark as Complete**.
    4.  Test the HTTP connection.

        1.  In the Test Connection section, select **Configure**.
        2.  To test the connection configuration, select **Test Connection**.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        3.  Set the Test Connection task to complete by selecting **Mark as Complete**.
    5.  In the Create Default Notification Payload Template section, select **Configure**.

        **Note:** You need an access token with the following scopes:

        -   Read configuration \(ReadConfig\)
        -   Write configuration \(WriteConfig\)
        -   Read log content \(LogExport\)
        -   Read metrics \(metrics.read\)
        -   Read settings \(settings.read\)
        -   Write settings \(settings.write\)
        -   Read logs \(logs.read\)
        1.  Update the name of the payload template, if needed.
        2.  Select **Problem Notification Setup**.
        3.  Set the Create Default Notification Payload Template task to complete by selecting **Mark as Complete**.
    6.  If you want to support multiple instances, in the Upgrade Source Native Keys section, select **Configure**.

        1.  In the **Run script** text box of the background script page, enter the following script:

            ```
            var gr = new GlideRecord("sys_object_source");
            gr.addQuery("name", "SGO-Dynatrace");
            var grOR = gr.addQuery("id", "STARTSWITH", "HOST-");
            grOR.addOrCondition("id", "STARTSWITH", "PROCESS_GROUP_INSTANCE-");
            grOR.addOrCondition("id", "STARTSWITH", "PROCESS_GROUP-");
            grOR.addOrCondition("id", "STARTSWITH", "SERVICE-");
            grOR.addOrCondition("id", "STARTSWITH", "APPLICATION-");
            gr.query();
            while (gr.next()) {
                gr.setValue("id", "f379137e075820107add6a77c4a93538|||" + gr.getValue("id"));
                gr.update();
            }
            ```

        2.  Select **Run Script** to run the background script in the **global** scope.

            The script may take several minutes to execute.

        3.  After the script is executed, select **Close**.
        4.  From the application picker, select the **Service Graph Connector for Observability Dynatrace** application.
        5.  Select **Mark as Complete**.
5.  For a Grail-enabled tenant, configure the OAuth 2.0 client credentials and test the connection.

    For more information on Dynatrace OAuth credentials, see [Authentication for the Account Management API](https://docs.dynatrace.com/docs/dynatrace-api/basics/dynatrace-api-authentication/account-api-authentication) on the Dynatrace documentation site.

    1.  Set the Dynatrace Grail status to indicate whether using the Grail-enabled tenant.

        **Note:**

        You can check Grail enablement by contacting your Dynatrace administrator.

        1.  In the Configure Dynatrace Grail OAuth section of the Service Graph Connector for Observability Dynatrace Setup page, select **Get Started**.
        2.  For the Set Dynatrace Grail status task, select **Configure** and review or modify the property settings for a Grail-enabled tenant.
        3.  If you've Grail-enabled tenant, set the **Value** field of the **grailEnabled** property to `true`.

            Else, leave the value set to `false`.

        4.  Set the Configure Dynatrace Grail OAuth task to complete by selecting **Mark as Complete**.
    2.  Add a new OAuth connection.

        **Note:** You need an OAuth token with the following scope permissions in Grail:

        -   storage:logs:read
        -   storage:buckets:read
        1.  In the Configure OAuth credentials section, select **Configure**.
        2.  On the Workflow Studio page that opens in a new browser tab, select **Add Connection**.
        3.  Enter a name, the connection URL, OAuth client ID, and OAuth client secret details.
        4.  Select **Create and Get OAuth Token**.
        5.  Return to the guided setup page.
        6.  Set the Configure OAuth credentials task to complete by selecting **Mark as Complete**.
    3.  Test the new OAuth connection.

        1.  In the Test Connection section, select **Configure**.
        2.  To test the connection configuration, select **Test Connection**.
        3.  When the **Status** field is set to **Success**, select **Update** to close the Test the connection dialog box and return to the guided setup page.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test Connection task to complete by selecting **Mark as Complete**.
6.  Set up the additional configurations.

    1.  On the Guided setup page, in the Advanced section, select the **Advanced settings** task.

    2.  In the Advanced Settings section, select **Configure** and review or modify the existing settings for a custom configuration.

        You can configure the following settings:

        -   Review the page size used in REST API requests to fetch Dynatrace entities.
        -   Define number of days a configuration item \(CI\) can be inactive before it is ignored.
        -   Enter the percentage of an application cluster's nodes that need to be in a state to raise that state to its parent in the service map.

            For example, you can define the percentage of nodes that need to go critical for the parent of a cluster to be in a critical state. If there are 10 nodes in a cluster, setting the property value to `70` would require at least 7 out of the 10 nodes in the cluster to go into a critical state to reflect up to the parent service of the cluster.

        -   Enable ingesting events that do not have a matching CI in the CMDB.
        -   Enable populating the Application \(cmdb\_ci\_appl\) CIs from Dynatrace \(Dynatrace processes\) during scheduled imports.
    3.  Select **Save**.

    4.  Select **Mark as Complete** for the Advanced Settings task.

    5.  Configure connection properties for the Dynatrace connection.

        1.  In the Configure Instance Settings section, select **Configure**.
        2.  In the Service Graph Connection Properties related list, configure the properties of the connection record.

<table id="table_orp_332_4yb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

managementZoneNames

</td><td>

Enter the name of the management zone to fetch from your Dynatrace environment. For multiple entries, separate the zone names with commas.

</td></tr><tr><td>

tags

</td><td>

Enter the name of the tags to fetch from your Dynatrace environment. For multiple entries, separate the tags with commas.

</td></tr><tr><td>

serviceTypes

</td><td>

Enter the list of Dynatrace service types from where to ingest the data into CMDB. For multiple entries, separate the service types with commas.**Note:** All service types except for DATABASE\_SERVICE are mapped to the Calculated Application Service \[cmdb\_ci\_service\_calculated\] CMDB table. The DATABASE\_SERVICE service type is mapped to the Database Instance \[cmdb\_ci\_db\_instance\] CMDB table.

Valid values are:

-   BACKGROUND\_ACTIVITY
-   CICS\_SERVICE
-   CUSTOM\_SERVICE
-   DATABASE\_SERVICE
-   ENTERPRISE\_SERVICE\_BUS\_SERVICE
-   EXTERNAL
-   IBM\_INTEGRATION\_BUS\_SERVICE
-   IMS\_SERVICE
-   MESSAGING\_SERVICE
-   QUEUE\_LISTENER\_SERVICE
-   RMI\_SERVICE
-   RPC\_SERVICE
-   WEB\_REQUEST\_SERVICE
-   WEB\_SERVICE


</td></tr><tr><td>

managementZoneIds

</td><td>

Enter the management zone ID to fetch from your Dynatrace environment. For multiple entries, separate the zone IDs with commas.

</td></tr></tbody>
</table>        3.  Select **Update**.
        4.  Complete the Configure Instance Settings task by selecting **Mark as Complete**.
    6.  Execute the **Fix Older Ids** fix script to migrate the IDs of the imported data from the previous format to the latest format of the object IDs.

        **Note:** Beginning with the 1.9.0 version of the Service Graph Connector for Observability - Dynatrace, the latest format of the object IDs, which is Base64 Encoding, is used for data import. The **Fix Older Ids** fix script migrates any existing data with previous object IDs to the latest format.

    7.  Configure the notification settings.

        The setup enables pulling ITOM events from Dynatrace into the ServiceNow instance.

        1.  In the Configure Problem Notification section, select **Configure**.
        2.  To push the configuration to Dynatrace, select **Problem Notification Setup**.
        3.  To receive the configuration from Dynatrace, select **Fetch Notification Setup**.
        4.  Complete the Configure Problem Notification task by selecting **Mark as Complete**.
7.  Clean up records from the previous instance.

    **Note:** If you are not migrating from the previous Dynatrace version, you can skip this step.

    1.  On the Setup page, in the Clean Up Records From Previous Integration section, select the **Execute the New Integration** task.

    2.  On the next page, in the Execute the New Integration section, select **Configure** and select **Update**.

    3.  Select **Mark as Complete**.

    4.  In the Verify Integration Execution Has Completed section, verify the integration execution.

        1.  Select **Configure**.
        2.  In the **State** field, wait for the field to change to **Complete** or **Complete with errors**.

            It is normal to have errors during the migration from an older version.

        3.  To refresh the list, select and hold \(or right-click\) the header and select **Refresh List**.
        4.  Select **Mark as Complete**.
    5.  In the Delete Application Services Left Over From Previous Version section, select **Configure** to delete any application services that you no longer need from the previous integration.

    6.  Select **Mark as Complete**.

    7.  In the Cleanup Identification Remnants - Copy Script section, copy the script.

        1.  Select **Configure**.
        2.  Change the current scope to **Global**.
        3.  Select the menu icon \(![Menu icon.](../image/menu-icon.png)\).
        4.  Select **Insert and Stay**.
        5.  Select **Mark as Complete**.
    8.  In the Cleanup Identification Remnants - Execute Script section, execute the script.

        1.  Select **Configure**.
        2.  Select the record of the script you copied.
        3.  Select **Update**.
8.  Add multiple instances.

    **Note:** If you do not need to add multiple instances, you can skip this step.

    1.  In the Add Multiple Instances section of the Service Graph Connector for Observability - Dynatrace page, select **Get Started**.

    2.  Update the data source access to create a data source for the new connection.

        1.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table.
        2.  For the Update Data Source Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update** to return to the guided setup page.
        6.  Select the **Service Graph Connector for Observability Dynatrace** application scope from the application picker.
        7.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.
    3.  Update the scheduled data import access to create a scheduled import for the new connection.

        1.  Ensure that you have edit permissions for the Scheduled data import \[scheduled\_import\_set\] table.
        2.  For the Update Scheduled Data Import Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update** to return to the guided setup page.
        6.  Select the **Service Graph Connector for Observability Dynatrace** application scope from the application picker.
        7.  Set the Update Scheduled Data Import Access task to complete by selecting **Mark as Complete**.
    4.  Update the value access to create the data source for the new connection.

        1.  Ensure that you have edit permissions for the Value \[sys\_variable\_value\] table.
        2.  For the Update Value Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update** to return to the guided setup page.
        6.  Select the **Service Graph Connector for Observability Dynatrace** application scope from the application picker.
        7.  Set the Update Value Access task to complete by selecting **Mark as Complete**.
    5.  Clear the data source and import set cache for the new connection.

        1.  For the Clear Cache for Datasource and Import set task, select **Configure**.
        2.  In the **Run script** text box of the background script page, enter the following script:

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

        3.  Select **Run Script** to run the background script in the **global** scope.

            The script may take several minutes to execute.

        4.  After the script is executed, select **Close**.
        5.  Select the **Service Graph Connector for Observability Dynatrace** application scope from the application picker.
        6.  Set the Clear Cache for Datasource and Import set task to complete by selecting **Mark as Complete**.
    6.  Add another connection.

        1.  Ensure that the application scope is set to **Service Graph Connector for Observability** in the application picker.
        2.  For the Add Another Connection task, select **Configure**.
        3.  On the Workflow Studio page that opens in a new browser tab, select **Add Connection**.
        4.  On the form, fill in the fields.

<table id="table_vyj_kgv_y4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Display name for the connection.

</td></tr><tr><td>

Connection Hostname

</td><td>

Host name of the Dynatrace instance.

</td></tr><tr><td>

API Key

</td><td>

Dynatrace API Key.**Note:** The API Key must be prefixed with `api-token`.

</td></tr></tbody>
</table>        5.  Select **Create Connection**.
        6.  Return to the guided setup page.
        7.  Set the Add Another Connection task to complete by selecting **Mark as Complete**.
    7.  If using a Grail-enabled tenant, configure additional OAuth 2.0 connections.

        1.  For the Add another OAuth connection task, select **Configure**.
        2.  On the Workflow Studio page that opens in a new browser tab, select **Add Connection**.
        3.  Enter a name, the connection URL, OAuth client ID, and OAuth client secret details.
        4.  Select **Create and Get OAuth Token**.
        5.  Return to the guided setup page.
        6.  Set the Add another OAuth connection task to complete by selecting **Mark as Complete**.
    8.  If using a Grail-enabled tenant, select the OAuth 2.0 client credentials alias created earlier in the Add another OAuth connection task.

        1.  For the Link connection record with OAuth client credentials task, select **Configure**.
        2.  In the **OAuth 2.0 Connection and Credentials Alias** field, search for and select the OAuth connection alias you created in the step [8.g](configure-dynatrace-integration.md#substep_bbt_zxg_s1c).
        3.  In the **Service Graph connection record**, search for and select the connection record you created in step [8.f](configure-dynatrace-integration.md#substep_x21_3yg_s1c).
        4.  Select **Submit**.
        5.  Return to the guided setup page.
        6.  Set the Link connection record with OAuth client credentials task to complete by selecting **Mark as Complete**.
    9.  Set up the MID Server for the connection you created.

        1.  For the Configure Mid Servers task, select **Configure**.
        2.  Select the name of the connection you created.
        3.  Select the **Use MID server** check box.
        4.  Select **Update**.
        5.  Set the Configure Mid Servers task to complete by selecting **Mark as Complete**.
    10. Configure the instance settings.

        1.  In the Configure Instances section, select **Configure**.
        2.  Select the name of the connection you want to configure and then select **Update**.
        3.  Set the Configure Instances task to complete by selecting **Mark as Complete**.
    11. Test the new connections.

        1.  For the Test Connections task, select **Configure**.
        2.  Select the name of the connection you want to test.
        3.  To validate the data source configuration, select **Test Load 20 Records**.
        4.  When the **Status** field is set to **Success**, select **Update** to close the Test the connection dialog box and return to the guided setup page.

            If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test Connections task to complete by selecting **Mark as Complete**.
    12. Create default notification payload templates.

        1.  Ensure that you have the access token with the following scopes:
            -   Read configuration \(ReadConfig\)
            -   Write configuration \(WriteConfig\)
            -   Read log content \(LogExport\)
            -   Read metrics \(metrics.read\)
        2.  For the Create Default Notification Payload Templates task, select **Configure**.
        3.  Select the connection you want to create a default notification payload template for.
        4.  Update the name of the payload template, if needed.
        5.  Select **Problem Notification Setup**.

            The notification is created with the payload parameters as described in the following table.

<table id="table_cjc_gfn_jzb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Name of the notification. The name is automatically prefixed with `ServiceNow Default Problem Notification` and the instance name is added to it.

</td></tr><tr><td>

alertingProfile

</td><td>

ID of the alerting profile in Dynatrace.

</td></tr><tr><td>

type

</td><td>

Type of payload that is automatically set to `webhook`.

</td></tr><tr><td>

url

</td><td>

Webhook URL in the format `https://https://<instance name>.service-now.com/ /api/sn_em_connector/em/inbound_event?source=SGO-Dynatrace`.

</td></tr><tr><td>

payload

</td><td>

Custom payload created for notification in the following format:```
{  

  "ImpactedEntities": {ImpactedEntities},  

  "ImpactedEntity": "{ImpactedEntity}",  

  "PID": "{PID}",  

  "ProblemDetailsHTML": "{ProblemDetailsHTML}",  

  "ProblemDetailsJSON": {ProblemDetailsJSON},  

  "ProblemDetailsMarkdown": "{ProblemDetailsMarkdown}",  

  "ProblemDetailsText": "{ProblemDetailsText}",  

  "ProblemID": "{ProblemID}",  

  "ProblemImpact": "{ProblemImpact}",  

  "ProblemSeverity": "{ProblemSeverity}",  

  "ProblemTitle": "{ProblemTitle}",  

  "ProblemURL": "{ProblemURL}",  

  "State": "{State}",  

  "Tags": "{Tags}"  

} 
```

</td></tr></tbody>
</table>        6.  Repeat the steps for each connection.
        7.  Set the Create Default Notification Payload Templates task to complete by selecting **Mark as Complete**.
9.  Set up scheduled import jobs.

    1.  In the Set up scheduled import jobs section of the Service Graph Connector for Observability - Dynatrace page, select **Get Started**.

    2.  For the Configure the scheduled import jobs task, select **Configure**.

    3.  Select the name of the scheduled import you want to run.

    4.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Update**.

    6.  Set the Set up scheduled import jobs task to complete by selecting **Mark as Complete**.


