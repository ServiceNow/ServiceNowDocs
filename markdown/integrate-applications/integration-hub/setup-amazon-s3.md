---
title: Set up the Amazon S3 spoke
description: Use Amazon S3 as file storage in place of attachments in ServiceNow. Adds Amazon S3 storage to your ServiceNow instance and enables users to reference Amazon S3 files in ServiceNow records. Configure a connection for the Amazon S3 spoke to enable the spoke to connect to the Amazon S3 host. After connecting, the spoke can perform various actions on Amazon S3.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-amazon-s3.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Amazon S3 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon S3 spoke

Use Amazon S3 as file storage in place of attachments in ServiceNow. Adds Amazon S3 storage to your ServiceNow instance and enables users to reference Amazon S3 files in ServiceNow records.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon S3 spoke
-   Role required: admin

## Configure a connection for the Amazon S3 spoke

Configure a connection for the Amazon S3 spoke to enable the spoke to connect to the Amazon S3 host. After connecting, the spoke can perform various actions on Amazon S3.

### Before you begin

Create the AWS access key ID and the secret access key. For more information, see [create secret access key and key ID from AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/iam/create-access-key.html).

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Amazon S3 Spoke** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Amazon S3 spoke, click **View Details**.

        \[Omitted image "s3-connection.png"\] Alt text: Configure the default connection.

    -   To manage more than one Amazon S3 spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "s3-connection-conf.png"\] Alt text: Configure the default connection.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |Region|AWS region where your data resides.|
    |Credential Information|
    |Access Key ID|Access Key ID of your AWS account.|
    |Secret Access Key|Secret Access Key of your AWS account.|

    \[Omitted image "s3-conf-temp.png"\] Alt text: Configure the default connection.

6.  Click **Save**.


### Result

The connection record for the Amazon S3 spoke is configured and the spoke actions can be used.

