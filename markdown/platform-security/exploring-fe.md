---
title: Exploring Field Encryption
description: Learn the details of Field Encryption Starter and Field Encryption Enterprise
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 3
breadcrumb: [Field Encryption, Encryption]
---

# Exploring Field Encryption

Learn the details of Field Encryption Starter and Field Encryption Enterprise

## Encryption-backed access control

This video provides an overview of Field Encryption, including how it protects sensitive data at rest by encrypting individual fields and attachments, and how its key components work together. 

By default, Field Encryption blocks all users, scripts, and system processes from accessing encrypted data. However, Field Encryption has an access control feature that is used in combination with, but also separate from, Access Control Lists \(ACLs\) to ensure only the correct users, scripts, or system processes can access encrypted data.

You can configure Field Encryption access control feature through a combination of Field Encryption Modules, Encrypted Field Configurations, and Module Access Policies \(MAPs\). The next image shows how these three components work together.

![Field encryption and supporting components](../image/fe_field_encryption_components_diagram.svg)

By default, encrypted data is locked down from all access. A MAP defines which accessor \(users, scripts, and system processes\) can be authorized to access the data.

![Module access policy flow](../image/fe_map_diagram.svg)

You can configure multiple MAPs to apply different access rules to different encrypted fields. In this diagram, Module Access Policy A covers columns A, B, C, and D, and Module Access Policy B covers column E — each with its own rules per accessor.

![Multiple module access policy example](../image/fe_map_example_diagram.svg)

Access rules can differ between two policies for each accessor type. The following table reflects the access rules defined for Module Access Policy A, applied to columns A, B, C, and D, and Module Access Policy B, applied to column E.

<table><thead><tr><th>

Accessor

</th><th>

MAP A Columns A, B, C, D

</th><th>

MAP B Column E

</th></tr></thead><tbody><tr><td>

Role A

</td><td>

Allow

</td><td>

Block

</td></tr><tr><td>

Role B

</td><td>

Allow

</td><td>

Block

</td></tr><tr><td>

Role C

</td><td>

Block

</td><td>

Allow

</td></tr><tr><td>

Script A

</td><td>

Allow

</td><td>

Block

</td></tr><tr><td>

Script B

</td><td>

Block

</td><td>

Block

</td></tr><tr><td>

Script C

</td><td>

Block

</td><td>

Allow

</td></tr><tr><td>

System Context Processes

</td><td>

Block

</td><td>

Allow

</td></tr></tbody>
</table>## Differences between Field Encryption Starter and Field Encryption Enterprise

The feature-set is different between Field Encryption Starter and Field Encryption Enterprise.

<table id="table_uk2_b3n_b2c"><thead><tr><th>

Feature

</th><th>

Field Encryption Starter

</th><th>

Field Encryption Enterprise

</th></tr></thead><tbody><tr><td>

Number of encrypted fields

</td><td>

Up to 5 encrypted fields**Note:** Field Encryption Starter limits the number of encrypted fields, not encryption modules or contexts. Field Encryption replaces the deprecated Column Level Encryption product, which used a module and context-based limit.

</td><td>

No restriction on number of encrypted fields

</td></tr><tr><td>

Attachment encryption

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Key management

</td><td>

None \(Contact ServiceNow Support for key rotation\)

</td><td>

Manage keys from your instance with no involvement from ServiceNow Support

</td></tr><tr><td>

Supported data types

</td><td>

All supported data types

</td><td>

All supported data types

</td></tr><tr><td>

Number of Field Encryption Modules

</td><td>

No restriction

</td><td>

No restriction

</td></tr><tr><td>

Number of Module Access Policies

</td><td>

No restriction

</td><td>

No restriction

</td></tr></tbody>
</table>## Field Encryption users

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

