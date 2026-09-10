---
title: Launch an automated evaluation of an agentic AI asset
description: Evaluate your agentic AI asset's performance against defined scenarios to identify issues and opportunities for improvement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/launch-aia-eval.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [agentic evaluation, automated evaluation, automatic evaluation, batch testing, test scenarios, test objectives]
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Launch an automated evaluation of an agentic AI asset

Evaluate your agentic AI asset's performance against defined scenarios to identify issues and opportunities for improvement.

## Before you begin

Role required: sn\_aia.admin

## About this task

Evaluations use test scenarios, or saved objectives that you can reuse for a single test or select for an evaluation. Scenarios carry the objective text, but they don't carry live record identifiers, like a record name or number. Scenarios that refer to a record need one that is actually on the instance at run time.

Scenarios have to exist before an evaluation can be configured against them, and they can also be created from the test scenario selection in a single test. Where the evaluation configuration screen offers no way to create one, create it in the library first and then return.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the agentic AI asset you want to evaluate.

    After selecting an agentic AI asset, you're directed to the node map view that shows the components, such as AI agents or tools.

3.  Select **Run test**, then select **Evaluation**.

4.  Select your test scenarios.

    If you must create test scenarios for the agentic AI asset, select **test scenarios** to be redirected to the guided setup for the agentic AI asset. The **Test scenarios** section displays all of the possible scenarios generated for that specific agentic AI asset. For more information about creating test scenarios, see [Create test scenarios for an agentic AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-scenarios-aia.md).

    You can select test scenarios by tags. If you want to organize your test scenarios by tag, you can add or remove tags from the **Test scenarios** section in the agentic AI asset guided setup.

    If you have more test scenarios than your specified **Maximum number of records**, the additional ones won't be included in the test.

    The **Example of objectives** lists the test objectives of the scenarios you have chosen. If you don't see certain fields you want to include, update the test scenarios with the desired variables in the agentic AI asset guided setup.

5.  Select your metrics to calculate.

    **Overall task completion evaluation** is selected by default. Calculating multiple metrics at once can give you a better picture of overall performance.

    Custom metrics aren't supported in evaluations started in AI Agent Studio.

6.  Select whether you want to automatically generate insights and optimization suggestions.

    Evaluation run results includes detailed information about the performance of the agentic AI asset across all selected metrics. Selecting this option gives you additional analysis of identified issues and offers suggested prompt changes to address them. Insight generation and optimization suggestions add to the time required for an evaluation to complete.

    You can also trigger this process from the evaluation run's results page later.

7.  Select **Run evaluation**.


## Result

Your agentic AI asset is evaluated against your chosen metrics on the test scenarios you have configured.

## What to do next

You can track the evaluation's progress through the test scenarios. When the evaluation is complete, you can view the results page for performance breakdowns overall and by specific test scenarios.

