---
title: Configure Service Graph Connector for Microsoft Intune using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft Intune for pulling in Microsoft Intune data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Microsoft Intune, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Intune using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft Intune for pulling in Microsoft Intune data into the CMDB.

## Before you begin

Install Service Graph Connector for Microsoft Intune version 2.5.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

Obtain the following information from your Microsoft Intune administrator:

-   Client ID
-   Client Secret
-   Token URL

For the connector to access the data in Microsoft Intune, the credential information is required to use the Microsoft Graph API. Therefore, you must grant the following Graph API permissions from the App registrations page in the Microsoft portal:

-   DeviceManagementManagedDevices.Read.All \(Type: Application\)
-   DeviceManagementApps.Read.All \(Type: Application\)
-   User.Read.All \(Type: Application\)

Dependencies and requirements:

-   The [Integration Commons for CMDB](../../configuration-management/concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../../configuration-management/concept/cmdb-ci-class-models.md).
-   Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see Request Discovery.
-   ServiceNow IntegrationHub Zip step \(com.glide.hub.action\_step.zip\), which is automatically installed.
-   ServiceNow IntegrationHub JSON Parser step \(com.glide.hub.action\_step.jsonparser\), which is automatically installed.
-   The SGC Central application \(sn\_sgc\_central\), which is automatically installed.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts, to provide access to global tables to the SGC-Admin user, and to configure advanced data sources. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see Interact with Playbook.

For more details on permissions, see [Service Graph Connector for Microsoft Intune - Troubleshooting connection issues](https://community.servicenow.com/community?id=community_blog&sys_id=a405ef9bdbbd7018bb4a474d13961903) on ServiceNow Community and [Microsoft Graph permissions reference](https://learn.microsoft.com/en-us/graph/permissions-reference) on the Microsoft documentation site.

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Microsoft Intune connector type and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Select the data source type.

    1.  In the **Setup** stage of the playbook, select the **Select data source type** activity.

    2.  Select a data source type:

        -   **Advanced data sources**: Advanced data sources offer faster data import and better performance, and include software publisher details. Select this option if you have a large number of Microsoft Intune devices.

            **Note:**

            -   The admin role is required to configure advanced data sources.
            -   To enable the creation of attachments, the **glide.attachment.extensions** system property must be set to either null or `zip, json`.

                For more information, see the [Service Graph Connector For Microsoft Intune – Advanced \[KB1641546\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1641546) article in the Now Support Knowledge Base.

        -   **Regular data sources**: The standard option, which doesn't include software publisher details.
    3.  Select **Continue**.

6.  Enter connection details and test the API connection for importing Microsoft Intune data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the Microsoft Intune connection record.For example, `SG-Intune connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Microsoft Intune application. Based on the region of your Microsoft Intune application, enter the connection URL in one of the following formats:

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

Client ID of the Microsoft Intune application as noted in the [Before you begin](sgcc-configure-intune-integ.md#prereq) section.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret of the Microsoft Intune application as noted in the [Before you begin](sgcc-configure-intune-integ.md#prereq) section.

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

</td></tr><tr><td>

Use MID server

</td><td>

Option to use the MID Server for connecting to the Microsoft Intune instance.**Note:** A MID Server is required only if a direct connection between the ServiceNow and Microsoft Intune instances isn’t possible.

</td></tr><tr><td>

Mid Selection

</td><td>

MID Server for the connection.This field appears only when you select the **Use MID Server** check box.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Configure the connection properties to enable the connector to access resources.

    1.  In the **Setup** stage of the playbook, select the **Configure properties** activity.

    2.  In the **Configure properties** section, update the connection properties for advanced and regular data sources if required.

    3.  Select **Continue**.

8.  Configure the report trigger job for advanced data sources.

    The **Activate report trigger job** activity appears only if you selected **Advanced data sources** in step [5.b](sgcc-configure-intune-integ.md#substep_vrc_r5m_ygc). The advanced data sources require device reports and software reports to be triggered in the Microsoft environment before related jobs and scheduled imports are run.

    1.  In the **Setup** stage of the playbook, select the **Activate report trigger job** activity.

    2.  Fill in the fields on the **Scheduled Script Execution** form.

        |Field|Description|
        |:----|:----------|
        |Name|Specify a name for the report trigger job.|
        |Active|Select this check box to activate the report trigger job.|
        |Run|Specify the schedule for the job to be run.|
        |Time|Specify the time when the job should run.|
        |Run as|Specify the user role required to run the report trigger job.|

        **Note:** After you configure the report trigger job, all related jobs and the device and software reports scheduled imports are automatically scheduled to run in a specific sequence a few hours later \(typically 3–4 hours\). You can review the scheduled imports that are already activated and their scheduled time in step [9](sgcc-configure-intune-integ.md#step_dbq_wws_ygc).

    3.  Select **Continue**.

9.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **_Connection Name_-SG-Intune Devices** import schedule.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see Schedule a data import.

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

10. In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Microsoft Intune](../../configuration-management/concept/cmdb-integration-intune.md)

[CMDB classes targeted in Service Graph Connector for Microsoft Intune](../../configuration-management/reference/cmdb-intune-classes.md)

[Accessing the connection details of Service Graph Connector for Microsoft Intune](../../configuration-management/concept/sgc-cmdb-intune-conn.md#)

