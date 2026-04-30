---
title: Configure Service Graph Connector for GCP using the guided setup
description: Set up scheduled import jobs to pull in data from a GCP project into your CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 12
breadcrumb: [GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for GCP using the guided setup

Set up scheduled import jobs to pull in data from a GCP project into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This app must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** If you have an earlier version of the Service Graph Connector for GCP, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for GCP application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **GCP** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the connection to send requests to the GCP application.

    1.  In the Configure the Connection and Credentials section of the Service Graph Connector for GCP page, select **Get Started**.

    2.  Set up the GCP environment and create a Java KeyStore \(JKS\) certificate to encrypt the security certificates obtained from a GCP application.

        Make a note of the destination keystore password. You need to specify this password while importing the JKS certificate into the Service Graph Connector for GCP application.

        For instructions, see the [Service Graph Connector for GCP - Setup Instructions \[KB1220598\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1220598) article in the Now Support Knowledge Base.

        **Note:** After you have set up the GCP environment, return to the guided setup and set the GCP Setup Instructions task in the Configure the Connection and Credentials section to complete by selecting **Mark as Complete**.

    3.  Create an X.509 certificate to associate the JKS certificate for the GCP application with the Service Graph Connector for GCP.

        1.  For the Create X.509 certificate task, select **Configure**.
        2.  On the form that opens in a new tab, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the X.509 certificate. For example, `SG-GCP-509Certificate-Org1`.|
            |Notify on expiration|Users to be notified when the certificate expires. If no users are selected, the logged-in user is added by default, along with the last two logged-in users with the administrator role.|
            |Warn in days to expire|Number of days to send a notification before the certificate expires.|
            |Active|Option to activate the certificate.|
            |Type|Certificate container that is automatically set to **Java Key Store**. Leave the field value set to **Java Key Store**.|
            |Expires in days|Number of days until the certificate expires.|
            |Key store password|Password to access the JKS certificate as noted down in the [previous step](sgc-config-gcp-integration.md#keystorepwd).|
            |Short description|Description of the X.509 certificate.|

        3.  Select the manage attachments icon \(![Manage Attachments icon.](../../../common/image/AttachmentIcon.png)\).
        4.  Select **Choose file** to browse and upload the keystore.p12 file for the JKS certificate you created in step [4.b](sgc-config-gcp-integration.md#jks).
        5.  Close the dialog box.
        6.  Select the **Validate Stores/Certificates** related link.
        7.  On successful validation, select **Update** to return to the guided setup page.
        8.  Set the Create X.509 certificate task to complete by selecting **Mark as Complete**.
    4.  Edit the default connection.

        1.  For the Edit Default Connection task, select **Configure**.
        2.  In the Flow Designer, select **SG-GCP Default Connection**, and then select **Edit**.
        3.  On the form that opens in the Edit Connection dialog box, fill in the fields.

<table id="table_qk3_3xv_22c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account Email

</td><td>

Service account created in and associated with the GCP application.

</td></tr><tr><td>

Keystore

</td><td>

Name of the keystore that you created in step [4.b](sgc-config-gcp-integration.md#jks).

</td></tr><tr><td>

Key Password

</td><td>

Destination keystore password associated with the keystore.

</td></tr><tr><td>

Organization Id

</td><td>

ID of the organization associated with the GCP application.

</td></tr><tr><td>

Discovery Scope

</td><td>

Discovery scope of the GCP application. The available options are:-   **organizations**

Select **organizations** when the ServiceNow service account has access to data within the GCP organization.

-   **projects**

Select **projects** when the ServiceNow service account has access to data within GCP projects only.

</td></tr></tbody>
</table>        4.  Select **Edit and Get OAuth Token**.
        5.  After the OAuth token flow is completed successfully, close the dialog box and the browser tab, and return to the guided setup page.
        6.  Set the Edit Default Connection task to complete by selecting **Mark as Complete**.
    5.  Test the GCP API connection to import data from the GCP application.

        1.  For the Test the Connection task, select **Configure** to open the SG-GCP Default Connection page in a new browser tab.
        2.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection may take a few moments. The page is refreshed to show the test results.

        3.  When the **Status** field is set to **Success**, close the browser tab and return to the guided setup page.

            If any of the tests have an error code or message or error sign, the connection failed and further troubleshooting is required.

        4.  Set the Test the Connection task to complete by selecting **Mark as Complete**.
    6.  Configure the scheduled jobs to import data from the GCP application.

        1.  For the Configure the Scheduled Imports task, select **Configure** to open the Scheduled Data Imports list in a new browser tab.
        2.  Select the SG-GCP Organization scheduled job.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Active** check box to activate the SG-GCP Organization scheduled job.
        5.  In the **Run** field, select **Periodically** to specify how often the job will run.
        6.  Select **Update**.
        7.  Return to the guided setup page.
        8.  Set the Configure the Scheduled Imports task to complete by selecting **Mark as Complete**.
5.  Add multiple GCP instances.

    1.  In the Add Multiple Instances section of the Service Graph Connector for GCP page, select **Get Started**.

    2.  Create data sources for the new GCP connection.

        1.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table.
        2.  For the Update Data Source Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  Return to the guided setup page.
        7.  From the application picker, select the **Service Graph Connector for GCP** application scope.
        8.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.
    3.  Create a scheduled import job for the new GCP connection.

        1.  Ensure that you have edit permissions for the Scheduled data import \[scheduled\_import\_set\] table.
        2.  For the Update Scheduled Data Import Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Scheduled Data Import form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  Return to the guided setup page.
        7.  From the application picker, select the **Service Graph Connector for GCP** application scope.
        8.  Set the Update Scheduled Data Import Access task to complete by selecting **Mark as Complete**.
    4.  Clear the cache on the Data Source \[sys\_data\_source\] and Scheduled Data Imports \[scheduled\_import\_set\] tables.

        1.  For the Clear Cache for Data Source and Scheduled Data Imports tables task, select **Configure**.
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
        5.  Return to the guided setup page.
        6.  From the application picker, select the **Service Graph Connector for GCP** application scope.
        7.  Set the Clear Cache for Data Source and Scheduled Data Imports tables task to complete by selecting **Mark as Complete**.
    5.  To create an X.509 certificate for the new GCP instance, repeat the step [4.c](sgc-config-gcp-integration.md#x509cert), and then set the Create X.509 certificate task to complete by selecting **Mark as Complete**.

    6.  Add a new connection.

        1.  For the Add New Connection task, select **Configure**.
        2.  In the Flow Designer, select **Add Connection**.
        3.  On the form that opens in the Create Connection dialog box, fill in the fields.

<table id="table_hkl_lkw_22c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Unique name for the new connection.

</td></tr><tr><td>

Service Account Email

</td><td>

ServiceNow service account associated with the GCP application.

</td></tr><tr><td>

Keystore

</td><td>

Name of the keystore that you created in step [5.e](sgc-config-gcp-integration.md#multi-inst-cert).

</td></tr><tr><td>

Key Password

</td><td>

Destination keystore password associated with the keystore.

</td></tr><tr><td>

Organization Id

</td><td>

ID of the organization associated with the GCP application.

</td></tr><tr><td>

Discovery Scope

</td><td>

Discovery scope of the GCP application. The available options are:-   **organizations**

Select **organizations** when the ServiceNow service account has access to data within the GCP organization.

-   **projects**

Select **projects** when the ServiceNow service account has access to data within GCP projects only.

</td></tr></tbody>
</table>    7.  Test the new connection.

        1.  For the Test New Connection task, select **Configure**.
        2.  In Service Graph Connections page that opens in a new browser tab, select the new connection that you want to test from the list of available connections.
        3.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection may take a few moments. The page is refreshed to show the test results.

        4.  When the **Status** field is set to **Success**, close the browser tab and return to the guided setup page.

            If any of the tests have an error code or message or error sign, the connection failed and further troubleshooting is required.

        5.  Set the Test New Connection task to complete by selecting **Mark as Complete**.
    8.  To configure the scheduled jobs to import data from the new GCP instance, repeat step [4.f](sgc-config-gcp-integration.md#scheduled-import), and then set the Configure the Scheduled Imports task to complete by selecting **Mark as Complete**.

6.  Synchronize new data sources to import data from GCP instances.

    1.  In the Advanced Setup section of the Service Graph Connector for GCP page, select **Get Started**.

    2.  Synchronize new data sources for creating all the required credentials to make the new data sources work correctly.

        1.  For the Sync New Data source task, select **Configure**.
        2.  Select **Synchronize Datasources**.
        3.  Return to the guided setup page by closing the Sync New Data source window.
        4.  Set the Sync New Data source task to complete by selecting **Mark as Complete**.
7.  Set up OS Config Patch Jobs to enable deep discovery.

    1.  In the Setup OS Config Patch Jobs for extended discovery section of the Service Graph Connector for GCP page, select **Get Started**.

    2.  For the Download script files task, select **Configure**.

    3.  Save the Shell script and PowerShell script files.

        The Shell script contains commands that run on Linux VMs. The PowerShell script contains commands that run on Windows VMs.

    4.  In the Shell script and PowerShell script files, specify the name of and the path in the Cloud Storage Bucket where the output of the commands are to be uploaded.

    5.  Upload the deep discovery scripts to the Cloud Storage Bucket.

    6.  Navigate back to the guided setup page, and set the Download script files task to complete by selecting **Mark as Complete**.

    7.  For the Configure GCP Cloud Storage Bucket for running Patch Jobs task, select **Configure**.

    8.  To configure the GCP Cloud Storage Bucket to run patch jobs, follow the deep discovery setup instructions in the [Service Graph Connector for GCP - Deep Discovery Setup Instructions \[KB2213095\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2213095) article in the Now Support Knowledge Base.

    9.  Navigate back to the guided setup page, and set the Configure GCP Cloud Storage Bucket for running Patch Jobs task to complete by selecting **Mark as Complete**.

    10. For the Configure connection properties task, select **Configure**.

    11. On the SG-GCP Configuration Properties form, select the connection for which you want to run deep discovery from the **Connection** list.

        In the Properties section of the SG-GCP Configuration Properties form, the following fields are populated with the values for the connection that you selected. If required, update the field values.

        |Field|Description|
        |-----|-----------|
        |Name of the Cloud Storage Bucket where the .sh and .ps1 files are uploaded in Google Cloud Platform|Name of the Cloud Storage Bucket where the deep discovery scripts are saved.|
        |Path to the .sh file uploaded to Cloud Storage Bucket|Path of the deep discovery Shell script file.|
        |Generation number of the .sh file uploaded to Cloud Storage Bucket|Number used to identify the versioning of the cloud storage object.|
        |Path to the.ps1 file uploaded to Cloud Storage Bucket|Path of the deep discovery PowerShell script file.|
        |Generation number of the .ps1 file uploaded to Cloud Storage Bucket|Number used to identify the versioning of the cloud storage object.|
        |Name of the Cloud Storage Bucket provided in .sh and .ps1 files where the outputs of the commands have to be stored|Name of the output Cloud Storage Bucket.|
        |Folder path provided in .sh and .ps1 files where the outputs are uploaded in the Storage Bucket|Path of the output storage folder in the Cloud Storage Bucket.|

    12. Select **Save**.

    13. Navigate back to the guided setup, and set the Configure connection properties task to complete by selecting **Mark as Complete**.


**Related topics**  


[Service Graph Connector for GCP](../concept/sgc-cmdb-integration-gcp.md)

[Configure Service Graph Connector for GCP using SGC Central](../../sgc-central/task/sgcc-configure-gcp-integ.md)

[Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md)

