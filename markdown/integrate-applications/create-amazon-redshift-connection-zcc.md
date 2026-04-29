---
title: Create an Amazon Redshift connection
description: Establish a zero copy connection to the Redshift data warehouse service in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon Redshift, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Amazon Redshift connection

Establish a zero copy connection to the Redshift data warehouse service in Zero Copy Connector Hub.

## Before you begin

You can optimize queries to Amazon Redshift by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Amazon Redshift before enabling this option in Zero Copy Connector Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Amazon Redshift. For additional information about connecting to Amazon Redshift, refer to the [Amazon Redshift documentation](https://docs.aws.amazon.com/redshift/latest/mgmt/jdbc20-configuration-options.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Amazon Redshift connector and select **Connect**.

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

JDBC URL to establish the connection. For example: `jdbc:redshift://<host>:<port>`

</td></tr><tr><td>

Database

</td><td>

Name of the database that you want to connect to.

</td></tr><tr><td>

Enable table statistics

</td><td>

Option to enable table statistics. Optimize SQL queries using table statistics by selecting this option. Enabling table statistics allows the system to use estimates of stored data such as row count, distinct values, and data size for enhanced query processing.

**Note:** You must ensure that gathering table statistics is enabled in the data source before selecting this option.

</td></tr><tr><td class="sub-head" colspan="2">

Authentication method

</td></tr><tr><td>

Access key ID

</td><td>

Access key ID associated with the source.

</td></tr><tr><td>

Secret access key

</td><td>

Secret access key associated with the access key ID.

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

