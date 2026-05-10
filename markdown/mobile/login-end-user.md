---
title: Add a ServiceNow instance to ServiceNow mobile apps
description: Learn how to access an instance using a ServiceNow mobile app.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with mobile instances, Using the mobile apps, Mobile Platform]
---

# Add a ServiceNow instance to ServiceNow mobile apps

Learn how to access an instance using a ServiceNow mobile app.

## Before you begin

Role required: user

## About this task

After you add ServiceNow mobile apps to your mobile device, you must connect them to the web-based UI instance that you work with. To enable connectivity between the Now Mobile app and Mobile Agent® app, for example, for deep linking, you must add the same account to both apps.

**Note:** For more information about working with multiple ServiceNow accounts within a mobile app, see [Working with multiple ServiceNow instances on a single mobile device](instance-multiple.md).

If you download the mobile app from an enterprise mobility management \(EMM\) suite, enter your user credentials as prompted. For more details on EMM, see [Enterprise mobility management \(EMM\)](../concept/enterprise-mobility-management.md). If you didn't download the mobile app from an EMM suite, follow the steps in this topic.

## Procedure

1.  Tap the icon for one of the ServiceNow mobile apps.

    The mobile account login screen displays.

    **Note:** An account is your ServiceNow environment — it includes your company's URL address \(aka instance\), a nickname, and your sign-in credentials.

    ![The mobile instance log in screen.](../image/log-in-screen.png)

2.  In the instance address field, enter the instance address in one of two ways.

<table id="choicetable_dvq_y41_fwb"><thead><tr><th align="left" id="d45617e121">

Option

</th><th align="left" id="d45617e124">

Description

</th></tr></thead><tbody><tr><td id="d45617e130">

**Manual entry**

</td><td>

Type the instance address in the instance address field.

**Note:** You don't need to include  `.service-now.com ` at the end of the instance name.

</td></tr><tr><td id="d45617e147">

**Scan QR code**

</td><td>

Tap the QR icon \(![Mobile QR scan code.](../image/mobile-qr-scan.png)\), and then scan the QR code given by your administrator.

 The QR code automatically fills in the name of the instance.

</td></tr></tbody>
</table>    **Note:** For both the Now Mobile app and Mobile Agent app, there's an option to test with a demo account, where you can select a role that matches the demo you would like to see. For more information, see [Now Mobile app demo](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/sg-mobile-demo.md) and [Mobile Agent app demo](../concept/sg-agent-demo.md).

3.   Enter a nickname for this instance to help you easily locate changes you make within the instance.

4.  Tap **Save and Login**.

    The mobile app login screen displays.

    ![Mobile app login screen.](../image/mobile-app-login.png)

5.  Enter your **User name** and **Password** and then tap **Log in**.

    The mobile app landing page displays and you can start your work.


**Related topics**  


[Mobile authentication](../concept/mobile-authentication.md)

