---
title: Process Automation Content release notes
description: Version history for the Process Automation Content application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-process-automation-content.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Process Automation Content release notes

Version history for the Process Automation Content application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 28.1.6 - May 2026 \(Zurich\)**

    Fixed: Ad-hoc Approval handles custom date/time formatting and still renders the activity in the Playbook- Better support for Japanese language when using the mini activity picker

-   **Version 28.1.5 - March 2026 \(Zurich\)**

    Changed: Updated description for New Record Form with List

-   **Version 28.1.3 - August 2025 \(Zurich\)**
    -   Changed:
        -   Updated the View Approval Request Activity Definition
        -   Renamed Create Records to New Record Form with List
        -   Renamed Show List of Records to Record List
        -   Renamed Ad Hoc Approval to Ask for Ad Hoc Approval
        -   Renamed Request Manager Approval to Ask for Manager Approval
        -   Renamed Request Multi-Level Approval to Ask for Multi-Level Approval
-   **Version 27.0.3 - March 2025 \(Yokohama\)**

    Fixed: Made the Open List declarative action visible on the Show List of Records activity.

-   **Version 27.0.1 - February 2025 \(Yokohama\)**

    Changed: Improved accessibility, usability, and performance of the list function in the Create Records activity definition.

-   **Version 26.0.2 - August 2024 \(Xanadu\)**
    -   Changed:
        -   Moved into the "Common" section of the activity picker:
            -   Show List of Records
            -   Request Ad Hoc Approval
            -   Create Records
        -   Updated all out-of-the-box activity definitions to be read-only
        -   Categorized the following activities as "Interactive" instead of "Default" in the activity picker:
            -   Create Records
            -   View Approval Records
            -   Request Manager Approval
            -   Request Multi-Level Approval
            -   Request Ad Hoc Approval
    -   Fixed:
        -   Added missing Restart declarative actions back to some out-of-the-box activities.
        -   Updated custom Activity UIs from hardcoded use of the Global Playbook Experience to correct mapping.
        -   Fixed the list query in custom activity UIs.
    -   Removed:
        -   Removed the following activities from the activity picker:
            -   Create Child Case
            -   Create Child Task
            -   Update Record
            -   These activities still function in existing playbooks, but are no longer available to choose when configuring an activity. Use the Create Record activity in place of the Create Child Case and Create Child Task activities, and use the User Form and Automated Update Record activities in place of the Update Record activity.
-   **Version 25.1.3 - August 2024 \(Washington DC\)**
    -   Fixed:
        -   Added missing Restart declarative actions back to some out-of-the-box activities.
        -   Re-organized activities within the activity picker.
        -   Corrected the description of the Show List of Records activity definition.
-   **Version 25.1.1 - February 2024**
    -   Changed:
        -   These activities will now cancel when a process/playbook is canceled:
            -   Request Manager Approval
            -   Request Ad Hoc Approval
            -   Request Multi-Level Approval
-   **Version 23.0.5 - August 2023 \(Utah\)**

    Changed: For the Update Record activity, show the **Table**, **Record**, **Fields**, and **Wait for user input** fields in the Standard Modal and Side Panel.

-   **Version 23.0.3 - February 2023**
    -   New: Create Records out-of-the-box activity
    -   Changed:
        -   The Show List of Records out-of-the-box activity is now part of the store app instead of the PAD Core plugin.
        -   The Update Records out-of-the-box activity is now part of the store app instead of the PAD Core plugin.
        -   This app will now be installed with Playbook Experience.
-   **Version 22.0.4 - August 2022**

    The Process Automation Content app provides out of the box activity definitions, enabling developers to define connected, enterprise process automation with no code.


