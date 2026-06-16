---
title: Scan Engine release notes
description: Version history for the ServiceNow Scan Engine application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-impact-scan-engine.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Impact release notes, ServiceNow Store release notes]
---

# Scan Engine release notes

Version history for the ServiceNow® Scan Engine application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.4 - June 2026**
    -   What's New Starting June 11th:
        -   Real-Time Prevention Messaging Redesign — When the scan engine catches a problem in your code, developers now see a cleaner, easier-to-read breakdown of what needs attention. Issues are organized by severity — Act, Recommend, and Suggest — in a persistent side panel with improved contrast and reduced scrolling. Exception requests appear right next to the relevant finding, and developers get a clear confirmation once something is resolved.
        -   Parallel Bulk Remediation Processing — The Remediation Agent now handles multiple batches at the same time using an event-driven queue, so a large or slow batch no longer holds up everything else. A built-in safeguard automatically clears out any batch that gets stuck for more than six hours, keeping things moving without manual intervention.
        -   Analytics Dashboard — You can now click any segment of the donut chart to drill into the findings behind it. The heatmap has been updated to meet accessibility standards, making results easier to read for everyone. Dashboard data now refreshes in near real-time, with status updates so you always know where things stand.
        -   Scan Engine Backend — Each flagged finding in an update set now requires its own exception reason, so nothing is ignored. A new tooltip on the Level of Finding field explains what Act, Recommend, Suggest, and Review each mean — right in context, without needing to look it up.
-   **Version 2.1.0 - April 2026**

    Fixed: Fixed an issue where definition synchronization failed when email notifications required additional permissions.

-   **Version 2.0.3 - March 2026**
    -   New:
        -   Run scans directly from the Scan Results list view using UI actions. You can now trigger delta scans using Initiate Scan and start a full scan using Force Full Scan \(including cancelling an in-progress delta scan to immediately begin a full scan\).
        -   Scan Engine will now perform a Live Scan on any Record \(sys\_metadata\) during load of Form View. This means that Findings are immediately created in real-time. This “Passive Enforcement” mode allows the Real-Time Validation to be set to False so that Developers are not interrupted on Insert / Update of records, but when the Form View loads, a Scan is performed and Findings are generated.
        -   Creates exception reasons directly from findings \(without needing to navigate to the underlying scanned record\).
    -   Changed:
        -   Improved scan initiation behavior and visibility for scan UI actions. Updated behavior around when scan buttons appear and how scan initiation messaging behaves on the Scan      Results page.
        -   Out-of-box \(OOTB\) scanning is no longer customer-configurable. This change prevents Scan Engine from scanning partner/store application records and surfacing findings that customers can’t act on.
        -   Additional logging information has been added to the Scan Status page. This provides additional feedback to indicate where the current scan is within the process of loading application files.
    -   Fixed:
        -   Resolved issues where story/task details and links from a source instance were not fully syncing to the target \(production\) instance.
        -   Fixed cases where newly created Jira stories/tasks could have a blank short description.
        -   Corrected Exclude Approved Exception counts so governance totals reflect expected values.
        -   Fixed discrepancies in exception views where definitions and line numbers were incorrect.
        -   Ensured exceptions created during remediation are reliably linked to their originating findings for accurate governance and reporting.
    -   Removed:
        -   Removed the property that allowed enabling out-of-box scanning.
        -   The related setting is set to false \(off\) for any customer instances where it had previously been enabled.
-   **Version 1.1.1 - February 2026**
    -   Fixed:
        -   Scan Engine &amp; Definition Fixes
            -   Fixed Scan Engine definition logic and prefixing issues that caused incorrect findings.
            -   Prevented loss of findings from previous full and delta scans.
            -   Improved scan messaging and metadata accuracy.
        -   Findings &amp; Validation
            -   Blocked exception submission when conflicting Act-level and Recommend-level findings exist.
            -   Fixed incorrect “All findings resolved” messaging on scan errors.
        -   UI &amp; Platform Improvements
            -   Resolved Scan Status, dashboard data mismatch, and formatting issues.
            -   Migrated legacy Scan Engine workflows to Flow-based implementations.
-   **Version 1.0.4 - December 2025**

    The Scan Engine is a ServiceNow application designed to automate recommended practice enforcement, manage technical debt, and optimize workflows across ServiceNow environments. It enables administrators and developers to proactively identify, remediate, and track issues through real‑time, on‑demand, and scheduled scans, ensuring continuous improvement in platform health and compliance. Integrated directly into the development lifecycle, it provides real‑time checks within App Engine Studio and script editors to prevent non‑compliant changes before they reach production, while offering intelligent fix suggestions to accelerate resolution.


**Parent Topic:**[ServiceNow Store - Impact release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-impact-highlight.md)

