---
title: Care Team Mobile release notes
description: Version history for the Care Team Mobile application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-care-team-mobile.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences version history release notes, ServiceNow Store version history release notes]
---

# Care Team Mobile release notes

Version history for the Care Team Mobile application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.1 - October 2026**
    -   New Features:
        -   Care Team Task fulfillment in FSM Mobile: Care team agents can view, update, and complete Care Team Tasks, including attached smart assessments, in FSM Mobile. Status, notes, and assessment results sync back to the desktop task.
        -   Create Care Team Case: Care team members can create a Care Team Case from mobile with a title, description, and priority, all required.
    -   Enhanced:
        -   Care Team Case Assignment and Edit actions:
            -   The case record screen now has an Assignment action, shown only while the case is unassigned, and an Edit action covering 8 case fields.
            -   Care Team Task Assignment action: "Assign task" is renamed "Assignment" and now sets both assignment group and assignee.
            -   Both Assignment actions: The assignee must be an active member of the selected group, and the server rejects anyone else.
            -   Role-based user criteria for FSM Mobile icons: Six out-of-box user criteria records control home-screen icon visibility for the Biomed, EVS, Facilities, HCIT, catch-all, and base care team agent roles.
-   **Version 1.3.0 - July 2026**

    This release includes internal platform improvements and maintenance updates. No new customer-facing features in this version.

-   **Version 1.2.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 1.1.0 - December 2025**
    -   New:
        -   Create support requests based on installed Healthcare Operations case types directly from your mobile device.
        -   Scan asset tags on IT and medical assets and be redirected to the asset's record, where you can view its history, status, and associated cases.
        -   View requests for specific locations, such as patient rooms or supply closets, and access relevant details and preconfigured workflows for reporting issues like sanitation requests or facility repairs.
-   **Version 1.0.0 - August 2025**

    The ServiceNow Care Team Mobile application is built on theHealthcare Operations Core platform and delivers a native mobile experience that enables hospital care teams such as nurses, nurse assistants, unit secretaries, and unit managers to create and view shared support requests for IT, Biomed, Facilities, and Environmental Services departments while on the go.


**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)

