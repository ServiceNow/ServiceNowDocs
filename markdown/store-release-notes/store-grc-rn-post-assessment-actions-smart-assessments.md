---
title: Post Assessment Actions for Smart Assessments release notes
description: Version history for the Post Assessment Actions for Smart Assessments application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-post-assessment-actions-smart-assessments.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Post Assessment Actions for Smart Assessments release notes

Version history for the Post Assessment Actions for Smart Assessments application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New: Support for template versioning in post-assessment actions. Existing automations or assessments won't be impacted
    -   Changed:
        -   New Query Range Security Rules —  Authenticated users with read rights can query post assessment or Impact automation
        -   Automatic ACL Upgrade Handling — Two new upgrade scripts manage the transition: preload script registers ACL identifiers before upgrade; customisation detection script runs after to identify and process any administrator-modified ACLs through Cobalt Raven true-up flow.
        -   No Admin Action Required — New ACL rules install automatically during upgrade. Existing migration processes continue functioning; no previously permitted operations are blocked.
        -   Improved Reliability — Both upgrade scripts now execute in global scope, ensuring clean installation across all scenarios, including upgrades triggered from non-global application scopes.
        -   Post-Upgrade Review — If your instance had customised ACLs on migration tables, review those records after upgrade to confirm they reflect your intended access policy.
        -   Security defect fixes
        -   Localization changes
-   **Version 22.0.2 - March 2026**

    Fixed: Refreshed and corrected string translations to enhance localization and user experience across supported languages.

-   **Version 20.1.0 - May 2025**

    Fixed an issue where the automation name and description were not localized in the assessment template builder within the assessment workspace.

-   **Version 20.0.2 - February 2025**

    Post-assessment actions inSmart Assessment Engine are designed to streamline and automate tasks based on the responses or outcomes of an assessment. The purpose of post-assessment actions is to automate tasks like updating a record based on a response provided in the assessment, creating a new assessment after an assessment is submitted, eliminating the need for manual intervention.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

