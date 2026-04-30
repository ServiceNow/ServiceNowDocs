---
title: General guidelines for agentic AI asset evaluation
description: Learn about agentic evaluation runs and different recommendations for evaluating your agentic AI assets against datasets to check for completion, performance, and tool execution.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [agentic AI evaluation, AI agent testing, evaluation metrics, dataset creation, agentic execution logs]
breadcrumb: [Explore, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# General guidelines for agentic AI asset evaluation

Learn about agentic evaluation runs and different recommendations for evaluating your agentic AI assets against datasets to check for completion, performance, and tool execution.

## Overview of agentic evaluation runs

Agentic evaluations help you verify that your agentic AI assets perform as expected across different scenarios and data sets. Regular evaluation helps maintain quality and identify areas for improvement as you develop your agentic AI assets.

The evaluation process uses automated testing to measure how well your agentic AI assets performs. Metrics for evaluation include complete tasks, execute tools correctly, and maintain performance standards. You can also create your own custom metrics to evaluate agentic AI asset responses and tasks in other ways.

## When to run agentic evaluations

Run agentic evaluations at key points in your development and maintenance cycle to verify performance and catch issues early.

-   **Run after you have manually tested basic execution**

    Before running an automated evaluation, manually test the execution of an [AI agent](../task/test-ai-agent.md) or [agentic workflow](../task/test-aia-use-case.md). Manual testing helps you identify obvious issues and verify that the basic functionality works before investing time in automated evaluation.

-   **Run agentic evaluations when you make significant changes**

    After making updates to the agentic workflow, execute an agentic evaluation run to track the efficacy of the new version. This includes changes to prompts and tool configurations that might affect performance.

-   **Run evaluations before deploying to production**

    Evaluate your agentic AI assets in a test environment before deploying them to production. This helps verify that changes work correctly and maintain expected performance levels.

-   **Run periodic evaluations for ongoing monitoring**

    Schedule regular evaluation runs to monitor the ongoing performance of your agentic AI assets. This helps detect performance degradation over time and ensures consistent quality.

-   **Run evaluations after data source changes**

    When the underlying data sources or schemas change, run evaluations to verify that your agentic AI assets continue to function correctly with the new data structure.


## Choosing an evaluation method

Select evaluation methods based on what aspects of your agentic AI asset performance you want to measure. Different methods provide insights into different aspects of functionality.

-   **Review the evaluation method options**

    The agentic evaluation guided setup provides information about each evaluation method, including what they're measuring and how they work. You can also review the common questions in the sidebar for answers about the available metrics. Take time to understand each method before selecting which ones to use.

-   **Use multiple evaluation methods at a time**

    Choosing multiple evaluation methods can provide a better overall picture of the agentic AI asset's performance. Different methods measure different aspects, such as task completion rates, response accuracy, and tool execution success.

-   **Consider task completion metrics for workflow validation**

    Task completion metrics help you verify that your agentic workflows successfully complete their intended tasks and validate end-to-end workflow functionality.

-   **Apply tool execution metrics for technical validation**

    Tool execution metrics verify that your agentic AI assets correctly use the tools and APIs they're configured to access. This method helps ensure that integrations work as expected.


## Creating a dataset

Create targeted datasets that represent the scenarios and data your agentic AI assets will encounter in production. Well-designed datasets provide more meaningful evaluation results.

-   **Use filters to target the right data**

    Add filters to the execution logs to control exactly what you're measuring your agentic workflow against. You can select **See preview** to see a list of records. You can also use the check boxes to select individual records to measure against.

-   **Generate new execution data for your evaluation run**

    When going through the agentic evaluation guided setup, you can create new execution logs on multiple records before the evaluation begins. Use this option to reduce time and ensure you have fresh data for evaluation.

-   **Include diverse scenarios in your dataset**

    Create datasets that include various scenarios your agentic AI assets might encounter, including edge cases and error conditions. Comprehensive datasets help identify potential issues before they affect users.

-   **Maintain dataset quality and relevance**

    Regularly review and update your evaluation datasets to ensure they remain relevant to current use cases. Remove outdated scenarios and add new ones that reflect changing requirements or data patterns.

-   **Consider data volume for meaningful results**

    Include sufficient data volume in your datasets to generate statistically meaningful results. Small datasets might not reveal performance patterns or issues that become apparent with larger data sets.


## Interpreting evaluation results

Understanding evaluation results helps you make informed decisions about improving your agentic AI assets and identifying areas that need attention.

-   **Analyze trends across multiple evaluation runs**

    Compare results from multiple evaluation runs to identify trends in performance. Look for patterns that indicate improving or declining performance over time.

-   **Focus on metrics that align with business objectives**

    Prioritize the evaluation metrics that most closely align with your business objectives and user requirements. Not all metrics carry equal weight for your specific use case.

-   **Investigate unexpected results**

    When evaluation results differ significantly from expectations, investigate the identified issues and their traces. This might reveal issues with the agentic AI asset configuration, data quality, or evaluation setup.


## General guidelines for effective evaluation

Follow these general guidelines to maximize the value of your agentic evaluation efforts and ensure reliable results.

-   **Establish baseline performance metrics**

    Create baseline measurements when you first deploy your agentic AI assets. These baselines provide reference points for comparing future evaluation results and tracking improvements.

-   **Monitor evaluation performance over time**

    Track how your evaluation processes themselves perform over time. This includes evaluation run times, resource usage, and the reliability of the evaluation infrastructure.

-   **Validate evaluation methods periodically**

    Periodically review and validate your evaluation methods to ensure they continue to provide meaningful insights. Update methods as your agentic AI assets evolve and requirements change.


