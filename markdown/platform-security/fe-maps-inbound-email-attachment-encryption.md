---
title: Module access policies for inbound email attachment encryption
description: Encrypting inbound email attachments associated with matched records requires one or more module access policies \(MAPs\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2024-01-01"
reading_time_minutes: 1
keywords: [encryption, email attachments, module access policies]
breadcrumb: [Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Module access policies for inbound email attachment encryption

Encrypting inbound email attachments associated with matched records requires one or more module access policies \(MAPs\).

When an inbound email is matched to a record, the attachments from that email are associated with that record. If the matched record's table has an encryption configuration, you may need more than one MAP to confirm those attachments encrypt correctly.

Both MAPs must be in place for attachments to encrypt correctly in all processing contexts. If only the system MAP exists, attachments associated with a record during a user process won't encrypt.

The MAPs you need depend on how your instance processes inbound emails. See [Inbound email action processing](https://www.servicenow.com/docs/r/platform-administration/inbound-action-processing.html).

-   **System MAP** — Required when inbound email processing runs as the system user, which is the default behavior. See [Create a system module access policy](../task/fe-create-system-map.md).
-   **User MAP** — Required when the email is matched to a user in your instance and processing runs as that user. Any MAP type can be used as long as the user has access to the cryptographic module. If you use a role-based MAP, you must enable impersonation. See [Create a user module access policy](../task/fe-create-user-map.md).

-   **[Create a system module access policy](../task/fe-create-system-map.md)**  
Create a module access policy \(MAP\) for a matched user to encrypt attachments when inbound email processing runs as that user.
-   **[Create a user module access policy](../task/fe-create-user-map.md)**  
Create a module access policy \(MAP\) for a matched user to encrypt attachments when inbound email processing runs as that user.

**Parent Topic:**[Encrypting fields and attachments](field-encryption-key-management.md)

