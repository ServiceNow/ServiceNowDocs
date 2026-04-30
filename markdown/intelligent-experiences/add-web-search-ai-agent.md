---
title: Add a web search to an AI agent
description: Add a web search to an AI agent in AI Agent Studio using a third-party search API such as Microsoft Bing or Google.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a web search to an AI agent

Add a web search to an AI agent in AI Agent Studio using a third-party search API such as Microsoft Bing or Google.

## Before you begin

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global data center for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Please consider your organization's data policies before adding a web search tool with Google as the provider.

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a web search to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Web search**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your web search.

</td></tr><tr><td>

Resource

</td><td>

Resource for the web search.

</td></tr><tr><td>

Provider

</td><td>

Third-party search API provider.**Note:** You can configure the default provider for the Web Search API capability on the OneExtend Definition Config table \[sys\_one\_extend\_definition\_config\].

</td></tr><tr><td>

Inputs

</td><td>

Information for the search API to include in the web search. You can select value overrides or leave them blank for generative AI to fill in the details for you.-   **Country**: Country where results come from.
-   **Max tokens**: Maximum number of tokens to include in the response.
-   **Number of results**: Total number of results acquired.
-   **Search query**: Value to search for
-   **Sites or domains**: Websites where you want to search.
**Note:** If the agent uses multiple tools, you can choose to use another tool's output as an input value override. Select the data picker icon \(![Data picker icon.](../image/data-picker-icon.png)\) to review the available options.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected web search:-   **Supervised**: Inputs from your live agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**


</td></tr><tr><td>

Processing message

</td><td>

Message to display to users when the tool is running.

</td></tr><tr><td>

Output transformation strategy

</td><td>

Style for the LLM to present the results as it passes information between tools and to other agents.-   None
-   Concise
-   Paragraph
-   Verbose
-   Custom


</td></tr></tbody>
</table>5.  Select **Add**.

    A web search is added in the Web search list on the Add tools and information page.


