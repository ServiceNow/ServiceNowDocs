---
title: Column Level Encryption for email attachments
description: Secure attachments in inbound and outbound emails using Column Level Encryption.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Column Level Encryption for email attachments

Secure attachments in inbound and outbound emails using Column Level Encryption.

Using Column Level Encryption for email attachments requires you to have Column Level Encryption configured on your instance. For more information, see [Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/column-level-encryption-landing.md).

For each inbound email action, when an email includes attachments and the target record table is Column Level Encryption-enabled, the attachments added to the target record are encrypted.

If an inbound email with attachments is received from an external user who does not have access to the target table, the attachments are not added to the target record such as an incident or case. Instead, the attachments are added to the sys\_email record and the email logs.

When you send an outbound email from a workspace with attachments encrypted on the target table, the attachments are decrypted before sending the email so recipients can access them.

**Note:** To disable adding encrypted attachments to outbound emails, create a system property named **glide.attachment.restrict\_cle\_attachments**, and set it to **true**. By default, this property is set to **false**.

