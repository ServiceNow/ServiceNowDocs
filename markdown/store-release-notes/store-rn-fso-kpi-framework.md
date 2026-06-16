---
title: KPI Framework release notes
description: Version history for the KPI Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-kpi-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# KPI Framework release notes

Version history for the KPI Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   Performance enhancement for supplier overall dashboard
        -   Fixed domain and score calculation
-   **Version 6.0.4 - June 2026 \(Yokohama\)**
    -   Fixed:
        -   Performance enhancement for supplier overall dashboard
        -   Fixed domain and score calculation
-   **Version 6.0.1 - March 2026**
    -   New:
        -   Action Plans in Related Work Tab: Action plans are now surfaced directly in the Related Work tab of the supplier record, eliminating the need to navigate away to find associated plans.
        -   Threshold Modal: Creating or modifying a threshold now opens in a modal dialog instead of a new browser tab, keeping users in context during configuration.
        -   Score Precision: Supplier performance scores are now displayed with 3-decimal precision \(e.g., 72.450\) instead of whole numbers, providing greater accuracy in performance evaluation.
    -   Changed: Gantt Chart Progress Bar Colours: Task and milestone colours now reflect both due date status and completion state. Tasks and milestones not yet due are displayed in Teal colour. Once the due date is reached, completed items turn Blue, incomplete items turn Orange, and milestones with no data collected are displayed in Gray colour.
-   **Version 5.0.0 - December 2025**
    -   New:
        -   Automated KPIs
            -   The automated KPI collection system improves SLO performance by seamlessly managing performance monitoring by:
                -   Automated Data Collection: Pull KPI data directly from ServiceNow tables at a defined frequency
                -   Configurable Conditions: Set rules to extract and aggregate data accurately
                -   Exception Handling: Automatically revert to manual collection if automated processes fail
            -   The Automated KPIs feature reduces manual effort, ensures timely KPI updates, and provides a reliable fallback mechanism for uninterrupted performance tracking.
-   **Version 4.0.0 - August 2025**

    Fixed: Minor fixes

-   **Version 3.0.0 - May 2025**
    -   Action Plan: Addresses performance gap by creating action plans link to under performing KPIs enabling visual tracking of milestones and tasks.
    -   Multiple dimension KPIs: Create supplier-level and contract-level KPIs using KPI templates to measure supplier performance. Contract-level KPIs are created under supplier-level KPIs.
-   **Version 2.0.0 - February 2025**
    -   New: Ability to create KPIs without using KPI templates
    -   Fixed: Minor fixes
-   **Version 1.0.0 - November 2024**

    Performance framework to support the process of evaluation, measurement, and continuous improvement of suppliers.


