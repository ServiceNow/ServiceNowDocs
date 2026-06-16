---
title: Smart Assessment for Field Service Questionnaire release notes
description: Version history for the Smart Assessment for Field Service Questionnaire application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-smart-assessment-fs-questionnaire.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Smart Assessment for Field Service Questionnaire release notes

Version history for the Smart Assessment for Field Service Questionnaire application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.2.0 - June 2026**
    -   New:
        -   Support smart assessment template versioning.
        -   Image recognition using ServiceNow Lens for auto-populating smart assessment mobile form fields.
-   **Version 2.1.1 - June 2026**

    Fixed: Fixed category role on Field Service smart assessment template category.

-   **Version 3.1.0 - March 2026**
    -   New:
        -   Enable saving the responses before final submission including offline mode.
        -   Ability to view completed responses in mobile.
        -   Retake previously submitted smart assessment questionnaires for work order tasks in Needs Information state including offline mode.
-   **Version 3.0.2 - March 2026**

    Changed: Enable support to trigger smart assessment instances for work order extensions when the template or questionnaire setup is done at the work order task level

-   **Version 1.0.5 - October 2025**
    -   Fixed:
        -   Assessment instances are now visible in related list on work order task extension record page.
        -   Updated reference qualifier to restrict assessment template selection on questionnaire template record.
        -   View completed questionnaires in the workspace.
-   **Version 2.0.0 - August 2025**
    -   New:
        -   Generate assessment instances in Asynchronous mode without blocking user interface interactions.
        -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
        -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
        -   Support scoring to transalte responses into quantitive data.
        -   Create follow-up work order tasks from a work order questionnaire based on the score.
        -   Allow users to retry or replace an attachment if the upload is unsuccessful.
        -   View completed questionnaires in the workspace.
    -   Fixed:
        -   Related list cross scope error on questionnaire record page.
        -   Assessment instances not visible in related list on work order task extenstion record page.
-   **Version 1.0.0 - February 2025**

    ServiceNow Smart Assessment for Field Service Questionnaire provides templates for creating and configuring work order questionnaires. The templates provide for comprehensive instructions comprised of rich text and images, as well as conditional questions, comments, and attachments. Available via the Now Mobile Agent application, this feature offers a paginated layout that combines the ability to group questions with inline choices.


