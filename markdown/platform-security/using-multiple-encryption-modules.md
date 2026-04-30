---
title: Using multiple encryption modules
description: Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but used to help prevent them from viewing each other's encrypted data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Using multiple encryption modules

Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but used to help prevent them from viewing each other's encrypted data.

There are two ways to encrypt data using multiple encryption modules in the platform: Row Conditions and multiple module.

## Row Conditions

Enables admins to define the encryption crypto module to be used. This option provides a deterministic approach and permits multiple Encryption Field Configurations \(EFCs\) to a single column. You can encrypt different records for a field or attachment by configuring distinct encryption keys to specific fields. This is achieved by assigning multiple Encryption Field Configurations \(EFCs\). Row Conditions is the preferred method of encrypting data with multiple modules. See [Encrypt data using Row Conditions](../task/encrypt-data-using-row-conditions.md).![Diagram displays the functional and administrative flow for Row Conditions.](../image/MMASSET0021136-encryption-field-configuration-horizontal.svg)

## Multiple module

Enables users to the crypto module to use to encrypt data. Since multiple module depends on the user selecting the correct crypto module to encrypt the data, this configuration is nondeterministic and is considered legacy and not preferred, even though the feature is still currently available. See [Encrypt data using the Multiple Modules feature](../../key-management-framework/task/encrypt-data-using-multiple-modules-feature.md).

-   **[Encrypt data using Row Conditions](../task/encrypt-data-using-row-conditions.md)**  
Encrypt fields with multiple Field Encryption modules using Row Conditions to define the data being encrypted and the associated encryption keys. Row Conditions can also be used to define the users that have access using the condition builder.
-   **[Encrypt data using the Multiple Modules feature](../../key-management-framework/task/encrypt-data-using-multiple-modules-feature.md)**  
Encrypt data with more than one encryption module permitting the user to determine which keys are used for specific rows within the encrypted data.

**Parent Topic:**[Using Field Encryption](using-column-level-encryption.md)

