---
title: Major Security Incident Management release notes
description: Version history for the Major Security Incident Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-major-security-incident-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Major Security Incident Management release notes

Version history for the Major Security Incident Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.6.2 - June 2026**
    -   Fixed:
        -   Fixed Card view option on MSIM status report list.
        -   Fixed free form text fields population on Preview section.
-   **Version 3.6.1 - May 2026**
    -   Fixed:
        -   Fixed an issue where MSIM Status Report were failing to load after updating plugin to v3.6.
        -   Fixed an issue where duplicate work notes were being created when a custom timeline event was created.
-   **Version 3.6.0 - March 2026**
    -   New:
        -   Recipient fields are now pre-populated when sharing status reports, providing a smoother experience.
        -   Additionally, recipient options for status report emails have been enhanced to offer greater flexibility.
-   **Version 3.5.1 - January 2026 \(Yokohama\)**
    -   Fixed:
        -   Fixed a 404 error that occurred when previewing MSIM Status Report templates. You can now save and preview these reports.
        -   Fixed an issue where the Delete option was missing for user-created “My Lists” in the Major Security Incident Management workspace. This fix restores standard list control functionality, ensuring consistency with other workspaces.
-   **Version 3.5.0 - December 2025 \(Yokohama\)**
    -   New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.
    -   Fixed:
        -   Security fixes.
        -   Corrected an issue where the Status Report visualization displayed all incidents even when no incidents were linked to the Major Security Incident \(MSI\). The visualization now correctly shows only the relevant linked incidents.
        -   Resolved an issue in MSI Workspace where the "Next Update On" date-picker opened in read-only mode. Users can now select a date normally without any restrictions.
-   **Version 3.4.22 - December 2025 \(Xanadu\)**

    Fixed: Resolved an issue in MSI Workspace where the “Next Update On” date-picker opened in read-only mode. Users can now select a date normally without any restriction.

-   **Version 3.4.31 - October 2025**

    Fixed:

    -   Fixed issue where SharePoint setup failed to grant site access to the Azure App Registration
    -   Security fixes
-   **Version 3.4.30 - August 2025 \(Yokohama\)**

    Fixed: Resolved an issue where accessing the MSIM Status Report caused session timeouts when the glide.authenticate.limit.concurrent.interactive.sessions property was enabled \(set to true\).

-   **Version 3.4.21 - August 2025**
    -   Fixed:
        -   Fixed an issue where, after manually assigning an assignment group and assignee to a task under a Major Security Incident \(MSIM\), subsequent updates to the assignment group \(especially when updated to a value higher in the hierarchy or different group\) caused the assignee field to reset or clear unexpectedly.
        -   Fixed an issue where users were unable to select records from the Linked Record table to perform the unlink action.
-   **Version 3.4.3 - June 2025**

    Fixed: Resolved an issue where tasks deleted from the List View were not being removed from the sn\_msi\_task table.

-   **Version 3.4.2 - May 2025**
    -   New:
        -   Developed new Administration section​ in Major Security Incident to consolidate configurations for SharePoint/Teams etc. and removed need to import credentials.
        -   Upgraded MSIM Playbooks to run on the latest engine. This ensures to get all the latest features and performance improvements.
    -   Fixed: Provided support to add users to share status report in MSIM workspace.
-   **Version 3.3.5 - December 2024**

    Fixed: Accessibility violations related to Status Report loading etc.

-   **Version 3.3.0 - November 2024**
    -   New:
        -   Zero-day Vulnerability Playbook created in PAD and linked to an MSI in MSIM.
            -   Generate response tasks to assess vulnerabilities and communicate with impacted customers.
            -   MSI Managers must specify the assignment group and may optionally assign specific individuals for each task.
    -   Fixed:
        -   Accessibility issues in the MSIM Workspace in tabs such as, Status Report, Collaboration, etc.
        -   The ARIA violation in UI Builder - MSIM Workspace supports Localization &amp; Internationalization.
        -   The CSRF token in the Status report tab so that you are no longer logged out during a preview of the status report.
        -   Security bugs related to the ACL.
-   **Version 3.1.3 - August 2024**
    -   Changed:
        -   Improvements to Timeline
        -   Improvements to Status Reports
-   **Version 3.1.0 - May 2024**
    -   New:
        -   Added Slack Chat integration
            -   Auto-create channels in Slack with added members
            -   Create MSI tasks in the workspace from Slack channels
        -   Code Names and Simplified Categories for MSIs
        -   AddedLegal Request Playbook.
    -   Changed:
        -   Teams Enhancements on the Collaboration tab:
            -   Adding groups to channels
            -   Adding members or groups directly to Teams or general channel without being part of any individual channels
            -   Rename the existing team name
        -   Next Update on:
            -   Pre-populated PDF Status Reports
            -   Displayed as a widget on the Overview tab
        -   Sharing Status Reports with external recipients
-   **Version 3.0.4 - March 2024**
    -   New:
        -   Added MSIM VTB Task Card component as a dependency to MSIM. Updated the logic to show tasks without priority.
        -   Added link to Microsoft Teams channel from Collaboration tab.
        -   Added email template for Incident Responders who are assigned a task.
    -   Changed:
        -   Updated the logic for filtering visualizations in Status Reports.
        -   Minor UI fixes in the Overview tab, Timeline component, and Collaboration tab.
        -   Added character count validation for Executive Summary.
