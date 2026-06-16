---
title: Service Level Objective Management for Service Operations Workspace release notes
description: Version history for the Service Level Objective Management for Service Operations Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-level-objective-mgmt-sow.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Level Objective Management for Service Operations Workspace release notes

Version history for the Service Level Objective Management for Service Operations Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - June 2026**
    -   New:
        -   Added a dedicated reliability tasks table, extending the base task framework so operators and SREs can track and manage reliability improvement work.
        -   Added service level objective \(SLO\) tier classification \(platinum, gold, silver, and bronze\) to define service objectives based on business criticality.
        -   Added an slo\_operator role with scoped access to view SLOs and their associated reliability tasks.
-   **Version 1.6.2 - May 2026**

    New:  Included REST APIs used in MCP tools.

-   **Version 1.6.1 - March 2026**
    -   New: Added work notes for service level objectives \(SLOs\) to record and track updates in one place. Posted work notes appear in the Activity panel, providing a unified view of both manual and automated SLO changes.
    -   Fixed:
        -   Fixed the service level indicator \(SLI\) display on the SLO form.
        -   Fixed issues with SLO notification destinations.
-   **Version 1.5.1 - December 2025**
    -   Changed:
        -   Filter SLIs to specific outages, in addition to alerts, to accurately measure downtime.
        -   Navigate service level objectives \(SLOs\) more efficiently with a redesigned SLO table on the Reliability metrics tab.
        -   Analyze high burn rates on the Service reliability dashboard with chart links that now open in chart view instead of list view.
        -   Open SLOs directly from Microsoft Teams notifications using a new button that replaces the previous text link.
    -   Fixed:
        -   Resolved CI dropdown rendering issues in the SLI form.
        -   Track real downtime and customer impact using outage-based service level indicators \(SLIs\).
-   **Version 1.4.2 - September 2025**

    Fixed: Inconsistent dropdown behavior when filtering by child CI during SLI addition

-   **Version 1.4.0 - August 2025**
    -   New: Error budget now updates in real-time as issues occur.
    -   Changed: Microsoft Teams integration UX for notification destinations.
    -   Fixed: Error Budget policy actions trigger for notifications.
-   **Version 1.3.0 - May 2025**

    New: Links CIs to Application Services to roll their reliability into parent Service SLOs and Error Budgets.

-   **Version 1.2.0 - February 2025**

    Changed: SLO naming improvements.

-   **Version 1.1.1 - November 2024**
    -   Fixed:
        -   UX issues and validations related to SLO and Error Budget Policy creation.
        -   Internationalization and localization bugs.
        -   ACL security vulnerabilities.
-   **Version 1.0.1 - September 2024**

    Fixed: Addressed a user interface issue where SLO summary and other graphs fail to refresh or reload when the time period is changed.

-   **Version 1.0.0 - August 2024**

    Service Level Objective \(SLO\) management is a crucial aspect of Site Reliability Engineering \(SRE\) that focuses on defining, monitoring, and maintaining the reliability and performance standards for services. Effective SLO management involves several key components, including Service Level Indicators \(SLIs\) and error budgets.


**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

