---
title: Data Loss Prevention Incident Response release notes
description: Version history for the Data Loss Prevention Incident Response application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-data-loss-prevention-incident-response.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Data Loss Prevention Incident Response release notes

Version history for the Data Loss Prevention Incident Response application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.0 - June 2026**
    -   Fixed:
        -   Fixed an issue where the DLP Incident Response End User Workspace displayed an infinite loading spinner instead of rendering the record page for users with ACL-based access but          without
        -   Resolved a security vulnerability in the "Save Custom Fields" Data Broker within the DLP Incident Response integration with Proofpoint, preventing potential ACL bypass.
        -   Addressed an ACL bypass vulnerability in the "Fetch Archived Incidents Count" Data Broker to ensure proper authorization enforcement.
        -   Fixed an ACL bypass issue in the "Execute Cancel Approval" Data Broker, improving access control validation and security enforcement.
        -   Resolved ACL bypass and encoded query injection vulnerabilities in the "Fetch DLP Header" Data Broker, strengthening input validation and access control handling.
        -   Implemented fixes related to Cobalt Raven Non-Glide Query ACL directives, ensuring proper ACL enforcement for non-Glide query operations.
-   **Version 2.2.2 - February 2026**
    -   Fixed:
        -   Enhanced EmailUtility to correctly extract all attachments from EML files according to RFC standards.
        -   Fixed security bugs.
-   **Version 2.2.1 - December 2025**
    -   New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.
    -   Fixed: Resolved the functional issues in the DLP IR End User Workspace that occurred after upgrading to version 2.1.30. All affected components are now functioning as expected.
-   **Version 2.1.50 - October 2025**

    Fixed:

    -   Disabled auditing on the DLP download table to prevent unnecessary relationship change logs when records are deleted.
    -   Removed unwanted reference to the Field Level Restrictions table in the DLP Script Include.
    -   Endpoint DLP Storage: Resolved internal storage issue affecting Endpoint DLP data consistency.
    -   ACL on 'sn\_dlir\_incident' Table: Strengthened ACLs to ensure proper access control and data security for DLP incidents.
-   **Version 2.1.40 - September 2025**

    Fixed: Security issues for inadequate ACL for the sn\_dlir\_incident table and the relevant Databroker.

-   **Version 2.1.30 - August 2025**

    Fixed: Fixed the end user roles by adding dependency on Explicit Role \(com.glide.explicit\_roles\) plugin.

-   **Version 2.1.21 - July 2025**
    -   Fixed:
        -   Core system optimizations implemented to improve the performance of Microsoft Data Loss Prevention \(DLP\) integrations.
        -   Security issues for inadequate ACL For sn\_dlir\_incident table and relevant Databroker.
-   **Version 2.1.20 - June 2025**
    -   Fixed:
        -   Accessibility bugs:
        -   -   Tab elements now visible and accessible.
-   Assessment text no longer overlaps with the number in the Assessment tab within the DLP IR Analyst Workspace.
        -   Default target state issue in Incident Response Options Rule resolved.
        -   UI Elevation and Theme issues:
        -   -   Assessment heading now properly visible in Coral Dark theme.
-   In the Preview File tab, the body is now visible and borders are correctly displayed in Coral Dark theme.
        -   Performance bugs addressed to improve overall responsiveness and stability.
        -   Security bugs fixed to improve system protection and compliance.
-   **Version 2.1.19 - May 2025**
    -   New:
        -   Implemented SLA \(Service Level Agreement\) feature for DLP Incidents.
        -   Added support of a New button in DLP IR Analyst Workspace for creation of Manual DLP Incidents.
    -   Fixed: Security Bugs related to ACL Bypass.
    -   Removed: Field Level Restrictions feature from DLP.
-   **Version 2.1.17 - February 2025**
    -   New:
        -   Implemented Playbook feature in DLP Workspace Evidence File:   
            -   introduced the Playbook feature in the DLP Workspace to improve operational efficiency.
        -   Preview with Download Option:
            -   Added a preview icon for evidence files in the DLP Workspace. Users can now preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval. 
        -   Field Renaming in DLP Incident Table: 
            -   Renamed the field 'Custom Fields' to 'Additional Incident Data Fields' in the DLP Incident table to better reflect its purpose and improve clarity for users. 
        -   Improved Incident Consolidation Rules: 
            -   Updated the incident consolidation rules in the DLP module to ensure that the parent incident is always assigned the highest priority among consolidated incidents, enhancing incident management accuracy. 
    -   Fixed:
        -   Added Export button to export incident data from Workspace. 
        -   Fixed duplicate filters created when creating a new list in DLP IR Analyst workspace. 
        -   Closure code option list is showing choices for another table.
