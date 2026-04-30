---
title: Getting started with agentic evaluations
description: Run your first agentic evaluation to assess the performance and effectiveness of your agentic AI assets using automated metrics and datasets.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 4
keywords: [automated evaluations, agentic AI, evaluation metrics, dataset, performance testing]
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Getting started with agentic evaluations

Run your first agentic evaluation to assess the performance and effectiveness of your agentic AI assets using automated metrics and datasets.

## Before you begin

Before you start your first evaluation run, verify that you have the following:

-   An agentic AI asset that has been built and saved in AI Agent Studio
-   At least one version of the agentic AI asset
-   Available dataset with a minimum number of test cases. You can create new datasets using [Now Assist Data Kit](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md).
-   You have the necessary permissions to run the agentic AI asset. You can verify whether you have the right permissions by checking the user access settings of the agentic AI asset in AI Agent Studio.

Role required: sn\_aia.admin

## About this task

Agentic evaluations help you measure the performance and reliability of your agentic AI assets before deploying them in production environments. The evaluation process runs your agentic AI asset against test datasets and measures various metrics such as overall completeness and tool use.

You can use existing datasets, create new datasets from previous execution logs, or generate new execution logs during the evaluation process. The system provides automated analysis and optimization recommendations based on the evaluation results.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

    The Agentic Evaluations page displays a list of existing evaluation runs and their status.

2.  Select **Create new evaluation run**.

    The Create Evaluation Run form opens with configuration options for your evaluation.

3.  Complete the basic configuration fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name for the evaluation run. Use a name that identifies the purpose and scope of the evaluation.|
    |**Agentic AI Asset**|Select the agentic AI asset you want to evaluate from the list of available assets in your instance.|
    |**Version**|Select the specific version of the agentic AI asset to evaluate. Different versions may have different performance characteristics.|
    |**Description**|Optional description providing additional context about the evaluation objectives and scope.|

    For example, name your evaluation run "Customer Service Agent - Version 2.1 - Performance Test" to clearly identify what you are testing.

    See [Version control for agentic AI](version-control.md) for more information about maintaining different versions of your agentic AI assets.

4.  Select the metrics to evaluate.

    Select multiple metrics to get a comprehensive evaluation of your agentic AI asset's performance across different dimensions.

5.  Configure the data for the evaluation run.

    |Option|Description|
    |------|-----------|
    |**Use existing dataset**|Select a pre-existing dataset that contains test cases and expected outcomes for evaluation.|
    |**Create dataset from execution logs**|Generate a new dataset using previous execution logs of the agentic AI asset. This option evaluates the actual historical executions of the agentic AI asset.|
    |**Generate new execution logs**|Create new execution logs as part of the evaluation run. The system generates test scenarios and captures the agentic AI asset's responses.|

    The system validates your data configuration and displays the selection of test cases that will be included in the evaluation.

6.  Review the configuration summary and select **Submit**.

    The configuration summary displays all selected options, including the agentic AI asset, version, metrics, and data configuration. Verify that all settings are correct before submitting.

    The evaluation run starts and appears in the Agentic Evaluations list with a status of "Running".

7.  [Monitor progress and review logs when prompted.](../task/track-aia-eval-progress.md)

    The evaluation process may take several minutes to hours depending on the size of your dataset and complexity of your agentic AI asset. You can track progress in real-time and review execution logs as they are generated.

8.  [Review results, issues, and traces once the run completes.](../task/review-aia-eval-outputs.md)

    After the evaluation completes, analyze the detailed results including metric scores, identified issues, and execution traces to understand your agentic AI asset's performance.

9.  [Apply recommended optimizations and trigger a re-evaluation.](../task/aia-eval-apply-optimization.md)

    Based on the evaluation results, the system may provide optimization recommendations. Apply these recommendations to improve your agentic AI asset's performance and run additional evaluations to measure improvements.


## Result

You have successfully created and executed your first agentic evaluation run. The evaluation results provide insights into your agentic AI asset's performance and areas for improvement. You can use these results to optimize your agentic AI asset before deploying it in production environments.

## What to do next

After completing your first evaluation, consider the following next steps:

-   Schedule regular evaluations to monitor performance over time
-   Create additional datasets to test different scenarios and use cases
-   Share evaluation results with AI architects and leads

