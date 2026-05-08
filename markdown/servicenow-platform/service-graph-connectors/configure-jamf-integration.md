---
title: Configure Service Graph Connector for Jamf using the guided setup
description: Set up authentication credentials and scheduled jobs to import Jamf data into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Jamf, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Jamf using the guided setup

Set up authentication credentials and scheduled jobs to import Jamf data into your Configuration Management Database \(CMDB\).

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by ITOM Visibility or ITOM Discovery, these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   ITOM Licensing plugin \(com.snc.itom.license\). An unlicensed plugin that contains computation logic for SU consumption as necessary. For more information, see Request Discovery.
-   Jamf Classic API version 10.x.

When using client credentials for authentication, obtain the OAuth credentials from your Jamf administrator. Make a note of the following details:

-   Application \(client\) ID
-   Client Secret

If using Client Credentials authentication in Jamf Pro, you need to utilize the API Roles and Clients functionality. For more details, refer to the [API Roles and Clients](https://learn.jamf.com/en-US/bundle/jamf-pro-documentation-current/page/API_Roles_and_Clients.html) section in the Jamf documentation. When creating a new API client in the Jamf environment, the **Access token lifetime** field on the form for creating a client enables setting how long the token remains valid. The default is `60` seconds, but due to ServiceNow AI Platform limitations, the value must be set to more than `60` seconds. Setting the token lifetime to `3600` seconds \(1 hour\) helps prevent potential issues.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Jamf** &gt; **Setup**.

2.  On the Getting Started page, select **Get started**.

3.  Set configuration properties.

    1.  On the Service Graph Connector for Jamf page, in the Set configuration properties section, select **Configure JSON data size limit**.

    2.  For the Configure JSON data size limit task, select **Configure**.

    3.  Select the **Global** application scope from the application picker.

    4.  Set the `com.glide.transform.json.max-partial-length` system property value.

        -   To create a system property, select **New** and enter `com.glide.transform.json.max-partial-length` as the name and `65536` as the value of the property.
        -   If the **com.glide.transform.json.max-partial-length** property already exists, verify that its value is set to `65536`.
    5.  Set the Configure JSON data size limit task to complete by selecting **Mark as Complete**.

4.  Configure the authentication credentials and HTTP connection for sending requests to the Jamf API.

    1.  Enter Basic or Bearer token authentication details.

        **Important:** Skip this step if using Client credentials for authentication, and instead go to step [4.c](configure-jamf-integration.md#client-credentials).

        1.  For the Configure Jamf authentication: Basic or Bearer token authentication task, select **Configure**.
        2.  On the form, fill in the fields.

<table id="table_ijh_2fw_1dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of this authentication configuration.

</td></tr><tr><td>

User name

</td><td>

User name that is used to authenticate the HTTP or HTTPS request when this Basic authentication profile is enabled.**Note:** Verify that the Jamf user has read privileges for the **Computers** and **Mobile Devices** categories in Jamf.

</td></tr><tr><td>

Password

</td><td>

Password that is used to authenticate the HTTP or HTTPS request when this Basic authentication profile is enabled.

</td></tr></tbody>
</table>        3.  Select **Update**.
        4.  Set the Configure Jamf authentication: Basic or Bearer token authentication task to complete by selecting **Mark as Complete**.
    2.  Configure the Jamf HTTP connection.

        **Important:** Skip this step if using Client credentials for authentication, and instead go to step [4.c](configure-jamf-integration.md#client-credentials).

        1.  For the Configure Jamf HTTP connection task, select **Configure**.
        2.  On the form, fill in the fields.

<table id="table_kjh_2fw_1dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection.

</td></tr><tr><td>

Credential

</td><td>

Credential value used by this connection.

</td></tr><tr><td>

Connection alias

</td><td>

Connection value that is used to refer to the connection.

</td></tr><tr><td>

Active

</td><td>

Option to activate the HTTP connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that contains the connection.

</td></tr><tr><td>

URL builder

</td><td>

Option to enable the system to build the connection URL.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL for the connection. You can either manually enter a URL or use the URL builder to build the connection string.**Note:** You can't modify the **Connection URL** field if you select the **URL builder** check box.

</td></tr><tr><td>

Mutual authentication

</td><td>

Option to set the connection with mutual authentication. This field appears only when the **URL builder** check box is selected.

</td></tr><tr><td>

Protocol

</td><td>

Underlying protocol used by the connection. This field appears only when the **URL builder** check box is selected.**Note:** Update the **Protocol** field if you are using anything other than `https`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to select a MID Server that sends this HTTP connection. Using a MID Server is not compatible with mutual authentication.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of milliseconds the system waits for a successful host connection. If a successful connection doesn't occur during this time, the connection request times out. Leave this field empty to use the system default connection timeout value.

</td></tr><tr><td>

Host

</td><td>

Target host value used by the connection. This field appears only when the **URL builder** check box is selected.**Note:** Update the **Host** field with your Jamf base URL or IP address. For example, `demojamfhost.com` or `127.0.0.1`.

</td></tr><tr><td>

Override default port

</td><td>

Target value port that is used by the connection. This field appears only when the **URL builder** check box is selected.

</td></tr><tr><td>

Base path

</td><td>

Base path for HTTPS connection. This field appears only when the **URL builder** check box is selected.**Note:** To use the Jamf Pro API, the **Base path** field must be empty. Therefore, clear any value in the **Base path** field.

</td></tr></tbody>
</table>        3.  Select **Update**.
        4.  Set the Configure Jamf HTTP connection task to complete by selecting **Mark as Complete**.
    3.  Configure the client authentication credentials.

        **Important:** Skip this step if using basic token for authentication, and instead go to step [4.a](configure-jamf-integration.md#basic-credentials).

        1.  For the Configure Jamf authentication: Client credentials task, select **Configure**.
        2.  Select **Edit** for the SG-Jamf OAuth Connection, the default connection.
        3.  In the Connection Information section of the Edit Connection window, fill in the fields.

<table id="table_uwz_zjg_3cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the Jamf connection record.`SG-Jamf OAuth Connection` is the default credential alias name and is read-only.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Jamf API.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr></tbody>
</table>        4.  \(Optional\) If a MID Server is required for the Jamf server connection, select the **Use MID Server** check box. Then, select the MID Server-related fields accordingly.
        5.  In the Credential Information section of the Edit Connection window, fill in the fields.

<table id="table_qfs_wkg_3cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Jamf client application as noted in the [Before you begin](configure-jamf-integration.md#prereq) section.**Note:** Verify that the Jamf client has read privileges for the **Computers** and **Mobile Devices** categories in Jamf.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Jamf client application as noted in the [Before you begin](configure-jamf-integration.md#prereq) section.

</td></tr></tbody>
</table>    4.  Test the connection.

        1.  For the Test connection task, select **Configure**.
        2.  Review the properties in the Service Graph Connection Properties related list.

            **Note:** The properties in the Service Graph Connection Properties related list of the connection record are modifiable. Be sure to complete the guided setup, review the property descriptions, and follow the instructions carefully before making any changes to them.

            -   For Basic authentication, set the **auth\_type** property value to `basic` \(applicable only for Jamf versions lower than 10.35. Note that Jamf no longer supports Basic authentication, and it will be disabled for all instances starting with Jamf version 11.5\).
            -   For Bearer token authentication, set the **auth\_type** property value to `bearer` \(available in Jamf version 10.35 or higher\).
            -   For Client credentials \(OAuth 2.0\) authentication, set the **auth\_type** property value to `oauth` \(available in Jamf version 10.49 or higher\).
            -   If no authentication type is selected, the connector defaults to Bearer token authentication.
        3.  Test the connection by selecting the **Test Load 20 Records** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

            **Note:** The connection is successful if the **HTTP Status** is **200**. If there is anything displayed in the **Error Code** and **Error Message** fields, then the connection failed and further troubleshooting is required. Do not select **Load All Records** during this setup.

        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
5.  Add multiple instances.

    **Note:** If you don't need to add multiple instances, you can skip this step.

    1.  In the Add Multiple Instances section of the Service Graph Connector for Jamf page, select **Get Started**.

    2.  Enable creating data sources for the new Jamf connection.

        1.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table.
        2.  For the Update data source Access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  Select the back icon \(&lt;\) to return to the guided setup page.
        7.  From the application picker, select the **Service Graph Connector for Jamf** application scope.
        8.  Set the Update data source Access task to complete by selecting **Mark as Complete**
    3.  Enable creating a scheduled data import job for the new Jamf connection.

        1.  Ensure that you have edit permissions for the Scheduled data import \[scheduled\_import\_set\] table.
        2.  For the Update scheduled data import access task, select **Configure**.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Scheduled Data Import form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  Select the back icon \(&lt;\) to return to the guided setup page.
        7.  From the application picker, select the **Service Graph Connector for Jamf** application scope.
        8.  Set the Update scheduled data import access task to complete by selecting **Mark as Complete**.
    4.  Select authentication type for new connection.

        **Note:** From the application picker, select the **Service Graph Connector for Jamf** application scope.

        1.  For the Select authentication type for new connection task, select **Configure**.
        2.  Select **sn\_jamf\_integrate.auth\_type** from the **Name** column.
        3.  Set the **sn\_jamf\_integrate.auth\_type** property to one of the following values:
            -   `basic`: Basic authentication that uses a user name and password.
            -   `bearer`: Bearer token authentication that uses a user name and password to retrieve a bearer token.
            -   `oauth`: Client credentials authentication that uses a client ID and client secret to authenticate via OAuth 2.0.
        4.  Navigate back to the guided setup.
        5.  Set the Select authentication type for new connection task to complete by selecting **Mark as Complete**.
    5.  Add another connection.

        **Note:** Verify that the **Service Graph Connector for Jamf** application scope is selected in the application picker.

        1.  For the Add another connection task, select **Configure**.
        2.  In the Workflow Studio, select **Add Connection**.
        3.  On the form, based on the authentication type fill in the fields.

            **Note:**

            -   For Basic or Bearer token authentication-based connection, don't include `https://` in the **Connection Host** field. Example connection host value: `test.jamfcloud.com`.
            -   For Client credentials authentication-based connection, include `https://` in the **Connection URL** field. Example connection URL value: `https://test.jamfcloud.com`.
        4.  Depending on the authentication type, select the button to create the connection.
        5.  Navigate back to the guided setup.
        6.  Set the Add another connection task to complete by selecting **Mark as Complete**.
    6.  When using the Jamf Pro API, the Jamf Pro 10.35 or higher version, or both, specify the Jamf Pro version and API.

        1.  For the Select JAMF Pro version and API task, select **Configure**.
        2.  In the **Use JAMF Pro API** column, for the connection you created, modify the value from **false** to **true** to use the Jamf Pro API instead of the Classic API.
        3.  Update the **Jamf Pro 10.35 or higher** column value to **true** when using the Jamf Pro 10.35 or higher version.

            **Note:** With the **Jamf Pro 10.35 or higher** column value set to **true**, the Bearer Token authentication is used to authenticate the Jamf API. Else, the basic authentication is used.

        4.  Set the Select JAMF Pro version and API task to complete by selecting **Mark as Complete**.
    7.  Test the new connections.

        1.  For the Test new connections task, select **Configure**.
        2.  Select the name of the connection you want to test.
        3.  To validate the data source configuration, select **Test Load 20 Records**.

            **Note:** If any of the tests have an error code or message or error sign, the connection failed and further troubleshooting is required.

        4.  Set the Test new connections task to complete by selecting **Mark as Complete**.
6.  Set up the scheduled import jobs.

    1.  For the Configure scheduled jobs task in the Set up scheduled import jobs section, select **Configure**.

    2.  Select the scheduled job that you want to activate.

        **Note:** By default, the SG-Jamf Mobile Devices scheduled job is automatically set as **Active** and runs the SG-Jamf Computer scheduled job as a parent.

    3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box to activate the scheduled job.

        For more information, see Schedule a data import.

    4.  Select **Update**.

    5.  Repeat the steps [6.b](configure-jamf-integration.md#select-job) to [6.d](configure-jamf-integration.md#exe-job) for each scheduled job for data import.

    6.  Set the Configure scheduled jobs task to complete by selecting **Mark as Complete** in the guided setup.


