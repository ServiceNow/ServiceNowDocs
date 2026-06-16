---
title: Parallel Review and Feedback release notes
description: Version history for the GRC Parallel Review and Feedback application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-parallel-review-feedback.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Parallel Review and Feedback release notes

Version history for the GRC Parallel Review and Feedback application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Standardized query range ACLs
            -   Consistent Access Control — All tables now include standardized query range security ACL's. Users with appropriate read access can query records consistently across the platform.
            -   Seamless Upgrade Experience — New Query ACL rules install automatically during upgrade with no administrator action required. Automated upgrade scripts handle the full transition, including detection and processing of any previously customized ACLs, so existing processes continue to work without interruption.
            -   Post-Upgrade Review for Customized ACLs — If your instance includes administrator-modified Query range ACLs, we recommend reviewing those records after upgrade to confirm they align with your intended access policy.
-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed: Resolved a security vulnerability that previously allowed unintended edits to read-only fields.

-   **Version 20.0.0 - February 2025**

    Fixed an issue where the Discuss button appeared incorrectly when the Polaris theme was disabled.

-   **Version 19.1.1 - November 2024**
    -   Fixed:
        -   Security fixes
        -   Fixed a concurrency issue that prevented an issue record from being created when closing feedback
    -   Changed: Disabled sandbox access for client-callable script includes
-   **Version 19.0.0 - August 2024**
    -   New: Define a specific group as the respondent type in the Feedback Integration Configuration form when the target record doesn't have a user or group.
    -   Fixed:
        -   The "Close all open items to send feedback for review" message appeared multiple times to the respondent, depending on the number of clicks on the change history.
        -   The feedback closing actions section was displayed next to the Activity section for non-ServiceNow records.
        -   Two email notifications were received when the feedback was completed by creating an issue.
        -   The feedback name was displayed in the breadcrumb when the change history was accessed from the record's side panel.
-   **Version 18.0.0 - February 2024**

    All organizations want the first line to manage their risks and compliance. This implies the second line does not want to actively participate in the workflow and becomes a bottleneck in the workflow to review and sign off. However, it is still important that the second line reviews a sample of these transactions, ensures they comply with the defined policy and standard operating procedures related to these workflows, and makes recommendations on areas of improvement. The parallel review and feedback application allows users to select any record in the Risk products for raising a review.


