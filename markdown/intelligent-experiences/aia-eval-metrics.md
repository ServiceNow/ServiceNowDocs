---
title: Agentic evaluation run results
description: Learn about agentic evaluation runs and the meaning behind different evaluation scores from the agentic evaluation results page.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Reference, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Agentic evaluation run results

Learn about agentic evaluation runs and the meaning behind different evaluation scores from the agentic evaluation results page.

## Agentic evaluations overview

Agentic evaluations measure how well AI agents and agentic workflows are accomplishing their objectives. A Now LLM Service model judges the AI agent or agentic workflow based on the execution logs. The results page of an evaluation run shows multiple metrics and scores measuring task completeness and tool use.

If you run an overall task completion evaluation, the results page shows recommended actions for the AI agent or agentic workflow. Recommended actions give you suggestions for deployment or improvement to help verify that the agentic workflows that you deploy are performing up to your standards.

After you've reviewed your evaluation results, you can archive your evaluation or copy it to run another evaluation with the same parameters and dataset.

You can export the evaluation results as a report. The report is formatted as a .csv file that includes the individual sys\_ids of the execution records and the metric scores for each.

For more information on AI agent usage and other analytics, you can review the [AI Agent Analytics dashboard](ai-agent-dashboard.md) in the AI Agent Studio.

## Evaluation results overview

For each evaluation method that you execute, the results page displays an overall score for the agentic workflow with a percentage of successful record evaluations and a label of Excellent, Good, Moderate, or Poor. You can change the metric thresholds for each label by selecting **Customize metric thresholds**.

In addition to the overall task completeness results, you can review a summary of the results of the other metrics.

<table><thead><tr><th>

Label

</th><th>

Description

</th><th>

Recommended action

</th><th>

Default threshold

</th></tr></thead><tbody><tr><td>

Excellent

</td><td>

Tasks were consistently performed at a high standard. The agentic workflow or AI agent is working well.

</td><td>

Proceed with confidence

</td><td>

90%–100%

</td></tr><tr><td>

Good

</td><td>

Most tasks were performed successfully, but some performance inconsistencies suggest areas for improvement.

</td><td>

Deploy with caution

</td><td>

70%–89%

</td></tr><tr><td>

Moderate

</td><td>

A significant number of tasks weren't fully completed. Performance is below the desired level.

</td><td>

Investigate the root causes of poor task completion

</td><td>

50%–69%

</td></tr><tr><td>

Poor

</td><td>

The agentic workflow is consistently failing to complete tasks adequately. Major issues are present.

</td><td>

Do not deploy

</td><td>

0%–49%

</td></tr></tbody>
</table>## Individual record metric scores

Evaluations are run against the log tables of agentic workflow executions. Each record is individually scored for each evaluation plan that you run. Individual record evaluations are scored according to the following metrics.

<table><thead><tr><th>

Number

</th><th>

Score

</th><th>

Description

</th></tr></thead><tbody><tr><td>

3

</td><td>

Successful

</td><td>

The main task was fully completed. All subtasks were resolved, and the steps followed a logical sequence with no critical errors.

</td></tr><tr><td>

2

</td><td>

Partially successful

</td><td>

The task was partially completed. Some subtasks remain unresolved or inefficiencies affected the process.

</td></tr><tr><td>

1

</td><td>

Unsuccessful

</td><td>

The task wasn't completed. Critical subtasks were abandoned or unresolved or the execution failed entirely.

</td></tr></tbody>
</table><table><thead><tr><th>

Number

</th><th>

Score

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

True

</td><td>

The right tool was chosen for the action in the plan.

</td></tr><tr><td>

0

</td><td>

False

</td><td>

The right tool wasn't chosen.

</td></tr></tbody>
</table><table><thead><tr><th>

Number

</th><th>

Score

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

True

</td><td>

Input key completeness, input value correctness, and input format correctness are all successful.

 -   **Input key completeness**: 1 - True – All required parameters are present with exact name matches, and no unexpected parameters are included.
-   **Input value correctness**: 1 - True – Tool input values are correctly mapped.
-   **Input format correctness**: 1 - True – Tool inputs are in the correct format.

</td></tr><tr><td>

0

</td><td>

False

</td><td>

One or more of input key completeness, input value completeness, or input format completeness wasn't successful.

 -   **Input key completeness**: 0 - False – A mandatory parameter is either missing, its name doesn't match exactly, or an unexpected parameter was found.
-   **Input value correctness**: 0 - False – Tool input values are not correctly mapped.
-   **Input format correctness**: 0 - False – Tool inputs are not in the correct format.

</td></tr></tbody>
</table>**Note:** The values of the sub-metrics are aggregated using an AND operator. If any one value is 0, then the entire tool calling records metric score will be 0.

