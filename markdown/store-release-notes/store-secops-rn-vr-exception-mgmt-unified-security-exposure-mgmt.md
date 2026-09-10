---
title: Exception Management for Unified Security Exposure Management release notes
description: Version history for the ServiceNow Exception Management for Unified Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-exception-mgmt-unified-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Exception Management for Unified Security Exposure Management release notes

Version history for the ServiceNow® Exception Management for Unified Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.7.5 - September 2026 \(USEM\)**
    -   Fixed:
        -   Missing approver levels after migrating to Unified Security Exposure Management \(USEM\).
        -   A security issue that might allow unauthorized access to exception settings.
        -   Cursor jumping in the script editor within USEM Workspace.
        -   Resolved packaging and translation issues in Exception Management for Security Exposure Management.
        -   Issues with change approval email notifications after migrating to USEM, including duplicate subject lines, an incorrect recipient greeting, and the requester's name displaying as an internal ID.
        -   Approvers receive email notifications if an exception request was unassigned.
        -   Editable Change Approval fields from the list view are now read-only as intended.
        -   After a policy exception is cancelled the source record's state is reverted.
        -   Expiring an exception or false-positive request doesn't create a duplicate remediation task.
        -   Fixed several hardcoded text strings in Exception Management so they can be properly translated.
        -   A performance issue where checking approver access to exception requests loads an excessive number of records, causing slowdowns.
        -   The Defer Until field's inconsistent behavior between the Security Exposure Management workspace and the native UI.
        -   The GRC exception flow when a policy exception is cancelled or closed.
        -   A security issue related to query handling in risk reduction eligibility checks.
        -   The deferral count on vulnerable items no longer intermittently fails to update.
        -   A security issue that might allow unauthorized access to record counts through a data broker.
        -   A security issue with user-controlled field names in a data broker.
        -   The Update button is no longer disabled when the requested date is within the allowed maximum duration.
        -   A vulnerable item opens as expected if the state-change approval flow fails.
        -   A security issue with read-only access that permitted modifications to exception change approval records.
        -   A security issue where request approvals are processed without verifying record assignment.
        -   Risk Reduction requests no longer get stuck in 'Draft' state when the questionnaire feature is enabled.
        -   Required-field validation errors are now properly identified for screen readers, and the Request Exception dialog now has an accessible title.
        -   Exception rules now correctly handle failure scenarios for new findings that don't yet have a remediation task configured.
    -   New: Exception rule handling for new findings without remediation tasks. The system now processes new findings that lack remediation tasks when exception rules fail, ensuring accurate workflow management.
    -   Changed:
        -   Bulk edit requests with questionnaires now progress correctly. When questionnaires are enabled, risk reduction requests initiated via bulk edit no longer get stuck in Draft state; mandatory fields are enforced through the questionnaire.
        -   Request exception dialog now displays a title. The request exception dialog includes a title, improving accessibility and compliance.
        -   Error handling for blank required fields in Security Exposure Management. The system now identifies errors when required fields are left blank in Security Exposure Management, ensuring users are notified of missing information.
    -   Fixed:
        -   Cursor jumping in the script editor within USEM Workspace has been resolved.
        -   Inconsistencies identified by customers after migrating to USEM have been addressed.
        -   The source record state now reverts correctly if a policy exception is cancelled before approval. When a policy exception is cancelled before approval, the associated vulnerable item returns to its previous state.
        -   Duplicate remediation tasks are no longer created when an exception or false positive expires.
        -   Large result set handling for approver access checks in exception workflows has been optimized, preventing performance issues.
        -   The "Defer until" field in Request Exception now behaves consistently across Security Exposure Management Workspace and Native UI.
        -   Approver levels missing after USEM migration have been restored.
        -   VIT deferral count updates reliably and no longer fails intermittently.
        -   Vulnerability state change approval flow errors now reopen the VIT from the in\_review state as expected.
-   **Version 30.6.6 - August 2026 \(USEM\)**
    -   Fixed:
        -   Expired False Positives or Exceptions reopen the original remediation task as expected instead of creating a duplicate remediation task.
        -   Canceling a policy exception reverts the associated vulnerable item back to its original state as expected.
        -   Fixed issues in the GRC exception flow so manually reopening a vulnerable item automatically cancels the related policy exception, and canceling an approved exception returns the item to an open state as expected.
        -   False Positive requests are no longer automatically rejected and the Reopen action works for users configured with a non-English language.
        -   Enhancements to the compensating controls \(Mitigating Control in Place\) workflow allows the risk rating to be increased, not just reduced.
        -   Custom exception rule scripts configured in feature settings no longer fail due to a platform scoped-script evaluation restriction.
-   **Version 30.6.1 - July 2026 \(USEM\)**
    -   New:
        -   Added bulk edit support for Risk modification requests, enabling users to evaluate and process multiple vulnerable items at once.
        -   Added Smart Assessment support to the Risk Reduction option in Request Exception workflows.
    -   Changed:
        -   Updated security exception form configuration, simplifying maintenance and enabling faster future updates.
        -   Updated access controls to correctly display the Request Exception action for authorized users.
        -   Enhanced application to align with security directives.
    -   Fixed:
        -   Fixed an issue where exception request types in multi-language environments caused incorrect behavior in False Positive auto-rejection and Deferred item reopen actions.
        -   Fixed a layout overlap on the Approvals page at narrow viewport widths.
        -   Fixed remediation task deferral extension workflow issues in Application Vulnerability Response and Container Vulnerability Response.
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

**Parent Topic:**[ServiceNow Store - Vulnerability Response version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

