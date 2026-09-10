---
title: Add a file upload tool to an AI agent
description: Upload files for analysis by an AI agent in AI Agent Studio to grant your AI agent access to specialized knowledge.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-file-retrieval-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a file upload tool to an AI agent

Upload files for analysis by an AI agent in AI Agent Studio to grant your AI agent access to specialized knowledge.

## Before you begin

Role required: sn\_aia.admin

## About this task

File upload tools allow AI agents to access specialized knowledge from uploaded files. When adding a file upload tool, you can configure which files the AI agent has access to, its execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

Attaching a document when building an AI agent conversationally only informs the draft configuration only. See Create an AI agent conversationally. You must add a file upload tool if you want the AI agent to access the file at run time.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **File upload**.

2.  Select **Attach file** or drag and drop to upload files.

    You can upload up to 5 files, with a maximum size of 5 MB each, in these formats: PDF, DOCX, TXT.

    **Note:** By giving AI agents access to these files, you're allowing users interacting with these AI agents to also see information in these files.

3.  Enter a name for the tool in the **Name** field.

4.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

5.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

6.  Toggle **Display output to users** to control whether the tool's output is shown to users.

7.  If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

8.  Choose whether to display a refined widget message under **Display refined widget message**.

9.  Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Analyzing files" when the tool is in progress and "Analysis complete" when the tool is done.


## Result

You have added a file upload tool to your AI agent with the appropriate files, execution mode, output settings, and processing messages configured.

