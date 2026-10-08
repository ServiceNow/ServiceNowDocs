---
title: Testing assistant conversations
description: The Testing tab in Assistant Designer helps you assess the quality and performance of your conversational assistant. You can test conversations manually or run automated evaluations on generated scenarios to measure the assistant's success in addressing the user request and usage of available assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/evaluations-ad.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 4
breadcrumb: [ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Testing assistant conversations

The **Testing** tab in Assistant Designer helps you assess the quality and performance of your conversational assistant. You can test conversations manually or run automated evaluations on generated scenarios to measure the assistant's success in addressing the user request and usage of available assets.

## Testing tab

The **Testing** tab provides evaluation capabilities across multiple conversation types including virtual agent topics, conversational catalog items, AI agents, knowledge base and external content search results, and small talk interactions. The feature analyzes conversations to help you identify areas for improvement in your assistant configuration.

From the **Testing** tab, you can create simulated experiences through manual tests or generate evaluation metrics by setting up automated evaluations. You can select an assistant and test it manually, or select **Set up automated evaluation** to create an automated evaluation. To set up automated evaluations, see [Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/create-auto-evaluation-ad.md).

\[Omitted image "evaluations-ad-01.png"\] Alt text: Testing tab with options to test an assistant manually or set up an automated evaluation

The **Testing** tab supports two evaluation approaches:

-   **Test one conversation at a time \(manual test\)**: Test conversations individually by chatting with your assistant. See how the assistant responds and review what it does. Select your assistant and use the **Test assistant** option to validate whether an assistant is configured correctly and is working as intended.

    **Note:** This is meant to be a simulated experience.

-   **Evaluate many conversations at a time \(automated evaluation\)**: Evaluate your assistant using auto-generated chats, explore multiple scenarios, and view detailed performance insights.

    Evaluation works by examining a conversation transcript: the full back-and-forth between a user and the assistant. When you run an evaluation, the simulated conversation transcripts are examined and selected metrics are applied to generate scores and insights.

    Each automated evaluation runs on one chat experience, either **Standard or enhanced chat** or **Premium chat**, which you select when you set up the evaluation. You can evaluate an assistant on either chat experience, even one that isn't configured for that assistant.

    **Note:** Before running your evaluation, upload a table that includes user requests, scenario context, and the correct ground truth responses. You can evaluate approximately 500 conversations per run. For more information about adding data sets for ground truth, see [Data sets for conversation evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/data-sets-con-eval-ad.md).

    You can also filter the table so that only records matching your conditions, such as a particular intent category or date range, are used to generate scenarios. For more information, see [Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/create-auto-evaluation-ad.md).


You can also clone a completed automated evaluation to reuse its configuration as a starting point for a new one. For more information about cloning an evaluation, see [Clone an existing evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/clone-evaluations.md).

## View failure pattern insights

After an automated evaluation with failed scenarios finishes running, Assistant Designer analyzes the results and clusters recurring failure patterns on the evaluation results page. You can prioritize what to fix without reviewing every failed scenario individually. For more information, see [Insights into failed scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/severity-insights.md). You can customize the default severity level assigned to each failure pattern. For more information, see [Customizing severity levels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/customize-severity-levels.md).

## Compare evaluations

Compare the results of multiple auto-evaluation runs side by side to see how your assistant's metrics change from one run to the next. You can view trends across evaluation runs by comparing the results between different evaluations. From the Automated evaluations section, select the evaluations to compare and select **Compare evaluations**. You can compare up to 5 evaluation runs at a time.

To see how your assistant performs on each chat experience, run an evaluation on each one and compare the results.

## Delete evaluations

To remove an evaluation, select the **Delete evaluation** icon \[Omitted image "icon-delete-evaluation.png"\] Alt text: at the end of its row in the Automated evaluations section. Then from the Confirm delete dialog box, select **Delete**. A message confirms that the evaluation was deleted. If the evaluation is still in progress, it stops running before it's deleted.

**Related topics**  


[Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/create-auto-evaluation-ad.md)

[Customizing severity levels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/customize-severity-levels.md)

[Insights into failed scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/severity-insights.md)

[Data sets for conversation evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/data-sets-con-eval-ad.md)

[Clone an existing evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/clone-evaluations.md)

