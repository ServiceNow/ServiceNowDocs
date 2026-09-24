---
title: Archive tables and Field Encryption
description: Understand how encrypted data in base tables is handled when it moves to archive tables and get guidelines for properly configuring Encrypted Field Configurations \(EFCs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/archive-tables-fe.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
keywords: [archive tables, field encryption, encrypted field configuration]
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Archive tables and Field Encryption

Understand how encrypted data in base tables is handled when it moves to archive tables and get guidelines for properly configuring Encrypted Field Configurations \(EFCs\).

## How Encrypted Field Configurations interact with archive tables

Encrypted Field Configurations \(EFCs\) interact with archive tables in two common scenarios, each with different encryption behaviors and recommended configurations.

## Basic concepts of archive tables

Archive tables are database tables that store historical or inactive records from base tables. Archive table names use the prefix `ar_` followed by the base table name. For example:

-   Base table: `incident`
-   Archive table: `ar_incident`

Data moves from base tables to archive tables during standard record archival processes. Archive tables follow the same structure as their corresponding base tables.

## How Field Encryption handles archived data

When encrypted data moves from a base table to an archive table, the encryption behavior depends on where the Encrypted Field Configuration \(EFC\) is defined:

**If the EFC is defined on the base table only:** Data moves to the archive table as ciphertext \(encrypted\). Data always appears as ciphertext on archive tables regardless of user permissions.

Users without access to the encryption key see empty fields, just as they would in a base table. Users with access to the encryption key see ciphertext. Archive tables don't have special encryption handling. They follow the same access control rules as base tables through Module Access Policies \(MAPs\).

## Encrypted Field Configuration and archive table interactions scenarios

Two scenarios illustrate how EFCs interact with archive tables, each with different encryption behaviors and configuration approaches.

## Scenario 1: EFC defined on base table only \(recommended\)

**Setup:**

-   Create an EFC on the base table \(for example, the `incident` table\).
-   Don't create an EFC on the corresponding archive table \(`ar_incident`\).
-   Mark the EFC as active.

**Behavior:**

-   Encrypted data on the base table is encrypted with the specified cryptographic module and key.
-   When data is archived \(moved to `ar_incident`\), it remains encrypted \(ciphertext\).
-   The archive table has no EFC defined, so the platform treats the column as raw ciphertext data.
-   Users with access to the encryption key can see the decrypted data only in the base table. In the archive table, the data appears as ciphertext regardless of their permissions.
-   Users without access to the encryption key see empty fields in both the base table and the archive table.

**When to use this scenario:** This is the recommended approach for most use cases. It provides a clear encryption path: define everything on the base table and let data flow to the archive table in an encrypted state. This approach is simpler to manage and reduces configuration complexity.

**Example:** If you create an EFC on the `incident.short_description` field and encrypt it with the module "Global Encryption," the data moves to `ar_incident.short_description` as ciphertext. Users with key access see decrypted data in the incident table but see ciphertext in the ar\_incident table. To view the data as plaintext in the archive table, they must restore the records to the base table. The decryption gate can then process the data.

## Scenario 2: EFC created on archive table during migration \(auto-generated, inactive\)

**Setup:**

-   Create an EFC on the base table and encrypt data.
-   Data on the base table is archived.
-   During a later migration, the platform discovers legacy unmigrated data on the archive table \(from before the EFC was created on the base table\).
-   The platform automatically creates an EFC on the archive table to facilitate the migration of that historical data.
-   The auto-generated EFC is marked as inactive.

**Behavior:**

-   The auto-generated EFC on the archive table exists but isn't active.
-   Users with both the admin and security admin role can manually activate the EFC if needed. When activated, any ciphertext on the archive table appears as plaintext. Because the EFC is inactive by default, the encrypted data on the base table flows to the archive table as ciphertext, consistent with Scenario 1.

**Why the EFC is created but not activated:** The platform creates this EFC as a technical mechanism to identify and facilitate the migration of legacy unmigrated data that exists on archive tables. However, having active EFCs on archive tables isn't recommended, so the platform creates these EFCs as inactive. Activate archive table EFCs only for short periods to decrypt and view historical data.

**When to use this scenario:** This scenario occurs automatically during migration processes and doesn't require manual configuration. Leave the auto-generated EFC inactive and follow Scenario 1 for new data. Activate it only temporarily to decrypt and view historical data on the archive table.

## Scenario comparison

|Aspect|Scenario 1: EFC on base table only|Scenario 2: Auto-generated migration EFC|
|------|----------------------------------|----------------------------------------|
|EFC Location|Base table \(active\)|Archive table \(inactive, auto-generated\) — Brazil release and later|
|Data encryption on base table|Encrypted|Encrypted|
|Data encryption on archive table|Ciphertext \(no decryption\)|Ciphertext \(EFC inactive\)|
|User with key access: base table|Sees decrypted data|Sees ciphertext \(unless EFC is toggled active, then sees plaintext\)|
|User with key access: archive table|Sees ciphertext|Sees ciphertext|
|User without key access: base table|Empty field|Empty field|
|User without key access: archive table|Empty field|Empty field|
|Recommended?|✓ Yes|For migration only; keep inactive|
|Complexity|Low \(single encryption path\)|Low \(handled automatically\)|

## General guidelines

**Recommended practices:**

-   **Define EFCs on base tables.** Create EFCs on your base tables where the data originates. This establishes a clear, single encryption path.
-   **Let data flow encrypted to archive tables.** Allow encrypted data from the base table to move to the archive table in ciphertext. The archive table inherits the encryption from the base table without requiring a separate EFC.
-   **Use Module Access Policies \(MAPs\) associated with the crypto module.** MAPs apply based on the crypto module, not on specific tables. When a MAP is configured for the crypto module, it applies to encrypted data in both base and archive tables. Configure MAPs to control who can access encrypted data based on key access. Without an EFC on the archive table, users with MAP access see only ciphertext regardless of their permissions.
-   **Monitor auto-generated archive table EFCs.** If the platform auto-generates an EFC on an archive table during migration, leave it inactive by default. Activate it only temporarily to decrypt and view historical data, then toggle it back to inactive. Keeping an EFC active on both the base and archive table creates two encryption gates, which is confusing to manage and doesn't follow security recommendations.
-   **Don't create active EFCs on archive tables.** The only exception is auto-generated EFCs created during migration, which the platform creates as inactive.

## Access control and permissions

When encrypted data is in an archive table, access control works the same way as in a base table:

-   **Without a MAP:** Users can't view encrypted columns in archive tables.
-   **With a MAP granting key access:** Users can decrypt and view encrypted data in archive tables if they have the required role or context conditions.
-   **With a MAP without key access:** Users see empty fields in encrypted columns in archive tables.

## Related topics

-   [Exploring Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/exploring-fe.md) – Overview of Field Encryption Starter and Enterprise versions
-   [Configuring Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/configuring-column-level-encryption.md) – Learn how to activate and configure Field Encryption
-   [Using Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/using-column-level-encryption.md) – Manage access to encrypted data
-   [Module Access Policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/module_access_policy_overview.md) – Control access to encrypted data with permissions and context

**Parent Topic:**[Using Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/using-column-level-encryption.md)

