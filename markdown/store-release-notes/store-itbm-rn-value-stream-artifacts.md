---
title: Value stream artifacts release notes
description: Version history for the Value stream artifacts application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-value-stream-artifacts.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Value stream artifacts release notes

Version history for the Value stream artifacts application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.0 - June 2026**
    -   New:
        -   Added out-of-the-box query\_range ACLs for multiple tables.
        -   Added two fix scripts to carry forward customizations seamlessly during the Cobalt directive upgrade.
-   **Version 2.2.0 - March 2026**
    -   New:
        -   Updated the Value Stream Stage record page with a redesigned layout that improves clarity and usability.
        -   Key metrics and related information are now easier to access, making it simpler to analyze stage performance.
-   **Version 2.1.0 - December 2025**
    -   New: Introduced a new administrative role, value\_stream\_admin, to support granular control within the Value Stream application.
    -   Changed:
        -   Users with the value\_stream\_admin role can now create, edit, and delete records in cmn\_value\_stream\_category.
        -   value\_stream\_admin can create, edit, and delete record in cmn\_value\_stream\_category. This update align with the Granular Admin Roles directive, ensuring more precise role-based permissions.
-   **Version 2.0.1 - August 2024**

    This plugin contains the data model artifacts required for value stream management. The core data model enables the creation of Value Streams and also breaks down value streams into various stages. The value stream and its stages can be associated with business processes or capabilities.


