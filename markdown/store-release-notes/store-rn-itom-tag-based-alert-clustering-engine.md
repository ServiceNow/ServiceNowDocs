---
title: Tag Based Alert Clustering Engine release notes
description: Version history for the Tag Based Alert Clustering Engine on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-tag-based-alert-clustering-engine.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Tag Based Alert Clustering Engine release notes

Version history for the Tag Based Alert Clustering Engine on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 18.24.0 - June 2026**

    New: Poactive grouping recommendations are now accessible on the Alert Automation &gt; Group page.Our advanced AI-driven data science model generates these insightful recommendations each month, analyzing alerts to suggest smart grouping automation based on tags. Transforming each recommendation into a rule is a breeze—just a single click with Now Assist lets you review, test, and activate them effortlessly. Dive in and explore this game-changing feature today!

-   **Version 18.22.0 - May 2026**

    Fixed: Fixed performance and scalability issue

-   **Version 18.20.2 - March 2026**
    -   New:
        -   Two additional grouping criteria have been added to the "Mixed Group" options:
            -   Related Log Properties \(HLA\): This allows you to create grouping automations that combine HLA and Event Management alerts within a single group.
            -   Impacted Service Instance: This enables you to adjust the grouping based on your organizational structure.
        -   Additionally, a new "Advanced Options" section has been introduced, allowing you to set prerequisite rules for group creation:
            -   Minimum Threshold: This option lets you configure a specific number \(two or more\) of alerts that must match the rule before the group is formed, helping you create more concise and effective groups.
            -   Seed Alert: This feature lets you define a filter that requires at least one alert in the group to meet before the group is formed, resulting in more meaningful groupings.
-   **Version 18.18.3 - December 2025**

    New: We’ve upgraded the Mixed Groups option with new grouping capabilities. You can now group by Service Instance, Related Logs Entities \(HLA\), or both to create precise and effective alert grouping rules.

-   **Version 18.17.1 - August 2025**

    New: You can now create grouping definitions that combine CI relationships and tags, allowing more flexible and accurate alert grouping.

-   **Version 18.14.0 - May 2025**

    No updates.

-   **Version 18.12.3 - February 2025**

    Two minor fixes.

-   **Version 18.12.1 - November 2024**
    -   Changed: Group simulation order is now executed in an ascending order
    -   Fixed:
        -   Fixed time window settings for Tag Based groups
        -   Removing unnecessary error message when saving a new Tag Clustering definition
-   **Version 18.11.2 - October 2024**

    Fixed: Groups are not being properly updated when new tags are added to an existing definition.

-   **Version 18.10.2 - August 2024**
    -   New: Enable group simulation using the Alert Automation in Service Operations Workspace.
    -   Fixed:
        -   Fixed upgrade of tag-based clustering definition.
        -   Fixed the population of the Assignment Group field.
-   **Version 18.8.0 - July 2024**
    -   Fixed:
        -   Pattern match happens when source type is one of: additional\_info, alert\_tags, and cmdb\_key\_value.
        -   Group criteria is working only for alerts with non empty value.
        -   ACL for the assignment group field.
        -   If a field is selected for group criteria, only alerts with not empty field value are grouped.
-   **Version 18.7.2 - June 2024**
    -   New:
        -   Tag-Based Alert Clustering Simulation: Helps users test and assess their implementation using simulation mode.
        -   Team-Based Rules: Adds the option for team-level rules that are executed only for assigned alerts.
        -   Out-of-the-Box Alert Clustering Definitions.
-   **Version 18.6.0 - March 2024**
    -   New: 12 new out-of-the-box Tag-based Alert Clustering definitions created.
    -   Removed: 4 existing out-of-the-boxTag-based Alert Clustering definitions removed for new customers.
-   **Version 18.5.3 - August 2023**

    Fixed: Fixing issues related to the custom description of Tag-Based groups.

-   **Version 18.4.8 - May 2023**

    New: Clustered alerts are aggregated under a virtual alert rather than one of the real alerts \(available starting Vancouver\).

-   **Version 18.3.3 - November 2022**
    -   New: Supporting alert tags field for alert clustering
    -   Fixed:
        -   Fixed the link in the blue box message
        -   Fixed localization issues
-   **Version 18.2.10 - April 2022**

    Fixed: Fixing tags and clustering definitions in a domain separated instance

-   **Version 18.1.4 - November 2021**
    -   New:
        -   Support tags on CI keys from cmdb\_key\_value table
        -   Support platform patterns on tags to extract values
        -   Exclude list property for alert fields
    -   Fixed: Bug fixes
-   **Version 18.0.6 - August 2021**

    New: The Tag Based Alert Clustering Engine app is a zero-code method that simplifies alert grouping and performs alert correlation without the need for CMDB, model training, or fine-tuning. The tag-based clustering capability enables alert clustering immediately from activation and works in parallel with existing ServiceNow alert correlation algorithms.


