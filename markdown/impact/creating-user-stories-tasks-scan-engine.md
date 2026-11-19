---
title: Create user stories and tasks for Scan Engine
description: Generate user stories from open or resolved findings to help resolve technical debt. Create tasks from Open Findings to track remediation work. Create tasks from Resolved Findings when you've already fixed issues, but want to document the work in your project management system retroactively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/creating-user-stories-tasks-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Create user stories and tasks for Scan Engine

Generate user stories from open or resolved findings to help resolve technical debt. Create tasks from Open Findings to track remediation work. Create tasks from Resolved Findings when you've already fixed issues, but want to document the work in your project management system retroactively.

## Before you begin

Role required: admin

**Note:** The Scan Engine integrates with agile project management tools, including Azure DevOps and ServiceNow Agile development. For information on configuring integration properties to automatically create work items from findings, see [User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/user-story-integration-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health**, and then select one of the following:

    -   **Open Findings**
    -   **Resolved Findings**
2.  Select the **Short Description** of the record of the finding you want to generate a story or task from.

3.  On the finding record, select **Create Task** in the form header or from the **Related Links**.

    The dialog displays integration-specific fields. For Azure DevOps, these are **Organization**, **Project**, and **Work Item Type**. These values are populated from your integration configuration.

4.  Select **Submit**.

    A work item is created in the configured destination, Azure DevOps or ServiceNow Agile Development \(stories/tasks tables\). A reference link is stored on the finding record.

5.  To create tasks from multiple findings, in the Open Findings or Resolved Findings window, select the findings that you want to create a story or task for, and then select **Create Task**.

    Ensure that all the findings you select are appropriate for the same project. The system processes bulk requests asynchronously for large selections.


Perform or validate the following if you experience one of the related issues:

-   **If user story or task creation fails, validate:**
    -   Your integration credentials are valid
    -   The target project exists and is accessible
    -   All required fields are configured.
-   **If the __Create Task__ button is missing:**

    -   Assign the `sn_se.scan_engine_admin` role to users who need to assign tasks or create user stories in Scan Engine. Alternatively, update the WRITE ACL on `sn_se_finding` to include `sn_se.scan_engine_user` if broader write access is acceptable.
    -   As an admin, on the instance where Scan Engine runs and the findings are generated, configure User Story Integration.
        -   Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine** &gt; **Properties** by setting the required fields for your integration type \(for example, `user_story_table` for ServiceNow, or the relevant fields for Azure DevOps\).
        -   For ServiceNow integrations, define the source and target instances in My SN Instances on the instance where the findings are generated. The target production instance needs a record with environment set to Production and valid credentials. Otherwise, task creation silently fail. See [Register your instance in My SN Instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/register-your-instance.md) for details.
    After these steps are completed, the **Resolution** tab fields are available and the **Create Task** button functions as expected.


You can view your created tasks through the **External References** related list on the finding record.

**Related topics**  


[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/user-story-integration-properties.md)

