---
title: Managing ServiceNow mobile apps with BlackBerry UEM
description: Learn how to manage ServiceNow mobile applications in the BlackBerry UEM \(Unified Endpoint Management\).
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [BlackBerry Unified Endpoint Management \(UEM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Managing ServiceNow mobile apps with BlackBerry UEM

Learn how to manage ServiceNow mobile applications in the BlackBerry UEM \(Unified Endpoint Management\).

## Before you begin

Role required: admin

## Procedure

1.  Sign into the BlackBerry UEM.

2.  In the menu bar to the left, click **Apps**.

    ![BlackBerry UEM menu bar](../image/BB-EUM-menu.png)

    You see a list of available apps tied to your BlackBerry UEM.

3.  In the search bar above the list of apps, type `ServiceNow`.

    ![BlackBerry UEM available apps list](../image/BB-UEM-2.png)

4.  Click the app you want to register.

5.  When the app opens, click on the blue text labeled **App Config With Default Values** to create the app configuration for this app.

    ![BlackBerry UEM app settings screen](../image/BB-UEM-app-config.png)

6.  In the app configuration form, fill in the fields as needed.

    |Field|Value|
    |-----|-----|
    |Default Instance URL|Your instance URL. For example, `https://INSTANCENAME.service-now.com`.|
    |iOS Authentication Browser|The browser your app will use for authentication on iOS devices.|
    |Android Authentication Browser|The browser your app will use for authentication on Android devices.|

    ![BlackBerry UEM app configuration form with example values.](../image/BB-UEM-app-config-2.png)

7.  Click **Save** to save the app configuration.

8.  Click **Save** to save the app.

    **Note:** If using the instructions above to setup the BlackBerry Access browser as your authentication browser, you must also have an app configuration setup for the BlackBerry Access app. This is necessary to successfully authenticate to ServiceNow integrated apps.


**Parent Topic:**[BlackBerry Unified Endpoint Management \(UEM\)](../concept/blackberry-uem.md)

