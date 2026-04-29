---
title: Configure mobile app token lifespan
description: Configure the length of time it takes for the app to time out.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile app token lifespan

Configure the length of time it takes for the app to time out.

## Before you begin

Role required: admin

## About this task

Mobile apps timeout when their associated OAuth token expires. Token lifespans are considered active if the app is in the foreground or if the app is processing a long running task in the background.

## Procedure

1.  Configure the OAuth entity for a mobile app.

    1.  Navigate to **System OAuth** &gt; **Application Registry** and open the OAuth entity for the application you want to modify.

        For example, open the **ServiceNow Agent** record to modify the timeout for your Mobile Agent. To modify the timeout for your Now Mobile app, open the **ServiceNow Request** record.

    2.  In the Refresh Token Lifespan field, change the number in seconds to the amount of time the refresh token is valid.

    3.  In the Access Token Lifespan field, change the number in seconds to the amount of time the access token is valid.


## Result

For example, if you want the mobile app's token to expire after 30 minutes, use the following configuration.

|Configuration point|Setting|
|-------------------|-------|
|Refresh Token Lifespan for the Mobile Agent mobile app or the Now Mobile app|1800 seconds|
|Access Token Lifespan for the Mobile Agent mobile app or the Now Mobile app|1800 seconds|

## What to do next

Sign out and sign back in to the mobile app. Otherwise the app uses the previously granted sessions and tokens.

**Parent Topic:**[Mobile authentication](../concept/mobile-authentication.md)

