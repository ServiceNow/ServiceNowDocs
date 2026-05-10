---
title: Configure Service Graph Connector for Active Directory
description: Configure your Lightweight Directory Access Protocol \(LDAP\) connections and verify them, set up scheduled imports, and optionally add multiple instances with the Guided Setup.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Active Directory, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Active Directory

Configure your Lightweight Directory Access Protocol \(LDAP\) connections and verify them, set up scheduled imports, and optionally add multiple instances with the Guided Setup.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-license-module.md), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

-   The [Integration Commons for CMDB](../../../configuration-management/concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../../../configuration-management/concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_ActivateTheDiscoveryPlugin.md).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This app must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

After you have followed the instructions provided to you to download and activate the Service Graph Connector for Active Directory application, refer to [Download an application from the ServiceNow Store for the first time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/download-app-first-time.md) and [Install a Security Operations integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/install-non-core-apps.md). There are a few steps you need to complete before you configure this integration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Active Directory** &gt; **Setup**.

2.  On the Welcome to Guided Setup Home page, select **Continue**.

3.  On the Experience page, select **Best Experience** followed by **Continue**.

    The Service Graph Connector for Active Directory \(AD\) page is displayed with the following tasks:

    -   Configure LDAP Server
    -   Add Multiple Instances
    -   Set up scheduled import jobs
4.  Select **Configure LDAP Server** to expand it.

    The following steps are displayed in the left navigation panel:

    -   Configure Inactive threshold
    -   Update LDAP OU definition
    -   Configure LDAP Server Details
    -   Test LDAP Server Connection
    A single LDAP server is supplied along with the application. This server includes a computer organizational \(OU\) unit that retrieves a computer's object information from the computers OU.

5.  Select **Configure Inactive threshold** to open the record.

    The System Property sn\_sec\_sgc\_ad.inactive\_threshold form is displayed.

6.  Select the **here** link in the message at the top of the form to edit the record.

7.  Alternatively, you can select the **Globe** icon in the upper right of the screen and select **Service Graph Connector for Active Directory** from the list to change the application scope so you can edit the form.

    As you progress through the Guided Setup, follow any instructions you see at the top of the pages in for modifying the application scope so you can open, edit, and save the record.

8.  Enter a threshold in the **Value** field.

    The default value is 90 days. Before you modify this value, refer to the information about the threshold setting at the top of the page. With this setting, assets that match the day threshold value are excluded from import.

9.  Right-click in the gray header titled System Property sn\_sec\_sgc\_ad.inactive\_threshold of the record and select **Save**.

10. Select **Mark as complete** followed by **Continue**.

    The LDAP OU Definition Access record is displayed.

11. Update LDAP OU Definition Access.

    1.  Follow the steps listed at the top of the page and on the LDAP OU Definition record to verify or switch the application scope to 'Global' with the application picker.

    2.  Select the **LDAP OU Definition** record on the table to open it.

    3.  On the record, if not selected, select the **Application Access** tab.

    4.  If displayed, select the link to edit the record followed by the check boxes for the permission settings you want.

    5.  Right-click in the gray header of the Table LDAP OU Definition record and select **Save**.

    6.  Select **Mark as complete** followed by **Continue**.

        The Configure LDAP Server Details page is displayed.

12. Provide the details for LDAP server connection.

    1.  Verify values or fill in the fields.

<table id="table_g4r_l2l_yyb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Read-only: Unique name for the LDAP server for example SGC-AD-computer.

</td></tr><tr><td>

Application

</td><td>

Read-only: Service Graph Connector for Active Directory \(AD\).

</td></tr><tr><td>

Active

</td><td>

Check box selected.

</td></tr><tr><td>

Login distinguished name

</td><td>

Login name for the AD server.

</td></tr><tr><td>

Login password

</td><td>

Password for the AD server.

</td></tr><tr><td>

Starting search directory

</td><td>

Directory you want to search for example `DC=Ops`.

</td></tr><tr><td>

\(Optional\) MID Server

</td><td>

Dedicated MID Server for the connection, if available.**Note:** A MID Server is required for on-premise connections if the instance is not publicly accessible.

</td></tr><tr><td>

LDAP Server URLs

</td><td>

Add the URL for the server for example `ladp://host-name:389/`.

</td></tr></tbody>
</table>    2.  Right-click in the gray header titled LDAP Server and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        The Test LDAP Server Connection page is displayed.

