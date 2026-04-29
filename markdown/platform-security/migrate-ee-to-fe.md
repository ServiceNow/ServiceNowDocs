---
title: Migrate from Edge Encryption to Field Encryption
description: Migrate from Edge Encryption to Field Encryption to take advantage of the latest security features.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Migrate from Edge Encryption to Field Encryption

Migrate from Edge Encryption to Field Encryption to take advantage of the latest security features.

## Migration process

This topic covers, which comprise the following steps:

1.  Migrate columns and attachment from Edge Encryption to Field Encryption.
2.  Stop and disabling Edge Encryption proxy servers.
3.  De-tokenize your data
4.  Decrypt Service Catalog item variables.

## Limitations

-   Field Encryption doesn’t currently support tokenizing data in the same way that Edge Encryption does. Data that is tokenized through Edge Encryption must be included in an encrypted field configuration for Field Encryption.
-   Field Encryption doesn’t currently support encrypting Service Catalog item variables.

-   **[Configure Field Encryption for your Edge Encrypted fields](../task/migrate-ee-to-fe-1.md)**  
Before migrating your existing edge encrypted fields to Field Encryption, you must configure field encryption for these fields.

**Parent Topic:**[Configuring Field Encryption](../../encryption/concept/configuring-column-level-encryption.md)

