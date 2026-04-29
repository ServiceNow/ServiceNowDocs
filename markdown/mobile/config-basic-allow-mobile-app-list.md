---
title: Configure a basic allowed mobile app list
description: As an admin, configure a system property that contains a list of mobile apps that can log in to ServiceNow instances.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Control app use, Configuring the Mobile Platform, Mobile Platform]
---

# Configure a basic allowed mobile app list

As an admin, configure a system property that contains a list of mobile apps that can log in to ServiceNow instances.

## Before you begin

Role required: admin

## About this task

To support your organization's authentication policies, you can configure a list of mobile apps that can log in to instances. When a mobile app that is not granted access attempts to log in to your instance, a message appears. This message informs users that their app cannot access the instance.

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Make sure you are in the global application scope.

    To check if you are in the global application scope, select the globe icon \(![Globe icon.](../image/globe-icon.png)\) in the banner. The application scope that you are in is displayed.

    If you aren't in the global application scope, then select **Application Scope** &gt; **Global**.

3.  Select **New**.

4.  In the **Name** field, enter `glide.sg.allowed_mobile_apps`.

    Enter this name exactly with no extra characters. This field is also case-sensitive, so enter the name with all lower-case characters.

5.  In the **Application** field, make sure the field is set to **Global**.

6.  In the **Type** field, select **string**.

7.  In the **Value** field, enter a comma-separated list of the iOS Bundle IDs and of the Android Package Names for the apps that can log in to your instance.

    The following example shows a configuration that only allows end users with the Intune Now Mobile app to log in to the instance. All other apps are restricted and unable to log in.

    ```
    com.servicenow.intune.requestor,com.servicenow.requestor.mam.intune
    ```

    For a list of iOS Bundle IDs and Android Package IDs, see [Bundle and Package IDs for ServiceNow mobile apps](../reference/sg-mobile-package-ids.md).

8.  Select **Submit**.


