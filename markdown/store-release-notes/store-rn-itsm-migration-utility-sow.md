---
title: Migration Utility for Service Operations Workspace release notes
description: Version history for the Migration Utility for Service Operations Workspace on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-migration-utility-sow.html
release: store
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Migration Utility for Service Operations Workspace release notes

Version history for the Migration Utility for Service Operations Workspace on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.1 - May 2025**
    -   New:
        -   Support for migrating ITSM child task tables
        -   Prereq action to make an update set the current update set
        -   Ability to remove ITSM Agent Workspace from the left navigation
-   **Version 2.2.1 - February 2025**
    -   New:
        -   Added a link to navigate to the list of basic authentication users
        -   Added an action to refresh the list of basic authentication users
        -   A default name for the base update set is provided
        -   During migration, you can set the new record form view to workspace
        -   Application scope name is appended to each update set
        -   Migration summary shows what was skipped if there was nothing to migrate
        -   Added an action to view update sets on the pre-reqs page
-   **Version 2.1.2 - November 2024**

    New: Additional prerequisites support the creation of multiple update sets, with one update set for each application scoped to the Service Operations Workspace.

-   **Version 2.0.1 - September 2024**

    Fixed: Migrated records not being tracked in right update set.

-   **Version 2.0.0 - August 2024**

    ITSM Agent Workspace is deprecated, and is no longer supported by ServiceNow. So, this utility allows an administrator to easily migrate configuration and customizations applied in ITSM Agent Workspace to Service Operations Workspace.


