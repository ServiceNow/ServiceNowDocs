---
title: Set up the X spoke
description: Integrate the ServiceNow instance and X account to authenticate the requests from ServiceNow.Create an app in the X developer account and obtain the values of Access Token, Access Token Secret, Consumer key, and Consumer Secret for authenticating the requests.Add and configure the X connections to authenticate ServiceNow requests in the X spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [X Spoke \(formerly Twitter Spoke\), Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the X spoke

Integrate the ServiceNow instance and X account to authenticate the requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the X spoke.
-   Role required: admin.

## Obtain the token and secret values from the X developer account

Create an app in the X developer account and obtain the values of Access Token, Access Token Secret, Consumer key, and Consumer Secret for authenticating the requests.

### Before you begin

Role required: X admin.

### Procedure

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


## Configure a connection for the X spoke \(formerly Twitter spoke\)

Add and configure the X connections to authenticate ServiceNow requests in the X spoke.

### Before you begin

-   Access Token and Access Token Secret of your X developer app.
-   Consumer key and Consumer Secret of your X developer app.
-   Ensure that the Application scope is X scope.
-   Role required: ServiceNow admin

See the [X Developers](https://developer.twitter.com) documentation for instructions on creating the developer application and gathering the required details.

### About this task

Two connections, **Twitter** and **Twitter\_Media**, are provided in the Flow Designer. You must configure both of these connections.

### Procedure

1.  Configure the **Twitter** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Select the **Connections** tab.

    4.  In the Search all connections field, enter `Twitter`.

    5.  On the Twitter tile, select **View Details**.

        ![](../image/twitter-alias-view-details.png)

    6.  Select **Configure**.

    7.  On the **Configure Connection** form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to identify the Twitter connection alias record.|
        |Connection URL|Enter `https://api.twitter.com`.|
        |Consumer Key|Consumer key of your X developer app.|
        |Consumer Secret|Consumer secret of your X developer app.|
        |Access Token|Access token of your X developer app.|
        |Access Token Secret|Access token secret of your X developer app.|

        ![Twitter alias connection form.](../image/twitter-conn-form.png)

    8.  Select **Create Connection**.

2.  Configure the **Twitter\_Media** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Select the **Connections** tab.

    4.  In the Search all connections field, enter `Twitter_Media`.

    5.  On the Twitter\_Media tile, select **View Details**.

        ![Twitter_media alias View Details.](../image/twitter-media-alias-view-details.png)

    6.  Select **Configure**.

    7.  On the **Create Connection** form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to identify the Twitter connection alias record.|
        |Connection URL|Enter `https://upload.twitter.com`.|
        |Consumer Key|Consumer key of your X developer app.|
        |Consumer Secret|Consumer secret of your X developer app.|
        |Access Token|Access token of your X developer app.|
        |Access Token Secret|Access token secret of your X developer app.|

        ![Twitter alias connection form.](../image/twitter-conn-form.png)

    8.  Select **Create Connection**.


