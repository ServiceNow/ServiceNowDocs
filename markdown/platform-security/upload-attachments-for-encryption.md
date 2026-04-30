---
title: Upload attachments for encryption
description: Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 1
breadcrumb: [Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Upload attachments for encryption

Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.

## Before you begin

Role required: Any role that aligns with the module access policy \(MAP\) created by the admin.

## Procedure

1.  Navigate to a record.

2.  Select the **Manage Attachments** paperclip icon.

3.  In the **Attachments** window, select the module to encrypt with from the **Encrypt with Module** drop-down options.

    ![Encrypt with Module drop-down options for attachments.](../image/encrypt-attachment-module.png)

    **Note:** If Row Conditions have been added to the Encryption Field Configuration, this option isn't displayed. The attachment would then be automatically encrypted with the module defined in the Row Condition. Similarly, this drop-down option only displays when using the Manage Attachments icon and not if the attachment is added by dragging and dropping.

4.  Select **Choose file** to locate the attachment and select **Open** to attach it.


## Result

Attached files display at the top of the form. Encrypted attachments are denoted by a lock icon. Only users with the encryption module to view encrypted files will see them listed.

**Parent Topic:**[Encrypting fields and attachments](../concept/field-encryption-key-management.md)

