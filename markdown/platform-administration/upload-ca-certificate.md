---
title: Upload a CA certificate
description: Upload a digital CA \(Certificate Authority\) certificate to validate email certificates for secure communication.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up S/MIME for email, Email encryption - S/MIME protocol, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Upload a CA certificate

Upload a digital CA \(Certificate Authority\) certificate to validate email certificates for secure communication.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **SMIME** &gt; **CA Certificate**.

2.  Select **New**.

3.  Select the attachment icon ![Attachment icon](../image/attach-icon.png) to upload the CA certificate.

4.  On the form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Name|Unique name for the CA certificate.|
    |Type|The type of CA certificate.|
    |Expiration notification|Option to enable expiration.|
    |Warn in days to expire|Number of days to send a warning prior to the expiration date.|
    |Active|Option to enable the CA certificate.|
    |Short description|Description for the CA certificate.|

5.  Select **Submit**.


## What to do next

[Upload an email certificate](upload-email-certificate.md).

**Parent Topic:**[Setting up S/MIME for email](../concept/smime-for-email-signing-and-encryption.md)

**Related topics**  


[Import an S/MIME key pair](import-smime-key-pair.md)

[Upload an email certificate](upload-email-certificate.md)

[Enable S/MIME](../concept/enable-smime-for-outbound-and-inbound.md)

