---
title: Create an Apache Iceberg connection
description: Establish a zero copy connection to Apache Iceberg in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Apache Iceberg, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Apache Iceberg connection

Establish a zero copy connection to Apache Iceberg in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Apache Iceberg. For additional information about connecting, refer to the [Iceberg connector documentation](https://trino.io/docs/current/connector/iceberg.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Apache Iceberg connector and select **Connect**.

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

Object storage authentication

</td></tr><tr><td>

Object storage system

</td><td>

Storage system used. The available options are:-   Amazon S3 \(the default\)
-   Azure Data Lake Storage \(ADLS\)
-   S3-Compatible


</td></tr><tr><td class="sub-head" colspan="2">

Amazon S3

</td></tr><tr><td>

AWS access key

</td><td>

Access key used to access AWS S3.

</td></tr><tr><td>

AWS secret key

</td><td>

Secret key used to access AWS S3.

</td></tr><tr><td>

AWS region

</td><td>

AWS region where your AWS S3 bucket is located.

</td></tr><tr><td class="sub-head" colspan="2">

S3-Compatible

</td></tr><tr><td>

S3 endpoint URL

</td><td>

Endpoint URL for the S3-compatible object storage system.

</td></tr><tr><td>

S3 access key

</td><td>

Access key used to authenticate with your S3-compatible storage service.

</td></tr><tr><td>

S3 secret key

</td><td>

Secret key used to authenticate with your S3-compatible storage service.

</td></tr><tr><td>

S3 region

</td><td>

Region where your S3-compatible object storage bucket is located.

</td></tr><tr><td class="sub-head" colspan="2">

Azure Data Lake Storage \(ADLS\)

</td></tr><tr><td>

Azure Access Key

</td><td>

Access key for ADLS.

</td></tr></tbody>
</table>4.  Configure the object storage system that you want to use with Apache Iceberg.

<table id="choicetable_q5x_dvj_xhc"><thead><tr><th align="left" id="d112034e362">

Option

</th><th align="left" id="d112034e365">

Description

</th></tr></thead><tbody><tr><td id="d112034e371">

**Amazon S3**

</td><td>

1.  Enter the access key used to access S3.
2.  Enter the secret key used to access S3.
3.  Enter the AWS region where your S3 bucket is located.
4.  Configure the metastore that you want to use with Apache Iceberg.


</td></tr><tr><td id="d112034e399">

**S3-Compatible**

</td><td>

1.  Enter the endpoint URL for the S3-compatible object storage system.
2.  Enter the access key used to authenticate with your S3-compatible storage service.
3.  Enter the secret key used to authenticate with your S3-compatible storage service.
4.  Enter the region where your S3-compatible object storage bucket is located.
5.  Configure the metastore that you want to use with Apache Iceberg.


</td></tr><tr><td id="d112034e431">

**Azure Data Lake Storage \(ADLS\)**

</td><td>

Enter the ADLS Access Key.

</td></tr></tbody>
</table>5.  Configure the metastore that you want to use with Apache Iceberg.

<table id="choicetable_xqf_z3l_rfc"><thead><tr><th align="left" id="d112034e451">

Option

</th><th align="left" id="d112034e454">

Description

</th></tr></thead><tbody><tr><td id="d112034e460">

**Hive Thrift**

</td><td>

1.  Attach the truststore file using one of the following options:
    -   Upload the truststore file by selecting **Attach TrustStore file** and selecting the file.
    -   Copy and paste the contents of the truststore file.
2.  Enter the truststore password.
3.  Enter the metastore URI that you want to connect to using the Thrift protocol. For example:

`thrift://<host>:<port>`

</td></tr><tr><td id="d112034e495">

**AWS Glue**

</td><td>

1.  Enter the AWS access key to connect to the Glue Catalog.
2.  Enter the AWS secret key to use to connect to the Glue Catalog.
3.  Enter the AWS region of the Glue Catalog.
 **Note:** AWS Glue appears when Amazon S3 is selected as the object storage system.

</td></tr><tr><td id="d112034e523">

**Rest**

</td><td>

1.  Enter the URI of your Iceberg REST Catalog server.
2.  Enter the location where table data files are stored \(Warehouse\).
3.  Enter the client ID used to authenticate your application via OAuth2.
4.  Enter the client secret used with the client ID to authenticate your application via OAuth2.
5.  Enter the scope that specifies which resources and operations the application is authorized to access via OAuth2.
 **Note:** Rest appears when S3-Compatible is selected as the object storage system.

</td></tr></tbody>
</table>6.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

