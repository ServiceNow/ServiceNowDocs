---
title: Set up Conversational Integration with LINE
description: Set up the Conversational Integration with LINE application so that you can engage customers in conversations with bots.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with LINE, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up Conversational Integration with LINE

Set up the Conversational Integration with LINE application so that you can engage customers in conversations with bots.

## Before you begin

Before you begin, do the following:

-   Get ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Conversational Integration with LINE
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Install the following applications on your ServiceNow instance:
    -   Integration Hub
    -   Conversational Integration with LINE
-   Activate the IHUB Spoke Util Pack plugin \(com.snc.ihub\_spoke\_util\_pack\). For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).
-   Get a developer account in the [LINE Developers console](https://developers.line.biz/console/).

Role required: external\_app\_install\_admin or va\_admin

## About this task

The LINE messaging app supports only one LINE channel for a ServiceNow instance. If you would like to configure a different LINE channel for your ServiceNow instance, you must first remove the previously configured LINE channel, and then set up the new channel.

## Procedure

1.  Connect your company's LINE account with your ServiceNow instance.

    1.  Log in to your [LINE Developers Console](https://developers.line.biz/console/).

    2.  [Create a channel on the LINE Developers Console.](https://developers.line.biz/en/docs/messaging-api/getting-started/#using-console)

    3.  Take note of the channel secret and the channel access token.

        You will use later use this information for authenticating the LINE account on your ServiceNow instance.

    4.  To enable your LINE account to send data to your ServiceNow instance, enter the webhook URL and click **Verify**

        You specify the webhook URL in the **Webhook URL** field on the Messaging API tab of the LINE Developers Console. Use the following format for the URL: `https://<instance-name>.service-now.com/api/sn_va_line/va_adapter_line`.

2.  On your ServiceNow® instance, go to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

3.  On the LINE integration section, click **Manage**.

    The Line Channel integration page opens.

4.  Click the three dots on the right hand side and choose **Edit Integration**.

5.  On the form, update the name of the bot if desired.

6.  Enter the channel secret and the access token from your LINE account.

7.  Click **Submit**.

    A success message displays confirming the integration with the LINE app.


