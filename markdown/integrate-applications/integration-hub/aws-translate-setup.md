---
title: Set up the AWS Translate spoke
description: Integrate the ServiceNow instance and AWS Translate using the AWS credential to authenticate ServiceNow requests.Create an access key for the required user in the AWS Management Console to authenticate requests from the ServiceNow instance.Create Credential record for the AWS Translate spoke. The AWS Translate spoke uses this credential to perform actions on AWS Translate.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [AWS Translate Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the AWS Translate spoke

Integrate the ServiceNow instance and AWS Translate using the AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the AWS Translate spoke.
-   Role required: admin.

## Create an access key

Create an access key for the required user in the AWS Management Console to authenticate requests from the ServiceNow® instance.

### Procedure

1.  Log in to the AWS Management Console and open the [IAM console](https://console.aws.amazon.com/iam/).

2.  In the navigation pane, click **Users**.

3.  Click the required user record for which you want to create or manage the access keys.

    **Note:** Ensure that the user has admin access to AWS Translate.

4.  Click the **Security credentials** tab.

5.  Under **Access keys**, click **Create access key**.

    ![Create access key.](../image/aws-access-key.png)

    The access key is created.

6.  Click **Download .csv file** to save the access key ID and secret access key to a CSV file and record them for later use.

    For more information, see [Managing access keys \(console\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey).


## Create credential record

Create Credential record for the AWS Translate spoke. The AWS Translate spoke uses this credential to perform actions on AWS Translate.

### Procedure

1.  Navigate to **Integration Hub** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **AWS Translate**.

3.  In the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **AWS Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record.|
    |Access key ID|Access key ID you had copied from the AWS Management Console.|
    |Secret Access Key|Secret access key you had copied from the AWS Management Console.|
    |Authentication algorithm|Authentication algorithm to authenticate the web services. Select **AWS Translate Authentication Algorithm**.|

6.  Click **Submit**.


### Result

The credential record for the AWS Translate spoke is created.

