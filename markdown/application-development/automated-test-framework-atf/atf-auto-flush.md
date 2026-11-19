---
title: Autoflush form
description: On the Auto Flush form, you specify a retention policy for a set of records on a given test results table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/automated-test-framework-atf/atf-auto-flush.html
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Table cleanup, Administration, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
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

**Note:** Table cleanup policies are platform-specific policies. See [Table cleaner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/table-cleaner.md) for more information.

**Parent Topic:**[Table cleanup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/automated-test-framework-atf/table-cleanup.md)

