---
title: Health and Safety Risk Management release notes
description: Version history for the Health and Safety Risk Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-health-safety-risk-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Health and Safety release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Health and Safety Risk Management release notes

Version history for the Health and Safety Risk Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.2.0 - June 2026**
    -   Fixed:
        -   Security issue where multiple flows were configured to run as System user instead of scoped credentials
        -   Removed a duplicate stale copy of an Angular provider in Risk Management that could cause conflicts
        -   Issue causing multiple identical Compose buttons appeared in the UI
        -   Display issue in Employee Center affecting rendering of long hazard names with spaces in JSA on a single line
        -   Error message related to insufficient access for the query\_rangeoperation on sys\_user.managerin the KB Feedback Task table
        -   Issue preventing Agent Assist from appearing in the side panel of the Audit Details page
        -   Issue where the Open Inspection Survey button did not appear for certain date format configurations
-   **Version 9.1.0 - May 2026**
    -   New: Added approval policy role called "Intelligent Policy Author for Health and Safety Permit to Work".
    -   Fixed:
        -   Resolved XSS security vulnerability in sn\_hs\_rm\_survey\_results.
        -   Fixed missing “Open inspection smart assessment” button in Health and Safety Workspace.
        -   Fixed file referencing error when adding an action to an attachment question in Smart Assessment on Mobile.
        -   Fixed incorrect ordering of days and months in date-related dropdowns.
-   **Version 9.0.1 - March 2026**
    -   New:
        -   New data model for Objectives, Criteria, and Items for review, providing the foundation for audit and inspection management.
        -   Create audits directly from the Workspace and import scope from existing audits to reduce duplicate efforts.
        -   People Involved section for tracking audit participants.
        -   Objectives tab for managing and tracking audit objectives in a dedicated view.
        -   Configuration and validation of audit schedules directly from the audit.
        -   Overview tab with progress indicators and record counts for at-a-glance audit status.
        -   Results tab for managing and reviewing audit outcomes and findings.
        -   Citation and referencing of specific sections within cited records in an audit.
        -   Configurable approval workflows for audit items, enabling structured review and sign-off.
        -   Roles and ACLs for the Risk Management application, defining access control for audit-related data.
    -   Changed: Migrated Health and Safety Risk Management files to updated APP-CBS-BU infrastructure as part of module realignment.
    -   Fixed:
        -   Smart Assessment scripted screen that was failing to load.
        -   Multiple issues with Audit surveys impacting functionality and user experience.
        -   Localization warnings across the Health and Safety Risk Management application.
        -   Assign To field uneditable on the Finding Details page for Safety agent and Safety manager roles.
-   **Version 8.1.2 - January 2026**
    -   New:
        -   Added Smart Assessments support for Health and Safety inspections:
            -   Smart Assessments in Health and Safety Workspace
            -   Smart Assessments on mobile
-   **Version 8.0.0 - December 2025**
    -   New:
        -   Added toggle to view residual and inherent risk in the Risk matrix.
        -   Added field for risk owners in risk analysis.
        -   Added categories to control components.
        -   Added action schedules to risk assessments.
        -   Enabled auto-fill for gaps in risk tolerance.
        -   Enhanced risk matrix visualization with heat map.
        -   Improved risks and control management.
        -   Enabled versioning for risk assessments.
    -   Fixed:
        -   Corrected question order in inspection surveys.
        -   Fixed location fields in inspection records.
        -   Fixed resizing issues in risk analyses on certain browsers.
        -   Fixed privilege issues during document migration.
        -   Restored search functionality in hazards.
        -   Improved UI for dark theme on mobile.
        -   Improved translation for audit survey messages.
        -   Improved hazard title display in the risk management widget.
        -   Enhanced accessibility for viewing safety documents and inspections.
        -   Updated tooltips and validation for risk analyses.
        -   Addressed privilege escalation and security issues.
-   **Version 7.0.0 - August 2025**
    -   Fixed:
        -   Accessibility button focus issue on JSA
        -   HTML code displayed on LOTO description on Permits to Work
        -   New button not shown on "People involved" section in observations
-   **Version 6.0.0 - May 2025**
    -   New:
        -   Added action creation to inspection survey forms on the Employee Center and Mobile Agent app
        -   Added Actions tab to the Findings record
        -   Added inspections to Mobile Agent app enabling agents to work on Health and Safety inspection records on mobile
        -   Easily re-assign inspection surveys to another employee within the assigned group with the click of a button
    -   Changed: Improved UI for inspections and audit findings records
    -   Fixed:
        -   Issue with action scheduler on exposures not working for one time actions
        -   Issue with opening surveys on notifications in Now Agent
        -   ACL security issue
        -   Issue with the misnamed KB article on the View permits page
        -   A11y on Permit to work on the Employee Center
        -   Hidden reason for suspension field when suspending a permit
        -   Issue with demo user unable to create risk actions on risk assessments
        -   Issue with broken links on users on the View permits page
