---
title: Obtain the token and secret values from the X developer account
description: Create an app in the X developer account and obtain the values of Access Token, Access Token Secret, Consumer key, and Consumer Secret for authenticating the requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up the X spoke, X Spoke \(formerly Twitter Spoke\), Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Obtain the token and secret values from the X developer account

Create an app in the X developer account and obtain the values of Access Token, Access Token Secret, Consumer key, and Consumer Secret for authenticating the requests.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the [Developer Portal - Twitter Developer - X \(formerly Twitter\)](https://developer.twitter.com/en/portal/dashboard).

2.  Obtain the values of **API Key**, **API Key Secret**, and **Bearer Token**.

    1.  Navigate to **Projects &amp; Apps** &gt; **Default project**.

    2.  Under **Apps**, click **+Add App**.

    3.  Under **App Environment**, choose the required environment and lick **Next**.

    4.  Under **App name**, provide the app name in **DEVELOPMENT APP** and click **Next**.

        Under **Keys &amp; Tokens**, the values of **API Key**, **API Key Secret**, and **Bearer Token** are displayed.![Values of API Key, API Key Secret, and Bearer Token.](../image/x-spk-keys-tokens.png)

    5.  Copy and record these values for later use.

3.  Provide the required permissions for OAuth 1.0.

    1.  Navigate to **Projects &amp; Apps** &gt; **Default project**.

    2.  Navigate to the app you had created.

    3.  In the **Settings** tab, under **User authentication settings**, click **Set up**.

    4.  On the User authentication settings page, under **App permissions** select the **Read and write and Direct message** option.![App permissions.](../image/x-spk-app-permissions.png)

    5.  Click **Save**.

        The systems prompts you to confirm the permissions.

    6.  Copy and record these values for later use.

    7.  Click **Done**.

4.  Obtain the values of **Access Token** and **Access Token Secret**.

    1.  Navigate to **Projects &amp; Apps** &gt; **Default project**.

    2.  Navigate to the app you had created.

    3.  Click the **Keys and tokens** tab.

    4.  Under **Authentication Tokens**, click **Regenerate** for **Access Token and Secret**.

        System prompts you to confirm.

    5.  Click **Yes, regenerate**.

        The values of **Access Token** and **Access Token Secret** are displayed.![Copy the values of Access Token and Access Secret.](../image/x-spk-access-tok-sec.png)

    6.  Copy these values for later use.