-   **Version 3.0.3 - March 2024**
    -   New:
        -   Added MSIM Conference Calling integration that supports MS Teams, Zoom, and WebEx.
        -   Added the capability to send Status Reports over rich-text email format \(in addition to PDF\).
        -   An Enforcement Restriction was added to decide which users or groups can access specific MSIs.
        -   Migrated workspace pages to Layout 3.0 to support accessibility.
    -   Changed:
        -   Redesigned and simplified the MSIM Overview Tab.
        -   Updated the Visual Task Board with the ability to pivot the board to a list.
            -   Make sure you have installed the "MSIM VTB Task Card: 1.0.1v" app separately after installing the MSIM app.
        -   Improved email notifications for Proposed and Promoted major security incidents.
    -   Fixed:
        -   Sharing status reports causes a frozen screen.
        -   Session messages disappear immediately from the MSIM workspaces Details tab.
        -   Clicking the tasks link on the closure modal opens the Details tab instead of the Tasks tab.
        -   Adding a Timeline label for collaborative activities does not create any timeline events.
        -   In the reference fields on the MSIM workspace, the magnifying glass is not displayed for all the reference fields.
        -   Unlinking the SIR or VUL data rolled up from SITs or VITs is not getting unlinked from the major security incident.
        -   The "Assigned to" reference is looked up by the "Assignment Group" value in the MSIM Workspace when creating a New MSI Task.
        -   Post Utah upgrade, choice field dependency on the MSIM workspace is broken after the Utah upgrade.
        -   Only on the Washington version:
            -   Navigating back to the closure modal by clicking continue displays an empty modal window.
            -   The MSIM workspace Timeline component displays a new label, "Timeline chart", which overlaps the "New event" action.
-   **Version 3.0.2 - February 2024**
    -   New:
    -   -   Added a conference calling feature to MSIM that supports Teams, Zoom, and WebEx.
-   Migrated workspace pages to Layout 3.0 to support accessibility.
-   Replaced the Tasks tab with Virtual Task Boards \(VTB\).
    -   Fixed:
    -   -   Session messages disappear immediately from the MSIM workspace Details tab.
-   Navigating back to the closure modal by clicking continue displays an empty modal window only in the Washington version.
-   Clicking the tasks link on the MSIM closure modal opens the Details tab instead of the Tasks tab.
-   The MSIM workspace Timeline component displays a new label, "Timeline chart", which overlaps the "New event" action only in the Washington version.
-   Adding a Timeline label for collaboration activities doesn't create any timeline event.
-   In the reference fields on the MSIM workspace, the magnifying glass is not displayed for all the reference fields.
-   The Share option on the Status Reports tab freezes after submission.
-   Unlinking the SIR or VUL data rolled up from SITs or VITs are not getting unlinked from the major security incident.
-   The "Assigned to" reference lookup is not filtered by the "Assignment Group" value in the MSIM workspace modal and creates a new sn\_msi\_task.
-   The Choice field dependency on the MSIM workspace is broken after the Utah upgrade.
-   **Version 2.2.5 - November 2023**

    Fixed:

    -   Major Security Incident \(MSI\) actions like Link, Propose, and Promote were not working on Vancouver instances.
    -   Reference "i" icons were hidden from the Security Incident Response workspace when Major Security Incident Management \(MSIM\) was also installed on the instance.
-   **Version 2.2.3 - September 2023**

    New: Added usage metrics to capture MTTR for major security incidents.

-   **Version 2.2.2 - August 2023**

    Changed: Major Security Incident Management is updated to support standard record pages.

-   **Version 2.1.6 - May 2023**
    -   Changed: Updated to support the application integration on the Security Incident Response workspace.
    -   Fixed:
        -   The error message displayed on the timeline custom event is shown in GMT time format instead of in logged-in user time format, which is now fixed.
        -   Incident Impact tab displays an empty list on the MSIM Worskapce with sn\_msi.incidentimpact\_read.
-   **Version 2.1.4 - April 2023**

    Changed: Updated to support this application on the Security Incident Response Workspace.

-   **Version 2.1.2 - February 2023**

    Fixed: Localization fixes.

-   **Version 2.1.1 - November 2022**

    Fixed: The tasks created on the MSIM workspace are not getting displayed on the Tasks tab, this occurs when the tasks do not have a priority field populated then the Tasks tab fails to load.

-   **Version 2.1.0 - August 2022**

    New:

    -   MSIM changes:
        -   Linking additional records within Major Security Incident Management \(MSIM\) workspace for the following record types \(out-of-the-box\):
        1.  Security Incidents
        2.  Remediation Tasks \(VR\)
        3.  Security Cases \(TI\)
    -   Roll-up configuration framework to link any type of task by extending table and its data to Major Security Incidents.
    -   Ability to unlink records from Major Security Incidents.
-   **Version 2.0.0 - March 2022**
    -   New:
        -   Create your own report template which can be applied to the major security incidents \(MSIs\) and generate the status report as required.
        -   You can add standard and custom Major Security Incident Response form fields to report templates that are dot-walkable. In addition, you can format and configure the report based on your requirements using report sections, report subsections, and its elements.
        -   Along with the template builder, you can:
            -   Add branding to your reports such as header and footer image, header and footer text.
            -   Use report widgets to define and include UIB elements like data visualizations in the status reports.
            -   Use report lists to define and include related table information in the status report.
            -   Use Template Scripts to include the related lists data, date operations, and any other data that are not directly dot-walkable.
        -   In addition, there are two default report templates provided:
            -   Technical Status Report
            -   Executive Status Report
        -   This feature also provides you with the ability to preview the template during design time and preview/share the report with stakeholders during run time.
-   **Version 1.1.1 - December 2021**

    Major Security Incident Management provides a unique user workspace and workflow methodology to coordinate various activities across different user groups and resolve major security incidents more efficiently.


