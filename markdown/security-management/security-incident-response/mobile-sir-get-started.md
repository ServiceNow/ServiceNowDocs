---
title: Log in to the Security Incident Response Mobile app
description: Open the Security Incident Response Mobile app and add a ServiceNow AI Platform instance with Security Incident Response to your mobile device.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile Experience for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Log in to the Security Incident Response Mobile app

Open the Security Incident Response Mobile app and add a ServiceNow AI Platform® instance with Security Incident Response to your mobile device.

## Before you begin

Role required: sn\_si.analyst

## About this task

Time to complete this task: 5-10 minutes.

Verify that you have completed the setup steps described in [Set up checklist for the Security Incident Response Mobile app](mobile-sir-setupinstll-mobile-app.md).



![Security Incident Response mobile landing page.](../image/mobile_landing-agent.jpg)

## Procedure

1.  On your mobile device, tap the **ServiceNow Agent** app to open it.

    ![ServiceNow Agent app.](../../vulnerability-response/image/mobile-agentapp-NY.png)

    If you are not already logged in to a ServiceNow AI Platform instance, the Instances screen is displayed.

2.  If the ServiceNow AI Platform instance with the Security Incident Response core application is not already added to your mobile device, follow these steps to add it.

    1.  On the Instances screen that is displayed, tap the ![Plus icon.](../../vulnerability-response/image/mobile_instances_plus.png).

        A screen is displayed that prompts you to enter and save an address of a ServiceNow AI Platform instance.

    2.  Fill in the fields.

<table id="table_tw5_2bl_thb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter the instance address or scan a QR code.

</td><td>

Choose one to continue:-   Before the `.service-now.com`, enter the name of your ServiceNow AI Platform instance, for example, `sirmobileny`.
-   Enter an address. This address is the URL of your ServiceNow AI Platform instance that you want to view on your mobile device, for example, https://sirmobileny.service-now.com.
-   Scan a QR code.


</td></tr><tr><td>

\(Optional\) Enter nickname

</td><td>

Enter a nickname for this instance. If you have multiple instances added to the device, nicknames can help you quickly locate a ServiceNow AI Platform instance.

</td></tr></tbody>
</table>    3.  Tap **Save and Login**.

3.  On the ServiceNow login screen that is displayed, enter the User name and Password for the ServiceNow AI Platform instance that you want to add and tap **Login**.

    The Security Incidents landing screen is displayed. You have successfully logged in to the Security Incident Response Mobile app.

4.  After you log in, verify notifications are enabled in the Security Incident Response Mobile app.

    1.  On the landing screen on the bottom, tap **Notification**.

    2.  On the Notifications screen, tap **Enable Notifications** if not enabled.

        Notifications from the ServiceNow AI Platform are displayed on the Notifications screen in the Security Incident Response Mobile app.

5.  After you log in to an instance on your mobile device, it is the default ServiceNow AI Platform instance on the device.

    If you want to view another ServiceNow AI Platform on the device, you are required to log out of the default instance. To log out:

    1.  Tap the settings icon.

    2.  Tap **Logout**.

        The Instances screen is displayed with any ServiceNow AI Platform instances you have added to the mobile device.

    3.  Tap another instance to log in to it, or, alternatively, follow the preceding steps to add another instance.

    If the instances screen for the Security Incident Response Mobile app is not displayed after you tap the **ServiceNow Agent** app on your device, verify that the **ServiceNow Agent** is permitted as a trusted app on your device. To permit access as a trusted app, navigate to the settings and general device management on your device and tap the option \(Trust app, etc.\) to permit access.

    If an error message is displayed after you enter your credentials in the log in screen, verify that your User name and password for the ServiceNow AI Platform instance is correct.

    If you have problems viewing the landing screen, verify your network connection.

    If you cannot view the Instances screen after you tap the **ServiceNow Agent** app, try uninstalling it from your device. Verify you have the most current version of the app from the Apple iOS App Store or the Google Play Store and try reinstalling it.


