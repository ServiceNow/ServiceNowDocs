---
title: Add a search retrieval to an AI agent
description: Add a search retrieval to an AI agent in AI Agent Studio. Leveraging the Retrieval-Augmented Generation \(RAG\) enables an AI agent to retrieve and incorporate relevant information from an external source.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a search retrieval to an AI agent

Add a search retrieval to an AI agent in AI Agent Studio. Leveraging the Retrieval-Augmented Generation \(RAG\) enables an AI agent to retrieve and incorporate relevant information from an external source.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a search retrieval to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Search retrieval**.

4.  On the form, fill in the fields.

<table id="table_jyb_lw5_cdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select a type of record operation to add

</td><td>

If you select **An existing one**, you can select a record operation tool used by the current AI agent or any other AI agent. You can make changes to the settings of that tool to fit the needs of your specific AI agent.

</td></tr><tr><td>

Name

</td><td>

Name that you want to specify for your search retrieval tool.

</td></tr><tr><td>

Description

</td><td>

Description of the search retrieval tool and what it's going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Search profile

</td><td>

Name of the search profile that you want to add to your RAG-based tool from the list. To learn more about a search profile, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Search sources

</td><td>

One or multiple sources that you want to add to your search profile. To learn more about the search sources, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Fields returned

</td><td>

One or multiple fields that you want your search profile to return from the search sources.

</td></tr><tr><td>

Results limit

</td><td>

Number of records to be retrieved from the defined search source. The default value is 10.

</td></tr><tr><td>

Search criteria

</td><td>

Type of search that needs to be used:-   **Semantic**: This search is carried out with the logical meaning of the search query.
-   **Keyword**: This search is carried out with the defined keywords.
-   **Hybrid**: This search is a combination of both keyword and semantic searches.


</td></tr><tr><td>

Semantic indexes

</td><td>

Fields on the source table that are indexed for a semantic search.**Note:** Semantic indexed fields are required if the search criteria are semantic or hybrid.

</td></tr><tr><td>

Document matching threshold

</td><td>

Cosine similarity score between 0 and 1 \(exclusive\). Default value is 0. The higher the number, the more variation in search results.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your search retrieval tool:-   **Supervised**: Inputs from your human agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the tool execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**
If you want the AI agent to work in Off Glide architecture with AI-native experience, you must turn-on the **Display output** toggle. When the toggle is turned-on, you can add widgets that can be used in assistants built with AI-native experiences. The widget configuration includes:

-   **Widgets**: Defines the display output to render the content in a better user experience. You can select the widget from the drop-down.
-   **Require widget transformation**: An additional LLM call is required to transform the raw tool. If you choose to skip this transformation step, the tool output will be directly mapped to the widget.
    -   **Yes**
    -   **No**
-   **Display refined widget message**: Refines the widget message when configured.
    -   **Yes**
    -   **No**
**Note:** The display output as a toggle is exclusively available for the AI-native experience when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard display output options.

</td></tr><tr><td colspan="2">

Advanced settings

</td></tr><tr><td>

Select an output transformation format

</td><td>

Style for the LLM to present the results as it passes information between tools and to other agents. Out transformation formats:-   None
-   Concise
-   Paragraph
-   Summary
-   Custom


</td></tr><tr><td>

Write processing messages for users

</td><td>

Message to display to users during tool execution.-   In-progress message: Write an in-progress message to be displayed to end-users while the tool is running.
-   Completion message: Write a completion message to be displayed to end-users once the tool finishes running.


</td></tr></tbody>
</table>5.  Select **Add**.

    A search retrieval tool is added in the Search retrievals section on the Add tools and information page.


