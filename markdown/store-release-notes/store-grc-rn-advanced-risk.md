---
title: GRC: Advanced Risk release notes
description: Version history for the GRC: Advanced Risk on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-advanced-risk.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 17
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Advanced Risk release notes

Version history for the GRC: Advanced Risk on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Standardized Query Range ACLs: All tables now include standardized query range ACLs, ensuring authenticated users with read permissions can reliably query records. New ACL rules install automatically during upgrade. Automated scripts handle detection and processing of any previously customized ACLs. Review customized query range ACLs after upgrade to confirm alignment with your access policy.
        -   Not Applicable Flag Configuration: A configuration option in Risk Assessment Methodology allows hiding the "Not Applicable" flag in Risk Assessments.
        -   Smart Assessment Template Versioning: Risk Identification now supports template versioning — modify existing templates by creating new versions instead of building from scratch. The latest published version is always used when creating assessments.
        -   Smart Assessment Template Versioning: Risk Identification now supports template versioning — modify existing templates by creating new versions instead of building from scratch. The latest published version is always used when creating assessments.
        -   Audit Entries for Risk Assessment Projects: Risk Assessment Projects now support audit entries for tracking changes and activity history.
        -   Worst Case Aggregation: A new rollup method in Risk Assessment Methodology that derives all aggregated scores from the single risk with the highest residual, ensuring rollup results reflect a real risk scenario rather than a composite across multiple risks.
    -   Changed:
        -   Email notification links for Advanced Risk records now redirect users to the appropriate workspace based on their access permissions.
        -   Risk Event administrators now have expanded control over the entire risk event workflow, beyond reopening risk events.
    -   Fixed:
        -   Currency locale is now respected when Risk scores roll up to Risk Statements.
        -   Non-breaking spaces in Guidance Text HTML no longer cause rendering issues in non-English languages.
        -   Risk Assessment Projects can no longer be submitted multiple times on slow networks.
        -   Initiation date can no longer be set to a past date in the Risk Assessment scheduler workflow.
        -   Smart assessment creation now works correctly for templates with a large number of questions.
        -   The Next button now saves values correctly in the Risk Assessment Project stakeholder section.
        -   Scheduler frequency no longer resets to default after request initiation.
        -   Notifications are now triggered for assessors when assessments are generated outside the Risk Assessment scope.
        -   Profile class is no longer overwritten when you customize the record.
        -   Original Assessor field now populates correctly after reassignment.
        -   Assessment ratings display accurately for scores with three decimal places.
        -   Duplicate numbering on out-of-box Risk Assessment Methodology records has been resolved.
        -   When multiple methodologies are available, the selection popup now displays all options instead of defaulting to one.
        -   Last Assessment Date now shows the assessment end date instead of the system updated date.
        -   Approval and rejection comments are now copied to the approval record for improved traceability.
-   **Version 22.0.3 - March 2026**
    -   New:
        -   Enhanced automation and scalability for Risk Event assignments by enabling dynamic user and stakeholder‑based assignments. You can now assign risk event owners, issues, and approvals using entity user fields or entity stakeholder personas, with assignments automatically resolved to the appropriate users or groups.
        -   With Control Objective workflow in place, risk objects now consume only published Control Objective versions, improving consistency and governance.
    -   Changed: Converted theName andDescription fields of Risk assessment project from Translated text type to String to address inconsistencies that occurred when users working in different languages modified the same record. For detailed information, please refer to this KBarticle.
    -   Fixed:
        -   Risk Assessment
            -   Improved risk assessment reliability by addressing issues related to methodology retirement impacting risk scores, qualitative rating precision, initiation date validation, and reassessment scope persistence.
            -   Enhanced the risk assessment workflow by fixing localization issues, incorrect form loading during issue creation, and validation handling when saving Risk Response Tasks.
        -   Smart Assessments &amp; Notifications
            -   Improved Smart Assessment usability and notifications by fixing issues with email‑based assessment access, reminder emails being sent for completed assessments, missing rejection reasons in non‑English languages, and unintended HTML formatting in notification content.
