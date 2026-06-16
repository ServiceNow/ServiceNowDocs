---
title: GRC: Continuous Authorization and Monitoring release notes
description: Version history for the GRC: Continuous Authorization and Monitoring on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-continuous-authorization-monitor.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Continuous Authorization and Monitoring release notes

Version history for the GRC: Continuous Authorization and Monitoring on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.3 - June 2026 \(Australia\)**
    -   Changed:
        -   This release includes the following changes:
            -   CAM email notifications now include references to records in the workspace.
    -   Fixed:
        -   This release resolves the following issues:
            -   Orphaned system elements not removed when an authorization boundary is deleted.
            -   CIA impact value columns not displaying in the Information Types popup.
            -   SSP HTML template reports displaying incorrect data for Rev 5 Authorization Packages.
-   **Version 22.0.2 - March 2026**
    -   Fixes:
        -   Security bugs.
        -   Resolved the visibility of Vulnerable item widget even without the security plugin in the Overview tab.
        -   Resolved Access Restricted error for the Packages Pending Approval widget in CAM Dashboard and AO Dashboard.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New:
        -   Relationships between boundaries can now be created. Hierarchy of boundaries is now supported.
        -   Adding a "Dynamic Filter" checkbox for boundary filters that updates system elements according to filter conditions when enabled.
        -   Automatic update of boundary status to Operational when a package moves to the Monitor state.
        -   Transition of Boundary status to Reauthorize as the Package Authorization date approaches.
    -   Changed:
        -   Inactive authorization packages cannot be moved to next steps.
        -   ISSO users can now edit implementation statement field of the Authorisation package’s controls.
    -   Fixed:
        -   Some of the missing information types have been updated with appropriate sub-categories.
        -   SSP Word Template is updated to include Rev5 controls where ever applicable.
        -   The applies\_to field of the Entity that is linked to the Authorisation boundary is now populated with the same authorization boundary itself.
        -   Fixed security defects.
    -   Removed: The sam\_user role has been successfully removed from the CAM Reader role.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Enhanced security on authorization boundary, authorization package, acceptance task, milestone task, information type, system element tables by introducing range queries.
        -   ISSM can now add information types in an authorization package.
    -   Fixed:
        -   Fixed localization issues in labels and messages across the CAM flow
        -   Reference of a control objective is now unique in a base line control. Duplicate control objectives cannot be added manually to baseline controls
        -   A control once marked as common, cannot be inherited further.
        -   Fixed security bugs.
-   **Version 20.2.1 - July 2025**

    Fixed: Resolved known bugs impacting core functionality and user experience.

-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.0 - May 2025**

    Fixed: Security and minor bug fixes.

-   **Version 20.0.3 - February 2025**

    Changed: Add button in Baseline control related list now shows all control objectives instead of NIST rev5/rev4 control objectives.

-   **Version 19.1.1 - November 2024**
    -   Changed: Security fixes.
    -   Fixed:
        -   Impact of NIST R5 control objectives are updated as per NIST standards.
        -   Implementation field made editable in Review state of the Control.
        -   System Owner can mark the Baseline controls as Not Applicable.
        -   Group attestations can be performed from task page.
-   **Version 19.0.3 - August 2024**
    -   New:
        -   Add related control objectives.
        -   Add attachments to assessment procedures and document notes.
    -   Changed:
        -   The Auth Reader, Executive Reader, and Authorization Official roles are considered Lite Operators if the Employee user plugin is installed.
        -   The Audit Reader role is added to Auth Reader.
    -   Removed: The Audit User role is removed from the Auth Reader role.
-   **Version 18.1.2 - June 2024**

    Changed: CAM dashboards are migrated to the Next Experience UI Framework.

-   **Version 18.0.1 - February 2024**
    -   New:
        -   Control Requirements: Allows you to break control into granular requirements and attest them individually \(auto-generated based on control objective requirements\).
        -   Hybrid Controls: Ability to partially inherit requirements from a common control provider while self-implementing the rest of the requirements.
        -   Assessment Procedures: Test the control more efficiently by determining the effectiveness of each assessment procedure, which would further impact the effectiveness of the control test.
        -   Out-of-box content: Control requirements data set and assessment procedures data set for NIST 800-53 rev 5 controls will be shipped out of the box.
    -   Changed:
        -   Generating assessment procedure plans for a test plan.
        -   Determine the effectiveness of a control test.
        -   The Implementation statement is now mandatory before moving the control out to the attest state.
        -   The Discussion field is introduced in the Control objective and Control forms.
        -   Assigning a Security Control Assessor is now mandatory before moving the Package to the assess state.
    -   Fixed: When user clicks Back to previous step, the changes and configurations in current step are reverted.
-   **Version 17.0.1 - August 2023**
    -   Changed:
        -   Authorization package workflow
        -   Access controls on tables extending planned task
    -   Fixed:
        -   When new engagements are created for a authorization package, issues created on the engagement are not coming up on package.
        -   When authorization package is moved from select to implement state, audit history is populated with duplicate messages.
-   **Version 16.0.2 - February 2023**
    -   Changed: Update the new mappings between policy and control objectives provided by NIST RMF.
    -   Fixed:
        -   Access controls for viewing reports.
        -   CAM users cannot add notes and comments in Authorized Package form.
-   **Version 15.0.2 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.0 - August 2022**

    Fixed: Fixed typo in ACL that caused script errors.

-   **Version 14.1.0**
    -   New: Added Rev. 5 control objectives data
    -   Changed:
        -   Update authorization package to allows users to define which version to use \(Rev. 4 or Rev. 5\).
        -   Update control objectives to create parent-child relationships between control objectives.
        -   Filter the controls based on the version field.
        -   Ability to go back to previous steps in the authorization package.
-   **Version 12.0.3 - June 2021**

    Fixed: A recursive loop in a script include triggered by demo data in the GRC: Policy and Compliance Management application caused a stack overflow error.

-   **Version 12.0.0 - March 2021**
    -   Fixed:
        -   Redundant elements added with filters
        -   The count of elements doesn't update immediately
        -   SSP report in Authorize and Monitor Steps by System User / Information Owner role generated multiple copies of the report despite overwrite the selection
        -   CAM users cannot add notes and comments in the Authorized Package form
        -   Cleaned up labels and role-related tasks
        -   Fixed performance issues
-   **Version 11.0.1 - October 2020**

    New: New application to manage NIST Risk Management Framework \(RMF\) &amp; Cybersecurity Framework \(CSF\), Defense Federal Acquisition Regulation Supplement/NIST 800-171 \(DFARS\), FedRamp, ISO 31000, and high maturity standards.


