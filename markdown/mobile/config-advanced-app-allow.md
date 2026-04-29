---
title: Configure advanced app allowance with links to permitted apps
description: Configure a scripted extension point with a list of mobile apps that can log in to the ServiceNow instance. When a user attempts to log in with an unauthorized app, the admin can add a link that redirects the user to an authorized app.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Control app use, Configuring the Mobile Platform, Mobile Platform]
---

# Configure advanced app allowance with links to permitted apps

Configure a scripted extension point with a list of mobile apps that can log in to the ServiceNow instance. When a user attempts to log in with an unauthorized app, the admin can add a link that redirects the user to an authorized app.

## Before you begin

Role required: admin

## About this task

Only use the advanced app allowance configuration if you must configure a link that redirects end users to a mobile app that is authorized to connect to the instance. Otherwise, you should use the basic app allowance list configuration. For more information, see [Configure a basic allowed mobile app list](config-basic-allow-mobile-app-list.md).

If both basic and advanced app allowance modes are configured on the same instance, then the system prioritizes the advanced app allowance configuration and always uses it. The advanced app allowance configuration can cause performance issues if the scripted extension point is not written to maximize system performance.

## Procedure

1.  Navigate to **All** &gt; **Scripted Extension Points**.

2.  Search for the global.CustomPreAuthProperties API Name and select it.

    The CustomPreAuthProperties record appears. Do not change any field except the **Example** field.

3.  In the **Example** field, configure the two following properties:

    -   **allowed\_mobile\_apps**

        Add a comma-separated list of iOS Bundle IDs and Android Package Names. Use this list to add mobile apps that can connect to your instance. For example:

        ```
        ⋮
        customProperties['allowed_mobile_apps']='com.servicenow.fulfiller';
        ⋮
        ```

    -   **blocked\_mobile\_apps\_redirect**

        Add a redirect URL for the button that appears when an end user attempts to log in with an unauthorized app. For example:

        ```
        ⋮
        customProperties['blocked_mobile_apps_redirect']='https://play.google.com/store/apps/details?
        id=com.servicenow.fulfiller&hl=en_US&gl+US';
        ⋮
        ```

    For an example of a completed script, see [Advanced app allowance example script](../reference/adv-app-allow-sample-script.md).

4.  To save the record, select **Update**.

5.  Select **Create implementation**.


## Result

A new script include is created and registered as an extension point instance.

