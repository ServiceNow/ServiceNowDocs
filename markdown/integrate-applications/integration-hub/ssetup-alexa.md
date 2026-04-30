---
title: Set up the Amazon Alexa spoke
description: Integrate the ServiceNow instance and Amazon Alexa account by creating a custom OAuth application in Amazon Alexa to authenticate ServiceNow requests.Create and register a security profile through the Developer Console to use Login with Amazon on your ServiceNow instance.Add and configure a Amazon Alexa connection to authenticate ServiceNow requests in the Amazon Alexa spoke.Authenticate the inbound requests from Amazon Alexa account to your ServiceNow instance by creating a webhook registry.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Amazon Alexa Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon Alexa spoke

Integrate the ServiceNow instance and Amazon Alexa account by creating a custom OAuth application in Amazon Alexa to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Amazon Alexa spoke.
-   Role required: admin

## Create a security profile

Create and register a security profile through the Developer Console to use Login with Amazon on your ServiceNow instance.

### Before you begin

Role required: admin.

### Procedure

1.  Log in to [Amazon Developer Portal](https://developer.amazon.com/) with admin credentials.

2.  Create a security profile.

    For information about creating a security profile, see [Create an LwA Security Profile](https://developer.amazon.com/docs/dash/create-a-security-profile.html) in [Amazon Developer Documentation](https://developer.amazon.com/documentation).

3.  Copy and record the values of Client ID and Client Secret for later use.

4.  Configure the security profile and specify these values in **Web Settings**:

    |Field|Value|
    |-----|-----|
    |Allowed Origins|ServiceNow instance URL.|
    |Allowed Return URLs|ServiceNow instance redirect URL in this format: `https://<Instance-Name>.com/oauth_redirect.do`|

    For more information about configuring the security policy, see [Add your Website to your Security Profile](https://developer.amazon.com/docs/login-with-amazon/register-web.html#add-your-website-to-your-security-profile) in [Amazon Developer Documentation](https://developer.amazon.com/documentation).


## Configure a connection for Amazon Alexa spoke

Add and configure a Amazon Alexa connection to authenticate ServiceNow requests in the Amazon Alexa spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **AmazonAlexa** connection alias and click **View Details**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name to uniquely identify the record. By default, the name is `AmazonAlexa`.|
    |Connection URL|Base URL to connect to Amazon Alexa. Enter: `https://api.amazonalexa.com`|
    |API Version|Required API version of Amazon Alexa. Enter `v1`.|
    |Credential Information|
    |OAuth Entity Name|Name to identify the OAuth entity record. For example, `Amazon Alexa OAuth`.|
    |OAuth Client ID|Client ID created during the configuration of the security profile.|
    |OAuth Client Secret|Client Secret created during the configuration of the security profile.|
    |OAuth Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. Replace `<instance>` with the ServiceNow instance name.|

6.  Click **Configure and Get OAuth Token**.


## Setup webhook for the Amazon Alexa spoke

Authenticate the inbound requests from Amazon Alexa account to your ServiceNow instance by creating a webhook registry.

### Before you begin

Role required: admin.

### Procedure

1.  In the filter navigator, enter `token_verification.list`.

    Records in the Token Verifications \[token\_verification\] table are displayed.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the token record. For example, `Alexa token`.|
    |Description|Brief description of the token.|
    |Token|Value of token. This value is encrypted before it is used.|

4.  Click **Submit**.

5.  Navigate to **Alexa Webhooks** &gt; **Alexa Webhook Registries**.

6.  Click **New**.

7.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the webhook registry record. For example, `Alexa token`.|
    |Description|Brief description of the webhook registry record.|
    |Token|Token you have created. For example, `Alexa token`.|
    |Path|Scripted REST endpoint. A default endpoint is available. You can change the default value as per your requirement.|

8.  Right-click the form header and click **Save**.

9.  Click **Callback URL**.

    Webhook Callback URL is displayed in the confirmation message. Copy and record this value.

10. Log in to [AWS Management Console](https://aws.amazon.com/console/).

11. In the AWS Lambda function, specify the Webhook Callback URL and save the changes.

    ![Webhook Callback URL](../image/alexa-url.png)

12. Log in to [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask).

13. Navigate to **Build** &gt; **CUSTOM** &gt; **Endpoint** and specify ARN of the AWS Lambda function you had configured.

    ![AWS Lambda ARN](../image/alexa-lambda-arn.png)


