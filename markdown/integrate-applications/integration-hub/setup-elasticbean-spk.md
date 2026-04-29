---
title: Set up the AWS Elastic Beanstalk spoke
description: Create a credential record to integrate AWS Elastic Beanstalk with ServiceNow.Create an access key in Amazon Web Services to authorize actions.Create a credential record to integrate AWS Elastic Beanstalk with ServiceNow. The AWS Elastic Beanstalk connection and credential aliases use these credentials to authorize actions. Once connected, Elastic Beanstalk uses basic authentication to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AWS Elastic Beanstalk Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the AWS Elastic Beanstalk spoke

Create a credential record to integrate AWS Elastic Beanstalk with ServiceNow.

## Before you begin

Role required: admin

## Create an access key

Create an access key in Amazon Web Services to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [AWS Management Console](https://console.aws.amazon.com).

2.  From the menu under your user name, select **My Security Credentials**.

3.  Click **Create access key**.

4.  Copy the access key ID and the secret access key to a text file.

    You can only show the secret access key once, but you can delete and create keys if necessary. For more information, see [Create new access keys for an IAM user](https://docs.aws.amazon.com/keyspaces/latest/devguide/create.keypair.html) in [AWS documentation](https://docs.aws.amazon.com/).


## Create a credential record for the AWS Elastic Beanstalk spoke

Create a credential record to integrate AWS Elastic Beanstalk with ServiceNow. The AWS Elastic Beanstalk connection and credential aliases use these credentials to authorize actions. Once connected, Elastic Beanstalk uses basic authentication to authenticate ServiceNow requests.

### Before you begin

To set up the AWS Elastic Beanstalk spoke, you must be able to configure security credentials in Amazon Web Services and have a ServiceNow admin role.

-   Request an Integration Hub subscription.
-   Activate the AWS Elastic Beanstalk spoke spoke.
-   Role required: admin.

### Procedure

1.  Navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record **AWS\_Elastic\_Beanstalk**.

3.  In the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **AWS Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Elastic Beanstalk Cred`.|
    |Access Key ID|Access key ID you created in AWS Management Console. For more information, see [Create an access key](setup-elasticbean-spk.md#).|
    |Secret Access Key|Secret access key you created in AWS Management Console. For more information, see [Create an access key](setup-elasticbean-spk.md#).|
    |Authentication Algorithm|Select **AmazonElasticBeanstalkAuthAlgo**.|

    ![Create credential record for the spoke.](../image/elasticbeanstalk-cred.jpg)

6.  Click **Submit**.


### Result

The AWS Elastic Beanstalk spoke is set up and integrated with the ServiceNow instance.

