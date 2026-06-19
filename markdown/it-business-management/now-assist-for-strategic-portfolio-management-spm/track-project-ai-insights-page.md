---
title: Generate and track project details from AI insights page
description: Generate and monitor project insights directly from AI insights page in Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/now-assist-for-strategic-portfolio-management-spm/track-project-ai-insights-page.html
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate and track project details from AI insights page

Generate and monitor project insights directly from AI insights page in Project Workspace.

## Before you begin

Verify that the Project insights generation skill is active.

Role required: it\_project\_manager

## Procedure

1.  Open a project from the home page of Project Workspace.

    For information, see [Access the new Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/access-new-project-workspace.md).

2.  Open AI insights page by selecting **AI insights** from the list.

3.  Select **Generate insights** to generate AI insights of your project.

    \[Omitted image "ai-insights-page-project-workspace.png"\] Alt text: AI insights page in Project Workspace.

    Project insights are generated using the same Project insights generation skill used for email insights. Insights are displayed directly in the in‑app AI insights experience.

4.  Review the generation project insights.

    -   Project insights
    -   Executive summary
    -   Overall project health
    -   RAG


    The generated status report presents detailed health indicators along with supporting rationale to help you understand the current state of the project. You can review schedule variance information to identify delays and the sub‑indicators affecting progress, and view project status explanations that highlight recent achievements and issues requiring immediate attention. Additional sections can be expanded for deeper analysis. The report also includes schedule health to assess progress against planned timelines and thresholds, and budget and cost status to verify that financials remain within limits.


## Result

The project insights are generated from the AI insights page with access to current project insights in a single in‑app view.

## What to do next

-   Modify the project insights admin configurations:
    1.  Navigate to **All** and type `sn_spm_gen_ai_insight_topic.list` and press enter to open the configuration table.\[Omitted image "insight-topics-table.png"\] Alt text: Insights topic configuration table.
    2.  Locate the topic you want to update from the Topic name column.
    3.  Double-click \(or use the keyboard shortcut\) the Default topic config field to edit the required topic.
    4.  Update the values for threshold or critical state or time ranges according to your requirement.
    5.  Select the check mark or press enter to save the changes.
-   View and reuse stored insights:
    -   Generated insights are stored and reused based on a defined date threshold.
    -   When you revisit the AI Insights page, previously generated insights are displayed if they are still within the threshold.
-   Regenerate project insights:
    -   From the AI insights page, select **Regenerate** icon.
    -   Now Assist generates updated project insights.

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-now-assist-for-spm.md)

