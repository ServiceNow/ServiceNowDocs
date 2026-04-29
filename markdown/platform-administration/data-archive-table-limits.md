---
title: Archive table size limits
description: There are constraints to the size of the table you use to archive your instance data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Archive table size limits

There are constraints to the size of the table you use to archive your instance data.

## Limits on data archive tables

There is a limit on the size of an archive table you can create to store data. The limit is based on the size of the data, not the record count. If you receive an error that an archive table could not be created, it might be related to this size limitation.

|Table Attribute|Size|
|---------------|----|
|Static row size limit|65535 bytes|
|Row size limit|8126 bytes|
|Columns|1000 for Oracle 1011 for others|

Review the custom columns on the table being archived. Also review the custom fields on the tables the table extends from. Determine if those columns are no longer needed and are not being used by current customizations. If you identify unused columns, you can remove them. Doing this might reduce the row size of the table being archived. If that is unsuccessful, contact ServiceNow® Customer Service and Support to see what other alternatives are available.

**Parent Topic:**[Data Management reference](../../managing-data/reference/data-management-reference.md)

