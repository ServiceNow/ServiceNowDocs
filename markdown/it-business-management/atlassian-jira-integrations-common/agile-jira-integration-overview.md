---
title: Atlassian Jira Integration for Agile Development
description: Enable bidirectional synchronization of records between Atlassian Jira and ServiceNow Agile Development by integrating the two applications.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Strategic Portfolio Management]
---

# Atlassian Jira Integration for Agile Development

Enable bidirectional synchronization of records between Atlassian Jira and ServiceNow® Agile Development by integrating the two applications.

If the source of your work is in the ServiceNow platform while the progress of the work is tracked in Jira, you can perform integrated tracking of your product development efforts by integrating Agile Development 2.0 with Jira.

For example, if you update a record in Jira, you can find that update in Agile Development 2.0. Similarly, if you update a record in Agile Development 2.0, you can find the same update in Jira.

When you synchronize Jira with Agile Development 2.0, you can:

-   View available Jira projects and boards in Agile Development 2.0.
-   Perform a bulk import of records from Jira to Agile Development 2.0.
-   Perform single record updates between Jira and Agile Development 2.0.
-   Avoid duplicating record update entries in Jira and Agile Development 2.0.
-   Plan, track, and update your tasks from a single application.

Starting with version 1.1.1, Atlassian Jira Integration for Agile Development 2.0 supports map configuration at the project level and not at the instance level. Also, the application supports the following project types associated with Jira Cloud and Jira Server:

-   Classic
    -   Scrum
    -   Kanban
    -   Bug tracking
-   Next-gen
    -   Scrum
    -   Kanban

**Note:** Integration with Jira Data Center, Jira Align and other Atlassian products is not available.

## Importing issues from Kanban projects in Jira

Before importing Jira projects that are of the Kanban type, consider the following notes:

-   Issues such as epics and stories are imported to Agile Development 2.0
-   If your Kanban project has one or more Jira Boards, not all those Boards would be mapped to distinct Agile groups. The Jira project is mapped to a single group in Agile Development 2.0 and all issues of this project, regardless of their association to boards, would be assigned to one Agile group.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Components installed with Atlassian Jira integration for Agile Development](../task/components-installed-with-atlassian-jira-integration-for-agile-development.md)**  
Several types of components are installed with activation of the Atlassian Jira integration for Agile Development application, including tables, user roles, and scheduled jobs.
-   **[Setting up the integration between Jira and Agile Development 2.0](../task/setting-up-the-integration-between-jira-and-agile-development.md)**  
Understand the setup process of Atlassian Jira Integration for Agile Development 2.0.
-   **[Importing and exporting issues between Agile Development 2.0 and Jira](../reference/import-export-issues-sn-jira-workflow.md)**  
Understand the workflow for the import and export of issues between Agile Development 2.0 and Jira.
-   **[Troubleshooting issues of Jira integration with Agile Development 2.0](../reference/agile-jira-integration-troubleshooting.md)**  
Resolve common issues that you might face while working with the integration of Jira and Agile Development 2.0.

**Parent Topic:**[Strategic Portfolio Management](../../it-business-management/reference/r_ITBusinessManagement.md)

