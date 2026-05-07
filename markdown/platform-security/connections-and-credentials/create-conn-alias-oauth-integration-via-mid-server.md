---
title: Set up OAuth integration via MID Server
description: Create a connection record that enables the sending of an OAuth token request to a third-party server via a MID Server.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Set up OAuth integration via MID Server

Create a connection record that enables the sending of an OAuth token request to a third-party server via a MID Server.

## Before you begin

Confirm that you have subscribed to the ServiceNow IntegrationHub Standard Pack Installer. For more information, see [https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Role required: Admin

## Procedure

1.  Configure the connection with a configuration template.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Configuration Templates**.

    2.  Select **New**.

    3.  Select **HTTP Connection with OAuth Client Credentials grant type**.

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

Retry policy for the alias. For more information, see [Retry policy](https://www.servicenow.com/docs/access?context=retry-policy&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Configuration Template

</td><td>

Option to select the configuration template based on which you're creating the connection and credential alias. Select the template of the type **HTTP Connection with OAuth Client Credentials grant type** that you had created.

</td></tr></tbody>
</table>    8.  Select **Submit**.

        You have created the connection and credential alias record.

    9.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections Dashboard**.

    10. In the Search all connections field, enter the name of the connection and credential alias record that you created.

    11. On the connection and credential alias record, select **View Details**.

    12. Select **Configure**.

    13. Fill the form.

<table id="table_hwr_vjf_2cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection record. You can't update the name.

</td></tr><tr><td>

Connection URL

</td><td>

Option to provide the URL that connects with the third-party server.

</td></tr><tr><td>

Use MID

</td><td>

Option to specify that you want to send OAuth token requests via a MID Server.**Important:** Confirm that the option is selected.

</td></tr><tr><td>

MID Selection

</td><td>

Option to specify whether you want to use a specific MID Server or enable auto-selection of MID Server, or use a MID Cluster. Choose one of the following options.-   Auto-Select MID Server
-   Specific MID Server
-   Specific MID Cluster


</td></tr><tr><td>

Capabilities

</td><td>

Option to select one or more MID Server capabilities. Capabilities define the specific functions of a MID Server within an IP address range, allowing an application to select the most appropriate MID Server. Select the MID capabilities icon \(![MID capabilities selection icon.](../image/mid-capabilities-selection.png)\) to select one or more capabilities. **Note:** This option appears if you select **Auto-Select MID Server** in the MID Selection field.

</td></tr><tr><td>

MID Application

</td><td>

Option to specify a MID application or accept the default application choice.**Note:** This option appears if you select **Auto-Select MID Server** in the MID Selection field. By default, the **ALL** option is selected.

</td></tr><tr><td>

MID Server

</td><td>

Option to select a MID Server.**Note:** This option appears if you select **Specific MID Server** in the MID Selection field.

</td></tr><tr><td>

MID Cluster

</td><td>

Option to select a MID Cluster.**Note:** This option appears if you select **Specific MID Cluster** in the MID Selection field.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Option to specify the client ID.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Option to specify the client secret.

</td></tr><tr><td>

Connect to Auth Server via MID Server

</td><td>

Option to specify that the connection between the ServiceNow instance and the Auth server takes place via the MID Server. **Important:** Confirm that the option is selected.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Option to specify the OAuth token URL that is used to request OAuth tokens.

</td></tr></tbody>
</table>    14. Select **Configure and Get OAuth Token**.

        The connection and credential record is created.


