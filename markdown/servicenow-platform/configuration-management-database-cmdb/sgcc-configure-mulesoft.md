---
title: Configure API Service Graph Connector for MuleSoft using SGC Central
description: Set up scheduled import jobs to pull in MuleSoft Anypoint Platform data into your CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MuleSoft, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for MuleSoft using SGC Central

Set up scheduled import jobs to pull in MuleSoft Anypoint Platform data into your CMDB.

## Before you begin

Install API Service Graph Connector for MuleSoft version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).

Obtain the Connected App credentials from your MuleSoft Anypoint Platform administrator. Make a note of the following details:

-   Client ID: The unique identifier for your Connected App.
-   Client Secret: The secret key for authenticating your Connected App.
-   Directory \(tenant\) ID: The MuleSoft organization identifier from which data is imported.

For more information on connector setup, see the [API Service Graph connector for MuleSoft - Setup Instructions \[KB2560348\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2560348) article in the Now Support Knowledge Base.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-ui.md).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the MuleSoft connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing MuleSoft data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the MuleSoft connection record.For example, `MuleSoft connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the MuleSoft Anypoint Platform API service.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td>

OAuth client ID

</td><td>

Client ID of your MuleSoft Connected App as noted in the [Before you begin](sgcc-configure-mulesoft.md#prereq) section.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret of the MuleSoft Connected App as noted in the [Before you begin](sgcc-configure-mulesoft.md#prereq) section.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token endpoint URL used to securely authenticate your identity and authorize access to your MuleSoft Anypoint Platform API account via the API.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the property details.

<table id="table_nn3_31v_3cc"><thead><tr><th>

Property

</th><th>

Description

</th></tr><tr><th class="sub-head" colspan="2">

Data retrieval configuration

</th></tr></thead><tbody><tr><td>

Organization id

</td><td>

MuleSoft organization identifier from which API data is imported. If you have multiple organizations, create separate connections for each.For multiple organizations, create separate connections for each.

</td></tr><tr><td>

Environment filter

</td><td>

MuleSoft environments to include in the connection.For multiple environments, separate them with commas. Only API proxies in the environments listed in the **Environment filter** property are imported.

If you leave this field empty, the data sources within the connector import API proxies from all environments.

</td></tr><tr><td>

API Manager filter

</td><td>

API manager instance status filter.Accepts a single value: `active`, `inactive`, or `unregistered`. When specified, only APIs matching that status are imported.

If you leave this field empty, all APIs are imported regardless of status.

</td></tr><tr><td>

Only deployed API managers

</td><td>

Option to import only APIs currently deployed to runtime instances.

</td></tr><tr><td>

Import deployed applications

</td><td>

Option to collect deployed applications from runtime manager as Data Service Instances.

</td></tr><tr><td>

Collection period \(in days\)

</td><td>

Duration in days for collecting API usage data.

</td></tr><tr><td>

Collect usage data

</td><td>

Option to enable usage data collection to retrieve API usage metrics over a specified duration.

</td></tr><tr><td class="sub-head" colspan="2">

Tags settings

</td></tr><tr><td>

Import tags

</td><td>

Option to ingest tags from the MuleSoft API Manager.

</td></tr><tr><td>

Tag key/value indicator

</td><td>

Separator for key and value in tags.

</td></tr></tbody>
</table>    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **Gateway** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

