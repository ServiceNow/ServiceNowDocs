---
title: Auto Resolve De-Duplication tasks
description: Use the CMDB Duplicate CI Agent in ServiceNow Otto to automatically identify, analyze, and resolve multiple duplicate CIs using AI based recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-dedup-task.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 2
breadcrumb: [Using AI agents, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Auto Resolve De-Duplication tasks

Use the CMDB Duplicate CI Agent in ServiceNow Otto to automatically identify, analyze, and resolve multiple duplicate CIs using AI based recommendations.

## Before you begin

For more information on what duplicate CIs are, see the [Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md) topic.

Role required: cmdb\_dedup\_admin

## About this task

This agent analyzes duplicate CIs and generate recommendations covering CI selection, attribute conflict resolution, and relationship merging. Administrators can review and approve recommendations in configurable batches before execution, or configure templates to auto-resolve duplicates without manual intervention.

The CMDB Duplicate CI Agent identifies duplicate CIs and groups them into similar classes and internally uses the [De-Duplication Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/configuration-management-database-cmdb/dedup-ci-exp-cmdb-workspace.md) framework along with the [De-Duplication Task Resolution Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-dupe-task-resolution.md) skill to resolve the duplicates automatically.

**Note:** To experience a smoother procedure with the agent, avoid running manual templates at the same time.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CMDB Workspace**.

2.  Under the Management tools section and the Optimize section, select **CMDB success advisor**.

3.  In the Duplicate CIs panel or Duplicate CIs number table, select **Ask Otto**.

    The ServiceNow Otto panel opens.


## Show AI Recommendations, Track Progress, and Update Settings

The following example follows how users can use ServiceNow Otto to determine whether the AI recommendations are optimal choices to resolve de-duplication tasks.

**Note:** A group is a class. The agent will internally analyze and categorize the duplicate CIs based on their classes into what is organized into groups.

1.  The following image shows the beginning of the agent prompt that opens. The agent automatically organizes the duplicate CIs by group such as Servers, Hardware, Window Servers, etc. Select one of the following:

    -   Show me groups ready for review - This displays all the groups and their duplicate CIs and presents them as a subset of groups for review.
    -   Track progress
    -   Update settings
    \[Omitted image "na-cmdb-dedup-main-options.png"\] Alt text: Main options.

2.  The Duplicate CIs prompt shows up. Select one of the following:

    1.  Accept, apply all recommendations. If the agent is satisfactory across multiple duplicate CIs,to apply all the changes automatically.
    2.  Reject, don't show this group again. To reject recommendations and not see the group.
    3.  Skip for now. To skip the group.
    \[Omitted image "na-cmdb-dedup-ai-recs-ci-class.png"\] Alt text: Duplicate CIs.

    Select the Main CI name to see the de-duplication summary and review.

    \[Omitted image "na-cmdb-dedup-ai-recs-individual-ci.png"\] Alt text: De-duplication summary.

    To override AI recommendations, you can select the \[Omitted image "na-cmdb-dedup-expand-icon.png"\] Alt text: Expand icon.Expand icon.

3.  In ServiceNow Otto, enter `Track Progress` to track the duplicate CI resolution progress of the class. Select one of the following:

    -   Show me groups ready for review
    -   Track progress
    -   Update settings
    The groups are organized based on their automation status and select a group to view the progress of the group.\[Omitted image "na-cmdb-dedup-track-ci-class.png"\] Alt text: Track CI progress.

4.  When you select **Update settings**, you can customize which groups you want to show or hide, the automation status, and other properties in the settings. \[Omitted image "na-cmdb-dedup-update-settings.png"\] Alt text: Update Settings.


