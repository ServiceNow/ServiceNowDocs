---
title: Create user stories and tasks for Scan Engine
description: You can generate user stories from open or resolved findings to facilitate the resolution of technical debt.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Create user stories and tasks for Scan Engine

You can generate user stories from open or resolved findings to facilitate the resolution of technical debt.

## Before you begin

Role required: admin

**Note:** The Scan Engine integrates with Agile project management tools, including Jira, Azure DevOps, and ServiceNow Agile development. For information on configuring integration properties to automatically create work items from findings, refer to [User story integration](../concept/user-story-integration-properties.md).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health**, and then select one of the following:

    -   **Open Findings**
    -   **Resolved Findings**
    Create tasks from Open Findings to track remediation work. Create tasks from Resolved Findings when you've already fixed issues, but want to document the work in your project management system retroactively.

2.  To open the record of the finding you want to generate a story or task from, select its Short Description.

3.  On the finding record, select **Create Task** in the form header or from the **Related Links**.

    The dialog displays integration-specific fields. For Jira, these are **Organization**, **Project**, and **Issue Type**. For Azure DevOps, they are **Organization**, **Project**, and **Work Item Type**. These values are populated from your integration configuration.

4.  Select **Submit**.

    A work item is created in the configured destination, either Jira, Azure DevOps, or ServiceNow Agile Development \(stories/tasks tables\). A reference link is stored on the finding record.

5.  To create stories or tasks from multiple findings, in the Open Findings or Resolved Findings window, select the findings that you want to create a story or task for, and then select **Create Task**.

    Ensure that all the findings you select are appropriate for the same project. The system processes bulk requests asynchronously for large selections.


If user story or task creation fails, check and ensure the following:

-   Your integration credentials are valid
-   The target project exists and is accessible
-   All required fields are configured.

You can view your created tasks through the **External References** related list on the finding record.

