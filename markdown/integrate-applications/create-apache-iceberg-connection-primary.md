---
title: Create an Apache Iceberg connection
description: Establish a zero copy connection to Apache Iceberg in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
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

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|
    |Object storage authentication|
    |Object storage system|Storage system used. Default is Amazon S3.|
    |AWS access key|Access key used to access S3.|
    |AWS secret key|Secret key used to access S3.|
    |AWS region|AWS region where your S3 bucket is located.|

4.  Configure the object storage system that you want to use with Apache Iceberg.

<table id="choicetable_q5x_dvj_xhc"><thead><tr><th align="left" id="d129072e238">

Option

</th><th align="left" id="d129072e241">

Description

</th></tr></thead><tbody><tr><td id="d129072e247">

**Amazon S3**

</td><td>

1.  Enter the access key used to access S3.
2.  Enter the secret key used to access S3.
3.  Enter the AWS region where your S3 bucket is located.
4.  Configure the metastore that you want to use with Apache Iceberg.


</td></tr><tr><td id="d129072e271">

**Azure Data Lake Storage \(ADLS\)**

</td><td>

Enter the ADLS Access Key.

</td></tr></tbody>
</table>5.  Configure the metastore that you want to use with Apache Iceberg.

    **Note:** AWS Glue is only applicable when you select Amazon S3 as the object storage system.

<table id="choicetable_xqf_z3l_rfc"><thead><tr><th align="left" id="d129072e295">

Option

</th><th align="left" id="d129072e298">

Description

</th></tr></thead><tbody><tr><td id="d129072e304">

**Hive Thrift**

</td><td>

1.  Attach the truststore file using one of the following options:
    -   Upload the truststore file by selecting **Attach TrustStore file** and selecting the file.
    -   Copy and paste the contents of the truststore file.
2.  Enter the truststore password.
3.  Enter the metastore URI that you want to connect to using the Thrift protocol. For example:

`thrift://<host>:<port>`

</td></tr><tr><td id="d129072e339">

**AWS Glue**

</td><td>

1.  Enter the AWS access key to connect to the Glue Catalog.
2.  Enter the AWS secret key to use to connect to the Glue Catalog.
3.  Enter the AWS region of the Glue Catalog.


</td></tr></tbody>
</table>6.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.

