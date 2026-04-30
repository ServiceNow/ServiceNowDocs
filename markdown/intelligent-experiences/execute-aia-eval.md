---
title: Run an agentic evaluation
description: Evaluate an agentic workflow against a dataset of your choice to monitor performance and evaluate it against different benchmarks.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-04-03"
reading_time_minutes: 3
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Run an agentic evaluation

Evaluate an agentic workflow against a dataset of your choice to monitor performance and evaluate it against different benchmarks.

Process for guided setup for executing an agentic evaluation run 

## Before you begin

Evaluation runs require execution log data of the agentic workflow you want to evaluate. For a new agentic workflow, you can create execution logs by testing in AI Agent Studio. For more information about testing agentic workflows, see [Test an agentic workflow](test-aia-use-case.md).

For more information about getting started with agentic evaluations, see [General guidelines for agentic evaluation runs](../concept/gg-aia-eval.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

    You can also start from the testing page of the AI Agent Studio. Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**. Select an agentic workflow and then select **Set up evaluation run**. A modal appears to ask if you want to be redirected to Now Assist Skill Kit. Select **Open Skill Kit**. You’ll be redirected to the Guided Setup.

2.  On the evaluations home page, select **New evaluation run** to begin the guided setup.

3.  In the Add general info step, add a name and select the agentic workflow that you want to evaluate.

    ![Categorize Incident Agentic Workflow agentic evaluation guided setup step for adding general info with name, description, and categorize incident as the selected agentic workflow.](../image/aia-eval-info.png)

4.  Select **Continue** to go to the next step.

    Each time you navigate through a step, the evaluation run is saved automatically as a draft. At any point, you can select **Save as draft**.

    If you want to exit the guided setup, you can select **Exit setup**. You’re redirected to the Agentic Evaluations page.

    -   If you select **Save and exit**, the evaluation run appears in the list on the Agentic Evaluations page with the status of **Draft**.
    -   If you select **Discard and exit**, the evaluation run draft is deleted.
5.  Select your evaluation method.

    Overall task completeness evaluation is selected by default. Running multiple evaluation methods at a time can help provide a more comprehensive overview of the agentic workflow's performance.

    To see more information about each plan, you can expand the card for each evaluation plan by selecting the chevron icon \(![Chevron icon.](../../../reuse/icons/product-icons/chevron-down-outline-24.svg)\).

    ![Categorize Incident Agentic Workflow agentic evaluation guided setup step for selecting an evaluation method with four options selected (overall task completeness, plan, tool performance, and tool calling).](../image/aia-eval-plans.png)

6.  Choose your dataset.

    1.  Select an existing dataset or create your own.

    2.  To create a new dataset, fill out the form.

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the dataset.

</td></tr><tr><td>

Description

</td><td>

General description of the dataset and its intended purpose.

</td></tr><tr><td>

Max records \(optional\)

</td><td>

The maximum number of records within the dataset you want to run the evaluation on. If there are more records in the dataset than the maximum number of records, any records after the maximum number of records will be ignored for that evaluation run.

</td></tr><tr><td>

Filters

</td><td>

Conditions for narrowing down the AI execution log records you want to include in the dataset. By default, the agentic workflow that you’re evaluating is selected as a filter condition.

</td></tr></tbody>
</table>        ![Categorize Incident Agentic Evaluation dataset with no maximum records and a filter for the usecase field is categorize incident.](../image/aia-eval-dataset.png)

    3.  Select **See preview** to see a list of records based on the conditions you specified.

        You can narrow down the records further by only selecting some of the records in the preview list. Unselected records won’t be included in the dataset.

7.  Review the agentic evaluation details in the last step of the guided setup.

    If you notice any place where you want to make changes, you can select **Back** to go to a previous step, or you can select the step in the sidebar.

    ![Categorize Incident Agentic Evaluation review page of the guided setup.](../image/aia-eval-review.png)

8.  Select **Start evaluation**.


## Result

Your evaluation run executes. The time it takes for an evaluation run to complete varies, but once it has been complete you can select the evaluation from the Agentic Evaluations page to view the results.

For more information on the metrics on the results page, see [Agentic evaluation run results](../concept/aia-eval-metrics.md).