-   **Version 21.1.2 - December 2025 \(Zurich\)**
    -   New:
        -   Introduced Reporting Views for Advanced Risk Assessment to simplify report and dashboard creation. This feature consolidates risk factors, controls, issues, and responses into a single view, making reporting easier for non-technical users.
        -   Reporting Views are automatically generated when a Risk Assessment Methodology is published and these views can be used to create custom reports.
        -   Automatic creation of Reporting Views is not supported on Xanadu. For instructions on creating them manually, refer to KB2547071.
        -   Introduced a feature in Entity-Based Access \(EBA\) that allows lifecycle users to access records. You can now configure any user or user group field on the record to provide additional access beyond what is defined in the EBA configuration.
        -   Introduced an 'Active' flag in the GRC Choice table, with updates to these flags now reflected in the Advanced risk application.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unauthorized edits to read-only fields.
        -   Replaced hard-coded administrator role dependencies with granular roles to improve security and align with least privilege principles.
        -   Resolved an issue where the message“The residual score cannot be greater than the inherent score” was not displayed when using the 'Request for Approval' action in the Classic UI.
        -   Resolved an issue where sending final reminders for assessments linked to Risk Assessment Methodologies \(RAMs\) in Draft or Retire state could fail if the due date had passed.
        -   Resolved a problem where updates to risk color styles reverted to default values after an upgrade. Your customizations are now preserved.
        -   Resolved an issue where Risk Identification records remained in the Information Gathering state after completing the initial risk assessment. The state now correctly moves to Review as expected.
        -   The 'View Responses' action in the Risk Identification flow now works for users with the sn\_risk.reader role. Previously, this action was not functioning for these users.
        -   The 'Perform Inherent Assessment' button is now displayed only in the Review state of the Risk Identification workflow when using Smart Assessment integration. Previously, it was incorrectly visible in the Information Gathering state.
        -   Fixed role-based access issues for reopening risk events: only users with sn\_risk\_advanced.risk\_event\_admin can reopen closed events, and users with sn\_risk.manager role can now reopen rejected events as intended.
        -   The Group Factor Comment field in Risk Assessment now correctly retains comment text when navigating between pages. Previously, comments were lost when moving forward and then returning to a previous page. This behavior has been corrected, and data entered in the comment field will persist as expected.
        -   Currency values in the Risk Assessment workspace now display with proper delimiters. Previously, currency factors appeared without separators, making values harder to read.
        -   Deleting a risk associated with a risk assessment no longer creates an empty record in the sn\_risk\_risk table. Previously, removing a linked risk would generate a new entry with blank values.
        -   The 'Cancel Assessment' action in Risk record now works as intended. Previously, users with the sn\_risk.user role could see the option but clicking it had no effect. The functionality has been corrected so that only users with the sn\_risk.manager role can cancel a risk assessment, or sn\_risk.user can cancel it only if they are the entity owner.
        -   Non-admin assessors can now view updates to the qualitative score label in the Risk Assessment component. Previously, changes to the label were not visible to users without admin privileges.
        -   The Next Scheduled Date for Risk Assessments is now calculated accurately. Previously, it could inherit a future date from the previous assessment based on the scheduled job run time. This issue has been resolved.
-   **Version 21.0.3 - September 2025**
    -   New: Risk Event Summarization is available in the Native UI. This functionality is enabled when Now Assist for IRM is installed.
    -   Changed: The Summary section on Risk Event was renamed to Impact to better reflect its content.
-   **Version 21.0.2 - August 2025**
    -   New:
        -   Project Risk Assessment Grid:
            -   Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.
        -   Entity Based Access Enhancement:
            -   EBA is now automatically applied at the time of record insertion. Previously, users had to manually update records using the Bulk Update utility. This change streamlines access management by eliminating the need for post-insertion updates.
    -   Fixed:
        -   Translation inconsistencies were resolved.
        -   Load times on the Risk Assessment Home page are improved, especially for customers with large CMDB data volumes.
        -   Approvers list visibility is now consistent between Native and Workspace UIs on Risk Response tasks.
        -   The Approved on date field remains stable and no longer changes on every update when a Risk Assessment is in Monitor state.
        -   Business users can now view all Risk Events sent for approval and can create Risk Events of all types, not just Potential.
        -   Returning a Risk to Draft no longer incorrectly moves it to Monitor state when an open Risk Response task exists.
        -   Customizations to Metadata records such as, Risk Assessment Methodology, and Factors are preserved during upgrades.
        -   Redundant activity logs on Risk Identification records were removed.
        -   Strengthened security through resolution of identified issues.
