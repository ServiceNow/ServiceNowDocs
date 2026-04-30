---
title: Configure a connection to send OAuth request via the MID Server using external vault
description: Configure a connection to send requests for OAuth 2.0 tokens to a third-party auth server via the MID Server. The MID Server adds OAuth 2.0 credentials \(Client ID and Client Secret\) from the CyberArk external vault, OAuth scope, and token URL from the instance to the request and sends them to the third-party auth server.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 12
breadcrumb: [OAuth 2.0 authentication via MID Server using external credential storage, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure a connection to send OAuth request via the MID Server using external vault

Configure a connection to send requests for OAuth 2.0 tokens to a third-party auth server via the MID Server. The MID Server adds OAuth 2.0 credentials \(Client ID and Client Secret\) from the CyberArk external vault, OAuth scope, and token URL from the instance to the request and sends them to the third-party auth server.

## Before you begin

Verify the following items.

-   Confirm that you have subscribed to the ServiceNow IntegrationHub Standard Pack Installer. For more information, see [https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).
-   You have created a JAR file that enables the MID Server to resolve credentials with the CyberArk external vault. See [Create a JAR file to resolve credentials](../concept/external_cred_storage_configuration.md#).
-   You have imported the JAR file to the MID Server.
-   The MID Server is set up for CyberArk. See [Configure the MID Server for CyberArk AIM](t_ConfigureTheMIDServerForCyberArk.md).
-   OAuth 2.0 are configured on the CyberArk external storage. See [Configure OAuth 2.0 credentials on CyberArk](configure-oauth-2-0-credentials-on-cyberark.md).

Role required: none

## About this task

You can configure the connection and credential with a configuration template or manually. A configuration template defines the connection record form components and is reusable for other connection records. Manually, you can configure the connection for this purpose only. The topic shows both approaches.

## Procedure

1.  Configure the connection with a configuration template.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Configuration Templates**.

    2.  Select **New**.

    3.  Select **HTTP Connection with OAuth Client Credentials grant type \(External Storage\)**.

    4.  Update the form, as required.

        For example, you can provide the scope in the `oauth_entity_profile_scope` and `oauth_entity_scope` fields in the Default Data Template section. To learn to create a configuration template, see [Create a configuration template](create-template.md).

    5.  Select **Submit**.

        You have created the configuration template.

    6.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credential Aliases**.

    7.  Update the form.

<table id="table_oqy_4fl_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the alias. An alias can only contain alpha, number, and underscore characters. During an upgrade, the tag in the credential record migrates to a Connection &amp; Credential Alias. If the credential tag contains special characters other than alphabets, numbers, and underscores, it preserves the tag name after the upgrade. You can still use this migrated alias, but you cannot update the alias until you change the name to meet the naming restrictions.

</td></tr><tr><td>

Application

</td><td>

Unique identifier for the Connections &amp; Credentials alias, based on the format `scope_name.alias_name`. -   If the scope is Global, the ID is the alias name. For example, if you create a Workday alias in the global scope, it sets the ID to `workday`.
-   If you create a workday alias in the HR app scope, it sets the ID to `x_hr_app.workday`.


</td></tr><tr><td>

Parent Alias

</td><td>

Option to select the alias under which you're creating this connection and credential alias. The connection and credential alias that you're creating is a child alias. A child alias is listed under the **Child Aliases** tab on the parent connection and credential alias page.![Child alias under the Child Aliases tab.](../image/child-alias-location.png)

</td></tr><tr><td>

Type

</td><td>

Option to indicate the type of alias you're creating. Choose from the following options.-   Credential: Alias that contains a credential record.
-   Connection and Credential: Alias that contains both connection and credential record. This option is selected by default.
Confirm that Connection and Credential is selected.

</td></tr><tr><td>

Support Multiple Active Connections

</td><td>

Designator that indicates whether the alias supports multiple active connections. Add connections using the Connections table and associated them to the alias using the Connections related list.

</td></tr><tr><td>

Default Retry Policy

</td><td>

Retry policy for the alias. For more information, see [Retry policy](https://www.servicenow.com/docs/access?context=retry-policy&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Configuration Template

</td><td>

Option to select the configuration template based on which you're creating the connection and credential alias. Select the template of the type **HTTP Connection with OAuth Client Credentials grant type \(External Storage\)** that you had created.

</td></tr></tbody>
</table>    8.  Select **Submit**.

        You have created the connection and credential alias record.

    9.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections Dashboard**.

    10. In the Search all connections field, enter the name of the connection and credential alias record that you created.

    11. On the connection and credential alias record, select **View Details**.

    12. Select **Configure**.

    13. Fill the form.

<table id="table_qyb_hq4_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection. You can't update the name.

</td></tr><tr><td>

Connection URL

</td><td>

URL to the third-party server.

</td></tr><tr><td>

Use MID

</td><td>

Option to enable MID Server.**Important:** Confirm that the option is selected.

</td></tr><tr><td>

MID Selection

</td><td>

Option to specify MID Configuration for Connection.-   **Specific MID Server**: Option to indicate a manual selection of a specific MID Server.
-   **Auto-Select MID-Server**: Option to indicate that you want the MID Server automatically selected.
-   **Specific MID Cluster**: Option to indicate a manual selection of a MID cluster of MID Servers.
**Important:** Confirm that the MID Server you select resides on the same machine as the CyberArk AIM Client that is configured to access the CyberArk vault. See [Configure the CyberArk vault and install the AIM API](t_InstallCyberArkAIMAPI.md).

</td></tr><tr><td>

MID Server

</td><td>

Option to manually specify a MID Server. This option appears if you select **Specific MID Server** in the **MID Selection** field.

</td></tr><tr><td>

MID Cluster

</td><td>

Option to manually specify a MID Cluster. This option appears if you select **Specific MID Cluster** in the **MID Selection** field.

</td></tr><tr><td>

External Credential Store

</td><td>

Option to use the CyberArk external credential storage. When you select the option, the MID Server gets the OAuth 2.0 credentials \(Client ID and Client secret\) from the external credential storage.**Important:** Confirm that the option is selected.

</td></tr><tr><td>

Credential ID

</td><td>

Identifier for the CyberArk account that holds the Client ID and Client Secret details. To view the procedure to get the credential identifier, see [Configure OAuth 2.0 credentials on CyberArk](configure-oauth-2-0-credentials-on-cyberark.md).In the Credential ID field, enter an expression using one of these formats.

-   If all your credentials are in the same safe, configure this safe name in the MID Server `config.xml` file using the [ext.cred.safe\_name](t_ConfigureTheMIDServerForCyberArk.md) parameter, and then specify the credential ID by name only, as **&lt;credential ID&gt;**.
-   To name credentials for a given platform that reside is a specific safe, define the credential ID as **&lt;safe&gt;:&lt;credential ID&gt;:&lt;platform ID&gt;**.
-   If your credentials are in multiple safes, specify the credential ID in this format: **&lt;safe&gt;:&lt;credential ID&gt;**.


</td></tr><tr><td>

OAuth Token URL

</td><td>

URL that specifies the endpoint to get the access token from the OAuth server.

</td></tr></tbody>
</table>    14. Select **Configure Connection**.

2.  Configure a connection manually.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    2.  Select **New**.

    3.  Select **Connect to a third party OAuth Provider using an external vault**.

    4.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the application registry record. For example, enter: OAuth 2.0 token request via MID app.|
        |Application|Option to specify the names of applications that can access this application registry. The field is read only.|
        |Default Grant type|Default method to obtain access token by the client application from the OAuth server. The default and read-only grant type is Client Credentials.|
        |Accessible from|Option to specify which applications can access this application registry.|
        |Token URL|URL that specifies the endpoint to get the access token from the OAuth server.|
        |Send Credentials|Option to specify the method of sending the OAuth 2.0 in the request body.|
        |Comments|Enter related comments.|

    5.  Under the **OAuth scope** column, create one or more OAuth scopes by doing the following steps.

        1.  Under the Name column, double-click the field and enter a name of the OAuth scope.
        2.  Under the OAuth scope column, double-click the field and enter the scope.
    6.  Select **Submit**.

        You have created an OAuth entity profile and the application registry.

    7.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    8.  Select **New**.

    9.  Select **OAuth 2.0 Credentials**.

    10. Select **External Storage View**.

        **Important:** Select **External Storage View** only if the view is different from that of an OAuth 2.0 credentials external storage form.

    11. Fill the form.

<table id="table_fjn_vy4_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the credential record.

</td></tr><tr><td>

Applies to

</td><td>

Option to specify if the credential record is applicable for all MID Servers, or a specific MID Server. If specific, add the MID Servers.Choose from either of the following options.

-   All MID Servers: The MID Server is automatically selected from a collection of MID Servers.
-   Specific MID Servers: Option to specify one or more MID Servers.


</td></tr><tr><td>

MID Servers

</td><td>

Option to specify one or more MID Servers.**Note:** This field appears if you select **Specific MID Servers** in the Applies to field.

</td></tr><tr><td>

Active

</td><td>

Option to specify whether the credential record is available for use. By default, it's available.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

Option to specify an OAuth entity profile that the credential uses. Select the OAuth entity profile you had created above. See [Configure an OAuth entity profile](configure-oauth-2-0-authentication.md#substeps_lsc_5wj_wbc).

</td></tr><tr><td>

External credential store

</td><td>

Option to specify that the credentials are stored in an external storage and not in the ServiceNow instance. **Important:** Confirm that the option is selected.

</td></tr><tr><td>

Credential ID

</td><td>

Option to specify credential identifier for the CyberArk account which holds Client ID and Client Secret. To view the procedure to get the credential identifier, see [Configure OAuth 2.0 credentials on CyberArk](configure-oauth-2-0-credentials-on-cyberark.md).

</td></tr><tr><td>

Credential storage vault

</td><td>

Option to specify the name of the external credential storage vault. Verify that you have selected CyberArk.

</td></tr></tbody>
</table>    12. Select **Submit**.

        You have created the credential record.

    13. Create a connection and credential alias.

        To know the steps, see [Create a Connection &amp; Credential alias](connection-alias.md).

    14. Navigate to **All** &gt; **IntegrationHub** &gt; **Connections**.

    15. Select **New**.

    16. Select **HTTP\(s\) Connection**.

    17. Fill the form.

<table id="table_wrz_qhn_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this HTTP\(s\) connection.

</td></tr><tr><td>

Active

</td><td>

Option to set the connection that you're creating active. The option is selected by default.

</td></tr><tr><td>

Credential

</td><td>

Select the credential record used to authorize the connection. Select the credential that you had created above.

</td></tr><tr><td>

Connection alias

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td>

URL builder

</td><td>

Either manually enter the connection URL or use system to build the URL based on the inputs. Default is unchecked. If checked, the connection URL is calculated from the following fields: -   Mutual authentication — Check box if mutual authentication is used.
-   Protocol — If mutual authentication is not used, enter protocol. The default is HTTPs.
-   Protocol profile — If mutual authentication is used, enter protocol profile from sys\_protocol\_profile.
-   Host
-   Port
-   Base path — Path of the connection string.
**Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Connection URL

</td><td>

If URL builder is unchecked, enter the connection URL into this field.**Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Use MID server

</td><td>

Option to specify that you want to send OAuth token requests via a MID Server.**Important:** Confirm that the option is selected.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of milliseconds the system waits for a successful host connection. If a successful connection does not occur during this time, the connection request times out. Leave this field empty to use the system default connection timeout value.

</td></tr><tr><td>

MID Selection

</td><td>

Option to specify one of the following options.-   Auto-Select MID Server: Selects from MID Servers based on MID Server criteria, regardless of whether they are members of a cluster.
-   Specific MID Server: Manually select a MID Server.
-   Specific MID Cluster: Automatic reassignment to another MID Server only selects from members of the specified cluster.
**Important:** Confirm that the MID Server you select resides on the same machine as the CyberArk AIM Client that is configured to access the CyberArk vault. See [Configure the CyberArk vault and install the AIM API](t_InstallCyberArkAIMAPI.md).

</td></tr><tr><td>

Capabilities

</td><td>

Option to select one or more MID Server capabilities. Capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Select the MID capabilities icon \(![MID capabilities selection icon.](../image/mid-capabilities-selection.png)\) to select one or more capabilities. **Note:**

-   Confirm that the MID Server you select resides on the same machine as the CyberArk AIM Client that is configured to access the CyberArk vault. See [Configure the CyberArk vault and install the AIM API](t_InstallCyberArkAIMAPI.md).
-   This option appears if you select **Auto-Select MID Server** in the MID Selection field.


</td></tr><tr><td>

MID Server

</td><td>

Manually select a MID Server. This option appears if you select Specific MID Server from the MID Selection field.

</td></tr><tr><td>

MID Cluster

</td><td>

Manually select a MID cluster. This option appears if you select Specific MID Cluster from the MID Selection field.

</td></tr><tr><td>

MID Application

</td><td>

Option to specify a MID application or accept the default application choice.**Note:** This option appears if you select **Auto-Select MID Server** in the MID Selection field. By default, the **ALL** option is selected.

</td></tr></tbody>
</table>    18. Select **Submit**.

        You've created an HTTP\(s\) connection record.

    19. Navigate to **All** &gt; **Process Automation** &gt; **IntegrationHub** &gt; **Connections Dashboard**.

    20. In the Search all connections field, enter the name of the connection record that you created.

        The connection alias record appears.

        ![OAuth 2.0 connection record is created.]( "OAuth 2.0 connection record is created")

        ![OAuth 2.0 connection record is created.](../image/manual-connection-created.png)


**Parent Topic:**[OAuth 2.0 authentication via MID Server using external credential storage](../concept/oauth-2-0-support-in-external-credential.md)

