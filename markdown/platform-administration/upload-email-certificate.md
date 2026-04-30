---
title: Upload an email certificate
description: Upload an email certificate to validate a signature for inbound email or encrypt an outbound email or both for secure communication.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up S/MIME, Email encryption, Email Administration, Notifications, Configure core features, Administer]
---

# Upload an email certificate

Upload an email certificate to validate a signature for inbound email or encrypt an outbound email or both for secure communication.

## Before you begin

-   To enable signing in the instance, upload the private-public key pair corresponding to the instance email account.
-   To enable encryption in the instance and send encrypted email to a recipient's email address, upload the public key/certificate corresponding to the recipient’s email address.


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **SMIME** &gt; **Email Certificate**.

2.  Select **New**.

3.  Select the attachment icon ![Attachment icon](../image/attach-icon.png) to upload the email certificate.

4.  On the form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Email|Email address for sending the email.|
    |Expiration notification|Select the check box to enable expiration.|
    |Notify on expiration|Add yourself to be notified before expiration.|
    |Warn in days to expire|Number of days to send the warning prior to the expiration date.|
    |Active|Check box to enable the email certificate.|
    |Key store password|Key password to protect PKCS \#12 file.|
    |Short description|The description for this email certificate.|

5.  Select **Submit**.


## What to do next

Enable[Enable S/MIME](../concept/enable-smime-for-outbound-and-inbound.md).

**Parent Topic:**[Setting up S/MIME for email](../concept/smime-for-email-signing-and-encryption.md)

**Related topics**  


[Import an S/MIME key pair](import-smime-key-pair.md)

[Upload a CA certificate](upload-ca-certificate.md)

[Enable S/MIME](../concept/enable-smime-for-outbound-and-inbound.md)

