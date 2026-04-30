---
title: Autoflush form
description: On the Auto Flush form, you specify a retention policy for a set of records on a given test results table.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Table cleanup, Administration, Automated Test Framework reference, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Autoflush form

On the Auto Flush form, you specify a retention policy for a set of records on a given test results table.

|Field / Element|Description|
|---------------|-----------|
|Tablename|The table containing the records to which the policy applies.|
|Matchfield|The field for which the system monitors duration.|
|Age in seconds|The amount of time \(in seconds\) the system wait before deleting the records.|
|Active|**True** if this policy is active. Otherwise, **false**.|
|Application scope|The application scope to which this policy applies.|
|Cascade delete|If checked, the system deletes all matching records plus any records referring to them. If unchecked, the system deletes matching records, but not records referring to them.|
|Conditions|The filter conditions defining the records in this table to which the policy applies.|

**Note:** Table cleanup policies are platform-specific policies. See [Table cleaner](https://www.servicenow.com/docs/access?context=table-cleaner&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

**Parent Topic:**[Table cleanup](../concept/table-cleanup.md)

