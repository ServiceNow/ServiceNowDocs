---
title: Customize skill inputs and the prompt
description: Configure the input data and prompt for a ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) skill. These mechanics are the same for every TMT application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-tmt-customize-skill-inputs.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [ServiceNow Otto, Telecommunications, Media, and Technology, skill inputs, prompt customization]
breadcrumb: [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Customize skill inputs and the prompt

Configure the input data and prompt for a ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) skill. These mechanics are the same for every TMT application.

## Before you begin

Role required: admin

## About this task

This procedure covers the input data and prompt customization step of the skill configuration guided setup, in the AI Admin Hub. For locating a skill, activating and copying it, filling in general details, and setting availability, display, and activation, see [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

From the AI Admin Hub console, select the input table, related records, and fields for each input template. Then configure the prompt headers to include them in the generated summary. Each application's own documentation lists the specific tables and fields its skills rely on.

## Procedure

1.  View the input data for the skill, such as the base input fields and related lists for the different input templates.

    Configure the base input table fields and related lists for the different input templates for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_now_assist_tmt_input_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the record table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of the record, provides quick info about the issue.`

</td></tr></tbody>
</table>    2.  For each input template, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template, select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding input data sources, like the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

    4.  Select **Save and continue** to go to the next step.

2.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

    1.  For each input template, select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data prior to this step.

        You can add the **Waiting on customer** prompt to cases only if the case has an **Awaiting info** state. Otherwise, adding this header to other states could cause the Now LLM Service to generate inaccurate or unreliable results.

    2.  Select **Save** to continue to the test response.

    3.  Select a record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    4.  Select **Save and continue** to go to the next step.


## What to do next

Continue with the availability, display, and activation sub-steps in [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

