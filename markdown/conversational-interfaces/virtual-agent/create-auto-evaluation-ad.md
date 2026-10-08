---
title: Set up an automated evaluation
description: Run an automated evaluation to measure how well your assistant handles generated conversation scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/create-auto-evaluation-ad.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 6
breadcrumb: [Testing assistant conversations, Test and improve, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Set up an automated evaluation

Run an automated evaluation to measure how well your assistant handles generated conversation scenarios.

## Before you begin

Role required: virtual\_agent\_admin or admin

Assign severity levels to failure patterns. These levels apply across your instance, so you set them once rather than for each evaluation. For more information, see [Customizing severity levels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/customize-severity-levels.md).

## About this task

You can leave the setup at any step by selecting **Exit setup**. Select **Leave** to discard the unsaved changes and exit, or select **Cancel** to return to the setup. Leaving without saving doesn't delete the evaluation. Only the changes you haven't saved are lost. If you don't have unsaved changes, the setup closes right away.

## Procedure

1.  To set up an automated evaluation, select **Set up automated evaluation** from the **Testing** tab.

2.  Add the basic information.

    -   **Name**: Enter a unique name to identify your evaluation.
    -   **Description**: Add a brief description to explain the purpose of your evaluation, to help you identify the evaluation later.
    -   **Select assistant to evaluate**: Select the assistant you want to evaluate from the list.
    -   **Select a chat experience to evaluate**: Select the chat experience that the evaluation runs on. An evaluation runs on one chat experience at a time, and results can vary depending on the one you select.

        -   **Standard or enhanced chat**
        -   **Premium chat**
        Under each option, a label shows whether that chat experience is configured for the selected assistant. You can select either option even if it isn't configured, to see how the assistant could perform on that chat experience.

    \[Omitted image "evaluations-ad-02.png"\] Alt text: Basic information page showing the name, description, assistant, and chat experience fields.

3.  Select **Save and continue**.

4.  Choose evaluation metrics that define success.

    Select the metrics that define success for your evaluation.

    -   **Conversation success**: Measures whether your assistant interprets user requests and delivers the correct outcome.
    -   **Conversation fluency**: Measures whether your assistant's responses are clear, natural, and grammatically correct.
    -   **Faithfulness**: Checks whether your assistant uses only the information it can access, without fabricating details.
    -   **Skill selection accuracy**: Measures whether your assistant selects the correct assistant skill, AI agent, or QnA module to handle each user's request.
    -   **Turn count**: Counts how many back-and-forth exchanges it takes to complete a user's request.
    You must select at least one metric to continue. For detailed information about each evaluation metric, see [Evaluation metrics for automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/evaluation-metrics-auto-eval-ad.md).

    \[Omitted image "evaluations-ad-04.png"\] Alt text: Metrics page listing the evaluation metrics available to select.

5.  Select **Save and continue**.

6.  Provide the evaluation details.

    Select the table and map the table columns to provide inputs for automatically generated conversation scenarios.

    1.  Select a table with evaluation inputs.

        **Important:** To start your data set from a template, open the **What evaluation inputs do I need to provide?** help for this step and select **download an Excel file**. The sample test set, `template_conv_eval_dataset.xlsx`, defines each field and shows the formatting that the evaluation expects.

        1.  **Table**: Search for and select your table.
        2.  **Maximum number of scenarios to evaluate**: Specify the maximum number of scenarios to evaluate. You can select up to 500 per evaluation run.
        3.  Select **Select table**.
        \[Omitted image "evaluations-ad-07.png"\] Alt text: Table selection page showing the table and maximum number of scenarios fields.

    2.  Map the table columns.

        1.  Map your table columns to the provided fields so the automated evaluation knows which data to use. For each field, use the column selector to choose the table column that holds that data. Map your table columns to the following fields:

            -   **Run as user**: The user who's impersonated to run each scenario.
            -   **Initial query**: The user's question or comment.
            -   **Scenario context**: Details that support the assistant in its response.
            -   **End goal**: When the conversation should be considered complete from the user's perspective.
            -   **Ground Truth**: The correct answer or result to check if the task was successfully completed. This field appears only when you select the **Conversation success** or **Skill selection accuracy** metric. The column that you select is used as the ground truth for both metrics.

                For more information about adding data sets for ground truth, see [Data sets for conversation evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/data-sets-con-eval-ad.md).

        2.  Select **Apply mappings** to generate the scenarios.

        \[Omitted image "evaluations-ad-03.png"\] Alt text: Column mapping page showing the evaluation fields mapped to table columns.

    3.  Optional: Filter your data set.

        To evaluate only a specific set of records, such as a particular intent category or date range, build a filter on the table in the **Filter your dataset \(optional\)** section.

        1.  Select a field, an operator, and a value.
        2.  To filter on more than one attribute, add conditions with **and** or **or**, or select **New condition set**.
        3.  Select **Apply filter**.

            The scenarios update only after you select **Apply filter**.

        Only records that match the filter are used to generate scenarios, up to the maximum number of scenarios that you specified.

        \[Omitted image "evaluations-ad-11.png"\] Alt text: Filter your data set step with a filter condition applied.

    4.  Review scenarios for evaluation.

        Review the scenarios to confirm that they include the information you expect.

        If you applied a filter, the scenario count reflects only the matching records and **Filter applied** appears next to it. To remove the filter, select **Clear**.

        \[Omitted image "evaluations-ad-08.png"\] Alt text: Generated scenarios list for the automated evaluation.

7.  Select **Save and continue**.

8.  Review the automated evaluation setup.

    Review your selections before starting the evaluation.

    \[Omitted image "evaluations-ad-05.png"\] Alt text: Review page summarizing the selections for the automated evaluation.

9.  Select **Start evaluation** to begin the evaluation.

    **Note:** Depending on the volume, the evaluation time varies. You can return to view the results at any time. After the evaluation is complete, you can export the report for additional analysis.


## Result

The evaluation results provide scores and reasoning for each metric you selected. Review the insights to identify patterns in conversation quality and areas where your assistant performs well or requires improvement. The conversation transcripts and metric explanations help you understand the context behind each score.

Select **Clone** to reuse the configuration of a completed evaluation instead of setting up a new one from scratch.

Select **Export evaluation report** to get a CSV file with the metric results. You can also view the results from the Automated evaluations section on the **Testing** tab.

\[Omitted image "evaluations-ad-09.png"\] Alt text: Automated evaluation report.

The evaluation results page also shows the recurring failure patterns behind your assistant's failed scenarios, so you can prioritize what to fix without reviewing every failed scenario individually. For more information, see [Insights into failed scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/severity-insights.md).

Use the insights to refine your virtual agent topics, improve AI agent configurations, or adjust your knowledge base content. Regular evaluation lets you track the quality of your conversational assistant over time.

**Parent Topic:**[Testing assistant conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/evaluations-ad.md)

**Related topics**  


[Data sets for conversation evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/data-sets-con-eval-ad.md)

[Evaluation metrics for automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/evaluation-metrics-auto-eval-ad.md)

[Insights into failed scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/severity-insights.md)

[Clone an existing evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/clone-evaluations.md)

