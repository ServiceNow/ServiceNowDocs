---
title: Add a web search tool
description: Add a web search tool to your skill to retrieve web content and include it as context in your prompt.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 4
keywords: [web search, web search tool, Now Assist Skill Kit]
breadcrumb: [Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Add a web search tool

Add a web search tool to your skill to retrieve web content and include it as context in your prompt.

## Before you begin

Role required: sn\_skill\_builder.admin

To use web search as a tool, you must bring your own search engine API key and configure it on the ServiceNow AI Platform.

## About this task

The web search tool queries the web and returns results that the skill prompt can use. Two search result types are available depending on the providers you have configured:

-   **AI answers**

    Generates a single synthesized response to the search query using OpenAI, Perplexity, or Gemini. Requires a configured API key for the selected provider.

-   **Searching and scraping**

    Generates multiple responses using Now LLM Service. Requires a configured scraping API. Default search engine is Bing; Google requires additional configuration.


**Important:** If you select Google as your web search provider, the web search tool uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google global infrastructure routes traffic to a global datacenter for each web search request. This processing may differ from your data processing location. Consider your organization data policies before enabling skills that use Google web search.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to add web search to.

3.  Select the **2. Add tools** tab.

4.  Select the **\(+\)** icon on the canvas connector where you want to insert the tool, select **Tool node**, and then select **Add**.

5.  In the **Tool type** list, select **Web Search**.

    If you want this tool to run simultaneously with another tool at the same level in the flow, select **Add as parallel node**.

6.  Select **Configure tool**.

7.  On the **General info** step, enter a name in the **Name** field.

8.  In the **Resource** field, select the web search resource to use, then select **Continue**.

    The **Description** field is automatically populated based on the resource you select.

9.  On the **Tool inputs** step, fill in the fields and select **Continue**.

<table id="table_web_search_inputs"><thead><tr><th>

Field

</th><th>

Applies to

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search result type

</td><td>

All

</td><td>

The type of search result to return. Select **AI answers** to generate a single synthesized response using an AI provider, or **Searching and scraping** to return multiple results using Now LLM Service.

 The fields shown after change depending on which type you select.

</td></tr><tr><td>

AI Search Providers

</td><td>

AI answers only

</td><td>

The AI provider used to generate the search response. Options include OpenAI, Perplexity, and Gemini. The selected provider must be configured with a valid API key. **Note:** Although Azure OpenAI appears as an option, it does not support web search.

</td></tr><tr><td>

Search query \(required\)

</td><td>

All

</td><td>

The query to submit to the web search provider. You can enter a static value, reference a skill input using the reference icon, or use a script to generate the value dynamically using the script icon.

</td></tr><tr><td>

Number of results

</td><td>

Searching and scraping only

</td><td>

The number of search results to return. Default is 3.

</td></tr><tr><td>

Sites or domains

</td><td>

Searching and scraping only

</td><td>

Restricts the search to specific sites or domains.

</td></tr><tr><td>

Country

</td><td>

Searching and scraping only

</td><td>

Filters search results by country.

</td></tr><tr><td>

Max tokens

</td><td>

Searching and scraping only

</td><td>

The maximum number of tokens to include from search results. Default is 1000.

</td></tr></tbody>
</table>10. On the **Tool outputs** step, optionally select **Truncate** for any outputs that might exceed token limits, then select **Continue**.

    **Note:** Output names and types are fixed and cannot be edited. Avoid truncating the `response` output if it is critical to the prompt context.

11. On the **Tool conditions** step, select whether the tool should always run or only run under certain conditions, then select **Continue**.

    |Type|Description|
    |----|-----------|
    |None \(Always run\)|The tool runs every time the skill executes. This is the default.|
    |Script|The tool runs only if a custom script condition evaluates to true.|
    |Filters|The tool runs only if filter conditions based on field values are met.|

12. On the **Summary** step, review the tool configuration and select **Add tool**.


## What to do next

After adding the web search tool, reference its `response` output in your prompt using the **+ Inputs and tools** button in the prompt editor. To learn more, see [Create a prompt](create-prompt-template.md).

To learn more about configuring the web search capability, see [Configure AI search answers capability for web search](../../generative-ai-controller/task/configure-ai-search-answers-capability-for-web-search.md).

**Parent Topic:**[Create a prompt](create-prompt-template.md)

