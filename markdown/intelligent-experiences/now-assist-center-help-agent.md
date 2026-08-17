---
title: AI Admin Center help AI agent
description: Use the AI Admin Center help AI agent in the conversational experience to find answers to your AI admin questions based on ServiceNow documentation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-help-agent.html
release: zurich
topic_type: concept
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using the ServiceNow Otto panel conversational experience, Use, AI Admin Center, Enable AI experiences]
---

# AI Admin Center help AI agent

Use the AI Admin Center help AI agent in the conversational experience to find answers to your AI admin questions based on ServiceNow documentation.

## AI Admin Center help AI agent overview

The AI Admin Center help AI agent is a product help assistant in the AI Admin Center conversational experience that uses all available ServiceNow documentation and training resources to answer your questions about the product. The AI agent responses provide relevant descriptions, instructions, references, and links to source documents that support your product experience.

The AI Admin Center help AI agent is turned on by default.

The AI Admin Center help AI agent may work with other AI agents to accomplish tasks. For more information on AI agents, see [Explore AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/exploring-ai-agents.md).

## AI agent details

The AI Admin Center help AI agent capabilities are associated with the following agents.

<table id="table_vsk_1jj_yjc"><thead><tr><th>

Agent

</th><th>

Capability

</th></tr></thead><tbody><tr><td>

NAC Help Agent

</td><td>

Answers help questions by querying ServiceNow documentation. The agent is engaged when the user asks "How do I", "What is", "Help with", or similar help-seeking questions.

</td></tr></tbody>
</table>For more information on viewing your AI agents, see [View your AI assets in the asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-view-ai-assets.md).

## AI agent access

Role required: sn\_na\_center.nac\_user

## AI agent actions

When used, the AI agent may attempt the following actions.

-   Search and index all available ServiceNow documentation and training resources.
-   Generate a descriptive response to the question.
-   Provide references and links to the source documents that informed the response.

## How it works

1.  Ask a question in the conversational interface in AI Admin Center.
2.  The AI agent interprets your question and searches the available ServiceNow documentation and training resources for the answer.
3.  The AI agent displays the answer in the conversation including any links to related source documents.
4.  You review the answer. If necessary, provide additional details about the question for a more relevant answer.
5.  The AI agent retains the conversation throughout your session so you can ask follow-up questions without repeating context.

**Parent Topic:**[Using the conversational experience in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/using-now-assist-panel-now-assist-center.md)

