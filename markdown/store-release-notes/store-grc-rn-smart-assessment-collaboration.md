---
title: Smart Assessment Collaboration release notes
description: Version history for the Smart Assessment Collaboration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-smart-assessment-collaboration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Smart Assessment Collaboration release notes

Version history for the Smart Assessment Collaboration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   Changed:
        -   New Query Range Security Rules —  Adding query range ACL's based on user permissions
        -   Automatic ACL Upgrade Handling — Two new upgrade scripts manage the transition: preload script registers ACL identifiers before upgrade; customisation detection script runs after to identify and process any administrator-modified ACLs through Cobalt Raven true-up flow.
        -   No Admin Action Required — New ACL rules install automatically during upgrade.
        -   Improved Reliability — Both upgrade scripts now execute in global scope, ensuring clean installation across all scenarios, including upgrades triggered from non-global application scopes.
        -   Localization changes
-   **Version 22.0.1 - March 2026**

    New: The assessment owner can add or remove contributors to an assessment and assign them either full assessment access or section specific access based on their responsibilities and expertise. Contributors can work simultaneously on the assessment enabling real-time collaboration and efﬁcient progress.

-   **Version 21.0.1 - August 2025**

    Enhance assessments with real-time collaboration - assessment owners can now add multiple contributors to work together seamlessly. Changes are instantly reflected, and presence indicators show who is actively viewing or editing the assessment, enabling efficient and transparent teamwork.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

