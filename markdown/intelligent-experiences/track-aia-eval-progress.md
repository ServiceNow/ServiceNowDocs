---
title: Track and monitor agentic evaluation progress
description: Monitor the status of an active evaluation run to catch errors early and confirm when results are ready to review.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
keywords: [agentic evaluation, AI agent monitoring, evaluation progress, execution logs]
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Track and monitor agentic evaluation progress

Monitor the status of an active evaluation run to catch errors early and confirm when results are ready to review.

## Before you begin

You must have an active evaluation run to monitor. For information about creating evaluation runs, see [Execute an agentic evaluation run](execute-aia-eval.md).

Role required: admin

## About this task

Agentic evaluations can take time to complete, especially for large datasets. Monitoring progress helps you identify issues early and determine when results are ready for review.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  Select an evaluation with a trackable status.

    You can find evaluations to track in two locations:

    -   **Quick overview** section: Recent in-progress evaluations appear in the In-progress evaluations card
    -   **Automated evaluations** section: All evaluations, including older ones
    Evaluations you can track have a **Run status** of **In progress** or **Action needed**.

3.  Select the evaluation you want to monitor.

    The evaluation monitoring details page opens, showing the current status and progress information.

4.  If the status is **Action needed**, review the generated execution logs.

    The most common reason for the **Action needed** status is when execution logs have been generated but require approval before the evaluation phase can begin.

    1.  Examine the dataset artifacts to understand how the agentic AI performed on specific records.

        You can open individual incidents or other records to see how the agentic AI asset interacted with them during the test.

    2.  Select execution records to view detailed performance information.

        This opens the execution details in AI Agent Studio, where you can review the complete conversation between the simulated user and the agentic AI, including reasoning and processing messages from agents and tools.

    3.  Review conversation records and timestamps to understand the interaction flow.

        The start phrase and conversation records provide detailed information about how the AI agent interacted with the simulated user, including timestamps for each message.

5.  If you reviewed the execution logs and they meet your expectations, start the evaluation phase by selecting **Start evaluation**.

    After you approve the logs, the LLM judging and scoring phase begins. This phase analyzes the execution logs and provides quantitative scores for the AI agent's performance.

    The evaluation status changes to **In progress** and the LLM evaluation begins.

6.  Monitor the progress of the LLM evaluation phase.

    During this phase, you can track:

    -   Number of records evaluated
    -   Estimated time remaining
    -   Any errors or warnings that occur during evaluation
7.  Check for completion notifications or status updates.

    When the evaluation completes, the status changes to **Completed** and results become available for review.


## Result

You can monitor the evaluation progress and take action when required. When the evaluation completes successfully, you can review the detailed results to understand your agentic AI's performance.

## What to do next

After the evaluation completes, review the results to identify areas for improvement in your agentic AI configuration. For information about analyzing evaluation results, see [Review the results of an agentic evaluation](review-aia-eval-outputs.md).

