---
title: Generate a project status report with Now Assist
description: Generate an AI‑assisted project status report with predicted health indicators. Now assist pre-populates project health, an executive summary, and supporting rationale based on weekly project data.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate a project status report with Now Assist

Generate an AI‑assisted project status report with predicted health indicators. Now assist pre-populates project health, an executive summary, and supporting rationale based on weekly project data.

## Before you begin

Ensure project status generation skill is active.

Role required: it\_project\_manager

## About this task

When the Project status generation skill is enabled, project managers can generate a status report pre‑populated by Now Assist. Now Assist predicts overall and dimension‑level project health \(such as schedule, cost, resources, and scope\), generates an executive summary using weekly project data, and provides a rationale for each prediction.

After generation, project managers can review:

-   Predicted overall health
-   Predicted dimension statuses
-   Explanation/rationale text for each prediction in analysis sections
-   Executive summary text generated from the project’s recent data

After submission, the same information appears in the report view, including rationale text \(for example, a rationale/status explanation column\).

## Procedure

1.  Open a project from the home page of Project Workspace.

    For information, see [Access the new Project Workspace](../../project-workspace/task/access-new-project-workspace.md).

2.  Open the Status reports page of the project by selecting **Status Reports** from the list.

3.  From the Pages section, select **Generate status report**.

    You can create an AI status report from an existing template using **Generate from template**. To display AI-generated field data in the document, the template must include dynamic tokens. Without dynamic tokens, only the executive summary is displayed in the status report document.

    The system invokes LLM to pre-populate the form with predicted fields and an executive summary.

4.  Review the AI-generated fields:

    ![AI-generated status report in Project Workspace.](../images/ai-generated-status-report.png)

    -   Overall health \(predicted\)
    -   Dimension health such as schedule/cost/resources/scope \(predicted\)
    -   Executive summary \(generated from project data for the reporting period\)
    -   Rationale/analysis sections explaining each prediction \(for example, schedule health analysis, cost health analysis\).
    Overall status analysis is displayed in bullet points with highlighted key values and color coding based on the LLM response. The bullet point format with highlighting and coloring applies to all individual health sections such as AI scope health analysis, AI schedule health analysis and so on. The same format appears in the saved status report document.

    A new Project health analysis column has been added to the project workspace list view. When you publish an AI status report, the health analysis rolls up to the project level and appears in this column. If you publish a standard status report \(non-AI\), the project health analysis column is cleared.

5.  Edit any fields as needed.

6.  Select **Submit**.

7.  Verify the submitted report.

8.  Select **Now Assist** to ask more questions on the generated status report or select **Summarize** to generate a short summary of generated report.

    You can export and edit the AI‑generated status report. You cannot duplicate an AI‑generated status report.


## Result

An AI-assisted status report is generated with predicted health values, an executive summary, and rationale text.

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

