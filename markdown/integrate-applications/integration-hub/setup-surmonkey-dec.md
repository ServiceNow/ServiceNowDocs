---
title: Set up the SurveyMonkey spoke
description: Integrate the ServiceNow instance and SurveyMonkey account by creating a custom OAuth application in SurveyMonkey API Developer Portal to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SurveyMonkey Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SurveyMonkey spoke

Integrate the ServiceNow instance and SurveyMonkey account by creating a custom OAuth application in SurveyMonkey API Developer Portal to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SurveyMonkey spoke.
-   Role required: admin.

## Procedure

1.  Log in to [SurveyMonkey API Developer Portal](https://developer.surveymonkey.com/) as an admin and add an app.

    1.  In **OAuth Redirect URL**, enter the ServiceNow instance URL in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

    2.  Copy and record the values of **Client ID** and **Secret**.

    3.  Provide these scopes for the app:

        -   Create/Modify Surveys
        -   Create/Modify Collectors
        -   Create/Modify Responses
        -   View Response Details
        -   View Contacts
        -   Create/Modify Webhooks
        -   View Library Assets
        -   View Surveys
        -   View Collectors
        -   View Responses
        -   Create/Modify Contacts
        -   View Users
        -   View Webhook
        **Note:** If you provide any additional scopes, ensure that you add these scopes in the **OAuth Entity Scopes** tab of the default application registry available in your ServiceNow instance.

2.  Configure the default application registry.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Open the record, **Survey Monkey**.

    3.  On the form, fill these values:

        |Field|Description|
        |-----|-----------|
        |Client ID|Client ID of the app created in [SurveyMonkey API Developer Portal](https://developer.surveymonkey.com/).|
        |Client Secret|Secret of the app created in [SurveyMonkey API Developer Portal](https://developer.surveymonkey.com/).|
        |Redirect URL|ServiceNow instance URL in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`. Replace `<instance-name>` with your instance name.|

        **Note:** If you have provided additional scopes, create records for those scopes in the **OAuth Entity Scopes** tab.

3.  Create a credential record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message **What type of Credentials would you like to create?**.

    3.  Select **OAuth 2.0 Credentials**.

    4.  On the form, fill in the fields.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the record. Enter `SurveyMonkey Credentials`.|
        |Active|Option to actively use the credential record.|
        |OAuth Entity Profile|OAuth profile you created when you registered the SurveyMonkey app as an OAuth provider. Select **Survey Monkey default\_profile**.|
        |Applies to|MID Servers that can use this credential. Select **All MID Servers**.|
        |Order|Order to apply this credential. Enter `100`.|

    5.  Right-click the form header and click **Save**.

4.  Create a connection record.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open for the record for **SurveyMonkey**.

    3.  From the **Connections** tab, click **New**.

        The system displays a blank HTTP\(s\) Connection form.

    4.  On the form, fill these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the connection record. Enter`SurveyMonkey Connection`.|
        |Credential|Credential record you created for Zoom. Select **SurveyMonkey Credentials**.|
        |Connection alias|Alias record associated with this connection.|
        |Connection URL|Base URL to connect to your SurveyMonkey account. Enter `https://api.surveymonkey.net`.|
        |Active|Option to actively use the connection.|
        |Domain|Domain that the action or activity runs in.|

    5.  In the **Attributes** tab, provide your SurveyMonkey API version if it is different than the default value of v3.

    6.  Click **Submit**.

    The ServiceNow instance and SurveyMonkey account are integrated.


