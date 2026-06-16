---
title: Security Incident Response UI release notes
description: Version history for the Security Operations Security Incident Response UI on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-ui.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response UI release notes

Version history for the Security Operations Security Incident Response UI on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.4.10 - November 2024**

    Fixed: Users were experiencing session timeouts on the Security Incident Response page even while they are active.

-   **Version 11.4.8 - October 2024**

    Fixed: Security Incident Response plugin writing invalid queries.

-   **Version 11.4.7 - September 2024**

    Fixed: Cancelling a Security Incident Task/ Performing a Cancel task UI action was incorrectly marking State as Closed Complete instead of Cancelled.

-   **Version 11.4.4 - May 2024**

    Fixed: Security incident response task is not transferrable to different assignment groups from that on the parent SIR.

-   **Version 11.4.3 - February 2024**

    Changed: Upgraded dependent library package from version 2.18.1 to 2.29.4.

-   **Version 11.4.2 - November 2023**

    Fixed: Duplicate activities show up in the Timeline section of the new UI.

-   **Version 11.3.16 - June 2023**

    Fixed: The SIR UI displays the wrong date when the user modifies the profile date format.

-   **Version 11.3.15 - May 2023**
    -   Changed:
        -   Uncontrollable package for new UI.
        -   Demo data reduction.
-   **Version 11.3.13 - March 2023**
    -   Fixed:
        -   SIR UI shows the wrong date when the user has modified the profile date format
        -   Project Atkins: Migrate scoped app packaging to new parent POM to remove duplicated content.
-   **Version 11.3.12- December 2022**

    Fixed: Users who do not have access to security incidents are able to modify the incident fields.

-   **Version 11.3.9 - November 2022**

    Changed: Updated Oracle React plugin versions.

-   **Version 11.3.5 - July 2022**
    -   Fixed:
        -   Security Incident \(New UI\) work-space is displaying dates incorrectly when the time format is 'hh:mm:ss a' \(AM/PM format\)
        -   Slow searching on certain reference fields
-   **Version 11.3.4 - March 2022**
    -   Fixed:
        -   Non-admin user is unable to view tasks in the Playbook
        -   Close code choices are invisible in the SIR NEW UI.
-   **Version 11.3.0 - November 2021**
    -   Fixed:
        -   The worknotes are empty in the SIR new UI in the Incident timeline when it's filtered to display only worknotes.
        -   Cancel option is not seen for all the non-owner users.
        -   When a security incident gets mapped with "Security Incident - Phishing - Template V2" Workflow then name is not displayed on the new UI playbook section.
-   **Version 11.2.6 - August 2021**
    -   Fixed:
        -   Fixed an error which is displayed when the incident timeline loads an encrypted file.
        -   Updated playbook to get refreshed when the assignment group or assigned to fields are modified.
-   **Version 11.2.0 - February 2021**

    Changed: Removed read-only protection for all script includes.

-   **Version 11.2.0 - February 2021**

    Changed: Fixes related to accessibility, security, and data policies.

-   **Version 11.0.1 - November 2020**

    Changed: As part of the inclusive language initiative, words have been replaced with allow list and deny list respectively.

-   **Version 11.0.0 - September 2020**
    -   New:
        -   Post Incident Review Assessments change provides the configurations to define the assessment trigger conditions to generate both mandatory and optional assessments for specific security incidents.
        -   File type observable security change provides stringent security measures to store the suspicious files and enables the files type observables for sandbox integration.
-   **Version 10.4.3 - June 2020**
    -   New: Provided a feature for security analysts to select flow designer flows/playbooks from the Security Incident playbook section.
    -   Changed:
        -   Added the **Delete** action for all the related lists.
        -   Updated the related list configuration to avoid duplicate related list entries.
-   **Version 10.2.0 - April 2020**
    -   New:
        -   Administrator configurable related list and actions
        -   New form UI actions
    -   Changed:
        -   Incident timeline to display attachments and documents
        -   Simplified navigation
    -   Fixed:
        -   Persistence of filters
        -   Refresh data from latest actions
-   **Version 10.0.0 - March 2020**

    Fixed: Bug fixes.

-   **Version 9.0.0 - November 2019**
    -   New: User Reported Phishing 2.0 provides an updated way to ingest phishing emails. It includes email aggregation, email header extraction, and improved configuration capabilities.
    -   Fixed: Bug fixes
-   **Version 8.0.9 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Bug fixes
-   **Version 7.1.2 - May 2019**
    -   Additional Related Lists are now available for access in the UI
    -   Performance fixes to address slow page loading time
-   **Version 6.2.3 - April 2019**

    Fixed performance issue when loading the new UI.

-   **Version 6.1.0 - December 2018**
    -   Security Analyst Workspace: Use the tile-based Security Analyst Workspace to easily and efficiently perform day-to-day security analysis work. The customizable interface includes a peek feature for quickly browsing key incident details, and tools for rapidly transitioning from investigation to containment tasks.
    -   New in 6.1.0:
        -   Starting with Security Incident Response version 6.1.0, the Security Analyst Workspace is available only on the ServiceNow Store.
        -   You can create custom filters. Columns in lists and related lists can now be sorted and you can change the order of columns.
        -   You can create new security incident tasks and assign them from inside a security incident.
        -   You can add or remove tags in observables and security incidents. You can send email on the incident or task level, using predefined or blank templates.
        -   To use the Security Analyst Workspace, you must first upgrade to London Patch 3 and then install the Security Incident Response UI plugin \(com.app\_secops\_ui\) from the ServiceNow Store.
-   **Version 6.0.9 - November 2018**
    -   Security Analyst Workspace:
        -   Walk through the Security Incident Response setup process in a simple, step-by-step fashion. The Setup Assistant helps you discover which capabilities of Security Incident Response require configuration, identify what permissions are required to configure them, and learn what settings are recommended for your environment. Setup Assistant helps you deploy Security Incident Response quickly and efficiently.
        -   To use the Security Analyst Workspace, you must first upgrade to London Patch 3 and then install the Security Incident Response UI plugin \(com.app\_secops\_ui\) from the ServiceNow Store.

