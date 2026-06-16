---
title: GRC: Risk Management release notes
description: Version history for the GRC: Risk Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-risk-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Risk Management release notes

Version history for the GRC: Risk Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.3 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACL's
            -   Consistent Access Control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless Upgrade Experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-Upgrade Review for Customized ACLs — If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
        -   Enabled Audit entries support for Risk and related records.
    -   Changed: Email notification links for Risk Management now redirect users to the appropriate workspace based on their access permissions.
    -   Fixed:
        -   Risk response task due date validation now prevents users from entering past-dated entries.
        -   Delegated users can now review, approve, and reject action items on response sub-tasks.
        -   The "Closed At" field now populates correctly when a closed response task is reopened and closed again.
        -   Users can add controls to risks without being blocked by security constraints.
        -   Deactivating a risk framework now displays the correct count of affected risks and risk statements.
-   **Version 22.0.2 - March 2026**
    -   New: With Control Objective workflow in place, risk objects now consume only published Control Objective versions, improving consistency and governance.
    -   Changed: Updated theRisk Statement,Risk Name, andDescription fields to use String instead of Translated Text, ensuring consistent behavior when records are modified by users working in different languages. See the KB article for details.
-   **Version 21.1.2 - December 2025 \(Zurich\)**
    -   New:
        -   Introduced a feature in Entity-Based Access \(EBA\) that allows lifecycle users to access records. You can now configure any user or user group field on the record to provide additional access beyond what is defined in the EBA configuration.
        -   Introduced an 'Active flag' in the GRC Choice table; updates to these flags are now reflected in the Risk Management application.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Fixed an issue where assignees could not edit comments after an action item was rejected and returned to ‘Work in Progress’.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.2 - August 2025**
    -   New: Entity based access is now automatically applied at the time of record insertion. Previously, users had to manually update records using the Bulk Update utility. This change streamlines access management by eliminating the need for post-insertion updates.
    -   Fixed:
        -   Populated the "Run As User field" with Admin user in default Performance Analytics Data Collector jobs, resolving the issue where jobs were not executing automatically after application installation.
        -   Strengthened security by resolving identified issues.
        -       -   Removed: Removed deprecated actions from Risk Response tasks to streamline the user experience and reduce confusion.
-   **Version 20.1.1 - May 2025**
    -   New: Introduced entity-based access control for improved security on the following Risk Management tables: Risk, Risk Response Task, and Action Item.
    -   Changed: Updated field types for name and description on the Risk Statement and Risk tables from plain text to translatable text to support localization.
    -   Fixed:
    -   -   Improved performance on Risk Workspace home pages by adding indexes to the Risk table.
-   Resolved an issue where role mappings appeared without the Business User Lite application; mappings now only show when the app is installed.
-   Fixed an issue where the Assigned To field on the Action Item table became mandatory unexpectedly after sending it to the assignee.
-   Addressed a limitation where only 15 assessments were shown on the My GRC Assessments page in the Employee Center.
-   Fixed an issue where appetite values from the parent Risk Statement were not auto-populated before saving.
-   **Version 20.0.0 - February 2025**
    -   Changed: Inline dashboards are now set to read-only, resolving customization issues encountered during upgrades.
    -   Fixed: Addressed multiple issues related to Risk Response tasks:
    -   -   The Business User Lite role can now be reassigned to Risk Response Action Items.
-   The Business User Lite role can now view comments on Risk Response tasks.
-   Fixed an issue where the state of Risk Acceptance tasks did not update from "Accepted" to "Closed" in multi-language instances.
-   Resolved an issue preventing the rejection of Risk Response tasks when comments were not provided.
-   Risk Response tasks are now canceled correctly when the strategy on the risk record is changed to "None."
-   **Version 19.1.1 - November 2024**
    -   Fixed:
        -   Security issues
        -   Resolved an issue related to confidentiality
        -   Resolved an issue related to notification trigger when the risk state changes to Assess
    -   Changed: Disabled sandbox access for client-callable script includes
