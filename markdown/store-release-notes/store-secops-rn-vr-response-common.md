---
title: Vulnerability Response Common release notes
description: Version history for the Vulnerability Response Common application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-response-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Common release notes

Version history for the Vulnerability Response Common application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.4.2 - June 2026 \(USEM\)**
    -   New:
        -   Extended the Split Test Results framework.
        -   Added out-of-the-box query range Access Control Lists \(ACLs\) for the Vulnerability Response Common store application to harden security enforcement.
        -   Introduced read-only field protections to align with the Australia Security Directive.
    -   Changed:
        -   Smart Assessment templates now support category-based roles and a Quick Edit experience for template updates.
        -   Improved performance by removing unnecessary work note cascading from Remediation Tasks to associated findings.
    -   Fixed:
        -   Fixed an issue where Vulnerable Items could remain in a Deferred state after the associated Exception Rule was deleted.
        -   Fixed an issue where Vulnerable Items did not close correctly when their underlying detections were closed through exception rule processing.
        -   Fixed an issue where reopening a resolved Remediation Task did not reopen its associated resolved Vulnerable Items as expected.
        -   Fixed an issue where manually created Remediation Tasks without associated findings could remain stuck in the Resolved state instead of closing properly.
        -   Fixed inconsistencies with the closed-at timestamp and substate on Vulnerable Items when multiple Remediation Tasks with different substates were closed in varying orders.
        -   Fixed an issue where the Opened by field was not displayed for Remediation Tasks created from the workspace.
        -   Improved access control handling for the Unified Findings table on the Zurich platform release.
-   **Version 2.16.4 - June 2026**
    -   New:
        -   Added query-level access controls to strengthen record visibility enforcement and security across the Vulnerability Response common application.
        -   Added read-only field protections to support compliance with Australia Security Directive requirements.
    -   Changed: Reduced audit log noise by suppressing unnecessary delete audit entries for selected Vulnerability Response records.
    -   Fixed:
        -   Resolved a security issue in the vulnerability aggregation interface.
        -   Fixed an issue where reopening a resolved Remediation Task did not reopen its associated resolved Vulnerable items.
-   **Version 30.3.5 - April 2026 \(USEM\)**
    -   New:
        -   Added a Users and Groups list view to the Admin console in the Security Exposure Management workspace to centralize access and role management.
        -   Added support for configuring the unique identifier used for Tenable Compliance test results to prevent results from being overwritten when multiple tests share the same control identifier.
        -   Updated bulk deferral to validate that selected items are not already deferred and automatically exclude them from processing, preventing overlapping deferrals.
    -   Changed:
        -   Updated remediation tasks in the Security Exposure Management workspace to align one‑to‑one with findings, improving traceability and simplifying task management.
        -   Modularized system properties in the USEM workspace to simplify configuration and management.
        -   Updated the Advanced Settings page to display inline error notifications for easier issue identification.
        -   Updated auto‑close rules to process items in parallel, reducing the time required to close large volumes of items.
        -   Updated risk rollup calculations for Vulnerability Sources to align with other entity types for improved accuracy.
        -   Updated data ingestion to automatically pause during system migration, preventing data inconsistencies.
    -   Fixed:
        -   Fixed an issue where reopening a resolved remediation task did not reopen all associated resolved items.
        -   Fixed approval level records not displaying all approver field choices after upgrading to v30.
        -   Fixed remediation task state changes not propagating correctly when one or more related items were already closed.
        -   Fixed theOpened by field on remediation tasks not displaying the creating user when the task was initiated from the workspace.
        -   Fixed chart rendering and color‑coding issues in the Security Exposure Management workspace under the Japanese locale.
        -   Improved performance across background processes, including data ingestion, auto‑close evaluation, unified dashboard daily and weekly collection, and aggregated reporting.
        -   Fixed an issue where work note updates on configuration compliance test groups triggered excessive background jobs, causing processing delays.
-   **Version 2.16.1 - April 2026**
    -   New: Added support for configuring the unique identifier used for Tenable Compliance test results to prevent results from being overwritten when multiple tests share the same control identifier.
    -   Changed: Smart Assessment templates now support category-based role assignments and quick editing, giving administrators more flexibility when configuring assessment templates.
    -   Fixed:
        -   Fixed an issue where reopening a resolved remediation task did not reopen all associated resolved items, keeping task and item statuses in sync.
        -   Fixed theOpened by field on remediation tasks not displaying the creating user when the task was initiated from the workspace.
        -   Fixed vulnerable items not closing when associated detections were closed in instances where the close business rule was customized.
        -   Fixed vulnerable items remaining in a Deferred state after exception rule deletion by correctly clearing deferral-related fields.
        -   Improved performance of unified dashboard daily and weekly data collection jobs, reducing runtimes from hours to minutes.
