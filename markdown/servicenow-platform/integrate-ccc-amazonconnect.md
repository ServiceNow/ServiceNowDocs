---
title: Integrate ServiceNow Voice with Amazon Connect
description: Connect ServiceNow Voice of your ServiceNow instance with the Amazon Connect instance to provide a seamless inbound and outbound voice call experience for your callers and agents.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Integrating with applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate ServiceNow Voice with Amazon Connect

Connect ServiceNow Voice of your ServiceNow instance with the Amazon Connect instance to provide a seamless inbound and outbound voice call experience for your callers and agents.

## Before you begin

-   Procure an Amazon Web Services \(AWS\) account with the administrative access to complete the integration setup between Amazon Connect and ServiceNow. For information about creating the AWS account, see the Amazon [documentation](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/).
-   Review the pricing policies for the services provisioned during this setup. Required services, resources, roles are set up in your AWS account.
-   Create a service account in your ServiceNow instance to allow communication from your AWS account to your ServiceNow instance. If you do not have the permissions to create service accounts on your instance, contact your ServiceNow administrator for creating this service account.

Role required: sn\_cti\_amzn\_cct.admin

**Note:** ServiceNow Voice with Amazon Connect integration is not supported for AWS GovCloud.

## Procedure

1.  Log in to your Amazon Web Services \(AWS\) account and setup an Amazon Connect instance.

    For instructions on setting up this instance, see the [Amazon Connect documentation](https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-instances.html).

2.  Integrate the Amazon Connect with your ServiceNow instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **Amazon Connect Integration** &gt; **Setup Instance**.

    3.  On the form, fill in the fields.

<table id="table_abz_1tz_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Amazon Connect instance.

</td></tr><tr><td>

AWS ARN

</td><td>

