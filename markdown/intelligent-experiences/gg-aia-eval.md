---
title: General guidelines for AI agent and agentic workflow evaluation
description: Learn about agentic evaluation runs and different recommendations for evaluating your AI agents and agentic workflows against datasets to check for completion, performance, and tool execution.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Evaluate agentic AI, Now Assist AI agents, Enable AI experiences]
---

# General guidelines for AI agent and agentic workflow evaluation

Learn about agentic evaluation runs and different recommendations for evaluating your AI agents and agentic workflows against datasets to check for completion, performance, and tool execution.

## Overview of agentic evaluation runs

Evaluation runs for AI agents and agentic workflows evaluate their executions for different metrics, such as task completion, performance, and tool execution. You can create datasets using logs for agentic workflows.

## When to run agentic evaluations

-   **Run after you have manually tested basic execution.**

    Before running an automated evaluation, you can manually test the execution of an [AI agent](../task/test-ai-agent.md) or [agentic workflow](../task/test-aia-use-case.md).

-   **Run agentic evaluations when you make significant changes.**

    After making updates to the agentic workflow, you can execute an agentic evaluation run to track the efficacy of the new version.


## Choosing an evaluation method

-   **Review the evaluation method options.**

    The agentic evaluation guided setup provides information about each evaluation method, including what they’re measuring and how they work. You can also review the common questions in the sidebar for answers about the available metrics.

-   **Use multiple evaluation methods at a time.**

    Choosing multiple evaluation methods can provide a better overall picture of the AI agent's or agentic workflow's performance.


## Creating a dataset

-   **Use filters to target the right data.**

    Add filters to the execution logs to control exactly what you're measuring your agentic workflow against. Filter different time frames to verify that you're measuring the latest version of a workflow. You can select **See preview** to see a list of records. You can also use the check boxes to select individual records to measure against.

-   **Generate new execution data for your evaluation run.**

    When going through the agentic evaluation guided setup, you can create new execution logs on multiple records before the evaluation begins. Use this reduce time.


## Frequently Asked Questions

-   **Do I need to keep anything ready before an automated evaluation?**

    Before you begin, make sure you:

    -   Test your agent or workflow in the playground. Catch the obvious issues early—automated evaluations are best for deeper validation.
    -   Ensure your table has all the required inputs if you're generating test scenarios or using scenarios from previous agent or workflow runs during setup.
    -   Prep enough scenarios. We recommend at least 100. Your evaluation is only as strong as the situations you put your agent through.
    -   Define what success means. Be clear on what the right output for your agent should be.
-   **How do I set up my first automated evaluation?**

    To set up an evaluation, follow the guided flow:

    1.  Select your agent or workflow and its version.
    2.  Choose your metrics—built-in or custom.
    3.  Use an existing dataset or decide how you want to build one.
    That's it—you're ready to evaluate.

-   **When should I create a custom metric?**

    Create a custom metric when you have unique evaluation criteria and want to measure workflow or agent-specific behaviors that aren't covered by ServiceNow's built in metrics. For example, you might want to:

    -   Check whether a particular phrase appears in the agent's response.
    -   Measure response length to assess verbosity or brevity.
-   **How do I build a dataset for agentic evaluations?**

    There are two ways to build a dataset for agentic evaluations, but first, let's clarify what a dataset is. Your dataset should include logs of executions that capture what happens when your AI agent or workflow processes records like incidents, case, or tasks. You can create a dataset by either:

    -   Using logs from previous agent or workflow runs, or
    -   Generating new logs by running the agent or workflow after setup.
-   **What's next after an automated evaluation?**

    Review your evaluation results to:

    -   Identify configuration gaps in your agent or workflow
    -   Assess deployment readiness
    -   Analyze tool performance for issues with inputs or descriptions
    -   Drill down into individual executions and metric scores
    Return to AI Agent Studio to refine your configuration, then rerun evaluations to track improvements.

-   **How do I create a custom metric?**

    Create a custom metric in a few steps:

    1.  Name and describe your metric.
    2.  Define its evaluation scope—agentic workflow, agents, or both.
    3.  Specify what it measures, how it works, and its output format.
    4.  Add metric inputs and write your script-based metric.
    5.  Save and publish to make it available for use.
-   **How do I interpret evaluation results?**

    Based on the metrics you select, each execution will display a score for every metric. Refer to the "Metric guide" to understand what the scores mean. You can also customize metric thresholds to align with your organization's definitions of success and failure.

-   **How do I track the progress of my evaluations?**

    Evaluations may take some time, but you don't need to stay on the page. From the homepage, you can track all evaluations and even see if any action is required.

-   **How is the parser tool used during custom metric creation?**

    When creating a custom metric for agentic evaluations, providing a metric input is optional—we include the 'execution plan record sys\_id' by default. We also provide a parser tool that pulls structured data from your execution logs, so you won't need to manually parse through the XML or JSON. You can access the parser tool's outputs with tool output.


