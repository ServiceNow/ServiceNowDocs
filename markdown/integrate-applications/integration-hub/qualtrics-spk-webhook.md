---
title: Set up a bi-directional webhook for the Qualtrics spoke
description: Configure a webhook to subscribe to Qualtrics with a ServiceNow callback URL.Add a token for the Qualtrics spoke in the Token Verification \[token\_verification\] table. The webhook registry records use this token to authenticate requests.For the required default webhook registry, add token and generate callback URL.Subscribe to the required event in your ServiceNow instance by adding callback URL in the Create Subscription action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/qualtrics-spk-webhook.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 2
breadcrumb: [Qualtrics Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Qualtrics spoke

Configure a webhook to subscribe to Qualtrics with a ServiceNow callback URL.

## Before you begin

Role required: admin

## Add a token for the Qualtrics spoke

Add a token for the Qualtrics spoke in the Token Verification \[token\_verification\] table. The webhook registry records use this token to authenticate requests.

### Before you begin

Role required: admin

### Procedure

1.  In the filter navigator, enter `token_verification.list` and press the Enter or Return key.

    The records in the Token Verification \[token\_verification\] table are displayed.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the token record.|
    |Description|Description of the token.|

4.  Click **Generate Secure Token**.

    \[Omitted image "qualtrics-token.png"\] Alt text:

    Token value is generated and populated in the **Token** field.

5.  Click the toggle visibility icon \[Omitted image "qualtrics-toggle-icon.png"\] Alt text:.

    The value of token is displayed.

6.  Copy and record the value of token for later use.

    \[Omitted image "qualtrics-token-toggle.png"\] Alt text:


## Generate callback URL for the required webhook registry

For the required default webhook registry, add token and generate callback URL.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Qualtrics Spoke** &gt; **Qualtrics Webhook Registry**.

    The list of default webhook registry records is displayed.

2.  Click the required webhook registry.

    For example, **Recipient session started event**.

3.  On the Qualtrics Webhook Registry, for the **Token** field, search and select the token record you had previously created.

4.  Right-click the form header and click **Save**.

5.  Click **Callback URL Qualtrics**.

    The callback URL is generated and displayed.

    \[Omitted image "qualtrics-callback-url-gen.png"\] Alt text:

6.  Copy and record the callback URL for later use.


## Subscribe to webhook event in ServiceNow instance

Subscribe to the required event in your ServiceNow instance by adding callback URL in the Create Subscription action.

### Before you begin

Identify the events you want to get notified about. For the full list of events, see [Qualtrics API documentation](https://api.qualtrics.com/66b2ec694d5c2-webhooks). For example, to enable notifications when a survey is activated, enter `controlpanel.activateSurvey`. To scope notifications to one specific survey, add its Survey ID to the event name. For example, `surveyengine.startedRecipientSession.{SurveyID}`. Replace `{SurveyID}` with the required Survey ID.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click **Actions**.

    The list of actions is displayed.

3.  Search and open the **Create Subscription** action in the Qualtrics spoke.

4.  Click **Test**.

5.  On the Test Action form, fill these values.

    |Field|Description|
    |-----|-----------|
    |URL|Enter the callback URL you had generated previously.|
    |Topics|Enter the event for which you want to enable notifications. For example, `controlpanel.activateSurvey`.|
    |Shared Key|Enter the value of token you had generated previously.|

    **Note:** Do not select the **Encrypt** option.

6.  Click **Run Test**.

    Subscription is created for the event.


