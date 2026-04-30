---
title: Exploring Column Level Encryption
description: Learn more about Column Level Encryption.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Column Level Encryption, Encryption]
---

# Exploring Column Level Encryption

Learn more about Column Level Encryption.

## Column Level Encryption overview

Column Level Encryption is a base system feature that permits encryption of data stored within an instance using AES128, or AES256.

Column Level Encryption enables you to encrypt selected database fields and stored files through the use of encryption contexts. In these contexts you define what is encrypted, choose which algorithm to use, and supply the encryption key, which is stored within your instance.

After the context is created, you can associate it to a user role. Users assigned to this role, either directly of through a group, are able to access the encrypted data.

Because Column Level Encryption bases access to data on role assignment, it’s important to be familiar with administering roles on your instance. For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Column Level Encryption benefits

<table id="table_hb1_1br_ryb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Required Roles

</th></tr></thead><tbody><tr><td>

Configure access to your encrypted data based on assigned user roles.

</td><td>

Role-based access to encrypted data

</td><td>

security admin

</td></tr><tr><td>

Protect your data using the Advanced Encryption Standard \(AES\). You can choose to use either the AES-128 or AES-256 encryption algorithms.

</td><td>

AES Encryption

</td><td>

security admin

</td></tr><tr><td>

Create up to 5 modules and module access policies \(MAP\)s using the standard version of Column Level Encryption. MAPs expand on role-based access to allow considerations for:-   System users
-   Scripts
-   KMF Resource Exchange

Column Level Encryption Enterprise supports additional MAPs.

</td><td>

Support for up to 5 modules and module access policies \(MAP\)s

</td><td>

security admin

</td></tr><tr><td>

Encrypt common field types using the standard version of Column Level Encryption. Column Level Encryption Enterprise supports additional field types.

</td><td>

Encryption for String text, Date and Date/Time fields, attachments, and URLs

</td><td>

security admin

</td></tr><tr><td>

Choose between standard and equality preserving encryption. When enabled, equality preserving encryption ensures that the encrypted value of a field is the same when the field value remains the same. This type of encryption enables equality comparisons and group by operations on a field.**Note:** Non-deterministic encryption isn’t supported.

</td><td>

Equality preserving encryption support

</td><td>

security admin

</td></tr><tr><td>

Use `getDisplayValue()` and `setDisplayValue()` APIs to return cleartext values and insert encrypted data for encrypted fields.

</td><td>

`getDisplayValue()` and `setDisplayValue()` APIs

</td><td>

security admin, developer

</td></tr></tbody>
</table>## Column Level Encryption Enterprise benefits

Column Level Encryption Enterprise builds on the existing Column Level Encryption framework and provides these additional features after you purchase a subscription.

<table id="table_nhr_54z_ryb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Required Roles

</th></tr></thead><tbody><tr><td>

Encrypt additional field types.

</td><td>

Support for additional field types:-   HTML
-   Journal
-   Translated

</td><td>

security admin

</td></tr><tr><td>

Column Level Encryption Enterprise supports more than 5 modules and module access policies to provide more options for access to secured data.

</td><td>

Support for additional modules and MAPs

</td><td>

security admin

</td></tr><tr><td>

Keys from a key vault can be rotated on an automated schedule you configure. Using automatic key rotation can improve security while reducing administrative overhead.

</td><td>

Configurable automatic key rotation

</td><td>

security admin

</td></tr><tr><td>

Manage the full life cycle of your data encryption keys. Optionally, you can securely exchange data encryption keys generated within your environment.

</td><td>

Customer supplied keys

</td><td>

security admin

</td></tr><tr><td>

Ephemeral keys are cryptographic keys that are generated for each execution of a cryptographic process. These keys more secure because they’re generated for use in a single session.

</td><td>

Ephemeral cryptographic keys

</td><td>

security admin

</td></tr><tr><td>

Updated `setDisplayValue()` and `setDisplayValue()` APIs can insert encrypted data for encrypted fields.

</td><td>

Updated `getDisplayValue()` and `setDisplayValue()` APIs

</td><td>

security admin, developer

</td></tr></tbody>
</table>-   **[Column Level Encryption Guided Tour](../task/cle-tour.md)**  
The tour gives a brief overview of the Column Level Encryption Enterprise setup needed to encrypt table fields or attachments.​ Steps for the creation of Field Encryption Modules, Module Access Policies, and Encrypted Field Configurations are also covered. The tour includes links to detailed documentation and the ServiceNow University Column Level Encryption Enterprise Overview course.​
-   **[Configuring Column Level Encryption](configuring-column-level-encryption-2.md)**  
Learn how to activate and configure Column Level Encryption Enterprise, and manage migration from Encryption Support.

**Parent Topic:**[Column Level Encryption](column-level-encryption-landing.md)

