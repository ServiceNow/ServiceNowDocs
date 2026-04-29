---
title: Review agentic evaluation outputs
description: Assess your agent's overall performance after a run completes, including per-metric scores and issue counts. Use the results as your starting point for diagnosing quality issues and opportunities for improvement before deployment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
keywords: [agentic evaluation, AI agent assessment, LLM scores, evaluation metrics, traces, optimization]
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Review agentic evaluation outputs

Assess your agent's overall performance after a run completes, including per-metric scores and issue counts. Use the results as your starting point for diagnosing quality issues and opportunities for improvement before deployment.

## Before you begin

You must have a completed agentic evaluation.

Role required: sn\_aia.admin or admin

## About this task

Automated evaluations include scores and recommendations across the different metrics you chose. Each output provides information you can use to make decisions about development and deployment of the agentic AI asset. The evaluation results help you identify performance patterns, quality issues, and optimization opportunities before deploying your agent to production.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  Select the automated evaluation you want to review the results of.

    The evaluation details page opens, displaying the overall results and performance metrics.

3.  Review the evaluation summary section to understand the overall performance.

    The summary provides a high-level overview of your agent's performance across all evaluated metrics. Key information includes:

    -   Agentic AI asset information such as name and version
    -   Total number of test cases evaluated
    -   Average scores across all metrics
    -   Number of issues identified by severity level
4.  Review the overall LLM-judged scores for each metric.

    General LLM-judged scores for each metric demonstrate overall patterns and trends across the metrics you have evaluated against. These scores provide general recommendations for deployment based on the current version of the agentic AI asset. Detailed results include:

    -   Numerical score
    -   Performance rating \(Excellent, Good, Moderate, or Poor\)
    -   Individual record evaluations
5.  [Investigate any issues](aia-eval-review-issues.md) and their [associated traces](aia-eval-analyze-traces.md).

    If problems with the agentic AI asset's performance are found, they are categorized by severity level, metric, and use case. Issues can be tracked down to their sources in specific interactions, called "traces." Review issues and their traces to diagnose underlying issues. Issues are classified by severity level:

    -   Critical: Issues that can prevent the agent from functioning correctly, resulting in a poor user experience
    -   High: Significant problems that impact user experience or accuracy
    -   Medium: Moderate issues that may affect performance in some scenarios
    -   Low: Minor issues that have minimal impact on overall functionality
6.  [Apply optimizations](aia-eval-apply-optimization.md) based on the findings.

    The automated evaluation can include recommended optimizations to address issues found in the evaluation. After you have applied the optimization, you can rerun the evaluation to see the changes in behavior and performance. Track improvements by comparing results across evaluation runs.


## Result

You have a comprehensive review of your agent's performance across all evaluated metrics. Use these insights to make informed decisions about deployment readiness or identify areas requiring additional development work.

