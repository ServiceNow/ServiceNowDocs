---
title: Add a tool
description: Add and manage tools visually in the Tools editor, including decision branching, to execute different tools for your skill. Adding decision branches between tools enables you to define the conditions that need to be met for a tool to run. If no conditions are met, the default branch's step is executed.
locale: en-US
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Add a tool

Add and manage tools visually in the Tools editor, including decision branching, to execute different tools for your skill. Adding decision branches between tools enables you to define the conditions that need to be met for a tool to run. If no conditions are met, the default branch's step is executed.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

A tool is a utility that is configured to convert skill inputs into skill outputs. The tool outputs can be referenced in a prompt template to introduce context to a prompt. The input for a tool can be a skill input or the output of another tool.

You can use the Tool editor to configure tools and link them to each other.

Decision nodes enable you to execute different tools, based on the logic of the branch. A decision node can contain multiple branches but will always need one default branch.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill you want to add a tool to.

3.  Select the **Tool editor** tab.

4.  Select \(+\) icon to add a node.

5.  Select the type of node that you want to add.

<table id="table_ibf_j2z_12c"><thead><tr><th>

Node type

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Tool node

 Types of tool:

-   Script
-   SubFlow
-   Flow Action
-   Retriever
-   Skill
-   Web search

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global data center for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Please consider your organization's data policies before enabling skills that have Google web search tools.

-   Predictive Intelligence


</td><td>

1.  Select a tool type.
2.  Name the tool.
3.  Select a condition.


</td></tr><tr><td>

Decision node

</td><td>

1.  Name the node.
2.  Select **Add branch**
    1.  Name the branch.
    2.  Select a Destination node.
    3.  Set the conditions.
3.  Select a Destination node.


</td></tr></tbody>
</table>    ![Tool editor tab in Now Assist Skill Kit](../image/nask-tool-editor.png)

6.  Select **Add**.

7.  Select **Run tools** to test the tools.


-   **[Add a retriever](../task/add-retriever.md)**  
Add a retriever to your prompt to augment and add context to your prompts with AI search results.
-   **[Add a web search](../task/add-web-search.md)**  
Add a web search as a tool in Now Assist Skill Kit. Adding a web search as a tool enables you to add search results to your prompt.
-   **[Add Predictive Intelligence](../task/add-predictive-intelligence.md)**  
Add predictive intelligence as a tool in Now Assist Skill Kit. Predictive intelligence models enable you to predict, estimate, and identify patterns that can be used to route work, populate forms, estimate wait times, and more.
-   **[Add Document Intelligence](add-document-intelligence.md)**  
Add document intelligence as a tool in Now Assist Skill Kit. Document intelligence enables you to

**Parent Topic:**[Create a prompt](../task/create-prompt-template.md)

