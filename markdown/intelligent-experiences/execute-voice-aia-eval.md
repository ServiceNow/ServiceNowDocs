---
title: Execute a run for an AI voice agentic asset
description: Evaluate AI voice agentic assists against datasets to monitor performance and compare benchmarks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/execute-voice-aia-eval.html
release: zurich
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 5
breadcrumb: [Execute a run, Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Execute a run for an AI voice agentic asset

Evaluate AI voice agentic assists against datasets to monitor performance and compare benchmarks.

## Before you begin

Evaluation runs require execution log data of the agentic AI asset you want to evaluate. You can create execution log data by testing in AI Agent Studio or triggering agentic AI in Now Assist. You can also create execution log data after setting up your evaluation run.

For more information about testing agentic workflows, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-aia-use-case.md).

For more information about getting started with agentic evaluations, see [General guidelines for agentic evaluation runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gg-aia-eval.md).

Role required: sn\_voice\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

    You can also start from the testing page of the AI Agent Studio. Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**. Select **Start automated evaluation** to access the guided setup.

2.  On the evaluations home page, select **New evaluation run** to begin the guided setup.

3.  In the modal, select **Voice agent or assistant**, then select **Proceed**.

    The following steps are for voice agentic AI assets. If you are evaluating an AI voice agentic asset, see [Execute a run for a chat AI agentic asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/execute-aia-eval.md). Many steps are similar, but there are aspects specific to AI voice agentic assets that require special attention.

4.  In the **Add general info** step, add a name and description.

5.  Select whether the AI voice agentic asset is an agent or an assistant, then select the agentic AI asset that you want to evaluate.

    AI voice agents must be part of a voice assistant to evaluate them. To evaluate an AI voice assistant, it must be active.

6.  Select **Continue** to go to the next step.

    Each time you navigate through a step, the evaluation run is saved automatically as a draft. At any point, you can select **Save as draft**.

    If you want to exit the guided setup, you can select **Exit setup**. You're redirected to the Agentic Evaluations page.

    -   If you select **Save and exit**, the evaluation run appears on the Agentic Evaluations page with the status of **Draft**.
    -   If you select **Discard and exit**, the evaluation run draft is deleted.
7.  Select your evaluation metric.

    Overall task completeness evaluation is selected by default. Running multiple evaluation metrics provides a comprehensive overview of the agentic AI asset's performance.

    To see more information about each plan, you can expand the card for each evaluation plan by selecting the chevron icon \[Omitted image "chevron-down-outline-24.svg"\] Alt text: Chevron icon..

    Any custom metrics that you have published appear as options. If you don't see your custom metric, verify that it's published. See [Create a custom metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-custom-metric.md) for more information.

8.  Configure your dataset.

    -   Generate new conversations from scenarios, or
    -   Use conversations from previous runs.
    1.  Choose between [Generate new conversations from scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/generate-conversations.md) or **Use conversations from previous runs**.

        Instead of making a new dataset from scratch, you can choose to use a past dataset that you used in a different evaluation by selecting **Select from a past dataset**. Once you select a dataset, you can review the details including source table, record count, and the last agentic AI asset that used the dataset.

        If you choose to use existing execution logs, you must add a filter before records will display in the preview.

        **Note:** If you're evaluating an agentic AI asset created with AI Agent Advisor, the options for your dataset are automatically filled in for you. You can still make edits to the values.

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
</table>    2.  Select **See preview** to see a list of records based on the conditions you specified.

        You can narrow down the records by selecting specific records in the preview list. Unselected records won't be included in the dataset.

9.  Review the agentic evaluation details in the last step of the guided setup.

    If you want to make changes, you can select **Back** to go to a previous step, or you can select the step in the sidebar.

    When evaluating an AI voice agentic asset, you can choose a run mode in this step of the guided setup. Select **Pause to review** to stop after each stage and review results before continuing, or **Run continuously** to get your results without intermediary steps.

10. Select **Start evaluation**.


## Result

If you choose to generate new conversations from scenarios, you can track the progress of scenario generation after you select **Start evaluation**. If you choose **Pause to review**, you can select **Start simulation** after scenario generation is complete to create the conversation simulation execution logs. After the conversations have been simulated, select **Start evaluation** to begin the actual evaluation of the execution logs.

**Note:** If you chose the **Run continuously** run mode, the evaluation will run from scenario generation to evaluation end to end without additional input.

Completion time varies, but after completion you can select the evaluation from the Agentic Evaluations page to view results.

For more information on the metrics on the results page, see [Agentic evaluation run results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aia-eval-metrics.md).

