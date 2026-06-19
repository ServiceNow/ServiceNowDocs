---
title: Integrate ServiceNow voice assistant with Amazon Connect
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Amazon Connect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/integrate-voice-service-with-amazon-connect.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 6
keywords: [Amazon Connect, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, PSTN, Lambda]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Amazon Connect

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Amazon Connect.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/create-an-ai-voice-service.md) for more information.
-   Access to your Amazon Connect instance with permissions to create Lambda functions, configure contact flows, and manage Identity and Access Management \(IAM\) roles.

Role required: sn\_aia.admin

## About this task

Connect your Amazon Connect contact center to a ServiceNow voice assistant using the Public Switched Telephone Network \(PSTN\) communication channel. When a call arrives, Amazon Connect invokes a Lambda function that retrieves a PSTN number from the ServiceNow Call Context API and transfers the call to the voice assistant. After the voice assistant handles the interaction, the Lambda function retrieves the interaction context and routes the call to a queue or ends the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to Amazon Connect and select **Edit**.

3.  Select **Communication channels** from the guided setup navigation.

4.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

5.  Select the **Telephony provider** tab.

6.  From the **Select communication channels** dropdown, select **Public Switched Telephone Network \(PSTN\)**.

7.  From the **CCaaS provider** dropdown, select **Amazon Connect**.

    The following read-only fields are generated in the **Call context service** section. Copy and save these values — you will need them to configure the integration on the Amazon Connect side.

    |Field|Description|
    |-----|-----------|
    |Transfer method|Read-only. Set to **BYE** for Amazon Connect.|
    |Call context API|Read-only. The URL that Amazon Connect uses to send call context data to the voice assistant. Copy this value for use as the `call_context_api_path` and `voice_service_host_name` Lambda environment variables.|
    |Client ID|Read-only. Generated client ID for OAuth2 authentication. Copy this value for use in the AWS Parameter Store setup.|
    |Client Secret|Read-only. Generated client secret for OAuth2 authentication. Copy this value for use in the AWS Parameter Store setup.|
    |KB doc|Reference information for configuring the PSTN connection between Amazon Connect and the ServiceNow voice assistant. See [KB3027295](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3027295) for more information.|

    \[Omitted image "voice-agents-amazon-connect-integration.png"\] Alt text: Amazon Connect integration configuration showing the Transfer method, Call context API URL, Client ID, Client Secret, and KB doc fields.

    Also note the voice service `sys_id`, which you can find in the URL when viewing the voice service record. You will need this value in the Amazon Connect configuration steps.

8.  Enable context data persistence for the voice service.

    1.  Navigate to `sys_now_assist_deployment_config_attributes.list`.

    2.  Filter the list to find the configuration attribute records for your voice service.

    3.  Locate the attribute named `persist_context_data` and change its value from `false` to `true`.

        This setting allows the Lambda function to retrieve interaction context data from ServiceNow after the voice assistant completes the call.

9.  In your AWS account, create the Lambda function that connects Amazon Connect to the voice assistant.

    1.  From the AWS console, create a new Lambda function.

    2.  In the Lambda function code editor, replace the default handler code with the Lambda function code.

        See [Amazon Connect Lambda function code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/voice-agent-reference.md).

    3.  Set the following environment variables on the Lambda function.

        |Variable|Value|
        |--------|-----|
        |`call_context_api_path`|The path portion of the ServiceNow call context URL — the part of the URL after `.com`.|
        |`now_instance_host_name`|The ServiceNow instance URL.|
        |`now_instance_name`|The name of your ServiceNow instance.|
        |`ssm_oauth_path`|The AWS Parameter Store path for OAuth credentials. Set after completing the Parameter Store setup in the following steps.|
        |`voice_service_host_name`|The hostname from the ServiceNow call context URL.|

    4.  Grant your Amazon Connect instance permission to invoke the Lambda function.

        In the Amazon Connect console, navigate to your instance, select **Flows**, and under **AWS Lambda**, add the Lambda function with the Invoke Lambda use case. Confirm the policy was added in the Lambda console under **Configuration** &gt; **Permissions**.

    5.  Replace the Lambda execution role permissions policy with the Identity and Access Management \(IAM\) policy.

        See [Amazon Connect Lambda Identity and Access Management \(IAM\) policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/voice-agent-reference.md).

        In the Lambda console, navigate to **Configuration** &gt; **Permissions** &gt; **Execution Role** and replace the existing permissions policy. Replace `<region>`, `<account-id>`, and `<lambda-function-name>` with your values.

    6.  Create a CloudWatch log group for the Lambda function.

        In the AWS console, navigate to **CloudWatch** &gt; **Log Management**. If no log group exists for your Lambda function, create one named `/aws/lambda/<your_Lambda_name>`.

    7.  Create the OAuth credentials in AWS Parameter Store.

        From the AWS console, navigate to Parameter Store and create the following parameters using **SecureString** as the type.

<table id="table_param_store"><thead><tr><th>

Name

</th><th>

Value

</th></tr></thead><tbody><tr><td>

`/com.servicenow.cti/<sn-instance-id>/<voice-service-id>/client_id`Where `sn-instance-id` is the value of the `instance_id` system property, and `voice-service-id` is the voice service `sys_id`.

</td><td>

Client ID from the ServiceNow voice service configuration.

</td></tr><tr><td>

`/com.servicenow.cti/<sn-instance-id>/<voice-service-id>/client_secret`Where `sn-instance-id` is the value of the `instance_id` system property, and `voice-service-id` is the voice service `sys_id`.

</td><td>

Client Secret from the ServiceNow voice service configuration.

</td></tr></tbody>
</table>    8.  Add the AWS PowerTools layer to the Lambda function.

        In the Lambda console, navigate to the Lambda function and select **Layers**. Add the AWS layer `AWSLambdaPowertoolsTypeScriptV2`, version 2.33.0 or later.

10. Import and configure the Amazon Connect contact flow.

    1.  In your Amazon Connect instance, create a new contact flow by importing the Voice AI inbound flow JSON.

        See [Amazon Connect Voice AI inbound flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/voice-agent-reference.md).

        In the Amazon Connect console, navigate to **Routing** &gt; **Flows**, select **Create flow**, then use the import option. Replace all placeholder values with your own before importing.

    2.  In the first AWS Lambda function block of the contact flow, set the function ARN to the Lambda you created and set the `voice_service_id` input parameter to the `sys_id` of the voice service.

    3.  In the second AWS Lambda function block, set the function ARN to the same Lambda function.

    4.  Save and publish the contact flow.

        **Note:** When Amazon Connect transfers the call to ServiceNow, the contact flow must pass the original caller's phone number as the caller ID. Verify that your contact flow is configured to preserve the original caller ID during the transfer, not the Amazon Connect transfer number.

11. Associate a phone number with the contact flow.

    1.  In the Amazon Connect service dashboard, navigate to **Channels** &gt; **Phone numbers**.

    2.  Claim a new number or select an existing number to associate with the contact flow.

        Associating a phone number with the contact flow enables incoming calls to be routed through the voice assistant.


## Result

Amazon Connect is connected to your ServiceNow voice assistant. Incoming calls routed through Amazon Connect are handled by the AI voice agent, which responds with a greeting and processes the caller's requests. When call handling is complete, the contact flow routes the caller to a queue or ends the call.

## What to do next

Test the integration by placing a call through your Amazon Connect phone number and verifying that the voice assistant responds correctly. Review the CloudWatch logs for the Lambda function to troubleshoot any connection issues.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/integrating-voice-service-with-ccaas-providers.md)

