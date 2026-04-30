---
title: Log in to the BCM mobile application
description: Open the BCM mobile app and add a ServiceNow AI Platform instance with BCM to your mobile device.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing plans with BCM mobile application, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Log in to the BCM mobile application

Open the BCM mobile app and add a ServiceNow AI Platform® instance with BCM to your mobile device.

## Before you begin

Role required: sn\_bcm.manager

Verify that you have completed the setup steps described in [Set up the BCM mobile application](configure-mobile-app-setup.md).

## Procedure

1.  On your mobile device, tap the ServiceNow Agent app.

    If you aren’t already logged in to a ServiceNow AI Platform instance, the Instances screen is displayed.

2.  If the ServiceNow AI Platform instance with the BCM core application isn’t already added to your mobile device, follow these steps to add it.

    1.  On the Instances screen that is displayed, tap the plus icon \(![Plus icon.](../../grc-common/image/mobile_instances_plus.png)\).

        A screen is displayed that prompts you to enter and save an address of a ServiceNow AI Platform instance.

    2.  Fill in the fields.

<table id="table_ddl_2gx_zhb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter the instance address or scan a QR code.

</td><td>

Choose one to continue:-   Before the `.service-now.com` in the field, enter the name of your ServiceNow AI Platform instance, for example, `bcm-mobile`.
-   Enter an address. This address is the URL of your ServiceNow AI Platform instance that you want to view on your mobile device.
-   Scan a QR code.
 For more information about the mobile app, see "Log in to an instance with the mobile app" on the [ServiceNow product documentation website.](https://servicenow.com/docs)

</td></tr><tr><td>

\(Optional\) Enter nickname

</td><td>

Enter a nickname for this instance. If you have multiple instances added to the device, nicknames can help you quickly locate a ServiceNow AI Platform instance.

</td></tr></tbody>
</table>    3.  Tap **Save and Login**.

3.  On the ServiceNow login screen that is displayed, enter the User name and Password for the ServiceNow AI Platform instance that you want to add and tap **Login**.

    The BCM landing screen with the plans list is displayed. You have successfully logged in to the BCM mobile app.

4.  After you log in to an instance on your mobile device, it’s the default ServiceNow AI Platform instance on the device.

    If you want to view another ServiceNow AI Platform instance on your device, you must log out of the default instance. To log out:

    1.  At the bottom of the screen, tap **More**.

        The More screen is displayed.

    2.  Tap **Settings**.

    3.  On the screen that is displayed, tap **Logout**.

        The Instances screen is displayed with any ServiceNow AI Platform instances that you have added to the mobile device.

    4.  Tap another instance to log in to it, or, alternatively, follow the preceding steps to add another instance.

5.  Log in to the app using your credentials.

6.  Access the BCM mobile app interface.


If the instances screen for the BCM mobile app isn’t displayed after you tap the ServiceNow Agent app on your device, verify that the ServiceNow Agent app is permitted as a trusted app on your device. To permit access as a trusted app, navigate to the settings and general device management on your device and tap the option \(**Trust app**, and so on\) to permit access.

If an error message is displayed after you enter your credentials in the log in screen, verify that your User name and password for the ServiceNow AI Platform instance is correct.

If you have problems viewing the landing screen, verify your network connection.

If you can’t view the Instances screen after you tap the ServiceNow Agent app, try uninstalling it from your device. Verify you have the most current version of the app from the Apple iOS App Store or the Google Play Store and try reinstalling it.

## What to do next

View the plans list and generate the PDF of a plan.

