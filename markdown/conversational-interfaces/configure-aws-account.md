---
title: \(Legacy\) Configuring your AWS account for use with Conversational IVR
description: To enable the Conversational IVR functionality within your ServiceNow instance, you must utilize a third-party Contact Center application. One such option is Amazon Connect, which is part of the Amazon Web Services \(AWS\) platform. You must configure your organization’s AWS account prior to making it available for use in the Conversational IVR feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/configure-aws-account.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure, Conversational IVR with Amazon Connect, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Configuring your AWS account for use with Conversational IVR

To enable the Conversational IVR functionality within your ServiceNow instance, you must utilize a third-party Contact Center application. One such option is Amazon Connect, which is part of the Amazon Web Services \(AWS\) platform. You must configure your organization’s AWS account prior to making it available for use in the Conversational IVR feature.

## Configure your AWS account

1.  To grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console, see [\(Legacy\) Grant access to an IAM \(Identity and Access Management\) role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-user-assign-roles.md).
2.  To create an Amazon S3 bucket and to store objects within your AWS account, see [\(Legacy\) Create an Amazon S3 bucket](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-amazon-s3-bucket.md).

    This will host the files required to complete the configuration.

3.  To create an AWS CloudFormation Stack and to provide a common language to describe and provision all the infrastructure resources required to enable the Conversational IVR feature in your environment in a safe and repeatable way, see [\(Legacy\) Create an Amazon CloudFormation stack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-amzn-cloudformation-stack.md).

    You will be populating a template provided by ServiceNow that will then generate the required configuration.

4.  To claim a phone number for setting up Conversational IVR, see [\(Legacy\) Claim a phone number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/claim-phone-nmbr-ivr.md).
5.  To configure Conversational IVR with Amazon Connect application in your ServiceNow instance to store the conversation between the agent and the user over Softphone as a transcript, see [\(Legacy\) Set up transcription for Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/setup-amzn-transcription-ggl-sentiment.md).

-   **[\(Legacy\) Grant access to an IAM \(Identity and Access Management\) role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-user-assign-roles.md)**  
Grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console.
-   **[\(Legacy\) Create an Amazon S3 bucket](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-amazon-s3-bucket.md)**  
Create an Amazon S3 bucket to store the files required for configuring Conversational IVR within your AWS account.
-   **[\(Legacy\) Create an Amazon CloudFormation stack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-amzn-cloudformation-stack.md)**  
Create an AWS CloudFormation stack to provision all the infrastructure resources required to enable the Conversational IVR feature. You will be populating a template provided by ServiceNow that will then generate the required configuration.
-   **[\(Legacy\) Configure localization in Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/config-ivr-localization.md)**  
Configure localization in Conversational IVR to use localization with Virtual Agent in other supported languages.
-   **[\(Legacy\) Customize keywords in Conversational IVR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localize-ivr-keywords.md)**  
Customize the IVR integration-specific keywords that are provided by default for better conversation in another language with the Virtual Agent.
-   **[\(Legacy\) Claim a phone number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/claim-phone-nmbr-ivr.md)**  
Claim a phone number to set up IVR \(Interactive Voice Response\).
-   **[\(Legacy\) Create inbound and outbound Amazon Connect contact flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-inbound-outbound-amzn-connect-flows.md)**  
Create the inbound and outbound Amazon Connect contact flows to set up IVR \(Interactive Voice Response\).
-   **[\(Legacy\) Set up transcription for Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/setup-amzn-transcription-ggl-sentiment.md)**  
Configure Conversational IVR with Amazon Connect application to store the conversation between the agent and the user over Softphone as a transcript.

**Parent Topic:**[\(Legacy\) Configuring Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configuring-ci-ivr-amazon-connect.md)

