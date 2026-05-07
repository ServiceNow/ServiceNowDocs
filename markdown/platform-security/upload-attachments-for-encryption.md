---
title: Upload attachments for encryption
description: Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Upload attachments for encryption

Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.

## Before you begin

Role required: Any role that aligns with the module access policy \(MAP\) created by the admin.

**Note:** Additional setup is required when an email is matched to a record and the matched record's table has an encryption configuration. In this case, the attachments from the email are associated with that record. You need a module access policy \(MAP\) for the system user. If the sender is matched to a user in your instance, you also need a separate MAP that grants that user access to use the cryptographic module. This MAP is also required to permit impersonation. See [Module access policies for encrypting associated attachments](../concept/fe-maps-inbound-email-attachment-encryption.md).

## Procedure

1.  Navigate to a record.

2.  Select the **Manage Attachments** paperclip icon.

3.  In the **Attachments** window, select the module to encrypt with from the **Encrypt with Module** drop-down options.

    ![Encrypt with Module drop-down options for attachments.](../image/encrypt-attachment-module.png)

    **Note:** If Row Conditions have been added to the Encryption Field Configuration, this option isn't displayed. The attachment would then be automatically encrypted with the module defined in the Row Condition. Similarly, this drop-down option only displays when using the Manage Attachments icon and not if the attachment is added by dragging and dropping.

4.  Select **Choose file** to locate the attachment and select **Open** to attach it.


## Result

Attached files display at the top of the form. Encrypted attachments are denoted by a lock icon. Only users with the encryption module to view encrypted files will see them listed.

## What to do next

**Encrypted attachments and missing metadata**

When you encrypt an attachment, the hash and state fields on the sys\_attachment record aren't populated. This is by design.

The hash field stores a SHA-256 fingerprint of an attachment's content. Even though a file is encrypted, a hash is a deterministic and stable identifier. The same file produces the same hash value every time. Storing the hash would enable an attacker who has a copy of the file to confirm that it exists in your system and can weaken encryption.

Because of this, duplicate detection doesn't work for encrypted attachments, since ServiceNow uses the hash field to prevent identical attachments from being added to a record.

**Parent Topic:**[Encrypting fields and attachments](../concept/field-encryption-key-management.md)

