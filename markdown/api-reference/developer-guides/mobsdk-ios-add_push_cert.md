---
title: Add a push certificate record
description: After generating your iOS push certificate, you must save the push certificate record to your instance. The push certificate is stored in the X.509 Certificate \[sys\_certificate\] table.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Add a push certificate record

After generating your iOS push certificate, you must save the push certificate record to your instance. The push certificate is stored in the X.509 Certificate \[sys\_certificate\] table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the search field, select **Name** and enter `sys_certificate`.

3.  Open the X.509 Certificate \[sys\_certificate\] table.

4.  Create a certificate record by selecting the **New** button.

5.  Add the Personal Information Exchange \(.p12\) certificate that you exported in [Generate and retrieve an iOS push certificate](mobsdk-ios-retrieve-apple-cert.md) to the certificate record as an attachment.

    1.  In the upper-right corner, select the attachment icon.

    2.  In the **Name** field, enter a name for the certificate.

        You can enter any name that clearly identifies the purpose of the certificate to other team members.

    3.  In the **Type** field, enter or select `PKCS12 Key Store`.

    4.  In the **Notify on expiration** field, select the person to receive a notification when the certificate is about to expire.

    5.  In the **Warn in days to expire** field, enter the number of days prior to when the certificate is scheduled to expire, to send a notification about the expiration.

    6.  In the **Key store password** field, enter the password that you used when exporting the certificate from the keychain.

    7.  At the bottom left-corner of the form, select the **ValidateStores/Certificates** link.

        The system validates the attached certificate.

    8.  After the certificate validation is confirmed, select **Update** to submit the form.

    ![Push certificate form](../image/mobsdk-ios-push_cert_save.png)


