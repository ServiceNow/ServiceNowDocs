---
title: Auto Resolve De-Duplication tasks
description: Use the CMDB Duplicate CI Agent in ServiceNow Otto to automatically identify, analyze, and resolve multiple de-duplication tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-dedup-task.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 1
breadcrumb: [Using AI agents, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Auto Resolve De-Duplication tasks

Use the CMDB Duplicate CI Agent in ServiceNow Otto to automatically identify, analyze, and resolve multiple de-duplication tasks.

## Before you begin

For more information on what de-duplication tasks are, see the [Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md) topic.

Role required: cmdb\_dedup\_admin

## About this task

The CMDB Duplicate CI Agent uses the de-duplication templates framework and assistant skill to resolve the duplicates automatically.

**Note:** To experience a smoother procedure with the agent, avoid running manual templates at the same time. To manually resolve de-duplication tasks, see the [Remediate a de-duplication task \(manual\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/reconcile-dup-task.md) topic.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CMDB Workspace**.

2.  Under the Management tools section and the Optimize section, select **CMDB success advisor**.

3.  In the Duplicate CIs panel or Duplicate CIs number table, select **Ask Otto**.

    The ServiceNow Otto panel opens.


## Show AI Recommendations, Track Progress, and Update Settings

The following example follows how users can use ServiceNow Otto to determine whether the AI recommendations are optimal choices to resolve de-duplication tasks.

1.  The following image shows the beginning of the agent prompt that opens. The agent automatically organizes the duplicate CIs by group such as Servers, Hardware, Window Servers, etc. Select one of the following:

    -   Accept, all recommendations
    -   Reject, don't show this group again
    -   Skip for now
    \[Omitted image "na-cmdb-dedup-main-options.png"\] Alt text: Main options.

2.  Select the Main CI name to see the de-duplication summary and review.\[Omitted image "na-cmdb-dedup-ai-recs-individual-ci.png"\] Alt text: De-duplication summary.

    To retire and archive duplicate CIs, you can select the \[Omitted image "na-cmdb-dedup-expand-icon.png"\] Alt text: Expand icon.Expand icon to manually retire and archive the CIs.

    \[Omitted image "na-cmdb-dedup-ai-recs-ci-class.png"\] Alt text: Duplicate CIs.

    If the agent is satisfactory across multiple duplicate CIs, select **Accept, apply all recommendations** to apply all the changes automatically.

3.  In ServiceNow Otto, enter `Track Progress` to track the duplicate CI resolution progress of the class. Select one of the following:

    -   Show me groups ready for review
    -   Track progress
    -   Update settings
    \[Omitted image "na-cmdb-dedup-track-ci-class.png"\] Alt text: Track CI progress.

4.  When you select **Update settings**, you can customize which groups you want to show or hide, the automation status, and other properties in the settings. \[Omitted image "na-cmdb-dedup-update-settings.png"\] Alt text: Update Settings.


