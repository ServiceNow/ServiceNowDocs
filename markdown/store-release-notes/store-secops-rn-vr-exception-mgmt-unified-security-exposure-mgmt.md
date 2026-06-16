---
title: Exception Management for Unified Security Exposure Management release notes
description: Version history for the ServiceNow Exception Management for Unified Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-exception-mgmt-unified-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Exception Management for Unified Security Exposure Management release notes

Version history for the ServiceNow® Exception Management for Unified Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.5.0 - June 2026 \(USEM\)**
    -   New: Bulk edit now supports Risk Reduction, letting users evaluate and process risk reduction requests across multiple vulnerable items at once. - The Risk Reduction option via the Request Exception option now supports Smart Assessment.
    -   Changed:
        -   Migrated security exception form read-only configuration to the standard product codebase, improving maintainability and simplifying future updates.
        -   Updated access controls so the Request Exception action is correctly displayed for authorized users.
    -   Fixed: Application Vulnerability Response and Container Vulnerability Response remediation task deferral-extension workflow issues.
-   **Version 30.4.1 - June 2026**
    -   New: Added Smart Assessment versioning support for Exception templates to enable safer and more controlled template upgrades on customer instances.
    -   Changed:
        -   Migrated security exception form read-only configuration to the standard product codebase, improving maintainability and simplifying future updates.
        -   Updated access controls so the Request Exception action is correctly displayed for authorized users.
        -   Enhancements to support template-related record updates. You might see improved performance for record updating.
    -   Fixed:
        -   Application Vulnerability Response and Container Vulnerability Response remediation task deferral-extension workflow issues.
        -   Issues that were identified during unit-test coverage improvements.
-   **Version 30.3.4 - May 2026**
    -   Fixed:
        -   An issue where conditional questionnaires failed to trigger on exception submission after upgrading to Unified Security Exposure Management \(USEM\), affecting both pre-upgrade and newly created questionnaire configurations.
        -   The out-of-memory error and platform node restart caused by the scheduled job responsible for refreshing Change Approval fields. The job now completes successfully within memory limits.
        -   An issue where cancellation and deletion operations on exception rules did not execute as expected.
-   **Version 30.3.2 - April 2026**
    -   Fixed:
        -   An issue where vulnerable items were not transitioning to a closed state after their associated detections were closed, because the exception rule scheduled job was not checking for the closed state on finding records.
        -   A performance degradation in USEM ingestion caused by redundant repeated queries to the findings configuration table during exception processing. A static method has been implemented for invocation that eliminates the unnecessary per-instance overhead.
        -   The bulk approve and reject modal incorrectly opening for non-eligible records, preventing approvers from inadvertently acting on records that do not qualify for bulk processing. List view layout enhancements might improve usability.
        -   Resolved VIT records incorrectly remaining in a "Deferred" state after an Exception Rule was deleted, caused by deferral fields not being cleared properly during final state transitions.
        -   Fixed a security vulnerability where the "Design new questionnaire" UI action could be accessed by unauthorized users due to an ACL bypass, ensuring only permitted users can access questionnaire design functionality.
        -   Resolved multiple exception management issues in the Risk Reduction and Questionnaire approval flows, including incorrect state transitions and edge cases in approval handling.
    -   Changed:
        -   Introduced Bulk Approve and Reject capability for approvers, enabling them to process multiple exception requests simultaneously from a single list view, which can help with significantly reducing manual effort for high-volume approval workflows.
        -   Added new KPI tiles to the Exception Management dashboard for Expiring Exceptions, Exception Extensions, and Repeated Rejections, giving approvers and managers additional visibility into exception health and lifecycle trends.
        -   Exception Rule configurations can now be added to update sets, allowing administrators to capture and promote exception rule changes across environments as part of standard change management processes.
        -   Improved the Approval UI with clickable summary cards, providing a more intuitive navigation experience for approvers reviewing and actioning exception requests.
        -   Added support for category\_roles in Smart Assessments and enabled quick editing of assessment templates, improving configurability of assessment-driven exception workflows.
        -   Removed unnecessary UI action buttons \(Resolve and Close\) from the new AVIT creation form, preventing user confusion and unintended actions on records that have not yet been fully saved.
-   **Version 30.2.1 - January 2026**
    -   **Note:** This app version is intended for Unified Security Exposure Management \(USEM\), a significant architectural upgrade to the Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a safe and successful upgrade. If you do not intend to upgrade to USEM, please select a version below 30.x when installing or upgrading.

    -   Exception Management enables organizations to efficiently handle and document vulnerability exceptions. It provides a controlled process for requesting, reviewing, and approving exceptions to vulnerable findings, ensuring transparency and compliance. By automating workflows and capturing exception justifications, it helps reduce operational bottlenecks while maintaining risk visibility and audit readiness.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