13. Test the LDAP Server Connection.

    1.  Scroll to the Related links section on the form and select the **Test Connection** link

        If the connection is successful, a Connected Successfully message is displayed. If your connection test fails, a message is displayed with information about why the connection failed. Review the Message field for how to proceed.

    2.  If you edit the record to fix the connection, right-click in the gray header titled LDAP Server and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        Add Multiple Instances is displayed in the top header the tasks.

        Adding Multiple instances is optional. If you don’t want to add multiple instances, you can proceed to step 14 and the Set scheduled import jobs task.

14. Add multiple instances.

    To add multiple instances, you must update data source access. You must edit the permissions on the Datasource \[sys\_data\_source\] table to create a data source for the new connection in the Service Graph Connector for Active Directory.

15. Select **Add Multiple Instances** from the top header drop down list.

    The following tasks are displayed:

    -   Update Data Source Access
    -   Update Scheduled Data Import Access
    -   Add Another LDAP Server
    -   List of configured LDAP servers
16. Select **Update Data Source Access**.

    1.  Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    2.  Select the Data Import record from the list to open it.

    3.  With the **Application Access** tab selected, follow the instructions to edit the record and modify the check boxes.

    4.  Right-click in the gray header titled Table Data Source and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

        The Update scheduled data import access page is displayed.

17. Update scheduled data import access.

    1.  Select the **Scheduled Data Import** record from the list to open it.

    2.  With the **Application Access** tab selected, follow the instructions to edit the record and modify the check boxes.

    3.  Right-click in the gray header titled Table Scheduled Data Import and select **Save**.

    4.  Select **Mark as complete** followed by **Continue**.

    The Add Another LDAP Server page is displayed. There are two steps for this task:

    -   LDAP server configuration
    -   Basic LDAP server information
18. Provide LDAP server configuration information.

    1.  Fill out the fields.

        |Field|Value|
        |-----|-----|
        |Type of LDAP server|Active Directory|
        |Server name|Unique name of the LDAP server.|
        |Server URL|URL for example `ldap://host-name:389/`.|
        |Start search directory|Directory you want to search for example `DC=SecOps`.|

    2.  Select **Submit**.

        After you submit these edits, complete the second configuration step.

    3.  Fill in the fields for the basic LDAP server information.

<table id="id_zj4_nll_yyb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Application

</td><td>

Read-only Service Graph Connector for Active Directory.

</td></tr><tr><td>

Active

</td><td>

Check box selected.

</td></tr><tr><td>

Login distinguished name

</td><td>

Login name for the AD server.

</td></tr><tr><td>

Login password

</td><td>

Password for the AD server.

</td></tr><tr><td>

Starting search directory

</td><td>

Directory you want to search for example `DC=SecOps`.

</td></tr><tr><td>

MID Server

</td><td>

Dedicated MID Server for the connection.**Note:** A MID Server is not required for the LDAP server.

</td></tr></tbody>
</table>    4.  Right-click in the gray header titled LDAP Server and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

        The List of configured LADP server page is displayed.

    6.  Select your new record from the list to open it and test the connection.

    7.  Edit information on the form.

    8.  When you are satisfied with the information, scroll to the Related links and select the **Test Connection** link.

        If the connection is successful, a message is displayed. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    9.  After a successful connection, right-click in the gray header titled LDAP Server and select **Save**.

    10. Select **Mark as complete** followed by **Continue**.

19. To set up scheduled jobs, select **Set up scheduled import jobs** from the drop down list in the top header.

    You must activate a scheduled job from the configuration page.

    1.  On the Configure the scheduled jobs page, select a record from the Scheduled Data Imports list to open it.

    2.  Select the **Active** check box and fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Unique name for the LDAP server, SGC-AD-computer.|
        |Application|Read-only Service Graph Connector for Active Directory \(AD\).|
        |Run|How often you want the job to run. If you want to run a test import prior to scheduling it, you might prefer to set this to **Once**.|
        |Run as|Run the scheduled job with the credentials of another specified user.|
        |Time|When you want the job to run.|
        |Active|Select the check box.|
        |Conditional|Specific conditions under which this job is run.|
        |Use connection|Leave this deactivated for the first run. Specifies another connection and credentials for this job.|
        |Concurrent import|Leave activated. Splits data into multiple imports sets. See the message for more information.|
        |Partition Method|Leave as Custom size.|
        |Partition size|15,000. Import set size for early scheduling.|
        |Execute pre-import script|Leave activated. Specifies a script to run before the import is performed.|
        |Execute post-import script|Leave activated. Specifies a script to run after the import is performed.|

    3.  Select **Execute now** to run the job.

        If you do not choose to run the job on-demand, the next job runs according to the schedule you set.

    4.  Right-click in the gray Scheduled Data Imports header and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

20. On the Home page for Guided Setup, select **Complete** to finish the configuration.


