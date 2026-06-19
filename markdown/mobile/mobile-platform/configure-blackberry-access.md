---
title: Configure BlackBerry Access for mobile apps
description: Configure the BlackBerry Access browser to authenticate ServiceNow mobile apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/configure-blackberry-access.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [BlackBerry UEM, Device management, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure BlackBerry Access for mobile apps

Configure the BlackBerry Access browser to authenticate ServiceNow mobile apps.

## Before you begin

Role required: admin

## About this task

The following steps are only necessary if you are using the BlackBerry Access browser as the authentication browser for your ServiceNow mobile apps. The BlackBerry Access browser must be configured in order to authenticate with your ServiceNow mobile apps.

## Procedure

1.  Sign into the BlackBerry UEM.

2.  In the menu bar to the left, click **Apps**.

    \[Omitted image "BB-EUM-menu.png"\] Alt text: BlackBerry UEM menu bar

    You see a list of available apps tied to your BlackBerry UEM.

3.  In the search bar above the list of apps, type `BlackBerry Access`.

    \[Omitted image "BB-UEM-3.png"\] Alt text: BlackBerry UEM available apps list

4.  Click **BlackBerry Access** to open the app.

5.  When the app opens, click on the blue text labeled **App Config With Default Values** to create the app configuration for this app.

    \[Omitted image "BB-UEM-app-config.png"\] Alt text: BlackBerry UEM app settings screen

6.  Enable **Allow external apps** to open HTTP/HTTPS URLs through BlackBerry Access.

7.  Enable **Enable 3rd Part Applications**.

8.  Add these values: `snappauth,snempappauth`

    **Important:**

    -   Do not use any spaces in the above values.
    -   The **snappauth** is required for the Mobile Agent app. The **snempappauth** value is required for the Now Mobile app.
9.  Click **Save**.


**Parent Topic:**[BlackBerry Unified Endpoint Management \(UEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/blackberry-uem.md)

