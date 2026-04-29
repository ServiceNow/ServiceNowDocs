---
title: Data Management release notes
description: The ServiceNow Data Management capabilities enable you to manage the growth of data in your instance. Data Management capabilities were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Data Management release notes

The ServiceNow® Data Management capabilities enable you to manage the growth of data in your instance. Data Management capabilities were enhanced and updated in the Australia release.

## Data Management highlights for the Australia release

-   Store archive records and attachments in a secondary object storage outside the primary instance.
-   Enable users to complete administrative tasks in Data Management without the full admin role.

See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Archive data in secondary object storage](https://www.servicenow.com/docs/access?context=c_ArchiveData&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Store archive records and attachments in columnar format in an object storage outside the primary instance, freeing up primary storage and improving query performance for active data. The secondary object storage is exclusive to RaptorDB Professional V2.

-   **[Granular admin role](https://www.servicenow.com/docs/access?context=data-management-roles&version=australia&pubname=australia-platform-administration&section=data-management-role-1&ft:locale=en-US)**

    Enable administrators to perform basic Data Management tasks by granting the data\_mgmt\_tools\_admin role instead of the full admin role.


## Activation information

Data Management and system archiving are ServiceNow AI Platform capabilities that are active by default.

The ability to store archive data in object storage is available with activation of the Data Archiving \(com.glide.db.columnar.archive\) plugin, which requires a separate subscription. For details, see .

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Data Archiving\(com.glide.db.columnar.archive\): Enables you to archive data in object storage and set up scheduled jobs to migrate archive tables.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

