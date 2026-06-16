---
title: Security Incident Response Workspace release notes
description: Version history for the Security Incident Response Workspace on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response Workspace release notes

Version history for the Security Incident Response Workspace on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.1 - June 2026**

    New: Advanced Timeline in SIR for Correlated Security Data.

-   **Version 1.9.0 - April 2026**

    New: Vulnerabilities and related intelligence now appear on the TISC Context tab of Security Incidents. This allows analysts to quickly access the risk data during investigations.

-   **Version 1.8.5 - March 2026**
    -   New:
        -   Added the option to compose email in the Response Task details.
        -   Default landing tab is configurable \(Overview or Details\).
        -   Right-Side pane is collapsed by default and preferences are preserved.
        -   Option to add Quick-Filters configuration is added on the administration tab.
        -   Added the option to Auto refresh of security incident list view.
        -   System properties are added to the Administration tab.
    -   Fixed:
        -   Fixed the issue where the associated MITRE ATT&amp;CK and D3FEND modal titles do not support localization.
        -   Fixed the issue where the Link as children button on Similar Security Incidents is not working when Select All Items in the list is selected.
        -   Fixed the issue where inline editing was not supported for observables on the Investigation tab.
        -   Fixed the issue where there was an issue reading the "query" property from null showing under sirw security incident tabs.
        -   Fixed the issue where bulk close function is not fetching the custom close codes dynamically in the same way it fetches in record page.
        -   Fixed the issue where after the Yokohama upgrade, user was not able to add Group as recipient to MS Teams Bridge Call in SOW.
-   **Version 1.8.3 - January 2026**

    New: Added MITRE Attack Defend Relation Graph.

-   **Version 1.8.0 - December 2025**
    -   Fixed:
        -   Incident opening was taking more than 4 seconds, and page loading was unstable.
        -   Removed the "close" action from the security incident list view. Now available only from the Home -&gt; Overview page.
        -   In Workspace Overview, fixed the formatting issue in Close Notes.
    -   Changed:
        -   Added the "Create security incident" button in the Vulnerability Manager workspace.
        -   Enabled the AWA Inbox functionality in Security Incident Response \(SIR\) Workspace.
-   **Version 1.7.41 - November 2025**
    -   Changed:
        -   Updated the activity definitions for the playbook activities.
        -   As part of the granular admin directive, removed the direct system admin access for multiple pages and actions.
    -   Fixed:
        -   Fixed the correlation insights modal cache issue.
        -   Removed the Generate Insights button from the Related Records tab \(applicable only for Now Assist for SIR v4.0.1\)
        -   Fixed the issue where SIR Open incident was taking more than 4 seconds to open, and the page load was unstable.
        -   Restricted the modifications to the attachments after security incident closure.
        -   Removed the "close" action from the security incident list view \(only from the Home-&gt; Overview page.\)
-   **Version 1.7.31 - September 2025**
    -   Fixed:
        -   The SIR Response Task work note does not populate once work notes are posted.
        -   UX Screen "Edit User Preferences" for Security Incident Application has wrong parent macroponent defined.
-   **Version 1.7.21 - August 2025**
    -   New: Bulk Closure UI and Backend implementation
    -   Changed:
        -   The "sn\_si.read" user should not have the permission to add a security tag to a security incident.
        -   Enforce restriction/role restriction against security tags were not getting applied in SIR workspace.
    -   Fixed:
        -   Resolved multiple security issues.
        -   SIR Workspace - Unable to save Response Task from modal.
-   **Version 1.7.11 - July 2025**
    -   Fixed:
        -   Dropdown not working for a field in sn\_si\_aw\_entry\_point\_config table.
        -   Address ACL issues reported from ARC0016877.
-   **Version 1.7.10 - June 2025**
    -   Fixed:
        -   SIT page Related record section in SecOps workspace keeps loading.
        -   Runbook articles were not properly applied with dark theme on the SIR workspace.
        -   Drop down buttons on investigation tab were not visible properly.
        -   Backend name is showing up instead of display name in Reports section of the SIR Workspace.
        -   Schedules page in SIR workspace accessible for user with the sn\_si.read role.
-   **Version 1.7.9 - May 2025**
    -   New: On-Call Scheduling: Introduced a new on-call scheduling feature that allows users to efficiently manage and coordinate on-call duties within the SIR workspace.
    -   Changed: Relationship Graph Enhancement: Enhanced the Relationship Graph feature by introducing admin-level configuration options, enabling greater customization and control.
    -   Fixed: Various bugs have been addressed and resolved as part of this release.
-   **Version 1.7.3 - March 2025**

    Fixed: Various bugs have been addressed and resolved as part of this release.

-   **Version 1.7.0 - February 2025**
    -   New:
        -   Incident Status Reporting:
            -   Executive Summary and Analyst Report Templates
                -   Introduced ready-to-use, out-of-the-box templates for streamlined reporting processes.
                -   Report Templates: Users can now create reusable templates for consistent and standardized reporting.
                -   Report Generation: Effortlessly generate detailed reports for better decision-making and communication.
                -   Report Sharing: Seamlessly share reports with stakeholders to ensure alignment and collaboration.
        -   Conference call feature
            -   Zoom
            -   Teams
            -   WebEx
        -   Relationship graph visualizer
    -   Changed: The Discuss button for initiating native sidebar chat has been renamed to Start Chat and is moved under the Collaborate option.
    -   Fixed:
        -   On the SIR home page widget list, the Assign action did not work for the second time if the page was not refreshed.
        -   Response Task - Related Records Pane Is Empty
        -   After a SIR is closed, the associated playbooks are displayed as 'Cancelled' with the reason: "Cancelled by system," even though the playbook was completed before the closure.
        -   Issue with the assignment group and assigned-to fields lookup \(magnifying symbol\) within the Security Incident Response workspace on SIT.
        -   The Splunk ES-related file is to be removed from the analyst workspace.