Amazon resource name of the Amazon Connect instance. For information on AWS ARN, see the [Amazon Connect](https://docs.aws.amazon.com/connect/latest/adminguide/transfer-to-agent.html) documentation.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the record is active.

</td></tr><tr><td>

Override Params

</td><td>

Option to edit the domain for Amazon Connect instance parameters. You should select this option only when you want to integrate the ServiceNow instance with an Amazon Connect instance created before introducing the new domain for the Amazon Connect console. For information about this new domain, see the Amazon Connect [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-release-notes.html#new-domain).

</td></tr><tr><td>

Instance Params

</td><td>

Auto-generated parameters based on the name of the Amazon Connect instance.For example, here are the Amazon Connect instance parameters before and after introducing the new domain for the Amazon Connect console.

-   Before introducing the new domain

    ```
{"ccpHost":"acmesupport.awsapps.com","ccpUrl":"https://acmesupport.awsapps.com/connect/ccp-v2","audioRecordingUrlPrefix":"https://acmesupport.awsapps.com/connect/get-recording?format=wav&callLegId="}
    ```

-   After introducing the new domain

    ```
{"ccpHost":"acmesupport.my.connect.aws","ccpUrl":"https://acmesupport.my.connect.aws/ccp-v2","audioRecordingUrlPrefix":"https://acmesupport.my.connect.aws/get-recording?format=wav&callLegId="}
    ```

</td></tr></tbody>
</table>3.  Configure the Amazon Connect components in your ServiceNow instance.

    ![Amazon Connect integration setup homepage in theServiceNow instance](../image/amazon-connect-home.png)

    1.  Navigate to **Amazon Connect Integration** &gt; **View Instances**.

    2.  Select the instance you want to configure.

    3.  Click the **Setup Guide** related link.

    4.  Work through the guided setup steps in the order displayed, and complete the instructions for components specified in each section.

<table id="table_r2y_dsd_1nb"><thead><tr><th>

Guided setup step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select Application

</td><td>

Select an application for which you want to configure the Amazon Connect components.

</td></tr><tr><td>

Setup S3 Bucket

</td><td>

Host content that can be deployed by Amazon CloudFormation. For more information on creating an S3 bucket, see the Amazon [documentation](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/create-bucket.html)

</td></tr><tr><td>

Deploy Stack

</td><td>

Set up a collection of the required Amazon Web Services \(AWS\) resources. For more information on stacks, see the Amazon [documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html).You can deploy the AWS stack using AWS CloudFormation templates.

-   Use AWS Cloud Formation template to describe AWS resources and properties
-   Use AWS Cloud Formation stack to provision the resources described in the template
**Note:** If you are upgrading from a previous release, point your existing deployment of Lambda function running on Node.js 10.x to point it to Node.js 14.x. For more information, see the Amazon [documentation](https://aws.amazon.com/blogs/compute/node-js-14-x-runtime-now-available-in-aws-lambda/).

</td></tr><tr><td>

Deploy Lex Bot

</td><td>

Build voice-based conversational interfaces for your users. For more information on Lex Bot, see the Amazon [documentation](https://docs.aws.amazon.com/lex/latest/dg/chatbot-service.html)

</td></tr><tr><td>

Connect Setup

</td><td>

Integrate with your ServiceNow instance with AWS services

</td></tr><tr><td>

Import Contact Flows

</td><td>

-   To enable Advanced Work Assignment \(AWA\) Voice Routing, check the checkbox under the **AWA Voice Routing** heading. Complete the steps specified in the setup guide:

    -   Complete [AWS Lambda](https://www.servicenow.com/docs/access?context=aws-lambda-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) and Oauth credential setup.
    -   Download the recommended hold music using the link in the setup guide \(you can choose your own hold music, but it cannot be longer than 5 seconds\).
    -   Upload the hold music. See the [AWS documentation](https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html#howto-prompts).
-   Define a call tree for inbound and outbound calls between Amazon Connect and your ServiceNow instance. For more information on contact flows, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/connect-contact-flows.html).

-   Based on your subscription, you have default inbound and outbound contact flows. For example, for the integration of ServiceNow Voice with ITSM applications, see [Components installed with ServiceNow Voice for ITSM](../reference/instld-with-cloud-call-center-itsm.md).

-   For an inbound contact flow, create queues to route contacts from AWS queues to ServiceNow queues. For information on creating queues in AWS, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/transfer-to-agent.html).

-   Set up call transfer flows through Amazon Connect using Transfer to Agent Flow and Transfer to Queue Flow. The transfer flows are reusable and can also be applied to ServiceNow Voice for ITSM.

-   Amazon Connect \(Phone\) is a placeholder phone channel for Amazon Connect integration. For queues that you implement in your Amazon Connect instance, you can use this channel to create corresponding Advanced Work Assignment queues. For an example implementation, see [Associate Amazon Connect queues for ITSM to a ServiceNow instance](https://www.servicenow.com/docs/access?context=setup-cloudcallcenter-itsm-configurable-workspace&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) or [Associate Amazon Connect queues for CSM to a ServiceNow instance](https://www.servicenow.com/docs/access?context=setup-amazonconnect-configurable-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Setup Real Time Transcription

</td><td>

Set up the properties in the Amazon Connect integration in order to enable Real-Time Transcription. Refer to [Configure Real Time Transcription for ServiceNow Voice Customer Service Management](configure-rtt-sn-voice.md) for configuration instructions.

</td></tr><tr><td>

Call Recording Events

</td><td>

Send recording events to the ServiceNow instance by enabling call recording on your Amazon Connect instance. For more information on recording behavior, see the Amazon [documentation](https://docs.aws.amazon.com/connect/latest/adminguide/set-up-recordings.html)

</td></tr><tr><td>

Setup Authentication

</td><td>

Integrate your Amazon Connect instance with your ServiceNow account by creating a service account

</td></tr><tr><td>

Additional Configuration

</td><td>

-   Use the Amazon Connect softphone interface

Launch the Amazon Connect softphone interface within ServiceNow UI by configuring OpenFrame. The OpenFrame configuration created in your ServiceNow instance enables agents to launch the softphone from within the ServiceNow interface. You can also configure user groups to restrict this configuration to specific agent user groups.

**Note:** Agents should log in to the softphone interface in a separate browser tab using the Amazon Connect credentials or SSO credentials \(if configured\). Once logged in, the softphone can be launched and used within the ServiceNow interface.

-   Use ICC voice controls with Amazon Connect

To use the native voice control in ServiceNow Workspace, follow the steps in the **Enable Interaction Controls** section of the guided setup.

**Note:** If a queue with the same ServiceNow Voice External ID is already mapped to an Amazon Connect queue, update the Provider Queue ID field on the existing record instead of creating a duplicate queue.

See [Interaction Controls Component \(ICC\) for voice calls](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Configure a contact flow for an automated caller interaction](establish-automated-bot-interactions.md)**  
Invoke an automated caller interaction with bots to fulfill the caller's request within the ServiceNow instance.

**Parent Topic:**[Integrating Voice with other applications](../concept/integrate-ccc-other-apps.md)

