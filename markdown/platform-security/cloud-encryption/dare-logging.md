---
title: Cloud Encryption logging
description: Learn about logging options for Cloud Encryption.
locale: en-US
release: zurich
product: Cloud Encryption
classification: cloud-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Encryption with Key Management, Encryption]
---

# Cloud Encryption logging

Learn about logging options for Cloud Encryption.

## Cloud Encryption logging tables

Use these tables to find logging information related to Cloud Encryption transactions on your instance.

|Table|Description|
|-----|-----------|
|Cloud Encryption Metadata \[dare\_key\_metadata\]|Cloud Encryption Metadata captures key life-cycle management metadata. On this table you can find key life-cycle, state, and version information. This table is updated after each key operation.|
|Key Management Transactions \[dare\_key\_request\]|Key Management Transactions captures key management transaction information. On this table you can find logging for each step of a transaction. The table records any error information for a transaction in the **error message** field.|
|Sys Audits\[sys\_audit\]|The Sys Audits table captures inserts and updates to all audited records on your instance. On this table you can find changes to records on your instance, when the changes were made, and which user account initiated the change.|

## Monitor key rotation operations

Use the Cloud Encryption Key Metadata \[dare\_key\_metadata\] table to find information on the life-cycle of your key. In this table you can find information like the origin, activation date, state, and version of your keys.

Use the Key Management Transactions \[dare\_key\_request\] table to monitor transactions of key operations. In this table you can find all requests relating to your keys, including the state, status, and which step in the process the request is in. Completed requests are retained on this table with the **Completed** status.

This example shows a key rotation operation. During this operation, the old key life- cycle state updates from active to rotated, and the version state updates from active to retired.

![Key definition for a withdrawn key](../image/dare-log-3.png "Key definition for a rotated key")

Looking at the Sys Audits\[sys\_audit\] table, admins can see changes made to records on the Cloud Encryption Key Metadata \[dare\_key\_metadata\] table. Admins can see which records were updated and when. The log entries also record the field that was changed, and the old and new values.

![Key definition for a withdrawn key](../image/dare-log-4.png "Audit logs for a withdrawn key")

Admins can view the records on the Cloud Encryption Key Metadata \[dare\_key\_metadata\] table. In the audit records below, the request status was changed from processing to completed.

![Key definition for a withdrawn key](../image/dare-log-5.png "Audit logs for a withdrawn key")

## Logging for key withdrawal operations

Logging information on key withdrawal is stored in the Audits \[sys\_audit\] table. This logging information contains information on who initiated the key withdrawal and when the withdrawal took place.

This example shows a key withdrawal operation. During this operation, the key lifecycle state updates from generated, to active, to destroyed. The key version updates from unknown, to active, to retired.

![Key definition for a withdrawn key](../image/dare-log-1.png "Key definition for a withdrawn key")

Looking at the Sys Audits\[sys\_audit\] table, admins can the Cloud Encryption Key Metadata \[dare\_key\_metadata\] table changes.

![Key definition for a withdrawn key](../image/dare-log-2.png "Audit logs for a withdrawn key")

**Parent Topic:**[Cloud Encryption with Key Management](../concept/dare-overview.md)

