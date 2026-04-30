---
title: Enable auditing for a system table
description: Deletions from tables with a sys\_ prefix are not audited by default. To track deletions from these tables, add the table name to the glide.ui.audit\_deleted\_tables property. Enabling the Restore Deleted Records plugin adds several default values to this property.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring auditing for a table, Auditing]
---

# Enable auditing for a system table

Deletions from tables with a sys\_ prefix are not audited by default. To track deletions from these tables, add the table name to the **glide.ui.audit\_deleted\_tables** property. Enabling the Restore Deleted Records plugin adds several default values to this property.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the **List of system tables \(beginning with "sys\_", comma separated\) that will have the delete audited** property.

3.  Add or remove table names. Table names should be separated by commas, without any spaces.

4.  Click **Save**.

    **Note:** For more information about auditing, see [Understanding the sys audit Table](../../security/concept/c_UnderstandingTheSysAuditTable.md#).


