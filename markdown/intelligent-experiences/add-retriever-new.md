---
title: Add a search retrieval tool to an AI agent
description: Add a search retrieval tool to an AI agent to enable it to retrieve and incorporate relevant information from defined sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-retriever-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a search retrieval tool to an AI agent

Add a search retrieval tool to an AI agent to enable it to retrieve and incorporate relevant information from defined sources.

## Before you begin

Role required: sn\_aia.admin

## About this task

A search retrieval tool \(RAG or retrieval-augmented generation\) allows AI agents to retrieve and incorporate relevant information from defined sources. When adding a search retrieval tool, you can configure its search profile, sources, criteria, execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Search retrieval**.

2.  Choose whether to create a new search retrieval or use an existing one.

    Select **A new search retrieval** to create a new search retrieval, or select **An existing one** to use a previously created search retrieval.

3.  If you want to use an existing search retrieval, select the name from the dropdown.

    The search retrieval's name, tool description, search profile, search sources, and other settings are populated automatically.

4.  Enter a name for the tool in the **Name** field.

5.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

6.  Select a search profile from the **Search profile** dropdown.

7.  Configure search sources under **Search sources**.

    Search sources appear after you select a search profile.

8.  Enter the number of results to return in the **Results limit** field.

9.  Select search criteria under **Search criteria**.

    Choose from **Semantic**, **Keyword**, or **Hybrid** search criteria.

10. Configure semantic indexes under **Semantic indexes** if applicable.

11. Enter a document matching threshold in the **Document matching threshold** field.

12. Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

13. Toggle **Display output to users** to control whether the tool's output is shown to users.

14. If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

15. Choose whether to display a refined widget message under **Display refined widget message**.

16. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Searching sources" when the tool is in progress and "Search complete" when the tool is done.


## Result

You have added a search retrieval tool to your AI agent with the appropriate search profile, sources, criteria, execution mode, output settings, and processing messages configured.

