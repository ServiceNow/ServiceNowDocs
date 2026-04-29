---
title: Exploring Field Encryption
description: Learn the details of Field Encryption Starter and Field Encryption Enterprise
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Field Encryption, Encryption]
---

# Exploring Field Encryption

Learn the details of Field Encryption Starter and Field Encryption Enterprise

## Encryption-backed access control

This video provides an overview of Field Encryption, including how it protects sensitive data at rest by encrypting individual fields and attachments, and how its key components work together. 

By default, Field Encryption blocks all users, scripts, and system processes from accessing encrypted data. However, Field Encryption has an access control feature that is used in combination with, but also separate from, Access Control Lists \(ACLs\) to ensure only the correct users, scripts, or system processes can access encrypted data.

You can configure Field Encryption access control feature through a combination of Field Encryption Modules, Encrypted Field Configurations, and Module Access Policies. The next image shows how these three components work together.

![Field encryption and supporting components](../image/fe-diagram-1.png)

Module Access Policies \(shown in the next image\) are how users, scripts, or system processes can be authorized to access encrypted data \(but by default, the encrypted data is locked down from any access in the instance\).

![Module access policy flow](../image/fe-diagram-2.png)

## Differences between Field Encryption Starter and Field Encryption Enterprise

The feature-set is different between Field Encryption Starter and Field Encryption Enterprise.

|Feature|Field Encryption Starter|Field Encryption Enterprise|
|-------|------------------------|---------------------------|
|Number of encrypted fields|Up to 5 encrypted fields|No restriction on number of encrypted fields|
|Attachment encryption|No|Yes|
|Key management|None \(Contact ServiceNow Support for key rotation\)|Manage keys from your instance with no involvement from ServiceNow Support|
|Supported data types|All supported data types|All supported data types|
|Number of Field Encryption Modules|No restriction|No restriction|
|Number of Module Access Policies|No restriction|No restriction|

## Field Encryption users

<table id="table_k3r_dhn_b2c"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key Management Framework \(KMF\)Admin or KMF Cryptographic Manager

</td><td>

These roles are used to configure elements of Field Encryption.-   Field Encryption modules and module keys
-   Cryptographic Specifications
-   Module life-cycle policies
-   Encrypted field configurations for fields and attachments
-   Module Access Policies \(MAPs\)
-   Configures, wraps, and uploads customer supplied keys \(for Field Encryption Enterprise\)
-   Configures Access Observer and review Access Observer logs.
-   Schedule mass encryption, decryption, or re-keying

</td></tr><tr><td>

KMF Cryptographic Operator

</td><td>

Configures properties for customer supplied keys

</td></tr></tbody>
</table>## Field Encryption and record history

Changes to fields encrypted with Field Encryption are not tracked in the activity stream for the record or in the record history \[sys\_history\_set\] table.

## Encryption on system tables

Field Encryption currently doesn’t support the encryption of fields and attachments of system tables \(tables that begin with sys\_\).

## What to explore next

To learn more about configuring and using Field Encryption, see:

-   [Configuring Field Encryption](configuring-column-level-encryption.md)
-   [Using Field Encryption](using-column-level-encryption.md)

-   **[Field Encryption Enterprise](../../now-platform-encryption/concept/now-platform-encryption.md)**  
Field Encryption Enterprise uses the Key Management Framework \(KMF\) to enable you to customize and manage how fields and attachments are encrypted and decrypted on your instance. A subscription is required to use Field Encryption Enterprise.

**Parent Topic:**[Field Encryption](field-encryption.md)

