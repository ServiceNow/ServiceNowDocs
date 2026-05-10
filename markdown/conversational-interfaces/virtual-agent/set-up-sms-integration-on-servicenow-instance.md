---
title: Set up SMS integration on ServiceNow instance
description: Set up conversational SMS on a ServiceNow instance to enable customers to seamlessly talk to virtual or live agents.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Configure, Conversational SMS Integration with AWS End User Messaging, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up SMS integration on ServiceNow instance

Set up conversational SMS on a ServiceNow instance to enable customers to seamlessly talk to virtual or live agents.

## Before you begin

Role required: admin

## About this task

Procure an Amazon Web Services \(AWS\) account with the administrative access to complete the setup of SMS integration and ensure to set up integration on Amazon Web Services before this. To learn how to set up integration on AWS, see [Set up SMS End User Messaging Service and AWS resources](set-up-sms-integration-on-amazon-web-services.md).

## Procedure

1.  Create a Hash Message Verification record.

    1.  In the navigation filter, enter `hash_message_verification.list` and select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the auth token, such as AWSSMSTestAppAuthToken|
        |Description|Description of the auth token.|
        |Secret|Key value generated while uploading the key material to KMS key during the AWS setup. To learn more about key value, see [Set up SMS End User Messaging Service and AWS resources](set-up-sms-integration-on-amazon-web-services.md).|
        |Domain|Domain of the hash message, such as global.|

    3.  Select **Update**.

2.  Create a Message Auth record.

    1.  In the navigation filter, enter `message_auth.list` and select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the message auth, such as VA AWS SMS App Message Auth.|
        |Provider|Provider of the auth token. Enter `Amazon`.|
        |Group name|Name of the recipient group. Leave this field blank.|
        |Service portal|Portal that is associated with the message auth. Leave this field blank.|
        |Inbound message verification|Hash message token that you created.|
        |Outbound message verification|Hash message token that you created.|
        |Outbound service token|Authorized outbound service token. Leave this field blank.|

    3.  Select **Update**.

3.  Create a provider channel identity record.

    1.  In the navigation filter, enter `sys_cs_provider.list` and select **New Custom.**

    2.  Select the Provider Channel Identity related list and select **New**.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the provider channel identity record, such as VA SMS AWS Adapter Provider.|
        |Channel|The communication channel of the record, such as AWS EUM.|
        |Short Description|Description of the provider channel identity record.|
        |Inbound ID|The phone number associated with Amazon Web Services that you created.|
        |Message Auth|Name of the message auth, such as VA AWS SMS Test App Message Auth.|
        |Default portal|Portal that is associated with the channel identity record.|

4.  Add the following provider properties in the Provider Properties related list.

<table id="table_brc_42w_ydc"><thead><tr><th>

Property

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aws\_end\_user\_messaging\_configuration\_set\_arn

</td><td>

optional

</td><td>

Configuration to track the delivery of messages to the end user.

</td></tr><tr><td>

enable\_outbound\_media

</td><td>

true

</td><td>

Configuration to store the outbound media exchanged during a live or virtual chat.**Note:** The value of the field is **Empty** by default. If the value of the property is set to **True**, a bucket name must be provided and media is sent in its original form. If the value of the property is anything but **True**, bucket name is optional, and media is sent as a link.

</td></tr><tr><td>

aws\_eum\_api\_base\_url

</td><td>

AWS URL

</td><td>

Base URL for the AWS End User Messaging APIs configured based on region.To learn how to create a base URL, see [documentation](https://docs.aws.amazon.com/general/latest/gr/end-user-messaging.html)

</td></tr><tr><td>

outbound\_media\_s3\_destination\_folder

</td><td>

optional

</td><td>

Destination folder to store media.

</td></tr><tr><td>

outbound\_media\_s3\_bucket\_name

</td><td>

required

</td><td>

S3 bucket name for storing outbound media.

</td></tr></tbody>
</table>    **Note:** The provider properties' values can be provided at a provider channel. However, to override any property to make it specific to a provider channel identity record, then you must add the corresponding provider property at the provider channel identity.

5.  Add the Identity Access Management \(IAM\) user credentials.

    1.  In the navigation filter, enter `Connection & Credential Aliases` and add the **AWS credentials** for both **AWS\_EUM.** and **Amazon S3**.

    2.  Select **New** to create a new credential.

    3.  Select the type of AWS credentials from the list and select **Update** to open the AWS Credentials New record form.

    4.  On the form, fill in the fields.

<table id="table_ypl_tzh_d2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the credential.

</td></tr><tr><td>

Active

</td><td>

Whether the credential is active or not.

</td></tr><tr><td>

Access Key ID

</td><td>

AWS Access Key ID

</td></tr><tr><td>

Secret Access Key

</td><td>

AWS Secret Key ID

</td></tr><tr><td>

Credential Alias

</td><td>

Alias for the credential, either EUM or S3.The credential alias is auto-selected.

</td></tr><tr><td>

Algorithm

</td><td>

AWS IAM Auth.

</td></tr></tbody>
</table>    5.  Select **Submit**.


**Parent Topic:**[Configuring Conversational SMS Integration with AWS End User Messaging](../concept/configure-ci-sms-with-aws.md)

