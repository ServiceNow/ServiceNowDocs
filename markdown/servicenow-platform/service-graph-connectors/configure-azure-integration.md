---
title: Configure Service Graph Connector for Microsoft Azure using the guided setup
description: Set up data sources and scheduled import jobs to pull in data from Azure into your CMDB.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-01"
reading_time_minutes: 12
breadcrumb: [Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Azure using the guided setup

Set up data sources and scheduled import jobs to pull in data from Azure into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

**Important:** After the initial import of Azure data, the application performs a delta import of data. However, you can perform a full pull of data anytime later by disabling the delta synchronization and setting the **sn\_sg\_azure\_integ.is\_delta\_sync\_enabled** property to `false`. For more information, see [Configuring data synchronization in Service Graph Connector for Microsoft Azure](../concept/sgc-cmdb-azure-data-sync.md#).

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The connector uses the Azure Management APIs for the complete pull of data from Azure. However, to pull delta changes from Azure, the Azure Resource Graph APIs are used. The domain name system \(DNS\) is Microsoft Azure Management, but the path is a resource graph.

For more information on the Azure setup instructions, see the [Service Graph Connector for Azure - Overview](https://www.servicenow.com/community/cmdb-articles/service-graph-connector-for-azure-overview/ta-p/2301822) and [How do I configure the Azure Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/azure-service-graph-connector-version-1-12/ta-p/3308034) articles on the ServiceNow Community site.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Azure** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  Create data sources and scheduled imports for the new connection.

    1.  On the Service Graph Connector for Microsoft Azure page, in the Update Data Sources and Scheduled Imports Access, select the task **Update Scheduled Data Import Access**.

    2.  In the Update Scheduled Data Import Access section, select **Configure** and do the following:

        1.  For the Update Scheduled Data Import access task, select **Configure**.
        2.  Select the **Global** application scope by using the application picker.
        3.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.
        4.  Select **Update** to close the tab and return to the guided setup.
        5.  Modify the application scope again to **Service Graph Connector for Microsoft Azure** by using the application picker.
        6.  Set the Update Scheduled Data Import access task to complete by selecting **Mark as Complete**.
        7.  Repeat the steps [3.b.ii](configure-azure-integration.md#global) to [3.b.v](configure-azure-integration.md#app) for the Update Data Source Access task with the Data Source \[sys\_data\_source\] table and set the task to complete by selecting **Mark as Complete**.
    3.  Clear the cache for the new connection.

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
        5.  From the application picker, select the **Service Graph Connector for Microsoft Azure** application.
        6.  Select **Mark as Complete**.
4.  Create a connection to import hardware configuration items \(CIs\) from the Azure client application.

    **Note:** Ensure that you have the `User.Read` permission on the Microsoft Graph API for the hardware import.Also, ensure that the IAM policy for the Azure subscription has the Reader role. See [Assign a user as an administrator of an Azure subscription with conditions](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal-subscription-admin) on the Microsoft Azure documentation site.

    1.  Obtain the OAuth credentials from your Azure administrator.

        Make a note of the following details:

        -   Application \(client\) ID
        -   Client Secret
        -   Directory \(tenant\) ID
        -   Connection URL
        **Note:** After getting the OAuth credentials, in the guided setup for Service Graph Connector for Microsoft Azure, go to the Create connection for the hardware import section of theService Graph Connector for Microsoft Azure page and set the Get the OAuth credentials task to complete by selecting **Mark as Complete**.

    2.  Configure your Azure hardware connection and credentials.

        1.  In the Create connection for the hardware import section of the Service Graph Connector for Microsoft Azure page, select **Continue**.
        2.  For the Create or Edit connection task, select **Configure**.
        3.  On the Connections page of the Workflow Studio, select **Configure** for the **SG-Azure Hardware Connection** connection that is available by default for the hardware import.

            You can create multiple connections by selecting **Add Connection**.

        4.  On the form, review and modify the fields.

<table id="table_npd_v2z_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name to uniquely identify the hardware connection record. For example, `SG-Azure Hardware Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Azure client application. **Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td class="sub-head" colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token URL of your Azure client application.Based on the region of your Azure client application, enter the token URL in one of the following formats:

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

Where *&lt;tenantid&gt;* is the tenant ID of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr></tbody>
</table>        5.  Select **Configure and Get OAuth Token**.
        6.  When the OAuth token flow is successfully completed, return to the Create connection for the hardware import task page using the back button for your browser.
        7.  Set the Create or Edit connection task to complete by selecting **Mark as Complete**.
    3.  Test the Microsoft Graph API connection to import hardware data from the Azure client application.

        1.  For the Test Connection task, select **Configure**.
        2.  Select the data source associated with the newly created connection in the **Name** column of the Data Sources list.
        3.  Select the **Test Load 20 Records** related link.
        4.  When the state changes to **Complete**, return to the setup by selecting **Back to Guided Setup** in the Help panel.
        5.  Set the Test Connection task to complete by selecting **Mark as Complete**.
    4.  Review the scheduled data imports configuration.

        1.  For the Set up scheduled import jobs task, select **Configure**.
        2.  Select the **SG-Azure Subscriptions** scheduled job.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Update**.
        5.  Set the Set up scheduled import jobs task to complete by selecting **Mark as Complete** in the Help panel.
5.  Create a connection to import software information from the Azure client application.

    **Note:** Ensure that you have the `Data.Read` permission on the Log Analytics API for the software import.

    1.  Obtain the OAuth credentials and set up the Log Analytics workspace in the Azure.

        1.  Ensure that you have the OAuth credentials from step [4.a](configure-azure-integration.md#azure-oauth-details).
        2.  Configure the Log Analytics workspace in the Azure client application.

            -   Use an existing workspace, if available.
            -   Create another workspace.

                For more information, see [Create Log Analytics workspace](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/quick-create-workspace?tabs=azure-portal) in the Azure documentation.

            **Note:** Make a note of the Workspace ID.

        3.  Deploy Azure Monitor Agent \(AMA\), and then enable change tracking and inventory using AMA.

            For more information, see [Enable Change Tracking and Inventory using Azure Monitoring Agent](https://learn.microsoft.com/en-us/azure/automation/change-tracking/enable-vms-monitoring-agent) in the Azure documentationand the Configuring Azure for monitoring your Azure VMs section of the [How do I configure the Azure Service Graph Connector? \[KB2226163\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2226163) article in the Now Support Knowledge Base.

        **Note:** After obtaining the OAuth credentials, in the guided setup for Service Graph Connector for Microsoft Azure, go to the Create connection for the software import section of the Service Graph Connector for Microsoft Azure page and set the Get the OAuth credentials task to complete by selecting **Mark as Complete**.

    2.  Configure your Azure software connection and credentials.

        1.  In the Create connection for the software import section of the Service Graph Connector for Microsoft Azure page, select **Continue**.
        2.  For the Create or Edit connection task, select **Configure**.
        3.  On the Connections page of the Workflow Studio, select **Configure** for the **SG-Azure log analytics connection** connection that is available by default for the software import.

            You can create multiple connections by selecting **Add Connection**.

        4.  On the form, review and modify the fields.

<table id="table_vrd_2xz_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Information

</td></tr><tr><td>

Software Connection Name

</td><td>

Name to uniquely identify the software connection record. For example, `SG-Azure log analytics connection`.

</td></tr><tr><td>

Hardware Connection Name

</td><td>

Name of the hardware connection associated with the software as described in step [4.b.iv](configure-azure-integration.md#hw-connection).You add a hardware connection name to associate the software connection with the respective hardware.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Log Analytics workspace in the following format: ```
https://api.loganalytics.io/v1/workspaces/<workspace_id>
```

Where `<workspace_id>` is the ID of the Log Analytics workspace as described in step [5.a.ii](configure-azure-integration.md#config-log-ws). **Note:** This field is automatically set to the URL to connect to the Log Analytics workspace. Replace the `<workspace_id>` variable in the auto-generated URL with the workspace ID of your Log Analytics workspace.

</td></tr><tr><td class="sub-head" colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token URL of your Azure client application.Based on the region of your Azure client application, enter the token URL in one of the following formats:

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

Where *&lt;tenantid&gt;* is the tenant ID of your Azure client application as described in step [4.a](configure-azure-integration.md#azure-oauth-details).

</td></tr></tbody>
</table>        5.  Select **Configure and Get OAuth Token**.
        6.  When the OAuth token flow is successfully completed, return to the Create connection for the software import task page using the back button for your browser.
        7.  Set the Create or Edit connection task to complete by selecting **Mark as Complete**.
    3.  Test the Log Analytics API connection to import software data from the Azure client application.

        1.  For the Test Connection task, select **Configure**.
        2.  Select the data source associated with the newly created connection in the **Name** column of the Data Sources list.
        3.  Select the **Test Load 20 Records** related link.
        4.  When the state changes to **Complete**, return to the setup by selecting **Back to Guided Setup** in the Help panel.
        5.  Set the Test Connection task to complete by selecting **Mark as Complete**.
    4.  Review the scheduled data imports configuration.

        1.  For the Set up scheduled import jobs task, select **Configure**.
        2.  Select the **SG-Azure Software** scheduled data import.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Update**.
        5.  Set the Set up scheduled import jobs task to complete by selecting **Mark as Complete** in the Help panel.
6.  Enable extended discovery using the `run` command.

    The `run` command is used to run a set of commands on the VMs to fetch server information such as CPU count, cores, model, and manufacturer. For information about extended discovery using the `run` command, see the [Extended discovery with Run Command on Service Graph connector for Microsoft Azure \[KB2210811\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2210811) article in the Now Support Knowledge Base.

    1.  Download the scripts that are required to enable extended discovery.

        1.  For the Download the scripts task, select **Configure**.
        2.  After the scripts are downloaded, select **Mark as Complete** to set the Download the scripts task to complete.
    2.  Configure an Azure storage account for extended discovery.

        1.  For the Configure Azure Storage account for Run Command task, select **Configure**.

            For information about configuring an Azure storage account for extended discovery, see the [Instructions for setting up Run Command in Service Graph Connector for Azure \[KB2001668\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=kb2001668) article in the Now Support Knowledge Base.

        2.  Set up a new Azure storage account.
        3.  Set up a container to upload the script files.
        4.  Set up another container to store the results.
        5.  Provide `run` command access to the service principal.
        6.  Select **Mark as Complete** to set the Configure Azure Storage account for Run Command task to complete.
    3.  Configure the connection properties for the new instance that you created for Service Graph Connector for Microsoft Azure.

        1.  For the Configure connection properties task, select **Configure**.
        2.  In the **Connection\*** field of the SG-Azure Configuration Properties section, select the new instance that you created.

            The fields in the Properties section are populated with the details of the instance.

        3.  In the Properties section, provide the following details for the instance that you created:
            -   Name of the storage account where the containers are created
            -   Subscription ID where the storage account is created
            -   Resource group of the storage account
            -   Name of the container where the `sh` and `ps1` files are uploaded in Azure
            -   Name of the container where the results of the commands are to be stored
            -   URI of the `sh` file that has to be run on Linux machines
            -   URI of the `ps1` file that has to be run on Windows machines
        4.  Select **Save**.
        5.  Select **Mark as Complete** to set the Configure connection properties task to complete.

## Result

The data from Azure is pulled into your CMDB.

