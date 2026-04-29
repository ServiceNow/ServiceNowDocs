---
title: Configure Service Graph Connector for Microsoft Intune using the guided setup
description: Set up authentication credentials and a scheduled job to import Microsoft Intune data into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Microsoft Intune, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Intune using the guided setup

Set up authentication credentials and a scheduled job to import Microsoft Intune data into your CMDB.

## Before you begin

**Important:** The guided setup method is deprecated from version 2.7.0 of the Service Graph Connector for Microsoft Intune. Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Obtain the following information from your Microsoft Intune administrator:

-   Client ID
-   Client Secret
-   Token URL

For the connector to access the data in Microsoft Intune, the credential information is required to use the Microsoft Graph API. Therefore, you must grant the following Graph API permissions from the App registrations page in the Microsoft portal:

-   DeviceManagementManagedDevices.Read.All \(Type: Application\)
-   DeviceManagementApps.Read.All \(Type: Application\)
-   User.Read.All \(Type: Application\)

For more details on permissions, see [Service Graph Connector for Microsoft Intune - Troubleshooting connection issues](https://community.servicenow.com/community?id=community_blog&sys_id=a405ef9bdbbd7018bb4a474d13961903) on ServiceNow Community and [Microsoft Graph permissions reference](https://learn.microsoft.com/en-us/graph/permissions-reference) on the Microsoft documentation site.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   ServiceNow IntegrationHub Zip step \(com.glide.hub.action\_step.zip\), which is automatically installed.
-   ServiceNow IntegrationHub JSON Parser step \(com.glide.hub.action\_step.jsonparser\), which is automatically installed.

Multi-instance is supported for importing data from multiple Microsoft Intune instances in Service Graph Connector for Microsoft Intune version 2.1.1 and later. This feature involves dynamically creating data sources and scheduled imports, which requires the granting of additional permissions. The guided setup includes additional steps for this feature.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Intune** &gt; **Setup**.

2.  On the Getting Started page, select **Get started**.

3.  Configure the credentials.

    1.  On the Service Graph Connector for Microsoft Intune page, in the Configure the connection section, select the task **Configure credentials**.

    2.  On the next page, in the Configure credentials task section, select **Configure**.

    3.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the Microsoft Intune application. This field is automatically set.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL for the connection.Based on the region of your Microsoft Intune application, enter the connection URL in one of the following formats:

-   Global

    ```
https://graph.microsoft.com
    ```

-   US Government

    ```
https://graph.microsoft.us
    ```

-   China

    ```
https://microsoftgraph.chinacloudapi.cn
    ```

-   Germany

    ```
https://graph.cloudapi.de/
    ```

</td></tr><tr><td>

OAuth Client ID

</td><td>

The client ID of the Microsoft Intune application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The client secret of the Microsoft Intune application.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Callback URL for the Microsoft Intune application.Based on the region of your Microsoft Intune application, enter the token URL in one of the following formats:

-   Global

    ```
https://login.microsoftonline.com/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   US Government

    ```
https://login.microsoftonline.us/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   China

    ```
https://login.partner.microsoftonline.cn/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   Germany

    ```
https://login.microsoftonline.de/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

Where *&lt;tenantid&gt;* is the tenant ID of your Microsoft Intune application.

</td></tr></tbody>
</table>    4.  Select **Edit and Get OAuth Token**.

    5.  Go back to the guided setup page and for the Configure credentials task, select **Mark as Complete**.

4.  If needed, configure the MID Server.

    1.  In the Configure MID Server section, select **Configure**.

    2.  Select the **Use MID server** check box.

    3.  Select **Update** to save the record.

    **Note:** You do not need to update the other fields.

5.  Test the connection to the Microsoft Intune API.

    1.  In the Test the connection section, select **Configure**.

    2.  On the form, review the fields.

        |Field|Description|
        |:----|:----------|
        |Name|Unique name for this data source.|
        |Import set table label|Label of the table that will be created for this data source.|
        |Import set table name|Name of the table that will be created for this data source.|
        |Data in single column|Option to set to data in single column.|
        |Type|Data storage type of the data to be imported.|
        |Application|Application containing this record.|

    3.  Modify the properties in the Service Graph Connection Properties related list of the connection record.

        **Note:** Try to retain the default value of the **software\_path** property to ensure the proper retrieval of software details.

    4.  Select the **Test Connection** related link to start the testing process.

    5.  When the **Status** field is set to **Success**, return to the guided setup page.

        If any of the tests have errors, follow the suggestions for remediation.

    6.  In the Test the connection task section, select **Mark as Complete**.

6.  Add multiple instances.

    1.  On the left sidebar, select the Add Multiple Instances icon \(![Add Multiple Instances icon.](../image/duplicate-detection-rules.png)\).

    2.  On the Service Graph Connector for Microsoft Intune page, in the Add Multiple Instances section, select the Update Data Source Access task.

    3.  Select the **Global** application scope by using the application picker.

    4.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    5.  Select **Update** to close the tab and return to the guided setup.

    6.  Modify the application scope again to **Service Graph Connector for Microsoft Intune** by using the application picker.

    7.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.

    8.  Repeat the steps [6.c](configure-intune-integration.md#global) to [6.f](configure-intune-integration.md#app) for the Update Scheduled data import access task with the Scheduled data import \[scheduled\_data\_set\] table and set the task to complete by selecting **Mark as Complete**.

7.  Clear the cache for the new connection.

    1.  In the Clear Cache for Datasource and Import set section, select **Configure**.

    2.  In the **Run script** text box of the background script page, enter the following script:

        ```
        
              GlideTableManager.invalidateTable("sys_data_source");
              GlideCacheManager.flushTable("sys_data_source");
        
              GlideTableManager.invalidateTable("scheduled_import_set");
              GlideCacheManager.flushTable("scheduled_import_set");
        
              GlideTableManager.invalidateTable("sys_db_object");
              GlideCacheManager.flushTable("sys_db_object");
        ```

    3.  Select **Run Script** to run the background script in the **global** scope.

        The script may take several minutes to execute.

    4.  After the script is executed, select **Close**.

    5.  From the application picker, select the **Service Graph Connector for Microsoft Intune** application.

    6.  Select **Mark as Complete**.

8.  To either add or save the connection, select **Configure** for the Create or Edit connection task.

    -   To add a connection, select **Add Connection**.
    -   To save the edits for the existing connection, select **Edit**.
    **Note:** Obtain the following information from your Microsoft Intune administrator:

    -   Client ID
    -   Client Secret
    -   Token URL
    When a Microsoft Intune administrator registers an application, the Client ID, Client Secret, and Token URL will be available. To get more information about how to register an application, see the [Microsoft Intune documentation site](https://docs.microsoft.com/en-us/mem/intune/developer/intune-graph-apis).

    1.  On the form, fill in the fields or edit as needed.

<table id="table_vyj_kgv_y4b"><thead><tr><th>

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

Connection URL for the new connection.Based on the region of your Microsoft Intune application, enter the connection URL in one of the following formats:

-   Global

    ```
https://graph.microsoft.com
    ```

-   US Government

    ```
https://graph.microsoft.us
    ```

-   China

    ```
https://microsoftgraph.chinacloudapi.cn
    ```

-   Germany

    ```
https://graph.cloudapi.de/
    ```

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID for the Microsoft Intune application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret for the Microsoft Intune application.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Callback URL for the Microsoft Intune application.Based on the region of your Microsoft Intune application, enter the token URL in one of the following formats:

-   Global

    ```
https://login.microsoftonline.com/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   US Government

    ```
https://login.microsoftonline.us/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   China

    ```
https://login.partner.microsoftonline.cn/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

-   Germany

    ```
https://login.microsoftonline.de/*&lt;tenantid&gt;*/oauth2/v2.0/token
    ```

Where *&lt;tenantid&gt;* is the tenant ID of your Microsoft Intune application.

</td></tr></tbody>
</table>    2.  Either add or save the connection.

        -   To create the new connection, select **Create and Get OAuth Tokens**.
        -   To save the edits for the existing connection, select **Edit and Get OAuth Token**.
    3.  Navigate back to the guided setup and select **Mark as Complete**.

    4.  Set up the MID Server for the connection you created.

        1.  In the Configure Mid Servers section, select **Configure**.
        2.  Select the name of the connection you created.
        3.  Select the **Use MID server** check box.
        4.  Select **Update**.
        5.  When you're finished with the task, select **Mark as Complete**
9.  Test the API connection to import data from the Microsoft Intune application.

    1.  Test the connection, in the Test New Connections section, by selecting **Configure**.

        1.  Select the name of the data source associated with the newly created connection.
        2.  Select the **Test Connection** related link to start the process.
        3.  Optionally modify the properties in the Service Graph Connection Properties related list.

<table id="table_f4m_xhf_4yb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

The version of the Microsoft Intune Graph API.

</td></tr><tr><td>

software\_path

</td><td>

The path of the software code for finding apps and associated devices or vice versa. Leave the property value as is.

</td></tr><tr><td>

include\_primary\_user\_details

</td><td>

Enable retrieving the details of the primary user during import and populating the **assigned\_to** attribute in the records of the cmdb\_ci table by setting the property value to `true`. For retrieving the enrolled user details, set the property value to `false`.Retrieving primary user details increases the time for importing data because of additional API calls.

**Note:** When a user is assigned to a device initially, the enrolled and primary users are the same. If the device is reassigned to another user, the primary user name is reassigned to the new user, but the enrolled user is still the original enrolled user name.

</td></tr><tr><td>

include\_ip\_address\_details

</td><td>

Enable retrieving the IP addresses of devices during import and populate the records in the cmdb\_ci\_ip\_address table by setting the property value to `true`. To skip retrieving IP addresses, set the property to `false`.Retrieving IP addresses increases the time for importing data because of additional API calls.

</td></tr></tbody>
</table>            **Note:** The properties in the Service Graph Connection Properties related list of the connection record are modifiable. However, try to retain the default value of the **software\_path** property to ensure the proper retrieval of software details.

        4.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        5.  Return to the guided setup and select **Mark as Complete** for the Test New Connections task.
10. Set up the scheduled import jobs.

    1.  For the Configure scheduled jobs task in the Set up scheduled import jobs section, select **Configure**.

    2.  Select the name of the scheduled import you want to run.

    3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Update**.

    5.  Set the Configure scheduled jobs task to complete by selecting **Mark as Complete**.

11. Use advanced options to resolve server errors and improve performance with the SG-Intune Computer, SG-Intune Devices, and SG-Intune Software data sources while importing a large number of devices into the Microsoft Intune portal.

    **Note:**

    -   The SG-Intune Device Reports data source serves as an alternative to the SG-Intune Computer and SG-Intune Devices data sources, importing the same information while optimizing the data retrieval process by minimizing API calls and reducing import time.
    -   The SG-Intune Software Reports data source serves as an alternative to the SG-Intune Software data source.
    -   Both the SG-Intune Device Reports and SG-Intune Software Reports data sources require the paid ServiceNow IntegrationHub Professional Pack Installer \(com.glide.hub.integrations.professional\) plugin.
    -   To enable the creation of attachments, the **glide.attachment.extensions** system property must be set to either null or `zip, json`.

        For more information, see the [Service Graph Connector For Microsoft Intune – Advanced \[KB1641546\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1641546) article in the Now Support Knowledge Base.

    1.  Configure the scheduled jobs to import data using the SG-Intune Device Reports and SG-Intune Software Reports data sources.

        1.  In the Advanced \[Beta\] section, for the Configure scheduled jobs for advanced data sources task, select **Configure**.
        2.  In the Scheduled jobs list, select **SG-Intune Trigger Device Reports** job.
        3.  On the Scheduled Script Execution form, verify the field values for the scheduled job and select the **Active** check box.

            For more information, see [Schedule script execution form](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=australia&pubname=australia-platform-administration&ft:locale=en-US#t_ScheduleScriptExecution).

        4.  Select **Update**.
        5.  To activate the scheduled job for the SG-Intune Software Reports data source, repeat steps [11.a.ii](configure-intune-integration.md#select-job) to [11.a.iv](configure-intune-integration.md#exe-job) by selecting the **SG-Intune Trigger Software Reports** scheduled job.
        6.  Return to the guided setup page and set the Configure scheduled jobs for advanced data sources task to complete by selecting **Mark as Complete**.
        **Important:**

        -   Deactivate the SG-Intune Computer and SG-Intune Devices scheduled imports after setting up the SG-Intune Trigger Device Reports scheduled job for the SG-Intune Device Reports data source.
        -   Deactivate the SG-Intune Software scheduled import after setting up the SG-Intune Trigger Software Reports scheduled job.
        -   Activate the ServiceNow IntegrationHub Professional Pack Installer \(com.glide.hub.integrations.professional\) plugin on your instance.
        For more information, see the [Service Graph Connector For Microsoft Intune – Advanced \[KB1641546\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1641546) article in the Now Support Knowledge Base.

    2.  Configure the scheduled import for the SG-Intune Device Reports and SG-Intune Software Reports data sources.

        1.  In the Advanced \[Beta\] section, for the Configure the scheduled import for advanced data sources task, select **Configure**.
        2.  In the Scheduled Data Imports list, select the **SG-Intune Device Reports** scheduled import.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled data import and select the **Active** check box.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Update**.
        5.  Return to the guided setup page and set the Configure the scheduled import for advanced data sources task to complete by selecting **Mark as Complete**.
        **Important:** Verify that the SG-Intune Device Reports scheduled import is configured to run 3 hours after the SG-Intune Trigger Device Reports and SG-Intune Trigger Software Reports scheduled jobs.

        Example: If the SG-Intune Trigger Device Reports job is set for 9 a.m. and SG-Intune Trigger Software Reports for 10 a.m. daily, schedule the SG-Intune Device Reports scheduled import for 1 p.m. daily.

    3.  When using multiple instances, update the permissions on the Scheduled Script Execution \[sys\_autoscript\] table so that you can add scheduled jobs for the new connections.

        1.  For the Update scheduled job access task, select **Configure**.
        2.  Select the **Global** application scope from the application picker.
        3.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes.
        4.  Select  **Update**.
        5.  Switch back to the Service Graph Connector for Microsoft Intune application scope using the application picker.
        6.  Return to the guided setup page and set the Update scheduled job access task to complete by selecting **Mark as Complete**.
    4.  When using multiple instances, clear the Scheduled Script Execution \(sysauto\_script\) table cache to configure scheduled jobs for the new connections.

        1.  For the Clear cache for scheduled job task, select **Configure**.
        2.  Select the **Global** application scope from the application picker.
        3.  In the **Run script** field, enter the following code:

            ```
            GlideTableManager.invalidateTable("sysauto_script"); 
            GlideCacheManager.flushTable("sysauto_script"); 
            GlideTableManager.invalidateTable("sys_db_object"); 
            GlideCacheManager.flushTable("sys_db_object");
            ```

        4.  Select  **Run Script**.
        5.  Switch back to the Service Graph Connector for Microsoft Intune application scope using the application picker.
        6.  Return to the guided setup page and set the Clear cache for scheduled job task to complete by selecting **Mark as Complete**.
    5.  When using multiple instances, create advanced data sources, scheduled jobs, and scheduled imports for the new connections.

        **Tip:** You can create additional connections for multiple instances by following the instructions in the [Add Multiple Instances](configure-intune-integration.md#add-multi-instance) section of the guided setup.

        1.  For the Set up advanced data sources for multiple instances task, select **Configure**.
        2.  On the form, fill in the fields to configure your scheduled job details for the new connection.

<table id="table_uhc_5nx_dcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instance Prefix to Data source and Scheduled data import sets

</td><td>

Identifier that is used in all of the data source and scheduled import names for this distinct SG-Intune connection. In a multiple instance deployment, keep prefix short, meaningful identifier that enables you to identify a set of related data sources.**Note:** Try to keep the prefix the same as your connection name.

</td></tr><tr><td>

Connection and Credentials Alias

</td><td>

Connection alias that was created in the previous step.

</td></tr><tr><td>

Run Scheduled Import as User

</td><td>

User to populate the field on the scheduled data import.

</td></tr></tbody>
</table>        3.  Select **Submit** to create scheduled imports for your new connection.
        4.  To activate any newly created scheduled jobs, repeat steps [11.a.ii](configure-intune-integration.md#select-job) to [11.a.iv](configure-intune-integration.md#exe-job).
        5.  To activate any newly created parent scheduled import, repeat steps [11.b.ii](configure-intune-integration.md#data-import-start) to [11.b.iv](configure-intune-integration.md#data-import-exe).
        6.  Return to the guided setup page and set the Set up advanced data sources for multiple instances task to complete by selecting **Mark as Complete**.

