---
title: Generate new conversations from scenarios
description: Create execution log data for AI voice agentic assets By creating new conversations from typical scenarios you configure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/generate-conversations.html
release: zurich
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 4
breadcrumb: [Execute a run for an AI voice agentic asset, Execute a run, Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Generate new conversations from scenarios

Create execution log data for AI voice agentic assets By creating new conversations from typical scenarios you configure.

## Before you begin

The following steps are for the second step of the guided setup for executing an AI voice agentic asset evaluation. For more information about how to access the guided setup, see [Execute a run for an AI voice agentic asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/execute-voice-aia-eval.md).

To create conversation logs for your AI voice agentic asset, it must run before the judges can evaluate it. Ensure that you have the correct permissions to run the AI voice agentic asset. For more information, see [Security for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aia-security-implementation.md).

Role required: sn\_voice\_aia.admin

## About this task

The scenarios you generate are the context for creating new execution logs for your AI voice agentic asset. For the evaluation to reflect real performance, choose scenarios that are representative of the work the agentic asset will actually handle.

## Procedure

1.  Select either **Generate scenarios** or **Add scenarios manually**.

    If you're choosing to add scenarios manually, skip to step 8.

2.  Download the reference template for scenario generation.

    The reference template includes all of the information necessary to automatically generate scenarios in the correct format for the automated evaluation.

    The template includes:

    -   Domain knowledge, capabilities, and available tools
    -   Authentication, error handling, and forbidden behaviors
    -   Voice channel conventions, conversation length targets, and recap and read back rules
    -   Topic taxonomy, follow-up question strategy, and status lifecycle
    -   Reference data and entities
3.  Fill in the template according to the specifics of your AI voice agentic asset.

    You can use as many aspects of the default template as you like. For example, the phonetic alphabet or time expressions in the template are general enough that they may serve most use cases for English-speaking AI voice agentic assets.

4.  Select **Add file**, then select **Upload**.

    If there are any validation errors in the uploaded file, the modal displays a warning.

5.  Choose the number of scenarios to generate based on the information in the template.

    The number of scenarios affects generation time. As a reference, generating 100 scenarios typically takes about 5 minutes.

6.  Select **Continue**.

    Once you select **Continue**, a sparkle animation appears and the scenarios are generated in the background.

    After generation is complete, view their details by selecting **View scenarios**. You can delete or edit any individual scenario.

    You can proceed to the next step in the guided setup as soon as at least one scenario is generated. You don't need to wait for all scenarios to finish.

7.  If you generated scenarios, skip to step 11.

8.  Select records manually by either uploading a file or using a guided form.

    If you're choosing to add scenarios with a guided form, skip to step 10.

9.  If you choose to upload a file, select the option and press continue.

    1.  Download the template for the scenario details.

        If you have previously uploaded a scenario file, you can select it from the list of attachments.

    2.  Fill in the information in the CSV file.

        The CSV file requires four comma-separated values: the scenario description, the opening message \(how the user starts the conversation\), the expected output \(a description of the full conversation\), and the end goal \(what the AI voice agentic asset needs to accomplish\). You can include as many scenarios in a single file as you want.

        Using special characters in the CSV file content can cause problems during the upload process.

        When uploading a new attachment, the previous attachment is still shown. You must delete the existing attachment via the UI action before uploading a new one.

    3.  Select **Add file**, then select your completed template.

    4.  Select the attachment you added, then select **Upload**.

10. If you choose to use a guided form, select the option and press continue.

    1.  Enter a description of the scenario.

        The description provides context for how the AI voice agentic asset is used, which an LLM uses to generate scenarios. Make sure the description is thorough enough for the LLM to accurately interpret the asset and produce relevant scenarios.

    2.  Craft an opening message.

        The opening message represents what a user says at the start of an interaction with the AI voice agentic asset. When creating multiple scenarios, vary the opening messages to cover the range of inputs the asset is likely to encounter.

    3.  Describe the expected output.

        The expected output field should describe the full conversation between a user and the AI voice agentic asset. The clearer and more specific this description is, the better the generated scenarios will be.

    4.  Select **Create** to add the scenario.

    5.  Repeat for additional scenarios.

11. Name your dataset.

    Choosing a descriptive name for your dataset makes it easier to find if you want to use it again.

12. Select **Continue** to move to the next step of the guided setup.


## What to do next

After generating your scenarios, you can move on to the final step of the guided setup. See step 9 of [Execute a run for an AI voice agentic asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/execute-voice-aia-eval.md).

