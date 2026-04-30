---
title: Configure push applications for iOS branded apps using certificate based authentication
description: Install an iOS push certificate to use push notifications on your branded ServiceNow mobile apps for iOS.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure push applications for iOS branded apps using certificate based authentication

Install an iOS push certificate to use push notifications on your branded ServiceNow mobile apps for iOS.

## Before you begin

Role required: admin

To use push notifications on your branded ServiceNow mobile apps for iOS, you must upload your Apple certificates p12 file, and enter your key store password into your instance.

**Note:** These steps are not necessary if you are not using a custom branded mobile apps. For more detail on custom branding, see [Request, test, and publish a branded mobile app](../concept/request-test-pub-branded-mob-app.md).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Application**.

2.  Open the record for the push application you want to modify.

    -   Open **ServiceNow Mobile Application** for the Mobile Agent app.
    -   Open **ServiceNow Request Application** for the Now Mobile app.
    If you are using a branded mobile application, select the record for the branded app. For example, select **ServiceNow Intune Mobile Application** if you are using the Microsoft Intune branded application.

3.  In the **Push** field, change the value from **REST API** to **Direct**.

4.  In the Apple-Certificate Based Authentication tab, click the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) next to the **Certificate** field.

5.  In the X.509 Certificates list pop-up, click **New**.

6.  In the X.509 Certificates form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Name for your certificate.|
    |Notify on expiration|User to receive a notification when the certificate expires.|
    |Type|Certificate type. Enter **PKCS12 Key Store** in this field.|
    |Key store password|Your Apple key store password.|
    |Warn in days to expire|Number of days before certificate expiration to receive an expiration warning.|
    |Short Description|Description for your certificate.|

7.  Click the attachment icon \(![Attachment icon](../image/attach-icon.png)\).

8.  Upload your .p12 certificates file.

    **Note:** Due to an Apple internal policy, all iOS push certificates \(.p12 files\) expire after 13 months. To continue using push notifications without disruption, you should request an updated build within 60 days of your certificate expiration date to receive a new .p12 file. New .p12 files cannot be generated without an updated or new build.

9.  Click **Save**.

10. Re-open your X.509 Certificates record and click the **Validate Stores/Certificates** link at the bottom of the form to validate your certificates and stores.

11. On the push application form, click **Update**.


**Parent Topic:**[Mobile push notifications](../concept/sg-mobile-push-notifications.md)

