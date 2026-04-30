---
title: Create a Snowflake connection
description: Establish a zero copy connection to an external Snowflake account in Workflow Data Fabric Hub.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-04-29"
reading_time_minutes: 2
breadcrumb: [Snowflake, Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Create a Snowflake connection

Establish a zero copy connection to an external Snowflake account in Workflow Data Fabric Hub.

## Before you begin

You can optimize queries to Snowflake by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Snowflake before enabling this option in Workflow Data Fabric Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Snowflake. For additional information about connecting to Snowflake, refer to the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth).

## Procedure

1.  Navigate to the available primary connectors in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Snowflake connector and select **Connect**.

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

Connection URL

</td><td>

JDBC URL to establish the connection. For example: `jdbc:snowflake://<account>.snowflakecomputing.com`

</td></tr><tr><td>

Database

</td><td>

Name of the database that you want to connect to.

</td></tr><tr><td>

Warehouse

</td><td>

Name of the warehouse that you want to connect to.

</td></tr><tr><td>

Connection user

</td><td>

Connection user to connect to Snowflake.

</td></tr><tr><td>

Role

</td><td>

Role that determines your permissions within Snowflake.

</td></tr><tr><td>

Enable table statistics

</td><td>

Option to enable table statistics. Optimize SQL queries using table statistics by selecting this option. Enabling table statistics allows the system to use estimates of stored data such as row count, distinct values, and data size for enhanced query processing.

**Note:** You must ensure that gathering table statistics is enabled in the data source before selecting this option.

</td></tr></tbody>
</table>4.  Configure secure authentication by uploading a private key file or by entering the private key details manually.

<table id="choicetable_imc_rnn_k2c"><thead><tr><th align="left" id="d458461e272">

Option

</th><th align="left" id="d458461e275">

Description

</th></tr></thead><tbody><tr><td id="d458461e281">

**Upload private key file**

</td><td>

1.  Select **Attach Private key**.
2.  Browse and select the PEM file.


</td></tr><tr><td id="d458461e302">

**Enter private key contents manually**

</td><td>

Copy and paste the contents of the PEM file, ensuring the content begins with: ```
-----BEGIN PRIVATE KEY-----
```

 and ends with: ```
-----END PRIVATE KEY-----
```

</td></tr></tbody>
</table>5.  Enter the passphrase if the private key is secured with a password.

6.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-wdf.md).

If the connection fails, verify the connection details with your data source administrator and try again.