-   **Version 1.6.9 - December 2024**
    -   Fixed:
        -   An error where the investigation tab displayed: "Error while fetching entry points data" message.
        -   Issue with the assignment group and assigned-to fields lookup \(magnifying symbol\) within the Security Incident Response workspace on SIT.
-   **Version 1.6.4 - November 2024**
    -   New:
        -   Supporting UI changes for the below skills added for Now Assist for Security Operations:
            -   Post-incident analysis
            -   Recommended Actions
    -   Fixed:
        -   Custom new records in SIR are cleared once a reference field is selected from the pop-out in the SIR workspace
        -   A Performance Analytics indicator installed with "Security Incident Response Workspace" does not have an indicator source, causing errors in PA job logs.
-   **Version 1.6.2 - August 2024**
    -   New: Added Native sidebar chat.
    -   Fixed:
        -   If the response task has an Assignment group field value but not an Assigned to field value, then the assignment details from the security incident are not automatically filled.
        -   There are no ACLs on the Sighting Search Details remote table.
        -   When a user from another session closes the security incident, the user from the current session sees a closing modal.
-   **Version 1.5.3 - July 2024**

    The Security Incident Response Workspace is designated as a dependent application for Security Incident Response. Therefore, it cannot be installed directly.

-   **Version 1.5.1 - June 2024**
    -   New:
        -   Now Read and privileged access users will also have access to view the security incidents from the workspace.
        -   Security Incident Response workspace\(sn\_si\_aw:1.5.1\) will be installed automatically with Security Incident Response \(sn\_si:13.4.5\).
-   **Version 1.5.0 - May 2024**
    -   New: Added Shift Handover Report
    -   Changed:
        -   The Risk score configuration in the Security Incident Response workspace has been improved with the following:
            -   Ability to set up a Risk Score Calculator from either script or condition builders.
            -   Ability to apply multiple conditions while setting up rule-based scoring.
            -   Ability to apply weightage to each scoring line.
            -   Weights should add up to 100. For rule-based scoring, the ability to select tables/fields and values for setting up the condition.
            -   Ability to capture the conditions and scoring via script.
            -   Ability to manually execute the risk score calculators to recalculate after making changes.
    -   Fixed:
        -   The 'Security Incident Overview' page takes longer to load due to the missing null check.
        -   The default filter for the 'Visible to Me' list on the SIR workspace is incorrect.
        -   The 'Post' action disappears when the Worknotes field is made mandatory by UI Policy or the client script.
        -   The Close code choices are not listed per user-preferred language in the closure flow event.
-   **Version 1.4.0 - February 2024**
    -   New: Added Security Incident Response Request functionality.
    -   Fixed:
        -   The Playbook and Related record tabstook longer to load than other tabs.
        -   When the work notes are mandatory, and the user tries to close a response task without filling in the work notes, an error message is not displayed.
        -   The latest result filter data for Running Processes, Running Services, and Net stats is incorrect.
        -   The State field in Security Incident Response \(GlideChoiceList\) displays "Analysis" incorrectly instead of "Identification."
-   **Version 1.3.1 - December 2023**
    -   New: You can now monitor Scan Requests from the Security Incident Response workspace.
    -   Fixed:
        -   Changing the Assignment Group of SIT did not refresh the options for Assigned to.
        -   The data was not loading when users tried to load the affected services using the SIR workspace.
        -   The Create Outage Modal window was not loading on Vancouver instances.
        -   The Response Task modal's height did not stay constant when users switched between tabs.
        -   The magnifying glass option was not working in a few places.
-   **Version 1.3.0 - November 2023**
    -   New:
        -   Added the "Report Risk Event" action.
        -   Security Incident Managers \(sn\_si.manager\) can now edit all dashboards.
    -   Fixed:
        -   Sent or Received Emails body field was not rendered in HTML format.
        -   The playbook context menu item was not visible when the Investigation tab was open.
        -   Performance issue on the "Link" action on the Configuration Item-related lists.
        -   While scrolling up, the Playbook tab hides the other tabs on the Security Incident form.
        -   In the Lists view, while zooming in, the left or right scroll is difficult to find at the bottom of the page \(except the Security Incident form\).
        -   A user with the Security Manager role could not view related records on a security incident in the workspace view.
        -   Reference records failed to load.
-   **Version 1.2.2 - August 2023**

    New:

    -   Flow to Process conversion.
    -   Core Logic Changes
-   **Version 1.1.0 - May 2023**
    -   New:
        -   Support for CrowdStrike Falcon Host integration.
        -   CISO and Manager overview dashboards.
    -   Fixed: Performance issues.
-   **Version 1.0.4 - April 2023**

    Changed: The Security Incident Response workspace is updated to support standard record pages.

-   **Version 1.0.0 - February 2023**

    Security Incident Response Workspace will be used by Security Analysts and SOC Managers to solve Security Incidents and perform all SOAR related activities.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

