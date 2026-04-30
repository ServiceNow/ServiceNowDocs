---
title: Configuring Column Level Encryption
description: Learn how to activate and configure Column Level Encryption and manage migration from Encryption Support.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-02-01"
reading_time_minutes: 1
breadcrumb: [Column Level Encryption, Encryption]
---

# Configuring Column Level Encryption

Learn how to activate and configure Column Level Encryption and manage migration from Encryption Support.

-   **[Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption-2.md)**

    Learn how to active either Column Level Encryption or Column Level Encryption Enterprise.

-   **Roles Required for Configuring Field Encryption**

    Learn about the roles required to configure Column Level Encryption.


## Migration from encryption support

Use Scheduled jobs to migrate your keys and encrypted data from legacy Encryption Support to Column Level Encryption Enterprise. See details for this process at [Migrating to Field Encryption](../../now-platform-encryption/concept/migration-to-platform-encryption.md)

## Change attachment encryption settings

Improve security by preventing users from attaching unencrypted files. For details, see [Prevent users from attaching unencrypted files](../task/attach-enc-property.md).

-   **[Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption-2.md)**  
With subscription to Column Level Encryption Enterprise, an admin can activate the com.glide.now.platform.encryption plugin.
-   **[Migrating to Column Level Encryption Enterprise](../../now-platform-encryption/concept/migration-to-platform-encryption-2.md)**  
Scheduled jobs migrate your keys and encrypted data from Encryption Support to Field Encryption Enterprise.
-   **[Prevent users from attaching unencrypted files](../task/attach-enc-property.md)**  
Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.

**Parent Topic:**[Column Level Encryption](column-level-encryption-landing.md)

