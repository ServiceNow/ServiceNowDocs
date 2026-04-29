---
title: Enroll for the Password Reset program using an authenticator
description: Verify your identity while resetting your password by enrolling for the Password Reset program using a third-party authenticator app.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enrolling in the Password Reset application to reset your password, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enroll for the Password Reset program using an authenticator

Verify your identity while resetting your password by enrolling for the Password Reset program using a third-party authenticator app.

## Before you begin

Role required: none

## About this task

To verify your identity while resetting your password, you get a code from an authenticator app on your mobile device and then enter the code on the Password Reset web page.

Password Reset supports the following authenticator apps:

-   Google Authenticator
-   Microsoft Authenticator
-   Cisco Duo
-   Okta Verify

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Enroll**.

2.  Click the **Authenticator App Verification** tab.

    **Note:** If your organization requires you to enroll for the Password Reset Authenticator verification method, the tab is marked with an asterisk \(\*\).

3.  Download the authenticator app to your device.

4.  Open the app and then use the device to scan the QR code on the tab.

5.  When the device generates a code, enter the code in the text box, and then click **Pair Device**.

6.  Select **Submit**.

7.  If the system displays a success message, select **Submit**.

8.  If the system displays a failure message, enter the code again, click **Pair Device**, and then select **Submit**.

    When you submit the enrollment, the tab displays the following options:

    |Option|Description|
    |------|-----------|
    |Generate New QR Code|Enables you to pair a device with a new code. This option is useful if you have a new device. New data replaces the existing secure verification data.|
    |Disable Multi-factor Authentication|Deletes existing secure verification data. The Google Authenticator verification is no longer available.|

9.  Enroll for an additional identity verification using any of the other methods that your organization offers.

    For more information about enrolling using different methods, see the following topics:

    -   [Enroll for the Password Reset program using questions and answers](t_EnrollUsingASecurityQuestion.md)
    -   [Enroll for the Password Reset program using SMS codes](t_EnrollUsingSMS.md)
    -   [Enroll for the Password Reset program using emailed codes](enroll-email-verification.md)

