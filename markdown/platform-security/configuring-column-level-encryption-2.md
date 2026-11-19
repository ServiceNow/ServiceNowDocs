---
title: Configuring Column Level Encryption
description: Learn how to activate and configure Column Level Encryption Enterprise, and manage migration from Encryption Support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/configuring-column-level-encryption-2.html
release: yokohama
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 1
breadcrumb: [Exploring Column Level Encryption, Column Level Encryption, Encryption]
---

# Configuring Column Level Encryption

Learn how to activate and configure Column Level Encryption Enterprise, and manage migration from Encryption Support.

-   **Column Level Encryption**

    Learn how to activate Column Level Encryption or Column Level Encryption Enterprise.

-   **Roles Required for Configuring Column Level Encryption**

    Learn about the roles required to configure Column Level Encryption.


## Migration from encryption support

Use Scheduled jobs to migrate your keys and encrypted data from legacy Encryption Support to Column Level Encryption Enterprise. See details for this process at [Migrating to Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/migration-to-platform-encryption.md)

## Change attachment encryption settings

Improve security by preventing users from attaching unencrypted files. For details, see [Prevent users from attaching unencrypted files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/attach-enc-property.md).

-   **[Activate Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/activate-platform-encryption-2.md)**  
With subscription to Column Level Encryption Enterprise, an admin can activate the com.glide.now.platform.encryption plugin.
-   **[Migrating to Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/migration-to-platform-encryption-2.md)**  
Scheduled jobs migrate your keys and encrypted data from Encryption Support to Column Level Encryption Enterprise
-   **[Prevent users from attaching unencrypted files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/attach-enc-property.md)**  
Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.

**Parent Topic:**[Exploring Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/exploring-column-level-encryption.md)

**Parent Topic:**[Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/column-level-encryption-landing.md)

