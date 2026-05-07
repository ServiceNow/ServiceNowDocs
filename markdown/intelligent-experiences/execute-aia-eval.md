---
title: Execute an agentic evaluation run
description: Evaluate agentic AI assets against datasets to monitor performance and compare benchmarks.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 5
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Execute an agentic evaluation run

Evaluate agentic AI assets against datasets to monitor performance and compare benchmarks.

Process for guided setup for executing an agentic evaluation run 

## Before you begin

Evaluation runs require execution log data of the agentic AI asset you want to evaluate. You can create execution log data by testing in AI Agent Studio or triggering agentic AI in Now Assist. You can also create execution log data after setting up your evaluation run.

For more information about testing agentic workflows, see [Manually test the execution of an agentic workflow](test-aia-use-case.md).

For more information about getting started with agentic evaluations, see [General guidelines for agentic evaluation runs](../concept/gg-aia-eval.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

    You can also start from the testing page of the AI Agent Studio. Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**. Select **Start automated evaluation** to access the guided setup.

2.  On the evaluations home page, select **New evaluation run** to begin the guided setup.

3.  In the **Add general info** step, add a name and select the agentic AI asset that you want to evaluate.

    ![Custom Categorize ITSM incident AI agent guided setup step for adding general info with name, description, and generate resolution plan as the selected AI agent using version v1.](../image/aia-eval-info-526.png)

4.  Select **Continue** to go to the next step.

    Each time you navigate through a step, the evaluation run is saved automatically as a draft. At any point, you can select **Save as draft**.

    If you want to exit the guided setup, you can select **Exit setup**. You're redirected to the Agentic Evaluations page.

    -   If you select **Save and exit**, the evaluation run appears on the Agentic Evaluations page with the status of **Draft**.
    -   If you select **Discard and exit**, the evaluation run draft is deleted.
5.  Select your evaluation metric.

    Overall task completeness evaluation is selected by default. Running multiple evaluation metrics provides a comprehensive overview of the agentic AI asset's performance.

    To see more information about each plan, you can expand the card for each evaluation plan by selecting the chevron icon ![Chevron icon.](../../../reuse/icons/product-icons/chevron-down-outline-24.svg).

    Any custom metrics that you have published appear as options. If you don't see your custom metric, verify that it's published. See [Create a custom metric](create-custom-metric.md) for more information.

    **Note:** The tool calling correctness metric is not available for AI voice agents.

    ![Tool performance evaluation agentic evaluation guided setup step for selecting an evaluation method with three options selected (overall task completeness, tool performance, and tool calling).](../image/aia-eval-metrics-526.png)

6.  Configure your dataset.

    1.  Choose between generating new execution logs by running the agent or workflow or using execution logs from previous runs.

        **Note:** If you're evaluating AI voice agents, you must use existing execution logs.

    2.  To create a dataset by generating new execution logs, start by selecting a table.

        Instead of making a new dataset from scratch, you can choose to use a past dataset that you used in a different evaluation by selecting **Select from a past dataset**. Once you select a dataset, you can review the details including source table, record count, and the last agentic AI asset that used the dataset.

        **Note:** If you're evaluating an agentic AI asset created with AI Agent Advisor, the options for your dataset are automatically filled in for you. You can still make edits to the values.

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The source table for records that the agentic AI asset uses to perform tasks and create executions.

</td></tr><tr><td>

Added filters

</td><td>

Conditions for narrowing down the list of records for the agentic AI asset to use to generate execution log data.

</td></tr><tr><td>

No. of records to use

</td><td>

The maximum number of records within the dataset for evaluation. If the dataset contains more records than the maximum, additional records are ignored.

</td></tr><tr><td>

Task

</td><td>

Utterance given to the agentic AI asset to execute. Use the pill picker to select dynamic inputs for the task. For example, set the starting instruction to `Help me resolve {{incident.number}}`. Inputs from the record must be written between double curly braces.

</td></tr><tr><td>

Additional details about the agent or workflow

</td><td>

Information given to the large language model \(LLM\) that supplements table record information. For example, a tuition reimbursement agentic workflow requires the normal reimbursement allowance, which could be provided through a knowledge article.

</td></tr><tr><td>

Run as user

</td><td>

The user associated with the table record to run the agentic AI asset. For example, depending on your use case, you can run the user as the requester or as the fulfiller.

</td></tr><tr><td>

Name

</td><td>

Name for the dataset. This can be useful if you plan on using the same dataset again.

</td></tr><tr><td>

Description

</td><td>

Description of the records contained within the dataset. This can be useful if you plan on using the same dataset again.

</td></tr></tbody>
</table>        **Note:** If you're creating new execution logs, the user submitting the evaluation must pass the ACLs of the agentic AI asset and its components. Without correct role requirements, execution logs report access denial and the evaluation fails. See [Security for agentic AI](../concept/aia-security-implementation.md) for more information.

        ![Generate new execution logs selected. Sample records have a state and priority filter applied](../image/aia-eval-data-new-logs-1.png)

        ![Further options for generating new execution logs, including number of records to use, task, additional details about the agent or workflow, and the run as user](../image/aia-eval-data-new-logs-2.png)

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Added filters

</td><td>

Conditions for narrowing down the AI execution log records you want to include in the dataset.

 **Note:** Filter conditions are not supported for creating datasets of AI voice agent execution logs.

</td></tr><tr><td>

No. of records to use

</td><td>

The maximum number of records within the dataset for evaluation. If the dataset contains more records than the maximum, additional records are ignored.

</td></tr></tbody>
</table>

    3.  Select **See preview** to see a list of records based on the conditions you specified.

        You can narrow down the records by selecting specific records in the preview list. Unselected records won't be included in the dataset.

7.  Review the agentic evaluation details in the last step of the guided setup.

    If you want to make changes, you can select **Back** to go to a previous step, or you can select the step in the sidebar.

    ![Tool performance review page of the guided setup.](../image/aia-eval-review-526.png)

8.  Select **Start evaluation**.


## Result

Your evaluation run executes. Completion time varies, but after completion you can select the evaluation from the Agentic Evaluations page to view results.

For more information on the metrics on the results page, see [Agentic evaluation run results](../concept/aia-eval-metrics.md).

