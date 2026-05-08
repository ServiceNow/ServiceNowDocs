---
title: Configure API Service Graph Connector for Azure API Management using SGC Central
description: Set up scheduled import jobs to pull in Azure API Management data into your CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Azure API Management, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Azure API Management using SGC Central

Set up scheduled import jobs to pull in Azure API Management data into your CMDB.

## Before you begin

Install API Service Graph Connector for Azure API Management version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

Obtain the OAuth credentials from your Azure administrator. Make a note of the following details:

-   Application \(client\) ID
-   Client Secret
-   Directory \(tenant\) ID
-   Connection URL

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see Interact with Playbook.

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Azure API Management connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing Azure API Management data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Azure API Management Connection Name

</td><td>

Name to identify the Azure API Management connection record.For example, `Azure API Management Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Azure API Management service.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Azure client application as noted in the [Before you begin](sgcc-configure-azure-api-mgmt.md#prereq) section.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Azure client application as noted in the [Before you begin](sgcc-configure-azure-api-mgmt.md#prereq) section.

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

Where *&lt;tenantid&gt;* is the tenant ID of your Azure client application as noted in the [Before you begin](sgcc-configure-azure-api-mgmt.md#prereq) section.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Set the configuration properties for the connection.

    **Note:** To skip this step, select **Continue** for the **Set configuration properties** activity.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the property details.

<table id="table_nn3_31v_3cc"><thead><tr><th>

Property

</th><th>

Description

</th></tr><tr><th class="sub-head" colspan="2">

Azure API Management connection

</th></tr></thead><tbody><tr><td>

Discovery Scope

</td><td>

Discovery scope of the Azure client application. The available options are:-   **Management Group**

Select **Management Group** when the ServiceNow service account has access to data within the Azure management group.

-   **Subscription**

Select **Subscription** when the ServiceNow service account has access to data within the Azure subscription only.

</td></tr><tr><td class="sub-head" colspan="2">

Subscription

</td></tr><tr><td>

Subscription Id\(s\)

</td><td>

Subscription IDs of Azure API Management services.For multiple subscription IDs, separate them with commas. If the discovery scope is set to **Subscription** and this field is left blank, all subscriptions for the specified tenant in the credentials are discovered.

</td></tr><tr><td class="sub-head" colspan="2">

Management Group

</td></tr><tr><td>

Management Group Id\(s\)

</td><td>

Management group IDs of Azure API Management services. For multiple management groups, separate them with commas.

</td></tr><tr><td>

Get Nested Group Subscriptions

</td><td>

Option to enable retrieving data from all nested child subscriptions when **Management Group** is set as the discovery scope.Disable the property to exclude nested child subscriptions.

</td></tr><tr><td class="sub-head" colspan="2">

Optional Exclusive Configuration

</td></tr><tr><td>

ExcludeServices

</td><td>

Azure API Management services that should be excluded from the connection.For multiple services, separate them with commas. All gateways except those listed in the **ExcludeServices** property are fetched.

</td></tr><tr><td>

ResourceGroups

</td><td>

Resource group name of Azure API Management services.For multiple resource groups, separate their names with commas. If you leave this field empty, the data sources within the connector import data from all the available resource groups.

</td></tr><tr><td class="sub-head" colspan="2">

Usage Data Configuration

</td></tr><tr><td>

CollectUsageData

</td><td>

option to enable usage data collection to retrieve API usage data over a specified duration.

</td></tr></tbody>
</table>    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **API Management Services** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see Schedule a data import.

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

**Related topics**  


[API Service Graph Connector for Azure API Management](../../configuration-management/concept/api-sgc-azure-mgmt.md)

[Target tables for storing API Service Graph Connector for Azure API Management data](../../configuration-management/reference/api-sgc-azure-mgmt-tables.md)

