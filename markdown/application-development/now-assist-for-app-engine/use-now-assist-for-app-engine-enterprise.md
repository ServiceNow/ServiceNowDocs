---
title: Using Now Assist for App Engine
description: Enhance custom applications with generative and agentic AI capabilities.
locale: en-US
release: australia
product: Now Assist for App Engine
classification: now-assist-for-app-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [now assist, app engine, AI capability, AI feature, AI product, AI agent, skill, generative AI, genAI, Now Assist for App Engine, custom app, use generative AI]
breadcrumb: [Now Assist for App Engine, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Using Now Assist for App Engine

Enhance custom applications with generative and agentic AI capabilities.

With Now Assist for App Engine, you can enhance your custom applications with several AI capabilities: skills, AI agents, and agentic workflows. You can implement any number and combination of AI capabilities within your custom apps, depending on your app's workflow. To learn more about the types of AI capabilities that you can implement with Now Assist for App Engine, see [AI capabilities for enhancing custom applications](../../now-assist-app-engine/concept/ai-capabilities-with-now-assist-for-app-engine.md).

Certain app workflows might be well suited for AI agents and agentic workflows. Other workflows might be best handled with skills. To learn about which AI capability might be best for your use case, see [Choosing the right AI capability](../../now-assist-app-engine/concept/choosing-the-right-ai-capability.md).

## Implementing skills

The following list outlines the process for implementing a skill within a custom application:

1.  [Create a skill](https://www.servicenow.com/docs/access?context=create-new-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) or configure a Now Assist Platform skill for your app's use case.
2.  [Create a prompt](https://www.servicenow.com/docs/access?context=create-prompt-template&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to choose what skill inputs to use and the type of tool.
3.  [Test the prompt](https://www.servicenow.com/docs/access?context=test-prompt-template&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to verify that you’re seeing the expected prompt results before the skill is activated.
4.  [Evaluate the prompt](https://www.servicenow.com/docs/access?context=evaluate-prompt&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to assess the effectiveness of your skill prompts.
5.  [Finalize and publish the skill](https://www.servicenow.com/docs/access?context=publish-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to enable a Now Assist admin to activate it.
6.  [Activate the skill](https://www.servicenow.com/docs/access?context=activate-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), enabling you to trigger the skill within the UI.
7.  Use the skill in your custom application.

**Note:** Some skills might need to be reviewed and approved by a data steward before you can activate them.

## Implementing AI agents and agentic workflows

The following list outlines the process for implementing an AI agent and agentic workflow within a custom application:

1.  [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) or [duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) and [modify it](https://www.servicenow.com/docs/access?context=modify-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for your app's use case.
2.  [Add a tool to the AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to enable different functionalities and help your AI agent to achieve their objective.
3.  [Test the AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to see that it functions the way that you defined it.
4.  [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) or [modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) so that AI agents can coordinate to solve complex problems.
5.  [Test the agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to analyze its performance while it runs the instructions that you defined.
6.  [Evaluate the agentic workflow](https://www.servicenow.com/docs/access?context=execute-aia-eval&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to monitor performance and evaluate it against different benchmarks.
7.  Use the AI agent or agentic workflow in your custom application.

-   **[Summarize a record in-product using Now Assist for App Engine](../../now-assist-app-engine/task/summarize-record-in-product-na-for-app-engine.md)**  
Quickly understand the contents of a record in a custom application within Core UI or a custom workspace.
-   **[Summarize a record through chat using Now Assist for App Engine](../../now-assist-app-engine/task/summarize-record-through-chat-na-for-app-engine.md)**  
Quickly understand the contents of a record through a conversation with Now Assist.

**Parent Topic:**[Now Assist for App Engine](add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)