-   **Version 19.0.3 - August 2024**
    -   Change:
        -   Consistent workflow across all the Risk response tasks \(Draft Work in Progress Awaiting Approval Closed\)
        -   Integration of risk response task approval withGRC: Approver Configurator.
            -   Users will be able to configure multiple levels of approvals using approval configurations. By default, the risk owner will be the approver on all tasks. If the approver rejects the task, it will no longer be canceled and will move to Work in Progress.
    -   New:
        -   Elevate the current risk response strategy as a plan of action with granular tasks
            -   For risk mitigation, risk transfer, and risk avoidance tasks, there will be an option for detailed action planning with the ability to create multiple strategies using one or more action items within each risk response task.
            -   Each action item will have its own independent workflow: Draft Assigned Work in Progress Review Closed.
    -   Fixed:
        -   Updated to show a valid acceptance end date in the email sent to the user when the acceptance end date is reached for a risk.
        -   Business user lite is granted read access to the sn\_risk\_m2m\_risk\_mitigation\_control table
        -   Performance improvement to select the parent on the risk statement.
    -   Removed: Performance Analytics - GRC: Risk Management application is deprecated and has been removed as a dependency for the GRC: Risk management application.
-   **Version 18.1.2 - June 2024**
    -   New:
        -   Domain separation improvements
        -   Migration of Classic dashboards to Next Experience dashboards
-   **Version 18.0.2 - February 2024**
    -   Fixed:
        -   Internationalisation/Localisation enhancements
        -   Business user lite issues when accessing the risk response
        -   Risk heatmap theming issues
-   **Version 17.0.0 - August 2023**
    -   New:
        -   Edit Risk response task as a IRM Lite operator.
        -   Changes to allow only a single selection of the risk response.
    -   Fixed:
        -   Runtime access tracking field was getting set to enforce on application upgrade.
        -   Incorrect impact score for inherent impact=3.
-   **Version 16.0.3 - February 2023**
    -   New:
        -   Issue architectural changes to support adding risk statements to existing issues
        -   Common controls support
    -   Fixed:
        -   Localization support
        -   Retiring risk when an entity is deactivated
        -   ALE rollup issues
-   **Version 15.1.1 - December 2022**

    Fixed: Reduced application installation size

-   **Version 15.0.3 - November 2022**

    Fixed: Added GRC: Workbench as a dependency and will be installed and upgraded automatically with the Risk Management application.

-   **Version 15.0.2 - August 2022**
    -   Fixed:
        -   Risk reader will be having the ara\_assessor role
        -   Risk reader is not going to have sn\_grc.business\_user in its inherited roles hierarchy
        -   Risk.Name is read-only when creating Risk manually from Risk Statement's related list
        -   Residual score not populating - Intermittent Issue.
        -   Risk reader is not going to contain grc metric user role. Reader role should not contain any user/write role in system.
        -   When we add entity type in the Risk Statement, then Risks are not getting created in the appropriate domain but are created in Global
-   **Version 14.1.1 - March 2022**
    -   New:
        -   Using the GRC: Metrics application to enable threshold-based KRI monitoring.
        -   Support for record-level confidentiality on Risk events.
    -   Fixed: Replaced SNC Internal access with GRC Business User or appropriate GRC application role.
-   **Version 13.0.1 - September 2021**
    -   Fixed:
        -   Security fixes
        -   Localization fixes
-   **Version 12.0.1 - March 2021**

    New: Functional changes to Risk avoidance task, risk transfer task

-   **Version 11.0.2 - October 2020**
    -   New:
        -   Risks can now be created without the need for a mandatory association to a risk statement. These can be referred to as adhoc risks or orphan risks
        -   Risk statements at any level could be associated with orphan risk
-   **Version 10.1.0 - June 2020**

    New: New integration of Advanced Risk Assessments with standard Risks

-   **Version 10.0.0 - March 2020**

    New: Support for the new Advanced Risk Assessment feature

-   **Version 9.0.1 - November 2019**

    This application was updated in the New York release.


