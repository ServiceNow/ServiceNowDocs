---
title: Smart Assessment Migration tools release notes
description: Version history for the Smart Assessment Migration tools application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-smart-assessment-migration-tools.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Smart Assessment Migration tools release notes

Version history for the Smart Assessment Migration tools application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   Changed:
        -   New Query Range Security Rules — Four migration data tables \(Section, Question, Response Option, Template Migration\) now have consistent access control rules. Authenticated users with read rights can query migration records.
        -   Automatic ACL Upgrade Handling — Two new upgrade scripts manage the transition: preload script registers ACL identifiers before upgrade; customisation detection script runs after to identify and process any administrator-modified ACLs through Cobalt Raven true-up flow.
        -   No Admin Action Required — New ACL rules install automatically during upgrade. Existing migration processes continue functioning; no previously permitted operations are blocked.
        -   Improved Reliability — Both upgrade scripts now execute in global scope, ensuring clean installation across all scenarios, including upgrades triggered from non-global application scopes.
        -   Post-Upgrade Review — If your instance had customised ACLs on migration tables, review those records after upgrade to confirm they reflect your intended access policy.
-   **Version 22.0.0 - March 2026**

    Fixed: Refreshed and corrected string translations to enhance localization and user experience across supported languages.

-   **Version 21.1.1 - December 2025 \(Zurich\)**

    Fixed: Security enhancement for read-only fields.

-   **Version 21.0.1 - August 2025**
    -   New:
        -   Enhanced the migration tool to convert question dependencies into conditional visibility during migration.
        -   Enhanced the migration tool to migrate checkbox-type questions to radio button type questions with Yes/No options.
    -   Changed: "Template category" field on assessment template migration form is now labeled as "Purpose".
-   **Version 20.0.1 - February 2025**
    -   New:
        -   An API is now available to migrate a metric type to an assessment template.
        -   An event named "sn\_smart\_asmt\_mig.migrn\_status\_changed" is triggered when the template migration status changes to completed, partially completed, or errored.
    -   Fixed:
        -   Now able to migrate existing metric types with special characters in their names to the assessment template.
        -   The "Migrate" button is now hidden when the migration status is not "New."
-   **Version 19.1.0 - November 2024**

    Evaluate Sandbox Access for Client-Callable Script.

-   **Version 19.0.2 - August 2024**

    The ServiceNow Smart Assessment Migration Tools application enables you to migrate existing assessment designs from the ServiceNow Assessments and Surveys application. Your templates are automatically transferred as drafts with just one click. After you migrate the designs, you must review and publish these drafts, and confirm the results. The sets of questions in the Assessments and Surveys application are saved as metric types. When migrated, these metric types are saved as question types. Custom, Duration, Image scale, Percentage, Rankings, and Ratings question types aren't supported for migration.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

