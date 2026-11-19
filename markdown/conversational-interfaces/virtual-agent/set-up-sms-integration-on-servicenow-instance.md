---
title: Set up SMS integration on a ServiceNow instance
description: Set up conversational SMS on a ServiceNow instance to enable customers to seamlessly talk to virtual or live agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/set-up-sms-integration-on-servicenow-instance.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 4
breadcrumb: [Configure, SMS with Amazon End User Messaging, Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Set up SMS integration on a ServiceNow instance

Set up conversational SMS on a ServiceNow instance to enable customers to seamlessly talk to virtual or live agents.

## Before you begin

Role required: admin

## About this task

Procure an Amazon Web Services \(AWS\) account with administrative access to complete the SMS integration setup. Before starting, set up integration on AWS. To learn how, see [Set up SMS End User Messaging Service and AWS resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/set-up-sms-integration-on-amazon-web-services.md).

## Procedure

1.  Create a Hash Message Verification record.

    1.  In the navigation filter, enter `hash_message_verification.list` and select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the auth token, such as AWSSMSTestAppAuthToken.|
        |Description|Description of the auth token.|
        |Secret|Key value generated while uploading the key material to KMS key during the AWS setup. To learn more about key value, see [Set up SMS End User Messaging Service and AWS resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/set-up-sms-integration-on-amazon-web-services.md).|
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

    2.  On the **Provider Channel Identity** tab, select **New**.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the provider channel identity record, such as VA SMS AWS Adapter Provider.|
        |Channel|The communication channel of the record, such as SMS.|
        |Short Description|Description of the provider channel identity record.|
        |Inbound ID|The phone number associated with Amazon Web Services that you created.|
        |Message Auth|Name of the message auth, such as VA AWS SMS Test App Message Auth.|
        |Default portal|Portal that is associated with the channel identity record.|

4.  On the **Provider Properties** tab, add the following provider properties.

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

    1.  In the navigation filter, enter `Connection & Credential Aliases` and add the **AWS credentials** for both **AWS\_EUM** and **Amazon S3**.

    2.  Select **New** to create a new credential.

    3.  From the list of credential types, select **AWS Credentials** to open the AWS Credentials New record form.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the credential.|
        |Active|Whether the credential is active or not.|
        |Access Key ID|AWS Access Key ID.|
        |Secret Access Key|AWS secret access key.|
        |Credential alias|Alias for the credential. The system fills in this field automatically from the alias record that you opened, such as AWS\_EUM or Amazon S3.|
        |Authentication Algorithm|AWS IAM Auth.|

    5.  Select **Submit**.

6.  Activate SMS in Service Channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column, search for `SMS`.

    3.  Select the record.

    4.  If a message states that the record is in the Conversational SMS Service Channel application but Global is the current application, select **To edit this record click here**.

    5.  Select the **Active** check box.

    6.  Select **Update**.

7.  Activate SMS in Presence States.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  Open the presence state that agents use when available, such as **Available**.

    3.  In the **Service channels** field, move **SMS** from the **Available** list to the **Selected** list.

    4.  Select **Update**.

8.  Add agents to the Agent SMS Group.

    1.  Navigate to **User Administration** &gt; **Groups**.

    2.  Open the Agent SMS Group record.

    3.  On the **Group Members** tab, select **Edit** and add the agents who will handle SMS conversations.

    4.  Select **Save**.


**Parent Topic:**[Configuring Conversational SMS Integration with AWS End User Messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-ci-sms-with-aws.md)

