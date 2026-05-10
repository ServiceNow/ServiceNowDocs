---
title: Set up Conversational Integration with Facebook Messenger
description: Integrate Facebook Messenger with your ServiceNow instance using the Conversational Integration with Facebook Messenger application. Use the application to engage customers in conversations with bots.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational Integration with Facebook Messenger, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up Conversational Integration with Facebook Messenger

Integrate Facebook Messenger with your ServiceNow instance using the Conversational Integration with Facebook Messenger application. Use the application to engage customers in conversations with bots.

## Before you begin

-   Get ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Conversational Integration with Facebook Messenger
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Install the following applications on your ServiceNow instance:
    -   Integration Hub
    -   Conversational Integration with Facebook Messenger
-   Complete Facebook Messenger settings.
    1.  [Set up a Facebook developer account](https://developers.facebook.com/).
    2.  [Create a Facebook app](https://developers.facebook.com/docs/messenger-platform/getting-started/app-setup).
    3.  [Review the Messenger Platform Policy](https://developers.facebook.com/docs/messenger-platform/policy/policy-overview) and [Pre-Launch Checklist](https://developers.facebook.com/docs/messenger-platform/prelaunch-checklist) prior to submission.
    4.  [Submit the app for review](https://developers.facebook.com/docs/messenger-platform/#review---submission-process).
    5.  [Create a Facebook page within the Facebook app you created earlier](https://www.facebook.com/pages/creation/).
    6.  [Enable Facebook Messenger](https://www.facebook.com/help/994476827272050/?helpref=hc_fnav).

Role required: external\_app\_install\_admin or va\_admin

## Procedure

1.  Connect your company's Facebook Messenger service with your ServiceNow instance.

    1.  Log in to your [Facebook developer account](https://developers.facebook.com/) and open the Facebook app you created.

    2.  Enable your Facebook app to send data to your ServiceNow instance by entering the webhook URL.

        1.  Click **Add Callback URL** in the Webhooks section of the app.
        2.  In the Edit Callback URL dialog box, fill in the fields.

<table id="table_lf5_qfp_j4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Callback URL

</td><td>

Public URL for webhook.Enter the webhook URL in the following format:

 `https://<instance-name>.service-now.com/api/now/v1/cs/adapter/messenger/message`

</td></tr><tr><td>

Token

</td><td>

Token for webhook.By default, the token for ServiceNow webhook is `nowbot`. As a user with the admin role, you can set the **glide.cs.facebook\_messenger\_verify\_token** system property to a desired value and then enter that value in this field. Because the **glide.cs.facebook\_messenger\_verify\_token** system property isn't available by default, you must add it with the data type set to string. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

</td></tr></tbody>
</table>        3.  Click **Verify and Save**.
    3.  Make a note of your Facebook page ID and access token.

        1.  Click **Add or Remove Pages** and select your Facebook page.
        2.  Make a note of the page ID displayed below the page name.

            You can click the page ID to copy the ID to your clipboard.

        3.  In the Access Tokens section, click **Generate Token** for the Facebook page you created.

            **Note:** Make note of the page access token used later for authenticating the Facebook Messenger on your ServiceNow instance.

    4.  Subscribe your Facebook app to your Facebook page.

        1.  In the Webhooks section, click **Add Subscriptions**.

            For each authorized Page, the Webhooks section contains the fields the app can subscribe to.

        2.  In the Edit Page Subscriptions dialog box, select **messages** and **messaging\_postbacks**.
        3.  Click **Save**.
    5.  [Make a note of the App secret from Basic Settings](https://developers.facebook.com/docs/development/create-an-app/app-dashboard/basic-settings).

    6.  Send messages with timestamp in the customer's time zone by navigating to **Page settings** &gt; **Advanced messaging**, selecting the **Time zone** option in the Requested Features section, and clicking **Request** displayed next to the selected option.

2.  On your ServiceNow® instance, go to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

3.  On the Facebook Messenger integration section, click **Add**.

    The Facebook Messenger Channel integration page opens.

4.  Click the three dots on the right hand side and choose **Edit Integration**.

5.  On the form, update the name of the bot if desired.

6.  Enter the callback URL and the token from your Facebook Messenger account.

7.  Click **Submit**.

    A success message displays confirming the integration with the Facebook Messenger app.


**Parent Topic:**[Configure Conversational Integration with Facebook Messenger](messg-fbm-configure.md)

