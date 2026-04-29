---
title: Create an Amazon S3 Tables connection
description: Establish a zero copy connection to Amazon S3 Tables in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon S3 Tables, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Amazon S3 Tables connection

Establish a zero copy connection to Amazon S3 Tables in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Amazon S3 Tables. For additional information about connecting to Amazon S3 Tables, refer to the [Amazon S3 Tables documentation](https://aws.amazon.com/blogs/storage/query-amazon-s3-tables-from-open-source-trino-using-apache-iceberg-rest-endpoint/).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Amazon S3 Tables connector and select **Connect**.

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

Iceberg Rest Catalog URI

</td><td>

URI of Iceberg Rest Catalog to connect to the AWS S3 Tables Rest endpoint. For example:`https://s3tables.<region>.amazonaws.com/iceberg`

</td></tr><tr><td class="sub-head" colspan="2">

Authentication methods

</td></tr><tr><td>

S3 Table bucket ARN

</td><td>

Amazon Resource Name \(ARN\) of your S3 Tables warehouse. For example:`arn:aws:s3tables:<region>:<account-id>:bucket/<bucket-name>`

</td></tr><tr><td>

S3 Region

</td><td>

Amazon S3 Tables region.

</td></tr><tr><td>

S3 Access Key

</td><td>

Amazon S3 Tables access key used to connect.

</td></tr><tr><td>

S3 Secret Access Key

</td><td>

Amazon S3 Tables Secret Access key used to connect.

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.

