---
title: Configure Service Graph Connector for Jamf using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Jamf for pulling in Jamf data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Jamf, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Jamf using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Jamf for pulling in Jamf data into the CMDB.

## Before you begin

Install Service Graph Connector for Jamf version 2.13.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

When using client credentials for authentication, obtain the OAuth credentials from your Jamf administrator. Make a note of the following details:

-   Application \(client\) ID
-   Client Secret

If using Client Credentials authentication in Jamf Pro, you need to use the API Roles and Clients functionality. For more details, refer to the [API Roles and Clients](https://learn.jamf.com/en-US/bundle/jamf-pro-documentation-current/page/API_Roles_and_Clients.html) section in the Jamf documentation. When creating a new API client in the Jamf environment, the **Access token lifetime** field on the form for creating a client enables setting how long the token remains valid. The default is `60` seconds, but due to ServiceNow AI Platform limitations, the value must be set to more than `60` seconds. Setting the token lifetime to `3600` seconds \(1 hour\) helps prevent potential issues.

Role required: admin

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Jamf connector type and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Determine the type of authentication for the Jamf connection.

    1.  In the **Setup** stage of the playbook, select the **Select alias template** activity.

        If needed, expand the **Setup** stage to select an activity.

    2.  Select an alias template for the connection.

        -   **SG-Jamf OAuth Connection**: Select when using OAuth or client credentials for authentication.
        -   **SG-Jamf Basic Connection**: Select when using Basic authentication or Bearer token.
    3.  Select **Continue**.

6.  Enter connection details and test the API connection for importing data.

    1.  In the **Setup** stage of the playbook, select the **Configure and test connection** activity.

    2.  On the form, fill in the fields.

        -   When the **SG-Jamf OAuth Connection** template is selected, fill in the details as shown in the following table.

<table id="table_d1c_5h2_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the Jamf connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Jamf API.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Jamf client application as noted in the [Before you begin](sgcc-configure-jamf-integration.md#prereq) section.**Note:** Verify that the Jamf client has read privileges for the **Computers** and **Mobile Devices** categories in Jamf.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Jamf client application as noted in the [Before you begin](sgcc-configure-jamf-integration.md#prereq) section.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

Mid Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>        -   When the **SG-Jamf Basic Connection** template is selected, fill in the details as shown in the following table.

<table id="table_irk_cl2_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the Jamf connection record.

</td></tr><tr><td>

Connection Host

</td><td>

Target host value used by the connection.**Note:** Update the **Host** field with your Jamf base URL or IP address. For example, `demojamfhost.com` or `127.0.0.1`.

</td></tr><tr><td>

User Name

</td><td>

User name that is used to authenticate the HTTP or HTTPS request when this Basic authentication profile is enabled.**Note:** Verify that the Jamf user has read privileges for the **Computers** and **Mobile Devices** categories in Jamf.

</td></tr><tr><td>

Password

</td><td>

Password that is used to authenticate the HTTP or HTTPS request when this Basic authentication profile is enabled.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

Mid Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Set configuration properties for the connection to access Jamf resources.

    **Note:** To skip this step, select **Continue** for the **Set configuration properties** activity. If you skip this step, the default values of the properties are considered.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Set the fields for configuration properties as described in the following table.

<table id="table_qqk_pdk_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import managed application records only

</td><td>

Option to limit the import to managed application records only.**Note:** If the **Import managed application records only** check box is cleared, the default behavior is to import all application records.

</td></tr><tr><td>

Use JAMF Pro API

</td><td>

Option to enable the use of the Jamf Pro API for querying computer records. **Note:** When the **Use JAMF Pro API** check box is selected, the connector uses the Jamf Pro API, which offers pagination of response data and improved performance over the Jamf Classic API.

</td></tr></tbody>
</table>    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

    5.  Repeat steps from [8.b](sgcc-configure-jamf-integration.md#schedule-start) to [8.d](sgcc-configure-jamf-integration.md#schedule-save) for each job displayed on the page.

    6.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Jamf](../../configuration-management/concept/cmdb-integration-jamf.md)

[CMDB classes targeted in Service Graph Connector for Jamf](../../configuration-management/reference/cmdb-jamf-classes.md)

[Accessing the connection details of Service Graph Connector for Jamf](../../configuration-management/concept/sgc-jamf-conn.md#)

