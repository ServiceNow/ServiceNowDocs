---
title: Configuring your AWS account for use with Conversational IVR
description: To enable the Conversational IVR functionality within your ServiceNow instance, you must utilize a third-party Contact Center application. One such option is Amazon Connect, which is part of the Amazon Web Services \(AWS\) platform. You must configure your organization’s AWS account prior to making it available for use in the Conversational IVR feature.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Conversational IVR, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configuring your AWS account for use with Conversational IVR

To enable the Conversational IVR functionality within your ServiceNow instance, you must utilize a third-party Contact Center application. One such option is Amazon Connect, which is part of the Amazon Web Services \(AWS\) platform. You must configure your organization’s AWS account prior to making it available for use in the Conversational IVR feature.

## Configure your AWS account

1.  To grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console, see [Grant access to an IAM \(Identity and Access Management\) role](../task/create-user-assign-roles.md).
2.  To create an Amazon S3 bucket and to store objects within your AWS account, see [Create an Amazon S3 bucket](../task/create-amazon-s3-bucket.md).

    This will host the files required to complete the configuration.

3.  To create an AWS CloudFormation Stack and to provide a common language to describe and provision all the infrastructure resources required to enable the Conversational IVR feature in your environment in a safe and repeatable way, see [Create an Amazon CloudFormation Stack](../task/create-amzn-cloudformation-stack.md).

    You will be populating a template provided by ServiceNow that will then generate the required configuration.

4.  To claim a phone number for setting up Conversational IVR, see [Claim a Phone number](../task/claim-phone-nmbr-ivr.md).
5.  To configure Conversational IVR with Amazon Connect application in your ServiceNow instance to store the conversation between the agent and the user over Softphone as a transcript, see [Setup Transcript for Amazon Connect](../task/setup-amzn-transcription-ggl-sentiment.md).

