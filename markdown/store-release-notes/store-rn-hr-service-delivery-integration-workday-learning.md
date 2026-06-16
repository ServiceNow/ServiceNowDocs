---
title: Human Resources Service Delivery Integration with Workday Learning release notes
description: Version history for the Human Resources Service Delivery Integration with Workday Learning application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-service-delivery-integration-workday-learning.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Human Resources Service Delivery Integration with Workday Learning release notes

Version history for the Human Resources Service Delivery Integration with Workday Learning application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.0 - August 2025**
    -   The Workday Learning integration faced issues with tagging skills to courses due to unmatched or missing entries in the cmn\_skill table. There was no mechanism to harmonize and store new skills, and the existing process relied solely on direct lookups, leading to inefficient skill processing.
        -   New: Introduced a dual-path skill resolution mechanism using SkillResolverAPI for direct matches and SkillHarmonizationUtil for harmonizing unmatched skills.
        -   Changed: Enhanced the processSkills function in WorkdayLearningIntegrationUtilsSNC to support both direct and harmonized skill mapping workflows.
        -   Fixed: Ensured that all relevant skills - whether matched or harmonized - are correctly inserted into the Course Item Skills table, improving tagging accuracy.
        -   Removed: Eliminated the limitation of relying solely on direct skill lookups, enabling broader and more intelligent skill coverage.
-   **Version 1.3.0 - February 2025**

    Removed: With this release, we are dropping the Workday learning hard dependency with the Skill Intelligence Store app \(No other functionality or areas within the integration are impacted by this change\).

-   **Version 1.2.0 - November 2024**
    -   Sync Workday Learning Content, Tasks, and Users to ServiceNow
    -   Surface Workday Learning Content via the following applications:
        -   Learning Posts \(Employee Journey Management\)
        -   Learning \(Talent Development\)
        -   Coaching \(Workforce Optimization\)
-   **Version 1.1.1 - February 2024**

    Minor fixes.

-   **Version 1.1.0 - August 2023**
    -   New:
        -   oAuth Authorization
        -   Includes Skills and Proficiencies associated with the courses from Workday Learning
-   **Version 1.0.0 - November 2022**
    -   The integration with Workday Learning pulls learning tasks and to-dos from Workday Learning into ServiceNow so that employees can view all of their learning tasks from their unified employee portal.
    -   These learning tasks can be accessed from anywhere, on any device. Employees can find and complete their learning courses on-time, and HR and learning teams spend less time managing compliance and updating multiple systems.
    -   Leverage Workday Learning content in learning-focused applications such as Coaching, Learning Posts within Journeys, and Employee Growth and Development.

**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

