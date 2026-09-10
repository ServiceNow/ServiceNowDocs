---
title: Sales Quota Application release notes
description: Version history for the Sales Quota Application application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-sales-quota-app.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management version history release notes, ServiceNow Store version history release notes]
---

# Sales Quota Application release notes

Version history for the Sales Quota Application application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.4 - September 2026**
    -   New:
        -   Upgraded @servicenow/sdkfrom ^4.8.1to a pinned 4.9.3and added --emitDictionary=falseto the ci:buildcommand to resolve build failures.
        -   Added cwf-workspace, cwf-csm-workspace, and cwf-workspace-integrationsto the @WithScopedAppdependency list in AB\_LoadAppsIT.Added the corresponding cwf-workspacedependencies to the test POMs to resolve app-load test failures.
-   **Version 1.2.2 - August 2026**

    Fluent based development support added.

-   **Version 1.2.1 - July 2026**

    Added OOB query range support via new SA-based ACLs for the Quota bundle.

-   **Version 1.2.0 - April 2026**

    New: Quota support for product offering family.

-   **Version 1.1.0 - December 2025**

    New: Support for Quota creation for territory based hierarchies.

-   **Version 1.0.0 - May 2025**

    This application enables users to manage sales quotas and track attainment for sales reps against their quotas.


