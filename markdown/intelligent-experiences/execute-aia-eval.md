---
title: Evaluate agentic workflows and AI agents
description: Evaluate agentic workflow and AI agents against datasets of your choice to monitor performance and evaluate against different benchmarks.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 5
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Evaluate agentic workflows and AI agents

Evaluate agentic workflow and AI agents against datasets of your choice to monitor performance and evaluate against different benchmarks.

Process for guided setup for executing an agentic evaluation run 

## Before you begin

Evaluation runs require execution log data of the agentic workflow or AI agent you want to evaluate. You can create execution log data by testing in AI Agent Studio, triggering agentic AI in Now Assist in Virtual Agent or Now Assist panel. You can also create execution log data after setting up your evaluation run.

For more information about testing agentic workflows, see [Manually test the execution of an agentic workflow](test-aia-use-case.md).

For more information about getting started with agentic evaluations, see [General guidelines for agentic evaluation runs](../concept/gg-aia-eval.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

    You can also start from the testing page of the AI Agent Studio. Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**. Select **Start automated evaluation**. You’re redirected to the guided setup.

2.  On the evaluations home page, select **New evaluation run** to begin the guided setup.

3.  In the **Add general info** step, add a name and select the agentic workflow or AI agent that you want to evaluate.

    ![Generate Resolution Plan agentic evaluation guided setup step for adding general info with name, description, and generate resolution plan as the selected agentic workflow using version v1.](../image/aia-eval-info-new.png)

4.  Select **Continue** to go to the next step.

    Each time you navigate through a step, the evaluation run is saved automatically as a draft. At any point, you can select **Save as draft**.

    If you want to exit the guided setup, you can select **Exit setup**. You’re redirected to the Agentic Evaluations page.

    -   If you select **Save and exit**, the evaluation run appears on the Agentic Evaluations page with the status of **Draft**.
    -   If you select **Discard and exit**, the evaluation run draft is deleted.
5.  Select your evaluation metric.

    Overall task completeness evaluation is selected by default. Running multiple evaluation metrics at a time can help provide a more comprehensive overview of the agentic workflow's or AI agent's performance.

    To see more information about each plan, you can expand the card for each evaluation plan by selecting the chevron icon ![Chevron icon.](../../../reuse/icons/product-icons/chevron-down-outline-24.svg).

    Any custom metrics that you have published appear as options as well. If you don’t see your custom metric, make sure that it’s published. See [Create a custom metric](create-custom-metric.md) for more information.

    ![Tool performance evaluation agentic evaluation guided setup step for selecting an evaluation method with four options selected (overall task completeness, plan, tool performance, and tool calling).](../image/aia-eval-plans-new.png)

6.  Choose your dataset.

    1.  Select an existing dataset or create your own.

    2.  If you’re creating a dataset, give it a name and description.

    3.  To create a dataset, choose whether you want to run the agentic workflow or AI agent to generate new execution logs or use existing ones.

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The source table for records that the agentic workflow or AI agent uses to perform tasks and create executions.

</td></tr><tr><td>

Max records

</td><td>

The maximum number of records within the dataset you want to run the evaluation on. If there are more records in the dataset than the maximum number of records, any records after the maximum number of records are ignored.

</td></tr><tr><td>

Filters

</td><td>

Conditions for narrowing down the list of records for the agentic workflow or AI agent to use to generate execution log data.

</td></tr><tr><td>

Starting phrase

</td><td>

Utterance given to the agentic workflow or AI agent to execute. Use the pill picker to select the specific dynamic inputs necessary to perform its task. For example, your starting instruction for evaluating an agentic workflow that generates resolution plans, you can set the starting instruction to `Help me resolve {{incident.number}}`. Inputs from the record must be written between double curly braces.

</td></tr><tr><td>

Additional business context

</td><td>

Information given to the Large Language Model \(LLM\) acting as the invoking user that supplements information found within the table records. For example, a tuition reimbursement agentic workflow must know the normal reimbursement allowance, so the additional business context could be a knowledge article with that information.

</td></tr></tbody>
</table>        **Note:** If you are creating new execution logs, the user that submits the evaluation must successfully pass the ACLs of the AI agent or the agentic workflow and all of its AI agents. If the correct role requirements aren't met, the execution logs will only report that the user does not have access, and the evaluation will fail. See [Security for agentic AI](../concept/aia-security-implementation.md) for more information.

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max records \(optional\)

</td><td>

The maximum number of records within the dataset you want to run the evaluation on. If there are more records in the dataset than the maximum number of records, any records after the maximum number of records are ignored.

</td></tr><tr><td>

Filters

</td><td>

Conditions for narrowing down the AI execution log records you want to include in the dataset.

</td></tr></tbody>
</table>        ![Tool performance dataset, using new logs, on the Incident table, 500 maximum records and a filter closed incidents that contain "login" in the short description.](../image/aia-eval-dataset-new.png)

    4.  Select **See preview** to see a list of records based on the conditions you specified.

        You can narrow down the records further by only selecting some of the records in the preview list. Unselected records won’t be included in the dataset.

7.  Review the agentic evaluation details in the last step of the guided setup.

    If you want to make changes, you can select **Back** to go to a previous step, or you can select the step in the sidebar.

    ![Tool performance review page of the guided setup.](../image/aia-eval-review-new.png)

8.  Select **Start evaluation**.


## Result

Your evaluation run executes. The time it takes for it to complete varies, but once completed you can select the evaluation from the Agentic Evaluations page to view the results.

For more information on the metrics on the results page, see [Agentic evaluation run results](../concept/aia-eval-metrics.md).

