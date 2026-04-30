---
title: Configure your Alexa account
description: Configure your Alexa account to link it with your ServiceNow instance.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Account linking with Alexa, Configure Conversational Integration with Alexa, Integrating Virtual Agent with Alexa, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure your Alexa account

Configure your Alexa account to link it with your ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your Alexa developer console with your Alexa developer account.

2.  Navigate to the **Build** &gt; **MODELS** &gt; **ACCOUNT LINKING**.

3.  On the Account Linking form, swipe the **Do you allow users to create an account or link to an existing account with you?** toggle switch to the right.

4.  In the Settings section of the form, swipe the **Allow users to authenticate using your mobile application** toggle switch to the right.

5.  In the Security Provider Information section of the form, click **Auth Code Grant**.

6.  On the form, fill in the fields.

<table id="table_hhf_svd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Your Web Authorization URI

</td><td>

The URI that authorizes your web access.For example:`https://<instance-name>.service-now.com/oauth_auth.do`.

**Note:** The instance-name for Alexa is `voice`.

</td></tr><tr><td>

Your iOS App Authorization URI

</td><td>

The URI that authorizes your iOS app.Provide `voice` as the value.

</td></tr><tr><td>

Your Android App Authorization URI

</td><td>

The URI that authorizes your Android app.Provide `voice` as the value.

</td></tr><tr><td>

Access Token URI

</td><td>

The URI that authorizes the access to the API requests.For example, `https://<instance-name>.service-now.com/oauth_token.d`o

**Note:** The instance-name for Alexa is `voice`.

</td></tr><tr><td>

Your Client ID

</td><td>

Auto-generated unique ID of the client application requesting the access token.**Note:** Provide the Client ID generated while creating an OAuth API endpoint for external clients.

</td></tr><tr><td>

Your Secret

</td><td>

The shared secret string that the instance and the OAuth application use to authorize communications with one another.

</td></tr></tbody>
</table>7.  Click **Save**.

8.  Copy one of the URLs from the **Alexa Redirect URLs** field in the Auth Code Grant section.

    **Note:** Insert the copied URL in the Redirect URL field of the OAuth API record created in your ServiceNow instance.

    If you face an issue with one of the URLs, try to use the next available URL and pick the one that works.

9.  Click **Save**.


