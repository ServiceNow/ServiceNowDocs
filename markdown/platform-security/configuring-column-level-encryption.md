---
title: Configuring Column Level Encryption
description: Learn how to activate and configure Column Level Encryption, and manage migration from Encryption Support.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Column Level Encryption, Encryption]
---

# Configuring Column Level Encryption

Learn how to activate and configure Column Level Encryption, and manage migration from Encryption Support.

## Activation

-   **Column Level Encryption**

    The Column Level Encryption plugin \(com.glide.encryption\) doesn’t require a subscription, and can be activated on your instance by an administrator. For details on plugin installation see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Column Level Encryption Enterprise**

    Column Level Encryption Enterprise is an enhanced version of Column Level Encryption, which requires a subscription.

    -   For details on the product, see [Column Level Encryption Enterprise](../../now-platform-encryption/concept/now-platform-encryption.md).
    -   For installation details for Column Level Encryption Enterprise, see [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md).

## Migration from encryption support

Use Scheduled jobs to migrate your keys and encrypted data from legacy Encryption Support to Column Level Encryption Enterprise. See details for this process at [Migrating to Column Level Encryption Enterprise](../../now-platform-encryption/concept/migration-to-platform-encryption.md)

## Change attachment encryption settings

Improve security by preventing users from attaching unencrypted files. For details, see[Prevent users from attaching unencrypted files](../task/attach-enc-property.md).

-   **[Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md)**  
With subscription to Column Level Encryption Enterprise, an admin can activate the com.glide.now.platform.encryption plugin.
-   **[Migrating to Column Level Encryption Enterprise](../../now-platform-encryption/concept/migration-to-platform-encryption.md)**  
Scheduled jobs migrate your keys and encrypted data from Encryption Support to Column Level Encryption Enterprise.
-   **[Prevent users from attaching unencrypted files](../task/attach-enc-property.md)**  
Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.

**Parent Topic:**[Column Level Encryption](column-level-encryption-landing.md)

