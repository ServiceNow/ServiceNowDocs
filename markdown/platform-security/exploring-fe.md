---
title: Exploring Field Encryption
description: Learn the details of Field Encryption Starter and Field Encryption Enterprise
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/exploring-fe.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Field Encryption, Encryption]
---

# Exploring Field Encryption

Learn the details of Field Encryption Starter and Field Encryption Enterprise

## Encryption-backed access control

\[Omitted video\] Description: This video provides an overview of Field Encryption, including how it protects sensitive data at rest by encrypting individual fields and attachments, and how its key components work together.

By default, Field Encryption blocks all users, scripts, and system processes from accessing encrypted data. However, Field Encryption has an access control feature that works with Access Control Lists \(ACLs\). This feature ensures only the correct users, scripts, or system processes can access encrypted data.

You can configure Field Encryption access control feature through a combination of Field Encryption Modules, Encrypted Field Configurations, and Module Access Policies. The next image shows how these three components work together.

\[Omitted image "fe-diagram-1.png"\] Alt text: Field encryption and supporting components

Module Access Policies \(shown in the next image\) authorize users, scripts, or system processes to access encrypted data. By default, encrypted data is locked down from any access in the instance.

\[Omitted image "fe-diagram-2.png"\] Alt text: Module access policy flow

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

Field Encryption currently doesn't support the encryption of fields and attachments of system tables \(tables that begin with sys\_\).

## Field Encryption and archive tables

Archive tables store historical data from base tables. When you create Encrypted Field Configurations, define them on your base tables, not on archive tables. Encrypted data from base tables automatically moves to archive tables in an encrypted state. For detailed information on how encryption interacts with archive tables and best practices, see [Archive Tables and Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/archive-tables-fe.md).

## Cloning considerations

When you clone an instance that uses Field Encryption, the encrypted field data and encryption modules are copied to the target instance. Because encryption keys are re-encrypted with a secondary key that is unique to the source instance, the target instance can't decrypt the field data after cloning.

Until a key exchange is performed, encrypted fields on the cloned instance appear empty or unreadable. This is expected behavior and does not indicate data corruption or loss.

To restore access to encrypted fields on the target instance, complete a key exchange from the source instance. See [Configure Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/configure-key-exchange.md).

## What to explore next

To learn more about configuring and using Field Encryption, see:

-   [Configuring Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/configuring-column-level-encryption.md)
-   [Using Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/using-column-level-encryption.md)

-   **[Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-platform-encryption.md)**  
Field Encryption Enterprise uses the Key Management Framework \(KMF\) to enable you to customize and manage how fields and attachments are encrypted and decrypted on your instance. A subscription is required to use Field Encryption Enterprise.

**Parent Topic:**[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/field-encryption.md)

