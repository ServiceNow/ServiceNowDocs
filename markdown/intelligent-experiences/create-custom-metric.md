---
title: Create a custom metric for evaluating agentic workflows
description: Create a custom metric for evaluating AI agents and agentic workflows to test the outputs against expected responses.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-08-12"
reading_time_minutes: 4
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Create a custom metric for evaluating agentic workflows

Create a custom metric for evaluating AI agents and agentic workflows to test the outputs against expected responses.

## Before you begin

Role required: sn\_aia.admin

## About this task

Custom metrics enable you to choose you measure your AI agents and agentic workflow for effectiveness. You can create custom metrics that apply to one agentic AI asset or multiple ones. Once created, you can select custom metrics in the guided setup for agentic evaluations. You can select both or either custom metrics and metrics installed with Now Assist applications. Examples of custom metrics include:

-   Testing that a certain phrase is in the response
-   Measuring the length of a response to test verbosity

When writing the script, you have access to the output of a parser tool. See [agentic evaluation parser tool](../concept/eval-parser-tool.md) for more details on how it works.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  Go to the Evaluation metrics tab and select **Create metric**.

3.  In the **General information** step, enter a name and short description for your custom metric.

    You can navigate between steps in the guided setup with the **Continue** and **Back** buttons. After entering a name for your custom metric, you can skip directly to writing your script by selecting **Skip to Script Editor**. You can fill out the details later from the Metric settings tab in the Script Editor.

4.  In the **Metric details** step, add information about the evaluation metric, how it works, and what the output format of the metric is.

    If you select **Use this content**, then the details you provide are displayed along with the option in the guided setup for an agentic evaluation run.

    You do not have to fill in details, but you have the option to provide useful information and context to aid the custom metric development process. You can also add metric details from the **Metric settings** tab of the Script Editor.

5.  After reviewing your metric information in the **Summary** step of the guided setup, select **Finish setup** to be redirected to the Script Editor.

6.  Add metric inputs.

    By default, the execution plan record sys\_id is included as a metric input.

    The parser tool lets you access content from the execution plan log without having to parse through the XML or JSON content yourself. You can access the parser tool's outputs with `tool.output`.

    1.  In the Metric inputs section, select the plus icon to open the Add metric input modal.

    2.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Input datatype|Drop-down selector to choose what data type and format the input is|
        |Name|Short, user-friendly name for the input|
        |Description|Description of the input. You can view the description of any input by selecting it in the Metric inputs section of the Script Editor.|
        |Test values|Default input values used for testing your script in the Script Editor|
        |Mandatory|Determines whether providing the input is necessary for the evaluation to run|

    3.  Select **Add**.

7.  Write your script-based metric.

    The default code block in the Script Editor contains commented code that can guide you through the script-writing process.

    At any time, you can select **Metric output template** to see the code necessary for the output to display correctly when looking at the evaluation run results in Skill Kit. This content is also included in the default code block when you first open the Script Editor. If necessary, you can copy the template and paste it into the script. Be sure to change the values to the results of your custom metric.

    You can review the details of the custom metric from the guided setup from the Metric settings tab.

    When you have made changes, you can select the **Save** button to save your changes.

    **Important:** Even if you save, the metric won’t be available to use in agentic evaluation runs until you publish it.

8.  Select **Run test** to open the Run test modal, enter your metric test inputs, and run the test.

    After you have run at least one test, you can review the response and request of both the overall execution and the parser tool.

    After you have run at least one test, you can select the **Run test** drop-down button and select **Run test history** to open a new sidebar with past test results. You can filter test runs by the user who executed the test.

9.  Select **Publish metric** to save your script and activate the metric.

    Before publishing, ensure that your output matches the metric output template. If not, your metric may not work as expected or display correctly on the evaluation run results page.


## Result

You have a new custom metric that can be used for evaluating agentic AI assets.

## What to do next

Execute an evaluation run and select your custom metric in the guided setup. See [Evaluate agentic AI](execute-aia-eval.md) for more information on executing an evaluation run.

If you do not see your custom metric in the guided setup for an evaluation run, make sure that you have published it.

