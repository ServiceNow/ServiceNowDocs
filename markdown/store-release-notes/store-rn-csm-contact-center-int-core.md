---
title: Contact Center Integration Core release notes
description: Version history for the Contact Center Integration Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-contact-center-int-core.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Contact Center Integration Core release notes

Version history for the Contact Center Integration Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.2 - March 2026**

    Same functionality as V1.5.1: Certified for Australia family release.

-   **Version 1.5.1 - March 2026**

    Search queries are now sent to CCaaS providers. This allows CCaaS to return only matching values, which reduces the amount of unnecessary data sent back to ServiceNow.

-   **Version 1.5.0 - January 2026**

    New in this Release: This new table maps ServiceNow tasks to the CCaaS External Routing implementation, enabling any task type to be configured for external routing through CCaaS.

-   **Version 1.4.4 - December 2025**

    Queue import workflow was updated to allow multiple service channels to be applied simultaneously.

-   **Version 1.3.1 - September 2025**
    -   UI changes to align all data import workflows \(skills, queues, and wrap-up codes\)
    -   Updated field type of provider value to string
-   **Version 1.3.0 - August 2025**
    -   Added a post-import confirmation page to the queues import workflow
    -   Added an extension point to simplify the creation of CCaaS provider choice records
-   **Version 1.1.0 - February 2025**
    -   New:
        -   Ability to import individual pieces of data rather that all records at the same time
        -   Ability to use text to search for specific skills and wrap up codes
        -   Post import confirmation summary page for skills and wrap up codes
    -   Changed: Skills and wrap up codes are no longer automatically fetched from CCaaS provider upon page load. This reduces page load time.
-   **Version 1.0.1 - November 2024**

    This plugin provides different features that can be integrated with Contact Center as a Service \(CCaaS\).


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

