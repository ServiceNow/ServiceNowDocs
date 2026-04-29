---
title: Reviewing your Agentic AI assessment
description: This automated assessment process evaluates potential implementation impacts and provides actionable insights for agentic AI in Now Assist for IT Service Management \(ITSM\) and Now Assist for Customer Service Management \(CSM\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Use, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Reviewing your Agentic AI assessment

This automated assessment process evaluates potential implementation impacts and provides actionable insights for agentic AI in Now Assist for IT Service Management \(ITSM\) and Now Assist for Customer Service Management \(CSM\).

Navigate to **Workspaces** &gt; **Now Assist Readiness Evaluation** and select the agentic AI assessment icon ![](../image/agentic-ai-icon.png) to review your agentic AI assessment.

**Note:** Before viewing your agentic AI assessments, you must first have run the scheduled job to get the assessment results. If you haven't run your scheduled jobs, you are prompted to do so on an individual job level. For more information on running scheduled jobs, see [Run the GenAI/AgenticAI Assessment scheduled job](../task/run-genai-agenticai-assessment-scheduled-job.md).

The summary tab provides a consolidated summary of overall findings along with summarization and resolution notes for ITSM and CSM. The results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.

To better understand the estimated remediation effort, select the **Legends** button. The legend shows the estimated remediation effort using sizing verbiage and colors, along with an estimated timeline of remediation in development days. The legend also includes descriptions of the icons found next to the assessment questions.

![Legends button displays estimated remediation efforts such as None, Small, Medium, Large, XL, or XXL, and also includes icon descriptions.](../image/legends.png "Example of Legends estimated remediation effort sizing")

After reviewing the summary, select the individual assessment tabs to review those specific assessments. The questions for each assessment differ. For example, the questions and answers on the **Agentic AI - ITSM** assessment are different than the questions and answers on the **Agentic AI - CSM** assessment.

**Note:** The assessments gather information from tables. To view any of the tables' available questions, answers, assessments, or assessment run successes or failures, search for the applicable table in the navigation filter:

-   Questions \[sn\_assess\_question\] table
-   Answers \[sn\_assess\_answer\] table
-   Assessment \[sn\_assess\_assessment\] table
-   Assessment Run \[sn\_assess\_assessment\_run\] table

For more information about how to search for tables in the navigation filter, see [Navigate directly to a table](https://www.servicenow.com/docs/access?context=t_NavigateDirectlyToATable&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

The assessments include visual indicators to guide you on non-blocker and blocker results. The following list details the descriptions of the assessment's visual indicators:

-   ![](../image/green-check-icon.png): Informational area and no further action needed.
-   ![](../image/red-check-icon.png): Further action is needed to resolve findings before implementation. These required areas include estimated remediation efforts.
-   ![](../image/yellow-warning-icon.png): Recommended area warning, but the finding should be evaluated before implementation. These recommendations are observations that should be reviewed prior to implementation but no estimated remediation effort is provided.

You can select **Download Report** to export the entire agentic assessment report in PDF format from the Summary tab. The exported report still includes hyperlinks to the specific individual assessments. Selecting **Download Report** on an individual assessment downloads only that report in PDF format. After selecting a hyperlink in the PDF, that record or table opens in a separate browser tab.

**Note:** You don’t have to select **Download Report** to work directly with the problematic records or tables found in the assessment. Each assessment includes hyperlinks to the records or tables that need attention. Selecting a hyperlink opens the record or table in a separate browser tab.

![The Agentic AI - ITSM assessment is shown and includes the relevant questions and records.](../image/nare-agentic-ai-assessment-itsm.png "Example of the Agentic AI - ITSM assessment")

After reviewing the assessment and making the suggested assessment changes, rerun your scheduled jobs to see how your results improve. For more information on rerunning a specific job or all jobs, see [Run the GenAI/AgenticAI Assessment scheduled job](../task/run-genai-agenticai-assessment-scheduled-job.md).

