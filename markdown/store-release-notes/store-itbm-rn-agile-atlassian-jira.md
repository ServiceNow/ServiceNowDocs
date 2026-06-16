---
title: Atlassian Jira integration for Agile Development release notes
description: Version history for the Agile Development Atlassian Jira integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-agile-atlassian-jira.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Atlassian Jira integration for Agile Development release notes

Version history for the Agile Development Atlassian Jira integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.5 - March 2026**

    The Agile Jira Integration now supports OAuth 2.0 authentication for custom Jira applications, providing a more secure and robust connection.

-   **Version 2.3.0 - December 2025**

    Performance improvements.

-   **Version 2.2.2 - September 2025**

    Fixed: For Jira server-based instances, the error with the Validate and fix mappings related link at the project level is fixed.

-   **Version 2.2.1 - June 2025**
    -   Fixed:
        -   Resolved an issue where board and sprint import requests were not completing successfully when triggered with the latest environment.
        -   Enhanced functionality to support mapping for user reference fields, ensuring consistent data synchronization.
        -   When a choice map is removed from status field map, epic record is not syncing to jira.
        -   Resolved Worknotes is being duplicated when cyclic payload check is failing.
        -   Updated error message when selecting Jira board for kanban project in Team Integration Settings.
-   **Version 2.2.0 - November 2024**

    Fixed: Minor fixes related to syncing comments and sprints with Jira.

-   **Version 2.1.6 - September 2024**

    Fixed: Jira createmeta Rest Endpoint deprecated changes.

-   **Version 2.1.5 - May 2024**

    Minor fixes related to security and features.

-   **Version 2.1.4 - February 2024**

    Minor fixes related to performance.

-   **Version 2.1.3 - May 2023**
    -   Bi-directional sync is now supported for Assigned\_to field.
    -   Import of comments from JIRA Cloud to ServiceNow is also supported.
    -   Issue related to creation of duplicate records has been fixed.
    -   Other minor fixes.
-   **Version 2.1.2 - December 2022**

    Fixed: Bug fixes

-   **Version 2.1.1 - February 2022**

    Fixed: Bug fixes

-   **Version 2.1.0 - June 2021**
    -   Changed:
        -   Support for multi-select fields in Jira integration.
        -   Support for reference field in Jira integration. I
        -   mproved troubleshooting and updated log details.
        -   Support for configuring the batch size to retrieve Jira project metadata.
-   **Version 2.0.2 - April 2021**
    -   Fixed:
        -   Import of Comments not working from Jira Servier and Jira Cloud
        -   Import fails while importing Stories associated with Sprints in Jira Cloud
        -   Flows stuck in Processing State when import fails from Jira
-   **Version 2.0.1 - September 2020**

    Changed: Simplified the process of importing issues from Jira into the ServiceNow platform. Jira projects now do not require project/team integration settings with assignment groups to import issues into Agile Development 2.0.

-   **Version 1.1.1 - July 2020**
    -   New:

        -   Jira Cloud support: You can synchronize the following Jira Cloud projects with the ServiceNow platform:
            -   Classic
                -   Scrum
                -   Kanban
                -   Bug tracking
            -   Next-gen
                -   Scrum
                -   Kanban
        -   Project-level mappings: Table, field, and workflow state mapping are supported at the project level.
        Project-level mappings: Table, field, and workflow state mapping are supported at the project level.

    -   Changed:
        -   Instance-level mapping: Mapping configuration for Jira projects is no longer generated at the instance level.
-   **Version 1.0.2 - March 2020**
    -   New: This app is compatible with New York
    -   Fixed: Minor bugs
-   **Version 1.0.1 - January 2020**

    Integrate Atlassian Jira with ServiceNow Agile Development to enable bi-directional synchronization of records between the two applications.


**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

