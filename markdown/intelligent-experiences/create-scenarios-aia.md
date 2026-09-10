---
title: Create test scenarios for an agentic AI asset
description: Create different scenarios to evaluate your agentic AI asset's performance across multiple executions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-scenarios-aia.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [agentic evaluation, automated evaluation, automatic evaluation, batch testing, test scenarios, test objectives]
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Create test scenarios for an agentic AI asset

Create different scenarios to evaluate your agentic AI asset's performance across multiple executions.

## Before you begin

If you're going to use existing table records for your test scenarios, the table should have at least 10 records.

Role required: sn\_aia.admin

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the agentic AI asset you want to create test scenarios for.

    After selecting an agentic AI asset, you're directed to the node map view that shows the components, such as AI agents or tools.

3.  Select the pencil icon \[Omitted image "pencil-outline-24.svg"\] to open the guided setup for the agentic AI asset.

4.  Scroll to the **Test scenarios** section, then select **Add scenarios**.

5.  Select an input method.

<table><thead><tr><th align="left" id="d186286e129">

Input method

</th><th align="left" id="d186286e132">

Description

</th></tr></thead><tbody><tr><td id="d186286e138">

**__Table records__**

</td><td>

Select records from an existing table to test against. You can use table fields as variables when you craft your test objective. Continue to the next step.

</td></tr><tr><td id="d186286e148">

**__Manual entry__**

</td><td>

Write your own test objectives without using table records. You won't be able to include variables. **Note:** If you select **Manual entry**, skip the next three steps and go straight to **Craft a test objective**.

</td></tr></tbody>
</table>6.  Select the table that contains the records you want to use.

7.  Select records to test your agentic AI asset against.

    For the most thorough and effective testing, you should choose many records that cover a wide range of scenarios your agentic AI asset can encounter.

    You can search for specific records by selecting the magnifying glass icon \[Omitted image "magnifying-glass-fill-24.svg"\] or select **Filter** to narrow down the types of records on the table to those that fulfill certain criteria.

8.  Select the maximum number of records to include.

    The default is 100. If more records match your criteria than the maximum you set, the extras are excluded from the test scenarios.

9.  Craft a test objective.

    The test objective is a starting phrase or user utterance for triggering the agentic AI asset.

    If you're using table records, you can select **Insert related columns** to include table fields as variables. You can use variables to use the same test objective on multiple records.

    If you're creating scenarios manually, each scenario will need its own test objective.

10. Add tags for the scenarios.

    You can assign multiple types of scenarios to the same agentic AI asset. Use tags to make it easier to choose which test scenarios work best for your automated evaluation.


## Result

Your agentic AI asset has test scenarios that can be used for automated evaluations.

## What to do next

Add new scenarios to your agentic AI asset, such as ones on different tables, select **Run test** then **Evaluation** to use the scenarios in an automated evaluation. See [Launch an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md) for the full process details.

