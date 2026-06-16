---
title: Case Playbook for Complaints release notes
description: Version history for the Customer Service Management Case Playbook for Complaints on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-case-playbook-complaints.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Case Playbook for Complaints release notes

Version history for the Customer Service Management Case Playbook for Complaints on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.0 - June 2026**
    -   Changed:
        -   AI Sparkle on Fields: AI-generated field indicators are now displayed consistently across both the platform UI and Workspace.
        -   Granular Read/Write Role Support: The Complaint module now supports app-level granular roles — reader role: sn\_complaint.viewer, writer role: sn\_complaint.admin.
        -   AI Research Agent Task Management: When a user confirms the AI research agent's suggested tasks, existing tasks are cancelled and replaced with the newly suggested ones.
-   **Version 8.0.1 - March 2026**
    -   New version of complaint playbook.By default, it is activated and published.
    -   New:
        -   UI Navigation Improvements
            -   Implemented back button navigation across playbook activities
            -   Consolidated multiple buttons into "Continue" or "Save and Continue" buttons on all activities
        -   Complaint Case summarization
    -   Changed:
        -   Enhanced triage stage activity
            -   Shown complaint details, attachment, and response compose components in triage activity
            -   Improved UI for complaint details display/edit.
        -   Research stage enhancements
            -   Replaced case tasks specific activities with case tasks list activity
            -   Improved navigation and task management
        -   Data model changes.  New fields added.
            -   Customer correspondence content
            -   Complaint submitted by
            -   Guest address
            -   Guest email
            -   Guest mobile
            -   Guest name
            -   External reference number
-   **Version 7.1.1 - December 2025**
    -   New: Contains new granular admin roles.
    -   Fixed: Contains minor security defect fixes.
-   **Version 7.0.1 - August 2025**

    Contains minor bug fixes.

-   **Version 6.3.0 - February 2025**

    This version of Case Playbook for Complaints includes minor bug fixes.

-   **Version 6.2.0 - May 2024**

    This version of Case Playbook for Complaints includes support for the Unified Consumer role.

-   **Version 6.1.0 - November 2023**
    -   This version of Case Playbook for Complaints includes improvements to the process page variants. Changes include:
        -   Added support for the Email tab in the Activity Stream.
        -   Support for email templates on Process Page templates and variants in the contextual side panel.
        -   Support for customization of the start and end states of the approval flow.
-   **Version 6.0.1 - August 2023**

    This version of Playbooks for Customer Service Management includes improvements to the process page variants. Changes include:

    -   Ability to add optional activities
    -   Edit case details in playbooks.
-   **Version 5.0.1 - June 2023**

    Fixed: This version of Playbooks for Customer Service Management includes minor fixes to the View Details action on process-based page templates and page variants in CSM Configurable Workspace, including:

    -   Improved saving experience on reference fields within the View Details modal.
    -   Increased View Details modal window.
-   **Version 5.0.0 - May 2023**

    This Case Playbook for Complaints release includes a process-based page variant that you can activate and use with the complaint case type in CSM Configurable Workspace. This page includes a horizontal stage picker at the top of the record that provides an end-to-end view of the complaint process. This page also displays the related list tabs in the Dynamic Related Records component in the contextual side panel and displays persistent account and contact information. Agents can create tasks as needed as well as view and update case details.

-   **Version 4.2.0 - February 2023**

    Changed: This release includes changes to support executing process definitions on flow engine instead of the process automation designer engine, Next Experience UI for the mobile app, demo data for service definitions, and Minor fixes.

-   **Version 4.1.0 - November 2022**

    Changed: This version of the Case Playbook for Complaints store app includes changes to support the new record pages included in Playbooks for Customer Service Management v2.1.0 or a later version.

    Please note that this version of the store app requires updating to CSM Configurable Workspace v23.0.5 or a later version.

-   **Version 4.0.2 - February 2022**
    -   Changed:
        -   Changed highlighted value colors for priority field
        -   Modal header, help text, and labels changed on case type selector to sentence case
        -   Response template: highlight text color changed
        -   Minor changes to activity titles
        -   Fixed minor issue with De-escalate Case declarative action
        -   Fixed flow so that the title for Playbook stages show correct names
-   **Version 3.0.6 - July 2021**
    -   Changed:
        -   New refined PAD process created for complaint case which optimizes the activity cards and removes any redundant cards.
        -   Update to the out-of-box record producer which provides the ability to add in the additional member data.
        -   Complaint Playbook displayed in focused view which enables agents to view one activity at a time and gives them more real estate to work on the task.
        -   Complaint Playbook displayed in Compact mode which enables agents to complete the Playbook in the contextual side panel.
        -   Playbook-specific Dynamic Related Records available in the contextual side panel so agents can quickly view related records without switching tabs.
        -   Activity stream and ribbon available in the contextual side panel so that agents can access information without leaving the playbook focus area.
-   **Version 2.0.2 - January 2021**

    New: Enables support for Playbook in CSM Configurable Workspace. Agents can use the simplified Playbook UI experience in Workspace to update records and complete tasks across multiple workflow activities.

-   **Version 1.0.5 - December 2020**

    Changed: Replaced the mailinator.com domain with example.com in the application demo data.

-   **Version 1.0.1 - July 2020**

    New: Use the ServiceNow® Case Playbook for Complaints to manage the process for handling customer complaints. This playbook provides an end-to-end life cycle for the tasks performed during the complaint handling process, from the time a complaint is logged to the final resolution and communication to the customer.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

