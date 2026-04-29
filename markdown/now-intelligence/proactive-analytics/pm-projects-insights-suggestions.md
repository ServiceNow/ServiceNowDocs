---
title: Creating Process Mining projects from Proactive Analytics suggestions
description: If you are using Proactive analytics with Process Mining, Proactive analytics can suggest new Process Mining projects. A single click from a suggestion creates and runs the project.If your instance meets the requirements, you can create Process Mining projects from Suggestions cards in your Insights panel. Such projects generate their own insights.
locale: en-US
release: australia
product: Proactive Analytics
classification: proactive-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Insights on dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Creating Process Mining projects from Proactive Analytics suggestions

If you are using Proactive analytics with Process Mining, Proactive analytics can suggest new Process Mining projects. A single click from a suggestion creates and runs the project.

An IT process owner might benefit from a Process Mining project that has not yet been created. If they are following their processes through indicators shown on a Platform Analytics dashboard, this feature can suggest Process Mining projects to create.

The feature works through a scheduled job, PA Indicator Recommendations. This job scans Performance Analytics indicators for anomalous behavior in the last 15 days and correlates that behavior against a set of variables to generate a score, which it stores on the par\_indicator\_model table. The job weighs the scores against the number of dashboards that each indicator is used in, then generates suggestions for the indicators with the three highest results. A single interaction with a suggestion creates a Process Mining project and generates insights based on that project. However, several requirements must be met.

## Requirements on the dashboard side

-   The DA Process Mining Insights plugin must be installed.
-   On each relevant dashboard, Process Mining insights must be turned on.
-   The relevant dashboard viewers must have the sn\_process\_optimization\_analyst role.

## Requirements for the suggestions to be created

-   The facts tables for the relevant indicators must be set up to generate audit logs. For more information, see [Configuring auditing for a table](https://www.servicenow.com/docs/access?context=t_EnableAuditingForATable&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   A process configuration must exist for the facts tables of the relevant indicators. For more information, see [Create process configuration using Classic view](../../../administer/process-mining/task/create-process-config.md).
-   A template project with table configurations specific to the facts table of the indicators should exist. To create such a project, see [Create a project or template using Project Builder](../../../administer/process-mining/task/define-workflow-model.md).

## Requirements for insights to be created from the new project

Automated finding definitions must exist within the relevant process configurations, to ensure that the indicators are linked through the **Impacted KPIs** field. For more information, see [Configuring improvement opportunities](../../../administer/process-mining/concept/configuring-finding-definitions.md).

**Related topics**  


[Dashboards in Platform Analytics](analytics-center-dashboards.md)

## Create a process mining project from a suggestion

If your instance meets the requirements, you can create Process Mining projects from Suggestions cards in your Insights panel. Such projects generate their own insights.

### Before you begin

Role required: sn\_process\_optimization\_analyst

### Procedure

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the relevant Platform Analytics dashboard.

3.  Select **Insights** to open the Insights panel.

    Insights are not available in responsive dashboards, including ones that have been migrated to Platform Analytics in compatibility mode.

4.  Open the Suggestions tab and review the suggestions.

    ![Suggestions tab in the Insights panel, showing a suggestion.](../image/insights-suggestions.png)

5.  In each suggestion, select all the indicators for which you want to create Process Mining projects.

    ![Suggestion card with an indicator selected.](../image/insights-selected-suggestions.png)

6.  Start the process analysis.


### Result

The system generates and runs the Process Mining project. You can follow the progress in the Suggestion card. When the process is complete, the Suggestion provides a link to any insights that the project created.

![Suggestion card showing that the suggested project has been run.](../image/insights-promin-project-complete.png)

If you select **See insights**, you see the cards for the insights that the project created. From such an insight card, you can open the Process Mining Analyst Workbench for the project.

![Insights card generated from Process Mining project created from a suggestion.](../image/insights-promin-generated.png)

