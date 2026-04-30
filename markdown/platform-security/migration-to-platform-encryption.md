---
title: Migrating to Field Encryption
description: Scheduled jobs migrate your keys and encrypted data from Encryption Support to Field Encryption.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2026-03-10"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Migrating to Field Encryption

Scheduled jobs migrate your keys and encrypted data from Encryption Support to Field Encryption.

When you install Field Encryption, the migration process triggers automatically. Once the key migration job completes, encryption context keys are restricted to decryption only. Use cryptographic module keys for all new encryption operations going forward.

You can review the scheduled jobs by navigating to **System Security** &gt; **High Security Settings** &gt; **Security Jobs**:

-   **autoKeyMigration**: Migrates encryption context keys to Key Management Framework \(KMF\) cryptographic module keys.
-   **autoDataMigration**: Migrates data that you already encrypted to use the KMF cryptographic module key.

You can modify when these scheduled jobs run, and can pause or restart them at any time.

Verify that the encrypted field configurations are using your newly migrated module keys by navigating to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**. Look for the following items:

-   The **Method** field is **Single Module**.
-   The **Crypto module** field is populated with the name of the cryptographic module that the system automatically creates. You can review that module and the module access policy, both of which are active and published.

-   **[Field Encryption migration status page](../../key-management-framework/concept/cle-migration-status-page.md)**  
Use the migration status page to track the migration of encryption contexts to encryption modules.

**Parent Topic:**[Configuring Field Encryption](../../encryption/concept/configuring-column-level-encryption.md)

