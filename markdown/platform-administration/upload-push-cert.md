---
title: Upload a push certificate to your instance
description: Upload a push certificate to your instance so that you can use it later to connect your iOS device to the push notification system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Push notification setup with a custom push application for ServiceNow mobile apps, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Upload a push certificate to your instance

Upload a push certificate to your instance so that you can use it later to connect your iOS device to the push notification system.

## Before you begin

Using your Apple developer environment, create a push certificate and convert it to a PKCS \(.p12\) file. For details on generating the .p12 file with the required certificate and private key, see [Enable push notifications](http://help.apple.com/xcode/mac/current/#/devdfd3d04a1) and [Communicate with APNs using a TLS certificate](https://help.apple.com/developer-account/#/dev82a71386a) in the Apple documentation.

**Note:** Ensure that your certificate is a push certificate and not a developer certificate. Also, if you're developing an app for testing purposes, ensure that you create a Sandbox certificate. If you're developing an app that you plan to launch in the Apple App Store, ensure that you create a Production certificate.

Role required: push\_admin or admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at [Mobile push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/sg-mobile-push-notifications.md)

## About this task

After you create a PKCS \(.p12\) file that contains the iPhone developer certificate and the private key used to sign the certificate, you need to upload the file to your instance. The system uses the information in the PKCS file to communicate with the APNs.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**, and then click **New**.

2.  On the form, fill in the following fields:

    -   Name: Enter a certificate name.
    -   Type: Select **PKCS12 Key Store**.
3.  Attach the PKCS \(.p12\) file to the record.

4.  Click **Submit**.


## What to do next

[Create a push application record for your custom app](t_CreateAMobileApplication.md)

