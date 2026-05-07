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

-   Store archive records and attachments in an object storage outside the primary instance.
-   Create and manage Data Management rules directly from the Data Management Console.
-   Search for archived records and restore them in bulk.
-   Enable users to complete administrative tasks in Data Management without the full admin role.

See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Archive data in object storage](https://www.servicenow.com/docs/access?context=c_ArchiveData&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Store archive records and attachments in columnar format in an object storage outside the primary instance, freeing up primary storage and improving query performance for active data. The object storage is exclusive to RaptorDB Professional V2.

-   **[Data Management rules wizard](https://www.servicenow.com/docs/access?context=data-management-policies&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Create and manage your archive, cleanup, and one-time delete rules in the Data Management Console.

-   **[Restore archive records in bulk](https://www.servicenow.com/docs/access?context=managing-archived-data&version=australia&pubname=australia-platform-administration&section=t_RestoreArchivedData&ft:locale=en-US)**

    Search for archived records and restore them in bulk to live tables from the Data Management Console.

-   **[Granular admin role](https://www.servicenow.com/docs/access?context=data-management-roles&version=australia&pubname=australia-platform-administration&section=data-management-role-1&ft:locale=en-US)**

    Enable administrators to perform basic Data Management tasks by granting the data\_mgmt\_tools\_admin role instead of the full admin role.


## Activation information

Data Management and system archiving are ServiceNow AI Platform capabilities that are active by default.

The ability to store archive data in object storage is available with the installation of Live Archive, which requires a separate subscription. For details, see .

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Live Archive\(com.glide.db.columnar.archive\): Enables you to archive data in object storage and set up scheduled jobs to migrate archive tables.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

