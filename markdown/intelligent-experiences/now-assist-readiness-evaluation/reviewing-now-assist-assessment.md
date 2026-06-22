---
title: Reviewing your Now Assist assessment
description: This automated assessment process evaluates potential implementation impacts and provides actionable insights for Now Assist products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-readiness-evaluation/reviewing-now-assist-assessment.html
release: zurich
product: Now Assist Readiness Evaluation
classification: now-assist-readiness-evaluation
topic_type: concept
last_updated: "2025-09-18"
reading_time_minutes: 3
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, agentic AI assessment]
breadcrumb: [Use, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Reviewing your Now Assist assessment

This automated assessment process evaluates potential implementation impacts and provides actionable insights for Now Assist products.

Navigate to **Workspaces** &gt; **Now Assist Readiness Evaluation** and select the assessment icon \[Omitted image "na-assessment-icon.png"\] Alt text: to review your Now Assist assessment.

**Note:** Before viewing your Now Assist assessments, you must first have run the scheduled jobs to get the assessment results. If you haven't run your scheduled jobs, you're prompted to do so on an individual job level. For more information on running scheduled jobs, see [Run the GenAI/AgenticAI Assessment scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-readiness-evaluation/run-genai-agenticai-assessment-scheduled-job.md) and [Configure the Now Assist Readiness Evaluation guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-readiness-evaluation/configure-nare-guided-setup.md).

The summary tab provides a consolidated summary of features, including Now Assist capabilities across AI Search, Virtual Agent \(VA\), IT Service Management \(ITSM\), Customer Service Management \(CSM\), and HR Service Delivery \(HRSD\), as well as their corresponding estimated remediation efforts. The results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.

To understand the estimated remediation effort, select the **Legends** button. The legend shows the estimated remediation effort using sizing verbiage and colors, along with an estimated timeline of remediation in development days. The legend also includes descriptions of the icons found next to the assessment questions.

\[Omitted image "legends.png"\] Alt text: Legends button that displays estimated remediation efforts such as None, Small, Medium, Large, XL, or XXL, and also includes icon descriptions.

After reviewing the summary, select the individual assessment links to be redirected to that specific assessment in a new browser tab. The questions for each Now Assist assessment differ. For example, the questions and answers on the Now Assist in AI Search assessment are different than the questions and answers on the Now Assist in Virtual Agent assessment.

**Note:** The assessments gather information from tables. To view any of the tables' available questions, answers, assessments, or assessment run successes or failures, search for the applicable table in the navigation filter:

-   Questions \[sn\_assess\_question\] table
-   Answers \[sn\_assess\_answer\] table
-   Assessment \[sn\_assess\_assessment\] table
-   Assessment Run \[sn\_assess\_assessment\_run\] table

For more information about how to search for tables in the navigation filter, see [Navigate directly to a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/t_NavigateDirectlyToATable.md).

The assessments include visual indicators to guide you on non-blocker and blocker results. The following list details the descriptions of the assessment's visual indicators:

-   \[Omitted image "green-check-icon.png"\] Alt text:: Informational area and no further action needed.
-   \[Omitted image "red-check-icon.png"\] Alt text:: Further action is needed to resolve findings before implementation. These required areas include estimated remediation efforts.
-   \[Omitted image "yellow-warning-icon.png"\] Alt text:: Recommended area warning, but the finding should be evaluated before implementation. These recommendations are observations that should be reviewed prior to implementation but no estimated remediation effort is provided.

You can select **Download Report** to export the entire Now Assist assessment report in PDF format from the **Summary** tab. The exported report includes hyperlinks to the specific individual assessments. Selecting **Download Report** on an individual assessment downloads only that report in PDF format. After selecting a hyperlink in the PDF, that record or table opens in a separate browser tab.

**Note:** You don’t have to select **Download Report** to work directly with the problematic records or tables found in the assessment. Each assessment includes hyperlinks to the records or tables that need attention. Selecting a hyperlink opens the record or table in a separate browser tab.

\[Omitted image "nare-assessment-nava.png"\] Alt text: Now Assist in Virtual Agent assessment is shown, along with relevant Virtual Agent questions and answers.

After reviewing the assessment and making the suggested assessment changes, rerun your scheduled jobs to see how your results improve. For more information on rerunning a specific job or all jobs, see [Run the GenAI/AgenticAI Assessment scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-readiness-evaluation/run-genai-agenticai-assessment-scheduled-job.md).