-   **Version 2.15.0 - January 2026**

    Minor fixes for this release.

-   **Version 30.2.8 - January 2026 \(USEM\)**

    Minor fixes for this release.

-   **Version 2.14.5 - December 2025**
    -   New: Introduced a backend API for Cloud Accelerate integration to support cloud-based vulnerability assessment and risk factor analysis.
    -   Fixed: Updated theApply Auto-Close Rules background job to run as a single-threaded process. This improves reliability and prevents race conditions that previously occurred with partition-aware execution.
-   **Version 2.13.6 - October 2025**

    Fixed: Resolved an issue that caused an infinite loop when NQ conditions were used in the exception rule.

-   **Version 2.13.5 - September 2025**

    Fixed: Minor fixes for this release.

-   **Version 2.13.3 - August 2025**
    -   Changed: Added supporting components and a data model to enable configurable granularity of Configuration Test Results \(CTR\) in Configuration Compliance.
    -   Fixed: Resolved the ACL issue to allow the active field for all auto-close rules
-   **Version 2.12.5 - July 2025**

    Fixed: An access control \(ACL\) issue preventing updates to the Active field for Auto-Close rules in the user interface.

-   **Version 2.12.4 - June 2025**

    Fixed resubmission of Exception Rule on a pre-approved record.

-   **Version 2.12.3 - May 2025**
    -   Changed:
        -   Added new data components and support for manually reapplying CI lookup rules on DIs based on conditions for Discovered Items and Discovered Applications.
        -   Added new components to support Smart Assessment Engine related changes
-   **Version 2.11.3 - February 2025**

    New: Improvements to allow the manual creation of Remediation Tasks \(RTs\) for host vulnerable items \(VITs\), application vulnerable items \(AVITs\), container vulnerable items \(CVITs\), and test results \(TRs\) in the Vulnerability Manager and IT Remediation Workspaces.

-   **Version 2.10.0 - December 2024**

    New: Introduced improvements to the framework for supporting compensating controls.

-   **Version 2.9.3 - December 2024**

    Minor fixes for this release.

-   **Version 2.9.2 - November 2024**

    Fixed: Updated indicator conditions based on the newly added columns in the Test Results table.

-   **Version 2.8.2 - August 2024**

    New: Added capabilities in the common framework to support the evaluation of the risk scores, assignments, remediation target date, and remediation tasks for a set of selected vulnerable items, application vulnerable items, container vulnerable items or test results.

-   **Version 2.7.0 - June 2024**

    New: A new common framework has been added to support the Exclusion Rules feature.

-   **Version 2.6.4 - May 2024**

    New: Added new components to support the bulk edit feature for application vulnerable items, and container vulnerable items in the Vulnerability Manager Workspace.

-   **Version 2.5.3 - March 2024**

    Fixed: The SLA widgets in the Vulnerability Response Unified Dashboard now considers only the active vulnerable items \(VIs\).

-   **Version 2.5.1 - February 2024**

    Minor changes to support Cybersecurity Executive Dashboard.

-   **Version 2.4.2 - January 2024**

    New: Created and Updated the PA indicators to support the benchmarking metrics.

-   **Version 2.4.0 - December 2023**

    New: Added Exploit Prediction Scoring System \(EPSS\) widgets in the Unified Vulnerability Response Dashboard.

-   **Version 2.2.3 - December 2023**
    -   Fixed:
        -   Updated the MTTR widget indicator formulae.
        -   Fixed missing references for indicators related to the Unified Vulnerability Response Dashboard.
-   **Version 2.2.2 - November 2023**

    New: Aggregated report: The Vulnerability Response users can create reports using Aggregated Reports Framework which is provided in Vulnerability Response Common. This framework can be used for rebuilding some of the slow running standard report.

-   **Version 2.0.4 - August 2023 \(Vancouver\)**

    Vulnerability Response Common is a framework that provides the necessary functionality to support Vulnerability Response applications like Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response and Configuration Compliance.

    Added a Unified Vulnerability Response Dashboard, which is accessible from the workspaces. This is a centralized aggregated dashboard that provides visibility from multiple vulnerability scanners and security tools to provide a comprehensive view of an organization's vulnerabilities and risks.