-   **Version 2.1.15 - December 2024**

    Fixed: Access Control Lists \(ACLs\) applied to the Data Loss Prevention Incident Response\(DLP IR\) end-user workspace to regulate and manage user permissions and access.

-   **Version 2.1.9 - November 2024**
    -   New: Closure Code Synchronization: Implemented automatic synchronization of closure codes to child incidents when a parent incident is closed, ensuring consistency across related incidents.
    -   Fixed:
        -   Accessibility Improvements: Resolved accessibility \(a11y\) issues, including ARIA violations, to enhance user experience in the UIB Assistant.
        -   Addressed an issue where the Download button was visible to end users during impersonation.
        -   Fixed the display of the Archived Incidents tab, which was incorrectly shown on the End User portal.
-   **Version 2.1.0 - August 2024**
    -   New:
        -   The DLP incidents view is now improved to support Closure code feature in background and foreground while closing DLP incidents.
        -   All the DLP admin configurations modules in DLP IR interface are now captured in update sets, which helps in migrating the configurations across instances.
-   **Version 2.0.15 - June 2024**
    -   Fixed:
        -   DLP IR Analyst workspace hangs when accessed after upgrading the plugin to 2.0.11.
        -   DLP - Configure workspace button from profile icon was not working.
        -   Unable to delete Custom fields from the list view as a DLP admin User.
        -   DLP Core - New button was not functional when users add new list menu items of other tables in the same list menu.
        -   The form view on the workspace was not showing expanded names for glide\_list type for duplicates.
        -   Close and Respond options in the form view of DLP ops portal was not working on Washington Platform.
        -   End user lookup rules failed when configured on customAttributes.
        -   Duplicate Related List on ops workspace on incident page.
        -   Unable to download node logs with DLP app installed.
-   **Version 2.0.13 - March 2024**
    -   Fixed:
        -   Incident state label is now visible for the DLP incident archived records.
        -   Match content information is now supported in ProofPoint integration for the DLP incident archived records.
        -   Re aligned the Additional Details tab for the DLP incident archived records.
        -   Re aligned individual list tabs for the Other incidents from end user tab on the DLP incident form view.
-   **Version 2.0.11 - February 2024**
    -   New:
        -   Implemented Archival rules for the DLP incidents.
        -   Form views and list views for the archived incidents is added on the DLP Analyst workspace.
        -   Added correlation ID field to map with the integration IDs within the DLP incident table.
    -   Fixed:
        -   The DLP Analyst workspace tab name displays with a unique name when the multiple tabs are opened.
        -   The incident count is displayed for the record level restricted users
        -   The incident assignment email notifications are sent to the end users as well when an incident is assigned.
        -   The Compose Email form action is now supported in the DLP Analyst workspace.
        -   Added a system property to support the read-only access for the the analysts to view the assessments submitted by the end users in the DLP Analyst workspace.
        -   Added support for analyst only having view access to assessment in workspace.
        -   The order of execution of Reapply assignment rules and end user rules
        -   The overriding functionality of any two matching rules is resolved.
-   **Version 2.0.8 - December 2023**
    -   Fixed:
        -   Resolved the issue where theCopy URLaction on the DLP Analyst Workspace did not copy the URL of that list but instead copied the URL of the page.
        -   Addressed the problem where theDetected Sensitive Information Typerelated list appeared twice for a single Microsoft DLP incident.
        -   Improved the performance by fixing the issues related to DB host utilization exceeding 80%. This was caused by Select SQL Query 2 during DLP 250k ingestion on 4.75M.
        -   Resolved the situation where Resolution notes were not populated when the option Nonewas selected from the Respond button on the End User Workspace.
        -   Fixed the DLP Assign Incident Modal, making it easier to identify the proper user when user display names are the same.
        -   Corrected the incident state in the DLP Ops Workspace. In the Assign Incident Modal, theIncident state pre-user responseis no longer reset to the default Pending assessment statewhen attaching an assessment.
        -   Fixed security issues related to the misconfiguration of table/field ACLs within thecom.glide.polaris.admin.configurationplugin.
        -   Fixed misconfiguration of table/field ACLs within the 'com.snc.data\_loss\_incident' plugin.
        -   Fixed an issue where the priority color changed in DLP for incidents based on the incident count priority chart in the Dashboard.
        -   Fixed DLP Assignment Rules with the user group setting assigned\_to if End user identifier is not None in the default config.
        -   Fixed the preview of attachments in emails not showing in incident Activity notes.
        -   Fixed the inability to assign a parent incident to any other users \(end-user\) when the parent has consolidated incidents \(child incidents\).
