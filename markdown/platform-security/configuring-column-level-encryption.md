---
title: Configuring Field Encryption
description: Learn how to activate and configure Field Encryption and manage migration from Encryption Support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/configuring-column-level-encryption.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Field Encryption, Encryption]
---

# Configuring Field Encryption

Learn how to activate and configure Field Encryption and manage migration from Encryption Support.

-   **[Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/activate-platform-encryption.md)**

    Learn how to active either Field Encryption or Field Encryption Enterprise.

-   **Roles Required for Configuring Field Encryption**

    Learn about the roles required to configure Field Encryption.


## Migration from encryption support

Use Scheduled jobs to migrate your keys and encrypted data from legacy Encryption Support to Field Encryption Enterprise. See details for this process at [Migrating to Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/migration-to-platform-encryption.md)

## Change attachment encryption settings

Improve security by preventing users from attaching unencrypted files. For details, see [Prevent users from attaching unencrypted files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/attach-enc-property.md).

-   **[Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/activate-platform-encryption.md)**  
Activate either Field Encryption Starter or Field Encryption Enterprise.
-   **[Role requirements for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/fe-roles.md)**  
Learn about the roles required to configure Field Encryption.
-   **[Configure Field Encryption modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-fe-modules.md)**  
Learn how to configure Field Encryption modules.
-   **[Cryptographic specifications for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-fe-crypto-specs.md)**  
Use cryptographic specifications to define the purpose, algorithm, key length, mode, and origin of your encryption key.
-   **[Module keys for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/fe-module-keys.md)**  
The Module Keys tab shows you summary level information about your Field Encryption Data Encryption Key\(s\). You can view the Key alias, Key type, Algorithm, Key lifecycle state, and Key version.
-   **[Module lifecycle policy exceptions for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/module-lifecycle-policy-exceptions-for-fe.md)**  
Use module lifecycle policy exceptions to customize the lifecycle of your module keys.
-   **[Configure Customer-supplied keys for Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/fe-config-customer-supplied-keys.md)**  
Bring your own data encryption key to the platform instead of using the one that ServiceNow generates.
-   **[Configure encrypted field configurations for fields or attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-fe-fields-attachments.md)**  
Create an encrypted field configuration to specify which fields are encrypted on a table, and whether that table's attachments are encrypted.
-   **[Configure multi-module encrypted field configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/multi-module-fe-config.md)**  
Create an encrypted field configuration that uses more than one encryption module.
-   **[Configure module access policies for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/maps-for-fe.md)**  
Create a module access policy to control which users, scripts, or system processes can encrypt or decrypt data encrypted by a field encryption module.
-   **[Migrating to Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/migration-to-platform-encryption.md)**  
Scheduled jobs migrate your keys and encrypted data from Encryption Support to Field Encryption.
-   **[Migrate from Edge Encryption to Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/migrate-ee-to-fe.md)**  
Migrate from Edge Encryption to Field Encryption to take advantage of the latest security features.
-   **[Field Encryption and system clones](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/fe-system-clones.md)**  
Cloning an instance with Field Encryption installed automatically generates new field encryption module encryption keys on the target clone instance.
-   **[Prevent users from attaching unencrypted files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/attach-enc-property.md)**  
Modify the com.glide.encryption.enable\_attachment\_key\_ui property to prevent your users with access to an encryption module key from attaching unencrypted attachments.

**Parent Topic:**[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/field-encryption.md)

