---
title: Status reporting in Project Workspace
description: A status report in Project Workspace is a snapshot in time that gives an overview of your overall project health across key areas such as cost, resources, milestones, health, and more.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Status reporting in Project Workspace

A status report in Project Workspace is a snapshot in time that gives an overview of your overall project health across key areas such as cost, resources, milestones, health, and more.

Status reporting in Project Workspace video.

The Status reports in Project Workspace provide a comprehensive, configurable, and customizable view of the current state of a project by capturing and displaying key project metrics such as overall health, schedule, scope, cost, and resource utilization. Status reports help project teams and stakeholders track progress, identify risks, and manage any project-related issues in real-time.

|Metric|Description|
|------|-----------|
|Overall health|The general condition of the project \(green, yellow, or red\).|
|Completion status|The percentage of project completion.|
|Schedule and scope|Key milestones and any changes in scope.|
|Cost metrics|Planned and actual costs, and budget variance.|
|Resource utilization|Allocation and effort tracking for project resources.|

## Key benefits

The status report feature in Project Workspace provides a clear view of the project’s overall health, progress, and key metrics, confirming effective communication and tracking throughout the project life-cycle.

With status reports in Project Workspace, you can:

-   Gain improved project visibility by having a concise summary of key metrics such as schedule, cost, and resource utilization, enabling stakeholders to track the progress.
-   Facilitate better decision-making by providing a snapshot of the project’s current state, helping project managers and stakeholders address potential challenges.
-   Enhance risk management by highlighting any risks, issues, or variances, enabling teams to respond proactively to project concerns.
-   Maintain consistent communication across teams and stakeholders by delivering regular, standardized updates, confirming everyone stays informed about the project's progress and health.
-   Increase efficiency through the use of templates that streamline the creation of reports, saving time and confirming consistency across projects while enabling for customization as needed.

## Status report templates

Status report templates simplify the process of generating project updates by providing pre-defined structures, confirming consistency and saving time. Two default templates are available:

-   One Page Status Report: This template provides a concise one-page summary of key project metrics, making it ideal for quick updates where a high-level overview is sufficient.
-   Default Status Report: This template includes a more comprehensive range of data points, covering areas such as milestones, risks, issues, decisions, and change requests. It offers a detailed view of the project's progress and status, similar to a classic status report.

-   You can create a status report using one of the existing templates: [Create a status report in Project Workspace](../task/create-a-status-report-in-project-workspace.md)
-   You can also create your own status report template from scratch: [Create a status report template in Project Workspace](../task/create-a-status-report-template-project-workspace.md)

## Now Assist project status reports

AI status reports help project managers create project updates faster by generating health assessments, executive summaries, and supporting rationales based on project data and configured criteria. When enabled, the generate status report action creates a status report draft where AI pre-populates key fields:

-   Overall project health
-   Health by dimensions \(schedule/cost/resources/scope\)
-   Executive summary
-   Rationale/analysis for each predicted health value

This reduces manual effort and helps stakeholders quickly understand what changed and what needs attention.

## Now Assist project health prediction

Now Assist health outcomes \(such as red/yellow/green\) are determined by admin-configured criteria. The test plan for the feature specifically validates rules such as:

-   Including all dimensions \(schedule/cost/resource/scope\) in overall health rollups.
-   Handling missing/incomplete dimension configuration.
-   Rollup behavior like “overall = red if any dimension is red”.

**Parent Topic:**[Exploring Project Workspace](exploring-project-workspace.md)

**Related topics**  


[Analyze the status report in Project Workspace](../task/view-status-report-in-project-workspace.md)

[Import old project status report to Project Workspace](../task/import-old-status-reports.md)

[Add dynamic content to status report in Project Workspace](../task/add-dynamic-content-to-status-report-in-pw.md)

