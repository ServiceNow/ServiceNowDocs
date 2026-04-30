---
title: Add a web search
description: Add a web search as a tool in Now Assist Skill Kit. Adding a web search as a tool enables you to add search results to your prompt.
locale: en-US
release: yokohama
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-02-25"
reading_time_minutes: 2
keywords: [web search, Websearch, web search skill, web search tool]
breadcrumb: [Add a tool, Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Add a web search

Add a web search as a tool in Now Assist Skill Kit. Adding a web search as a tool enables you to add search results to your prompt.

## Before you begin

Role required: sn\_skill\_builder.adminor admin.

To use web search as a tool, you must bring your own search engine API key and configure it on the ServiceNow AI Platform.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Create a skill or select the skill that you want to add web search to.

3.  Select the **Tool editor** tab.

4.  Select the \(+\) icon to add a node.

5.  Select **Tool node**, and then **Add**.

6.  Select **Web Search** in the **Tool type** field.

7.  Select **Configure tool**.

8.  On the General info form, enter a **Name** and select **Web Search** for the **Resource** field.

9.  Select **Continue**.

10. On the Tool inputs form, fill in the fields.

    ![Add a web search tool page in Now Assist Skill Kit.](../image/nask-web-search.png)

<table id="table_itg_hm5_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search result type

</td><td>

**AI answers** is the type of result that you want from the search. **AI answers** generates a single response to the search using either Perplexity, OpenAI, or Gemini.

</td></tr><tr><td>

AI search providers

</td><td>

The AI search provider used to perform the search.**Note:**

If you select Perplexity or OpenAI, you must complete the API key setup in the AI Search answers OneExtend capability table. For more information on that process, see [Configure AI search answers capability for web search](../../generative-ai-controller/task/configure-ai-search-answers-capability-for-web-search.md). Although Azure Open AI is an option to select, Azure Open AI doesn't support web search.

If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global data center for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Please consider your organization's data policies before adding a web search tool with Google as the provider.

</td></tr><tr><td>

Search query

</td><td>

The word, words, or phrase you’re searching for.

</td></tr><tr><td>

Sites or domains

</td><td>

This field appears but it's not supported.

</td></tr><tr><td>

Max tokens

</td><td>

This field appears but it's not supported.

</td></tr></tbody>
</table>11. Select **Continue**.

12. On the Tool outputs form, select **Continue**.

13. On the Tool conditions \(optional\) form, select **Continue**.

14. On the Summary screen, select **Add tool**.


**Parent Topic:**[Add a tool](../concept/add-a-tool.md)

