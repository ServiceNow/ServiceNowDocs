---
title: Prevent users from attaching unencrypted files
description: Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/attach-enc-property.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Prevent users from attaching unencrypted files

Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.

## Before you begin

Role required: security\_admin

You must elevate to the security\_admin role performing these steps. For instructions, see [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/t_ElevateToAPrivilegedRole.md)

By default, users who have access to an encryption module key are able to upload unencrypted attachments. Use the **com.glide.encryption.enable\_attachment\_key\_ui** system property to change this behavior.

When attaching, your users see a UI picker on records that have a multi-module encrypted field configuration. When this property is set to false, users no longer see an option not to encrypt an attachment.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the system properties list, find and open the system property.

3.  Set the **value** of the property to `false`.


**Parent Topic:**[Configuring Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/configuring-column-level-encryption.md)

**Parent Topic:**[Configuring Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/configuring-column-level-encryption-2.md)

