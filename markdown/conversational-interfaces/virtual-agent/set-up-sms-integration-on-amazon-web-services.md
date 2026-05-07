---
title: Set up SMS End User Messaging Service and AWS resources
description: Set up conversational SMS with Amazon Web Services \(AWS\) end user messaging to enable customers to seamlessly talk to virtual or live agents.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational SMS Integration with AWS End User Messaging, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up SMS End User Messaging Service and AWS resources

Set up conversational SMS with Amazon Web Services \(AWS\) end user messaging to enable customers to seamlessly talk to virtual or live agents.

## Before you begin

-   Procure an Amazon Web Services \(AWS\) account with the administrative access to complete the setup of SMS integration. This step is not required, if you already have an AWS account. To learn how to create an AWS account, see [documentation](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)

Role required: admin

## About this task

To set up integration on AWS, you must procure a phone number and an AWS SNS topic that subscribes to the AWS End User messaging phone number. The Lambda function on AWS that subscribes to the SNS topic signs the SMS messages with a secret key to verify and validate the messages that you receive. The Lambda function uses the Key Management Services \(KMS\) to create signatures using the SHA-256 algorithm.

This further enables IAM users to call the AWS End User Messaging APIs to send outbound SMS/MMS. You can also set up the S3 bucket to send media files to customers and store outbound media files.

![Overview of the setup and integration of SMS with AWS End User Messaging](../images/sms-aws-setup.png)

## Procedure

1.  Navigate to AWS end user messaging and select **Manage SMS** to procure a phone number.

    To learn how to procure a phone number, see [documentation](https://docs.aws.amazon.com/sms-voice/latest/userguide/phone-numbers-request)

2.  Setup a collection of the required Amazon Web Services resources and properties using a CloudFormation template.

    To learn how to deploy a stack, see [documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html). You can download the ServiceNow CloudFormation template from the Conversational SMS Integration with AWS End User Messaging store application from the ServiceNow store. This template creates an External \(Import key material\) type of KMS \(Key Management Service\) with no key material. You must upload the wrapped key material separately.

3.  Upload the wrapped key material to the key from step 2.

    The key value must be 32-byte in length and must use the HMAC\_256 algorithm. This key value is required for the setup on ServiceNow platform as well. To learn how to upload the wrapped key material to a KMS key, see [documentation](https://docs.aws.amazon.com/kms/latest/developerguide/importing-keys-conceptual.html).

4.  Link the phone number to enable Simple Notification Service \(SNS\) to support two-way SMS interaction between agents and customers.

    To learn how to link phone numbers to SNS, see [documentation](https://docs.aws.amazon.com/sms-voice/latest/userguide/two-way-sms-phone-number.html)

5.  After you run the CloudFormation template, generate the credentials for the IAM user that is created.

    The CloudFormation template creates an IAM user with permissions required to call the End User Messaging APIs, that enable outbound SMS and uploading media files to an S3 bucket. You must create an access key for the IAM user. The access key ID and secret access key are required during the setup on the ServiceNow platform. To learn how to create an access key for an IAM user, see [documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)


**Parent Topic:**[Configuring Conversational SMS Integration with AWS End User Messaging](../concept/configure-ci-sms-with-aws.md)