-   **Version 20.2.1 - July 2025**

    Fixed: Enhanced security by implementing Query range ACLs across multiple tables.

-   **Version 20.2.0 - June 2025**

    New: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.1 - May 2025**
    -   New:
        -   Implemented Entity-Based Access Control to strengthen security across key Advanced Risk Management tables: Risk Assessment, Risk Identification, Risk Assessment Project, and Risk Event.
        -   Delegated users can approve Risk Events, adding flexibility to the approval process.
    -   Changed:
    -   -   Changed the Description field type in the Factor table from plain text to translatable text to support localization and multi-language capabilities.
-   Replaced scripted ACLs with the Security Attributes feature to streamline and modernize access control.
-   The Date of Impact field in the Risk Event entry will now compare with the Date of Occurrence instead of the Date of Discovery for improved data accuracy.
    -   Fixed:
    -   -   Improved performance on Risk Workspace home pages by adding indexes to the Qualitative Rating Criteria table.
-   Enhanced security by reviewing and updating ACLs across multiple tables.
-   Resolved an issue where some modules were being deactivated when customized, due to a licensing bug.
-   Fixed a problem where there was an issue in creation of Risk Event Entry for Non-Financial Risk Events.
-   Corrected a display issue where the Due Date on Risk Response task cards showed one day earlier than the selected date.
-   Addressed a mismatch in rollup values between list and form views when single currency mode is enabled.
-   Fixed an issue where the Reject button was missing on Risk Events in the Awaiting Approval state.
-   **Version 20.0.1 - February 2025**
    -   New:
        -   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
        -   Copy risk responses from a previous risk assessment during reassessment of a risk assessment project.
        -   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
        -   Remove risks from a risk assessment project during the assessment to streamline the focus on relevant risks.
        -   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.
    -   Changed:
        -   Configure risk color styles for the Next Experience
            -   Define and preview colors for the risk and advanced risk components in the Next Experience through a configurable system rather than having to use hex codes. The transition has been made from a hex code color management system to a configurable system that supports the highlighted value component colors. This feature addresses theming and accessibility issues. You can define the color and variant, and preview them using the Next Experience color styles tab on the Risk color style form.
            -   The update ensures consistent and accessible risk rating colors across various pages, including Risk Assessment, Heatmap Workbench, Record Overview, Dashboards, and Project summary page.
        -   Inline dashboards are now set to read-only, resolving customization issues encountered during upgrades.
        -   Enhancements were made to streamline metrics creation and updates. Key logic for KRI and KCI metrics has been moved to new extension points for better maintainability. Additionally, business rules and script includes have been reorganized across scopes to align with their respective modules, improving modularity and functionality.
    -   Fixed:
        -   Addressed multiple security, licensing, and translation issues to improve overall usability.
        -   Improved load time of assessment page in Risk assessment project by fixing several performance issues.
-   **Version 19.1.2 - November 2024**
    -   New:
        -   The infrastructure for the Risk Assessment project is delivered as part of this application.
        -   Added a "Status" field to the Risk Assessment table, enabling workspaces to display the progress of assessments.
        -   Introduced a new field in Automated Factors to indicate dependency on responses from the same assessment.
        -   GRC Business Users can now add comments in the Risk Identification activity stream.
    -   Changed:
        -   Disabled sandbox access for client-callable Script Includes.
        -   On Risk Assessment records, the "State" field has been replaced with a "Status" field in Workspaces. The "State" will no longer update when navigating between sections in Workspaces.
    -   Fixed:
        -   Addressed various security issues.
        -   Resolved a licensing issue related to the Risk Events.
        -   Fixed several issues related to Risk Identification, Risk Assessment, Risk Appetite, and the Classic Heatmap.
        -   Resolved localization issues.