-   **Version 2.0.7 - November 2023**

    New: The application now supports Layout 3.0 which will be consistent across all the application versions starting from Tokyo.

-   **Version 2.0.5 - August 2023**
    -   New:
        -   Type column is added to the Response Option table default list view.
        -   Edit the DLP Analyst group field on the Analyst workspace.
        -   Form view and List view actions are hidden for the consolidated child incidents.
        -   Advanced response options were not available for the DLP analysts.
    -   Fixed:
        -   The assessment count in the related list was not displayed even though the assessments existed in the DLP workspace.
        -   My Lists on the DLP workspace cannot be deleted.
        -   DLP Ops Workspace Form view actions page was reloading with every click on the modal cancel/close without any record update.
        -   The expected action was not executed and performed from the list/related lists for all the selected incidents.
        -   DLP IR \(sn\_dlir\) app was causing performance issues during the upgrade when the sysapproval\_approver table contained a huge amount of data.
-   **Version 2.0.2 - June 2023**
    -   Fixed:
        -   Implemented Due date feature in the Emails section.
        -   Demo data is now visible under the Analyst workspace navigation list.
        -   The escalation email link to the user is now fixed.
        -   Inbound email actions are now functioning as expected.
-   **Verison 2.0.1 - May 2023**
    -   New:
        -   Approval: Digest email template for Pending Approval
        -   Update content in email templates
        -   List view controls - pending approval
        -   Migration: Record Page to Standard Record Page \(SRP\) for DLP ops and end-user portal
        -   New configuration tile for Azure blob storage and Amazon S3
        -   Escalation logic changes
        -   Encrypt match content stored in AWS/Azure and delete automatically
        -   MID App, MID capabilities in the Response Option
        -   Localization onboarding
        -   User instruction - Workspace
        -   End user lookup rules changes
        -   My Approvals module in End user workspace
        -   Incident consolidation
        -   Assessment: State transition for assessment attached from assignment rule
        -   Provide support of cloning the DLP incident
        -   Cancel Approval for Advanced Response Option
        -   Match content per sensitive info type in MSFT Integration and highlight exact matched text in the content
    -   Fixed:
        -   Advanced response actions are visible in the ""Close"" UI action of the DLP Ops portal
        -   DLP Custom Fields - Cannot order Choice values
        -   DLP Ops portal email button is not functional
        -   Quick messages are not available when composing an email in DLP Workspace
        -   Assessments are not loaded for the Tokyo Jan branch
        -   Implement integration run for Symantec DLP integration
        -   Move delegate info to the top in the emails
        -   Multiple work notes and comments columns are not needed in the form view
-   **Version 1.1.6 - March 2023**

    Fixed: Migration of record page to standard record page for DLP Ops portal and DLP End user portal.

-   **Version 1.1.2 - February 2023**
    -   New: Added a couple of tiles \(AWS, Azure\) for getting the matching content from the logs.
    -   Fixed:
        -   When we created Record level restrictions with an empty condition, no records were displayed in the List view of the DLP Ops portal.
        -   Age chart data is not displayed in the UI.
        -   DLP Form views based on scan sources are not working as expected in SD and Tokyo.
-   **Version 1.1.1 - November 2022**
    -   New: Record Level Restrictions.
    -   Fixed:
        -   Improve the logging for Data Loss Incident Response.
        -   Dark theme support for workspace.
-   **Version 1.1.0 - August 2022**
    -   New:
        -   Access control for DLP workspace
        -   Assessment as end user response
        -   Custom fields
-   **Version 1.0.9 - May 2022**
    -   New:
        -   Updates in the Incident Response options.
        -   Updates in the Escalation mechanism.
        -   Additional fields are introduced in DLP incidents.
        -   Added rules to identify Repeat Offenders more efficiently.

