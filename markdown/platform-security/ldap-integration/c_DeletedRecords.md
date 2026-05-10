---
title: Record LDAP deletions
description: By default, the instance does not delete any entries after they disappear from LDAP.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# Record LDAP deletions

By default, the instance does not delete any entries after they disappear from LDAP.

Deleting an entry, also referred to as a record, also deletes the entire history and references to the deleted entry.

For example, configuration items \(CIs\), SLA agreements, software licenses, purchase orders, and service catalog entries all have a reference to Department, and if a department is deleted, then the integration clears all references to the department. Also, deleting a user results in losing all history of what that user did.

Decide whether to retain or [Delete all records from a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_DeleteAllRecordsFromATable.md) according to your organization's needs.