-   **Version 19.0.3 - August 2024**
    -   New:
        -   Smart Assessment integration with Risk identification
            -   During the information gathering stage of risk identification, we integrated smart assessments. Risk managers can now send these smart assessments to the owners of the entities. This configuration can be done by the risk admin and is available in the Risk Identification Configuration record. The risk admin can select the 'Use smart assessment' field to choose smart assessment templates in the 'Questionnaire' field.
        -   Reopen Risk Events
            -   Earlier, customers could not re-open closed risk events and had to create a new one to track the same issue. This feature now allows them to re-open a closed risk event either individually or in bulk with a single action on the list page. Users must have the Risk Event Admin role to perform this action.
        -   Integration of an issue &amp; open risk response task within a risk response strategy
            -   In advanced risk assessment, users can link open risk response strategies and tasks from previous assessments at multiple stages. They can also create and link issues directly to the risk assessments if the 'Allow issue linking with risk assessment' flag is enabled in the RAM form.
    -   Change:
        -   Metrics will be active by default
            -   Metrics are now marked as 'active' upon creation if the item is in any state other than 'retired'. Metrics mapped to 'retired' items remain 'inactive' but can be reactivated if the item's state changes. A scheduled script is also available to update existing metrics accordingly.
        -   Currency Conversion improvements for Risk Events
            -   In the Risk event, we can now address inaccuracies in financial net loss reporting by selecting a specific currency conversion date at the system property level. There are options for various event dates, and you can override this selection at the risk response template level for both new and in-progress risk event workflows.
    -   Fixed:
        -   Accessibility and localization issues have been resolved.
        -   Support for single currency mode in Risk assessment has been added.
        -   Issue with moving Risk identification to the retired state when the associated entity is retired, resolved.
        -   In classic UI, issue with no info message displayed after reassigning the assessment has been resolved.
        -   Assessment scores displayed in the activity stream and assessment summary are now in sync.
        -   Risk assessment approvals now cancel correctly when a risk assessment is cancelled.
        -   Business user lite can no longer perform risk assessments without the ARA assessor role.
        -   Incorrect colour coding of the heatmap when transformation criteria display text exceeds 40 characters has been resolved.
-   **Version 18.1.2 - June 2024**
    -   New:
        -   Domain separation improvements
        -   Migration of classic dashboards to Next Experience dashboards
    -   Fixed:
        -   Security issues
        -   The risk assessment second-level approval issue was fixed
        -   Risk assessment approval notifications
-   **Version 18.0.2 - February 2024**
    -   New:
        -   Sidebar integration for Risk events and Issues
        -   Support for group factor comments
        -   ARA workspace for workspace enabled customers
    -   Changed:
        -   Multiple table support on Risk Assessment Methodology for any object-based assessments
        -   Risk admins can change assessor for in-progress assessments
        -   Accessibility enhancements
    -   Fixed: Security enhancements to create risk response tasks
-   **Version 17.0.3 - August 2023**
    -   New:
        -   Target risk assessment to define your desired future risk level.
        -   Updated configurability of the Advanced risk assessment form.
        -   Empower Integrated Risk Management Lite Operators with updated capabilities to perform additional risk and compliance operations.
        -   Refactoring of the workspace record pages for UIB usability
    -   Fixed:
        -   Risk identification state was changing automatically.
        -   New Risk Response Task was not opening when canceling an existing task and creating a new one again.
        -   When Risk identification is retired, and the risk assessment is in "monitor" status, it does not get closed or canceled.
        -   Redefine scope action was not visible on scheduler for Operational risk manager and IT risk manager.
        -   In the risk identification workflow, under the control mapping state, controls were not being created automatically.
    -   Removed: Removed snc\_internal role usage from advanced risk.
