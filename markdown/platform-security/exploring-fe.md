---
title: Exploring Field Encryption
description: Learn the details of Field Encryption Starter and Field Encryption Enterprise
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/exploring-fe.html
release: zurich
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 2
breadcrumb: [Field Encryption, Encryption]
---

# Exploring Field Encryption

Learn the details of Field Encryption Starter and Field Encryption Enterprise

## Encryption-backed access control

By default, Field Encryption blocks all users, scripts, and system processes from accessing encrypted data. However, Field Encryption has an access control feature that is used in combination with, but also separate from, Access Control Lists \(ACLs\) to ensure only the correct users, scripts, or system processes can access encrypted data.

You can configure the access control feature of Field Encryption through a combination of Field Encryption Modules, Encrypted Field Configurations, and Module Access Policies. The next image shows how these three components work together.

\[Omitted image "fe\_field\_encryption\_components\_diagram.svg"\] Alt text: Field encryption and supporting components

By default, encrypted data is locked down from all access. A MAP defines which accessor \(users, scripts, and system processes\) can be authorized to access the data.

\[Omitted image "fe\_map\_diagram.svg"\] Alt text: Module access policy flow

You can configure multiple MAPs to apply different access rules to different encrypted fields. In this diagram, Module Access Policy A covers columns A, B, C, and D, and Module Access Policy B covers column E — each with its own rules per accessor.

\[Omitted image "fe\_map\_example\_diagram.svg"\] Alt text: Multiple module access policy example

Access rules can differ between two policies for each accessor type. The following table reflects the access rules defined for Module Access Policy A, applied to columns A, B, C, and D, and Module Access Policy B, applied to column E.

<table id="table_zlm_fps_y3c"><thead><tr><th>

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

Field Encryption currently doesn't support the encryption of fields and attachments of system tables \(tables that begin with sys\_\).

## What to explore next

To learn more about configuring and using Field Encryption, see:

-   [Configuring Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/configuring-column-level-encryption.md)
-   [Using Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/using-column-level-encryption.md)

**Parent Topic:**[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/field-encryption.md)

