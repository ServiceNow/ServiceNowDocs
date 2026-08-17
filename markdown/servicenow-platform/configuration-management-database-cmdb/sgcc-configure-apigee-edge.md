---
title: Configure API Service Graph Connector for Apigee Edge using SGC Central
description: Set up scheduled import jobs to pull in Apigee Edge data into your CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-apigee-edge.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 5
breadcrumb: [Apigee Edge, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Apigee Edge using SGC Central

Set up scheduled import jobs to pull in Apigee Edge data into your CMDB.

## Before you begin

Install API Service Graph Connector for Apigee Edge from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/installing-applications-in-application-manager.md).

Obtain the API credentials from your Apigee Edge administrator. Make a note of the following details:

-   Organization name: The Apigee Edge organization name from which data is imported.
-   Authentication details: The OAuth 2.0 token URL for your Apigee Edge account, and the user name and password used to authorize the connection.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|sn\_cmdb\_int\_util.sgc\_admin or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sgc-intro.md).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-ui.md).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Apigee Edge connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing Apigee Edge data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_conn_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Apigee Edge connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Apigee Edge service.**Note:** For a cloud setup, this field is prepopulated with the Apigee Edge cloud host value. Leave the field value as is. For an on-premises \(custom\) setup, replace the value with the host URL for your Apigee Edge instance.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token URL used to obtain the OAuth 2.0 access token for your Apigee Edge account, as noted in the [Before you begin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-apigee-edge.md) section.**Note:** For an on-premises \(custom\) setup, you must obtain and enter this value along with the Connection URL. For a cloud setup, only this field requires manual entry.

</td></tr><tr><td>

Use Mid Server

</td><td>

Option to connect to the Apigee Edge service using a MID Server.

</td></tr><tr><td>

MID Selection

</td><td>

Select how the MID Server is chosen for the connection:-   **Auto-Select MID Server**: Optionally specify a MID application to select available MID Servers from.
-   **Specific MID Server**: Select the MID Server to use.
-   **Specific MID Cluster**: Select the MID Server cluster to use.


</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  In the **Enter Credentials** dialog box, enter the **User name** and **Password** for your Apigee Edge account, as noted in the [Before you begin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-apigee-edge.md) section, and then select **Proceed**.

        **Note:** This connector uses the OAuth 2.0 password grant type, which requires these credentials to obtain an access token.

    5.  Once the connection test is complete, select **Continue**.

7.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the property details.

<table id="table_config_props"><thead><tr><th>

Section

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Data retrieval configuration

</td><td>

Apigee Edge organization name

</td><td>

Comma-separated list of Apigee Edge organization names to import data from. If left empty, data is retrieved from all accessible organizations.

</td></tr><tr><td>

App types to import

</td><td>

Filters which app records populate the API Consumer and API Consumer Subscription tables. Available options are **Company**, **Developer**, or **Both**. Defaults to **Both**.

</td></tr><tr><td>

Include environments

</td><td>

Comma-separated list of Apigee Edge environments to include in the connection. If left empty, data is imported from all environments.

</td></tr><tr><td>

Single environment

</td><td>

Include revision in key

</td><td>

Option to include the proxy revision in the correlation key to disambiguate proxies across organizations and environments. Selected by default.

</td></tr><tr><td rowspan="3">

Tags settings

</td><td>

Import tags

</td><td>

Option to enable ingestion of tags associated with imported CIs. Not selected by default.

</td></tr><tr><td>

Tag key prefix

</td><td>

Prefix filter on tag keys. The prefix is stripped before the key is stored. For example, a tag key of **NOWtag=environment** is stored as **environment**.

</td></tr><tr><td>

Tag key allow list

</td><td>

Comma-separated list of exact-match tag keys to store in the Key Value \[cmdb\_key\_value\] table. Other tag keys are ignored.

</td></tr><tr><td rowspan="2">

Managed API settings

</td><td>

Internet facing

</td><td>

Option to mark all ingested Managed API CIs as internet facing. Not selected by default.

</td></tr><tr><td>

Managed API type

</td><td>

Forces a specific type on all ingested Managed API CIs. Available options include **REST**, **SOAP**, **WebSocket**, **gRPC**, **GraphQL**, and **HTTP**.

</td></tr></tbody>
</table>    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **Organization** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-managing-connection.md).