-   **Version 16.0.8 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.7 - February 2023**
    -   New:
        -   Support for risk appetite and monitor the appetite breach notifications
        -   Aggregated roll-up support for the risk appetite feature
        -   Common controls integration
        -   Issue architecture changes to support risks to issues integration
        -   AI/ML support for risk statement recommendations
        -   Ability to reassess risk assessments from risk heatmap workbench
    -   Fixed:
        -   Updated security
        -   Dark theme fixes
        -   Confidentiality-related bugs on the risk event form
        -   Missing comment link on assessment page - Classic view
        -   New button was not working on the risk event entries
-   **Version 15.0.3 - December 2022**

    Fixed: Reduced application installation size

-   **Version 15.0.2 - August 2022**
    -   New:
        -   Feature to support simulation of Risk assessment methodolgy prior to publishing
        -   Dynamic approval of risk assessments leverages the GRC Approval configurator
        -   Feature to support similar risk events
        -   Ensure residual risk score is not greater than inherent risk score
        -   Support for Design and operational effectiveness of the control in the control assessment phase
        -   New property 'Migrate to Metrics from indicators'
    -   Fixed:
        -   Issue with ' Send assessments nightly run' scheduled job
        -   Automated Factor aggregation annotation is not externalized for translation
        -   Unrelated error 'Please fill the mandatory Name field' shows up on saving the form in RAM
        -   User with ara\_creator role is unable to trigger risk assessments in workspace
-   **Version 14.2.3 - May 2022**
    -   Changed: Updated Angular version
    -   Fixed: Project Form related list display issue
-   **Version 14.1.2 - March 2022**
    -   New:
        -   Support multiple entity classes in Risk assessment methodology
        -   Support event-based or trigger-based risk assessments
        -   Ability to delegate risk assessments
        -   Support for integrating advanced risk assessments lifecycle on the Risk form
        -   Introduced new roles for advanced risk assessments. For any user to perform advanced risk assessment related activities like assessment creation, viewing assessments, assessment approval, responding to assessments these roles are needed. Please note that users with sn\_grc.business\_user role who were earlier able to perform advanced risk assessment actions now must be granted these roles for them to continue performing advanced risk assessment-related actions.
            -   sn\_risk\_advanced.ara\_creator
            -   sn\_risk\_advanced.ara\_reader
            -   sn\_risk\_advanced.ara\_approver
            -   sn\_risk\_advanced.ara\_assessor
    -   Fixed: Replaced SNC Internal access with GRC Business User or appropriate Risk management role on the risk tables
-   **Version 13.0.3 - September 2021**
    -   New:
        -   Reassign risk assessment
        -   Security fixes
        -   Capability to establish the relationship between the risk event and citation
    -   Fixed:
        -   End date does not get populated on risk assessments which do not have risk response and approval stages.
        -   Control assessment state is showing 2.0 on state field instead of published on version 10.0+ upgrade scenario.
        -   Accessibility issues on Advanced Risk Assessment page.
        -   Project form sections and related lists cannot be accessed by users without sn\_grc.business\_user role.
        -   When residual assessment has Factors same as inherent, rating criteria for inherent and residual should be in sync.
        -   Duplicate risks getting created when associating risks via risk assessment scope.
        -   Changing **Assess** field from 'Risk' to 'Any object' on the copied RAM is allowing risk-only related items.
-   **Version 12.0.2 - March 2021**
    -   Fixed:
        -   Risk tolerenace bug fix.
        -   Fix for the copy assessment results from previous assessments.
        -   Reassign should not check for mandatory fields.
        -   The related Risk assessment is not in the Closed state when a Risk has been retired.
-   **Version 11.0.1 - October 2020**
    -   New:
        -   Integration with Project Portfolio Management
        -   Integration with Application Portfolio Management
        -   Ability to retire Risk Assessment methodologies
        -   Ability to cancel/recall risk assessments
        -   Operational risk dashboard
        -   Deep copy of Risk assessment methodologies, factors
-   **Version 10.1.3 - June 2020**
    -   New:
        -   New capability to connect risk silos and automate your risk assessment responses using automated factors.
        -   New capability to assess any record in ServiceNow without creating a risk and entity.
-   **Version 10.0.0 - March 2020**

    New: Advanced Risk Assessments

-   **Version 9.0.3 - November 2019**

    This feature is new for New York.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

