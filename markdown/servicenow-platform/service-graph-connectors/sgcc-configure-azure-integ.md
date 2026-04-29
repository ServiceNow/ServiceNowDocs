---
title: Configure Service Graph Connector for Microsoft Azure using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft Azure for pulling in Microsoft Azure data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Azure using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Microsoft Azure for pulling in Microsoft Azure data into the CMDB.

## Before you begin

Install Service Graph Connector for Microsoft Azure version 1.9.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Important:** After the initial import of Azure data, the application performs a delta import of data. However, you can perform a full pull of data anytime later by disabling the delta synchronization and setting the **sn\_sg\_azure\_integ.is\_delta\_sync\_enabled** property to `false`. For more information, see [Configuring data synchronization in Service Graph Connector for Microsoft Azure](../../configuration-management/concept/sgc-cmdb-azure-data-sync.md#).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

The connector uses the Azure Management APIs for the complete pull of data from Azure. However, to pull delta changes from Azure, the Azure Resource Graph APIs are used. The domain name system \(DNS\) is Microsoft Azure Management, but the path is a resource graph.

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Microsoft Azure connector type and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Complete the prerequisites for setting up the Azure environment.

    1.  Complete the instructions required for setting up the Azure environment.

        1.  In the **Prerequisites** stage of the playbook, select the **Review setup instructions** activity.
        2.  Obtain the OAuth credentials including client ID, client secret, and token URL from your Microsoft Azure administrator.
        3.  For importing hardware data, grant the `User.Read` permission on the Microsoft Graph API in the Azure environment. Also, ensure that the IAM policy for the Azure subscription has the Reader role. See [Assign a user as an administrator of an Azure subscription with conditions](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal-subscription-admin) on the Microsoft Azure documentation site.
        4.  For importing software data, grant the `Data.Read` permission on the Log Analytics API in the Azure environment. In addition, set up a Log Analytics workspace in the Azure environment.
        5.  After completing the **Review setup instructions** activity, select **Continue**.
6.  Determine whether to import only hardware data or both hardware and software data.

    1.  In the **Setup** stage of the playbook, select the **Select services** activity.

        If needed, expand the **Setup** stage to select an activity.

    2.  To import both hardware and software data, select the **Hardware and software** check box.

        **Note:** Importing software data requires a hardware connection.

        If you need to import only hardware data, the **Hardware only** check box is already selected by default.

    3.  Select **Continue**.

7.  Enter the connection details and test the API connection for importing hardware data.

    1.  In the **Setup** stage of the playbook, select the **Create and test hardware connection** activity.

    2.  On the form, fill in the fields.

<table id="table_npd_v2z_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the hardware connection record.For example, `SG-Azure hardware connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Azure client application. **Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td>

OAuth client ID

</td><td>

Application \(client\) ID of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr><tr><td>

OAuth client secret

</td><td>

Client secret of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr><tr><td>

OAuth token URL

</td><td>

Callback URL for the Azure client application.Based on the region of your Azure client application, enter the token URL in one of the following formats:

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

Where *&lt;tenantid&gt;* is the tenant ID of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

8.  Configure the import schedule to import hardware data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure hardware import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **_Connection name_-SG-Azure Subscriptions** import schedule.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

9.  Enter the connection details and test the API connection for importing software data.

    The **Create and test software connection** activity for importing software data appears only when the **Hardware and software** check box is selected in step [6.b](sgcc-configure-azure-integ.md#prereq-sw).

    1.  In the **Setup** stage of the playbook, select the **Create and test software connection** activity.

    2.  On the form, fill in the fields.

<table id="table_vw2_jzw_fcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software connection name

</td><td>

Name to identify the software connection record.For example, `SG-Azure software connection`.

</td></tr><tr><td>

Hardware connection name

</td><td>

Name of the hardware connection record.**Note:** This field is automatically set to the hardware connection name specified in step [7.b](sgcc-configure-azure-integ.md#hw-id).

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Log Analytics workspace in the following format: ```
https://api.loganalytics.io/v1/workspaces/<workspace_id>
```

Where `<workspace_id>` is the ID of the Log Analytics workspace as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure). **Note:** This field is automatically set to the URL to connect to the Log Analytics workspace. Replace the `<workspace_id>` variable in the auto-generated URL with the workspace ID of your Log Analytics workspace.

</td></tr><tr><td>

OAuth client ID

</td><td>

Application \(client\) ID of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr><tr><td>

OAuth client secret

</td><td>

Client secret of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr><tr><td>

OAuth token URL

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

Where *&lt;tenantid&gt;* is the tenant ID of your Azure client application as noted in step [5.a](sgcc-configure-azure-integ.md#prereq-azure).

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

10. Configure the import schedule to import software data at regular intervals.

    The **Configure software import schedule** activity for importing software data appears only when the **Hardware and software** check box is selected in step [6.b](sgcc-configure-azure-integ.md#prereq-sw).

    1.  In the **Setup** stage of the playbook, select the **Configure software import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **_Connection name_-SG-Azure TCP** import schedule.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Repeat steps [10.b](sgcc-configure-azure-integ.md#parent) to [10.d](sgcc-configure-azure-integ.md#save) for any other parent import schedule if not already set to active.

    6.  Select **Continue**.

11. In the **Setup** stage of the playbook, select the **Connection setup complete** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Microsoft Azure](../../configuration-management/concept/cmdb-integration-azure.md)

[CMDB classes targeted in Service Graph Connector for Microsoft Azure](../../configuration-management/reference/cmdb-azure-classes.md)

[Data mapping for Service Graph Connector for Microsoft Azure](../../configuration-management/reference/cmdb-data-mapping-azure.md)

[Supported Microsoft Azure resource types](../../configuration-management/reference/cmdb-sgc-azure-resource-types.md)

[Service Graph Connector for Microsoft Azure properties](../../configuration-management/reference/cmdb-sgc-azure-props.md)

[Accessing the connection details of Service Graph Connector for Microsoft Azure](../../configuration-management/concept/sgc-cmdb-azure-conn.md#)

[Additional features within the Service Graph Connector for Microsoft Azure](../../configuration-management/concept/sgc-cmdb-azure-add-features.md)

