---
title: Integrate ServiceNow voice assistant with Amazon Connect
description: Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Amazon Connect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/integrate-voice-service-with-amazon-connect.html
release: zurich
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 7
keywords: [Amazon Connect, voice assistant, voice integration, CCaaS, telephony provider, AI voice agent, PSTN, Lambda]
breadcrumb: [Integrating voice assistant with CCaaS provider, Deploy AI voice agents, AI Agent Studio, Enable AI experiences]
---

# Integrate ServiceNow voice assistant with Amazon Connect

Enable users to get support from AI voice agents by integrating a ServiceNow voice assistant with Amazon Connect.

## Before you begin

-   Create a voice assistant. See [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-an-ai-voice-service.md) for more information.
-   Access to your Amazon Connect instance with permissions to create Lambda functions, configure contact flows, and manage Identity and Access Management \(IAM\) roles.

Role required: sn\_aia.admin

## About this task

Connect your Amazon Connect contact center to a ServiceNow voice assistant using the Public Switched Telephone Network \(PSTN\) communication channel. When a call arrives, Amazon Connect invokes a Lambda function that retrieves a PSTN number from the ServiceNow Call Context API and transfers the call to the voice assistant. After the voice assistant handles the interaction, the Lambda function retrieves the interaction context and routes the call to a queue or ends the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to Amazon Connect and select **Edit**.

3.  Select the **Settings** tab.

4.  Select **Communication channels** from the guided setup navigation.

5.  In the **Provider application** field, select the provider application to deploy the voice assistant to.

6.  Select the **Telephony provider** tab.

7.  From the **Communication channels** dropdown, select **Public Switched Telephone Network \(PSTN\)**.

8.  From the **CCaaS provider** dropdown, select **Amazon Connect**.

    The following read-only fields are generated in the **Call context service** section. Copy and save these values — you will need them to configure the integration on the Amazon Connect side.

    |Field|Description|
    |-----|-----------|
    |Transfer method|Read-only. Set to **BYE** for Amazon Connect.|
    |Call context API|Read-only. The URL that Amazon Connect uses to send call context data to the voice assistant. Copy this value for use as the `call_context_api_path` and `voice_service_host_name` Lambda environment variables.|
    |Client ID|Read-only. Generated client ID for OAuth2 authentication. Copy this value for use in the AWS Parameter Store setup.|
    |Client Secret|Read-only. Generated client secret for OAuth2 authentication. Copy this value for use in the AWS Parameter Store setup.|

    \[Omitted image "voice-agents-amazon-connect-integration.png"\] Alt text: Amazon Connect integration configuration showing the Transfer method, Call context API URL, Client ID, and Client Secret fields.

    Also note the voice service `sys_id`, which you can find in the URL when viewing the voice service record. You will need this value in the Amazon Connect configuration steps.

9.  Enable context data persistence for the voice service.

    1.  Navigate to `sys_now_assist_deployment_config_attributes.list` and check whether a `persist_context_data` attribute exists for your voice service.

    2.  If the attribute exists, open it and set **Value** to `true`.

        This setting allows the Lambda function to retrieve interaction context data from ServiceNow after the voice assistant completes the call.

        \[Omitted image "voice-agents-persist-context-data.png"\] Alt text: The persist\_context\_data configuration attribute record for the voice service with its value set to true.

    3.  If the attribute does not exist, navigate to `sys_now_assist_deployment_config.list`, open your voice assistant's deployment configuration record, and copy its `sys_id`.

        To copy the `sys_id`, right-click the record header bar and select **Copy sys\_id**.

    4.  Navigate to `sys_now_assist_deployment_config_attributes.list`, click **New**, set **Deployment Config** to the `sys_id` you copied, **Name** to `persist_context_data`, and **Value** to `true`, then click **Submit**.

10. In your AWS account, create the Lambda function that connects Amazon Connect to the voice assistant.

    1.  From the AWS console, create a new Lambda function.

    2.  In the Lambda function code editor, replace the default handler code with the Lambda function code.

        See [Amazon Connect Lambda function code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/voice-agent-reference.md).

    3.  Set the following environment variables on the Lambda function.

<table id="table_lambda_env_vars"><thead><tr><th>

Variable

</th><th>

Value

</th></tr></thead><tbody><tr><td>

`call_context_api_path`

</td><td>

The path portion of the ServiceNow call context URL — the part of the URL after `.com`.

</td></tr><tr><td>

`now_instance_host_name`

</td><td>

The ServiceNow instance URL, without the `https://` prefix.

</td></tr><tr><td>

`now_instance_name`

</td><td>

The name portion of your ServiceNow instance URL. For example, `myinstance`, not `myinstance.service-now.com`.

</td></tr><tr><td>

`ssm_oauth_path`

</td><td>

The base path for OAuth credentials in AWS Parameter Store: `/com.servicenow.cti/<sn-instance-id>`.

</td></tr><tr><td>

