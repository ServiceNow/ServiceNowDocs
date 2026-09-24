---
title: Code Signing change audit data
description: Review the create, update, and delete operations that users perform on records protected by Code Signing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/cs-vault-audit-data.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Code Signing, audit, audit trail, change tracking, protected records]
breadcrumb: [Administer and Troubleshoot, Code Signing, Platform Security]
---

# Code Signing change audit data

Review the create, update, and delete operations that users perform on records protected by Code Signing.

Code Signing records create, update, and delete operations on a protected record in the sn\_cse\_vault\_codesigning\_audit\_data table. Use this audit data to identify who changed a protected record, which record they changed, and when the change occurred.

Audit data is written by the platform after Code Signing is activated on your instance.

## Operations that generate audit data

The platform writes an audit record only when all of the following conditions are true:

-   Code Signing is activated on the instance. The **com.snc.kmf.signature.validation.optin** property is set to **true**.
-   The **sn\_cse.com.snc.csf.vault\_audit\_enabled** property is set to **true**. This property is set to **true** by default.
-   The instance is a production instance. Development and test instances don't generate audit data.
-   The record belongs to a table that has a Code Signing signature configuration. If the signature configuration includes a signature generation filter, the record must also match that filter.
-   The table isn't listed in the **com.glide.codesigning.tables.excluded\_from\_audit** property. By default, this property excludes the internal tables that Code Signing uses for certificate storage, cryptographic module and policy configuration, and signing job tracking.

For descriptions of these properties, see [Properties installed with Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-sign-properties.md).

## Audit record fields

|Field|Description|
|-----|-----------|
|Application scope \(sys\_scope\)|Application scope that the changed record belongs to.|
|Package \(sys\_package\)|Package that the changed record belongs to.|
|Document ID \(document\_id\)|Sys ID of the changed record.|
|Table name \(table\_name\)|Table that contains the changed record.|
|Modified by \(modified\_by\)|User who performed the operation.|
|Modified on \(modified\_on\)|Date and time when the operation occurred.|
|Operation \(operation\)|Type of operation: `create`, `update`, or `delete`. If the platform can't determine the operation type, the value is `unknown`.|

## Access to audit data

Users with the sn\_cse.codesigning\_auditor role can view the audit data and report on it. For more information about this role, see [Code signing auditor \[codesigning\_auditor\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-role-landing.md).

Create, update, and delete operations on the sn\_cse\_vault\_codesigning\_audit\_data table are restricted to the platform. No role grants write access to this table.

## Audit data retention

The **Vault Code Signing Audit Data Cleaner** scheduled job runs every 12 hours and removes audit records in two passes:

1.  Deletes audit records that are older than the retention period set in the **sn\_cse.com.snc.csf.vault\_audit\_data\_retention\_days** property. The default retention period is 90 days. Valid values are 30 through 360. If you set a value outside this range, the job uses the nearest limit and the property value remains unchanged.
2.  Compares the remaining record count against the **sn\_cse.com.snc.csf.vault\_audit\_data\_max\_size** property, which is set to 9,000 records by default. If the count is higher, the job deletes the oldest records until the count matches the configured maximum.

Only a user with the sn\_cse.codesigning\_admin role can change these properties. Export the audit data that you want to keep for longer than the retention period.

**Note:** Because the job enforces a maximum record count, it can delete older audit records before the retention period ends when the record count exceeds the configured maximum.

**Parent Topic:**[Code Signing reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-reference.md)

