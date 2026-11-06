---
title: Create user stories and tasks for Scan Engine
description: Generate user stories from open or resolved findings to help resolve technical debt.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/creating-user-stories-tasks-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Create user stories and tasks for Scan Engine

Generate user stories from open or resolved findings to help resolve technical debt.

## Before you begin

Role required: admin

**Note:** The Scan Engine integrates with Agile project management tools, including Jira, Azure DevOps, and ServiceNow Agile development. For information on configuring integration properties to automatically create work items from findings, refer to [User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/user-story-integration-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health**, and then select one of the following:

    -   **Open Findings**
    -   **Resolved Findings**
    Create tasks from Open Findings to track remediation work. Create tasks from Resolved Findings when you've already fixed issues, but want to document the work in your project management system retroactively.

2.  To open the record of the finding you want to generate a story or task from, select its Short Description.

3.  On the finding record, select **Create Task** in the form header or from the **Related Links**.

    The dialog displays integration-specific fields. For Jira, these are **Organization**, **Project**, and **Issue Type**. For Azure DevOps, they are **Organization**, **Project**, and **Work Item Type**. These values are populated from your integration configuration.

4.  Select **Submit**.

    A work item is created in the configured destination, either Jira, Azure DevOps, or ServiceNow Agile Development \(stories/tasks tables\). A reference link is stored on the finding record.

5.  To create tasks from multiple findings, in the Open Findings or Resolved Findings window, select the findings that you want to create a story or task for, and then select **Create Task**.

    Ensure that all the findings you select are appropriate for the same project. The system processes bulk requests asynchronously for large selections.


-   **If user story or task creation fails, validate the following:**
    -   Your integration credentials are valid
    -   The target project exists and is accessible
    -   All required fields are configured.
-   **The __Create Task__ button is missing:**

    -   Assign the `sn_se.scan_engine_admin` role to users who need to assign tasks or create user stories in Scan Engine. Alternatively, update the WRITE ACL on `sn_se_finding` to include `sn_se.scan_engine_user` if broader write access is acceptable.
    -   As an admin, on the instance where Scan Engine runs and the findings are generated, configure User Story Integration in **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine** &gt; **Properties** by setting the required fields for your integration type \(for example, `user_story_table` for ServiceNow, or the relevant fields for Jira/Azure\).
    -   For ServiceNow integration, define the source and target instances in My SN Instances on the instance where the findings are generated. The target production instance needs a record with environment set to Production and valid credentials. Otherwise, task creation silently fail.
    After these steps are completed, the **Resolution** tab fields are available and the **Create Task** button functions as expected.


You can view your created tasks through the **External References** related list on the finding record.

**Related topics**  


[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/user-story-integration-properties.md)

