---
title: Configure a connection for the X spoke \(formerly Twitter spoke\)
description: Add and configure the X connections to authenticate ServiceNow requests in the X spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/integrate-applications/integration-hub/twitter-spk-conf-temp-ol.html
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up the X spoke, X Spoke \(formerly Twitter Spoke\), Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure a connection for the X spoke \(formerly Twitter spoke\)

Add and configure the X connections to authenticate ServiceNow requests in the X spoke.

## Before you begin

-   Access Token and Access Token Secret of your X developer app.
-   Consumer key and Consumer Secret of your X developer app.
-   Ensure that the Application scope is X scope.
-   Role required: admin

See the [X Developers](https://developer.twitter.com) documentation for instructions on creating the developer application and gathering the required details.

## About this task

Two connections, **Twitter** and **Twitter\_Media**, are provided in the Flow Designer. You must configure both of these connections.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Select the **Connections** tab.

4.  In the Search all connections field, enter `Twitter`.

5.  On the Twitter tile, select **View Details**.

    \[Omitted image "twitter-alias-view-details.png"\] Alt text:

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

    \[Omitted image "twitter-conn-form.png"\] Alt text: Twitter alias connection form.

8.  Select **Create Connection**.

9.  Configure the **Twitter\_Media** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Select the **Connections** tab.

    4.  In the Search all connections field, enter `Twitter_Media`.

    5.  On the Twitter\_Media tile, select **View Details**.

        \[Omitted image "twitter-media-alias-view-details.png"\] Alt text: Twitter\_media alias View Details.

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

        \[Omitted image "twitter-conn-form.png"\] Alt text: Twitter alias connection form.

    8.  Select **Create Connection**.