-   **Version 5.0.0 - February 2025**
    -   New:
        -   Exposure Management:
            -   Track and manage workers' exposure to workplace hazards
            -   Bulk schedule actions to manage the exposures
        -   Permit to Work feature:
            -   Enable workers to request permits from the Employee Center
            -   Merge multiple work types into one permit
            -   Assign pre-work and closure checklists to permitted workers
        -   Link safety register records with risk assessments
    -   Changed: Grouped all Health and Safety Risk Management features under a single "Risk Management" icon in the Health and Safety workspace
    -   Fixed:
        -   Various accessibility issues
        -   Issue with blank home page on H&amp;S workspace
        -   ACL issue in Health and Safety Risk Management
-   **Version 4.0.1 - December 2024**
    -   New: Added "Create records at once" checkbox and Create Audits button under the Audit Schedule record to enable users to generate related scheduled records immediately.
    -   Fixed: Audit actions tab is displayed under the Audit record.
    -   Removed: Removed date validation for the Inspection record.
-   **Version 4.0.0 - November 2024**
    -   New:
        -   Audits
            -   Audit scheduling
            -   Related audit field added to the Observation catalog item for users currently assigned to an active audit
            -   People involved including their role
            -   Findings that can be extracted from the survey result
            -   Global standards and documents list
            -   Risk assessable audit findings
    -   Fixed:
        -   Batch update exception error when installing
        -   Field and button access issues on the Risk matrix form
        -   JSA UI action bar not showing on workspace JSA form
-   **Version 3.0.0 - August 2024**
    -   New:
        -   Job register. Safety teams can define jobs and optionally, the job's steps.
            -   These jobs can be applied to JSAs so that the JSA covers each step of their job.
            -   Each job and job step can have hazards associated with them so that the JSA user is aware of all the hazards that are related to the job they are doing when they complete a JSA.
        -   JSAs can be copied. If you have a JSA that you want to re-use, you can copy that JSA and edit or update it as required.
        -   Hazards and Controls can be imported into a risk assessment from a Job in the job register.
        -   Offline inspections. Inspection surveys are available in offline mode on the ServiceNow Mobile Agent app.
    -   Fixed:
        -   Issue with modals not working on JSAs in the Employee Center on mobile devices.
        -   Issue where JSA would not open in the workspace in Washington DC.
        -   UI inconsistencies on mobile JSAs.
        -   Job location field not shown on JSA in Workspace if the location was entered manually and not with the drop-down menu.
        -   Prevented saving informed workers when changing from a chosen employee to worker and not entering a name in the free text field.
        -   ACL improvements for table security.
        -   Inspection Action records not visible on the list view under safety inspections.
        -   Blank screen shown when clicking Home breadcrumb on JSA on mobile.
        -   Issue where add employee/worker on JSA would not pop up if System Localization was enabled on the instance.
-   **Version 2.0.1 - May 2024**
    -   New:
        -   Safety Inspections:
            -   Build and manage safety inspections built on the ServiceNow Surveys and Assessments platform feature. Use available surveys or build new ones with the Survey Builder.
            -   Schedule inspections at regular intervals with the Inspection Scheduler.
            -   Conduct inspection surveys on mobile with the NowMobile app.
        -   Safety Registers:
            -   Upload Safety Data Sheets \(SDS\) to the chemicals or asbestos registers.
            -   Keep track of important details on registers such as responsible parties and storage locations.
            -   Support chemical safety awareness through the Employee Center with searchable Safety Data Sheets for all employees.
    -   Changed: The label for the Settings list in the Health and Safety Workspace is changed to "Configuration" and has a new icon.
    -   Fixed
        -   JSA modal issues in the Employee Center
        -   JSA reporter search issue
-   **Version 1.0.0 - February 2024**
    -   ServiceNow Health and Safety Risk Management provides an efficient and simple way to track potential hazards and other risks within the workplace before they cause an accident. The application can be used from a desktop computer or a mobile device, providing flexible options to track and report on risks.
    -   A unified Health and Safety Workspace in the application enables safety teams to manage hazards and control lists, as well as create templates for Job Safety Analyses and Risk Matrices for Risk Assessments.