`voice_service_host_name`

</td><td>

The hostname from the ServiceNow call context URL.

</td></tr></tbody>
</table>        **Note:** Both `call_context_api_path` and `voice_service_host_name` are derived from the Call Context API URL in the voice service configuration. `voice_service_host_name` uses the hostname portion of that URL, and `call_context_api_path` uses the path portion after `.com`.

        \[Omitted image "voice-agents-amazon-connect-lambda-env-vars.png"\] Alt text: The Lambda environment variables panel showing call\_context\_api\_path, now\_instance\_host\_name, now\_instance\_name, ssm\_oauth\_path, and voice\_service\_host\_name populated with example values.

    4.  Grant your Amazon Connect instance permission to invoke the Lambda function.

        In the Amazon Connect console, navigate to your instance, select **Flows**, and under **AWS Lambda**, add the Lambda function with the Invoke Lambda use case. Confirm the policy was added in the Lambda console under **Configuration** &gt; **Permissions**.

        \[Omitted image "voice-agents-amazon-connect-lambda-permission.png"\] Alt text: The AWS Lambda section under Flows in the Amazon Connect instance, showing the Lambda functions dropdown and Invoke Lambda use case.

    5.  Replace the Lambda execution role permissions policy with the Identity and Access Management \(IAM\) policy.

        See [Amazon Connect Lambda Identity and Access Management \(IAM\) policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/voice-agent-reference.md).

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

`/com.servicenow.cti/<sn-instance-id>/<voice-service-id>/client_id`Where `sn-instance-id` is the value of the `instance_id` system property \(to find this value, navigate to `sys_properties.list` and search for `instance_id`\), and `voice-service-id` is the voice service `sys_id`.

</td><td>

Client ID from the ServiceNow voice service configuration.

</td></tr><tr><td>

`/com.servicenow.cti/<sn-instance-id>/<voice-service-id>/client_secret`Where `sn-instance-id` is the value of the `instance_id` system property \(to find this value, navigate to `sys_properties.list` and search for `instance_id`\), and `voice-service-id` is the voice service `sys_id`.

</td><td>

Client Secret from the ServiceNow voice service configuration.

</td></tr></tbody>
</table>        \[Omitted image "voice-agents-amazon-connect-param-store.png"\] Alt text: AWS Parameter Store filtered to the /com.servicenow.cti/ path, showing the client\_id and client\_secret parameters created as SecureString type.

    8.  Add the AWS PowerTools layer to the Lambda function.

        In the Lambda console, navigate to the Lambda function and select **Layers**. Add the AWS layer `AWSLambdaPowertoolsTypeScriptV2`, version 2.33.0 or later.

11. Import and configure the Amazon Connect contact flow.

    1.  In your Amazon Connect instance, create a new contact flow by importing the Voice AI inbound flow JSON.

        See [Amazon Connect Voice AI inbound flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/voice-agent-reference.md).

        In the Amazon Connect console, navigate to **Routing** &gt; **Flows**, select **Create flow**, then use the import option. Replace all placeholder values with your own before importing.

        \[Omitted image "voice-agents-amazon-connect-contact-flow.png"\] Alt text: The imported Voice AI inbound contact flow showing two AWS Lambda function blocks and a Transfer to phone number block.

    2.  In both AWS Lambda function blocks, set the function ARN to your Lambda and set the `voice_service_id` parameter to the voice service `sys_id`.

        \[Omitted image "voice-agents-amazon-connect-lambda-block.png"\] Alt text: The Destination Key dialog in an AWS Lambda function block showing the voice\_service\_id key with its value set to the voice service sys\_id.

    3.  Save and publish the contact flow.

        **Note:** When Amazon Connect transfers the call to ServiceNow, the contact flow must pass the original caller's phone number as the caller ID. Verify that your contact flow is configured to preserve the original caller ID during the transfer, not the Amazon Connect transfer number.

        \[Omitted image "voice-agents-amazon-connect-transfer-block.png"\] Alt text: The Transfer to phone number block configured with Transfer to set dynamically using the pstnNumber contact attribute, and Resume flow after disconnect set to Yes.

12. Associate a phone number with the contact flow.

    1.  In the Amazon Connect service dashboard, navigate to **Channels** &gt; **Phone numbers**.

    2.  Claim a new number or select an existing number to associate with the contact flow.

        Associating a phone number with the contact flow enables incoming calls to be routed through the voice assistant.


## Result

Amazon Connect is connected to your ServiceNow voice assistant. Incoming calls routed through Amazon Connect are handled by the AI voice agent, which responds with a greeting and processes the caller's requests. When call handling is complete, the contact flow routes the caller to a queue or ends the call.

## What to do next

Test the integration by placing a call through your Amazon Connect phone number and verifying that the voice assistant responds correctly. Review the CloudWatch logs for the Lambda function to troubleshoot any connection issues.

**Parent Topic:**[Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md)

