---
title: Create a Databricks connection
description: Establish a zero copy connection to the Databricks data analytics platform in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Databricks, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Databricks connection

Establish a zero copy connection to the Databricks data analytics platform in Zero Copy Connector Hub.

## Before you begin

You can optimize queries to Databricks by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Databricks before enabling this option in Zero Copy Connector Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Databricks. For additional information about connecting to Databricks, refer to the [Databricks documentation](https://docs.databricks.com/aws/en/dev-tools/auth/oauth-m2m).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Databricks connector and select **Connect**.

3.  On the form, fill in the fields.

<table id="table_kmx_fw1_2fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Name and description

</td></tr><tr><td>

Connection label

</td><td>

Unique name for this connection. This helps in identifying the connection within your system.

</td></tr><tr><td>

Connection name

</td><td>

System-generated name based on the Connection label. This field cannot be modified once the connection is established.

</td></tr><tr><td>

Short description

</td><td>

Description of the connection explaining what it is about.

</td></tr><tr><td class="sub-head" colspan="2">

Connection attributes

</td></tr><tr><td>

Catalog name

</td><td>

Catalog name used for organizing and locating data assets in Databricks.

</td></tr><tr><td>

Connection URL

</td><td>

JDBC URL to establish the connection. For example: `jdbc:databricks://<host>:<port>`

</td></tr><tr><td>

Warehouse or compute path

</td><td>

Databricks warehouse or compute path. For example:`/sql/1.0/warehouses/`

</td></tr><tr><td>

Enable table statistics

</td><td>

Option to enable table statistics. Optimize SQL queries using table statistics by selecting this option. Enabling table statistics allows the system to use estimates of stored data such as row count, distinct values, and data size for enhanced query processing.

**Note:** You must ensure that gathering table statistics is enabled in the data source before selecting this option.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with Databricks.

<table id="choicetable_h3q_4wg_b3c"><thead><tr><th align="left" id="d178070e257">

Option

</th><th align="left" id="d178070e260">

Description

</th></tr></thead><tbody><tr><td id="d178070e266">

**Databricks Service Principal**

</td><td>

Option to use Databricks as the OAuth provider.

 Select this option if you're using a Databricks service principal for authentication.

 1.  Enter the client ID issued by Databricks for authentication.
2.  Enter the secret key associated with the client ID.


</td></tr><tr><td id="d178070e290">

**Azure Service Principal**

</td><td>

Option to use Azure Entra ID as the OAuth provider.

 Select this option if you're using an Azure managed service principal for authentication. This option requires an established a trust relationship between Databricks and Azure Entra ID.

 1.  Enter the client ID issued by Azure for authentication.
2.  Enter the Azure tenant ID where your Databricks application is registered.
3.  Enter the secret key associated with the client ID.


</td></tr><tr><td id="d178070e317">

**Access Token**

</td><td>

Option to use a pre-configured OAuth entity profile.

 Select this option if you created a record in the Application Registries \[oauth\_entity\] table with a Databricks or IdP service principal for authentication.

 This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see Use a third-party OAuth provider. When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

 Select the OAuth entity profile for your Databricks or IdP service principal.

</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

