---
title: Exploring Build Agent
description: Build Agent enables developers to create, edit, and deploy full-stack ServiceNow applications to update sets that encompass both user interface and back-end components.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 6
keywords: [AI agent, application development, natural language, full-stack applications, conversational interface, autonomous AI, code generation, Now Assist, AI Agents, generative AI, agentic AI]
audience: developer
breadcrumb: [Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring Build Agent

Build Agent enables developers to create, edit, and deploy full-stack ServiceNow® applications to update sets that encompass both user interface and back-end components.

## How to use Build Agent

**Note:** Starting with the Australia release, you can also use Build Agent in ServiceNow Studio. This document provides guidance on using Build Agent in the ServiceNow IDE. For detailed instructions on using Build Agent in ServiceNow Studio, see [Build Agent in ServiceNow Studio](../../servicenow-studio/concept/build-agent-in-servicenow-studio.md).

Build Agent is an AI tool designed for developers within ServiceNow Studio the ServiceNow Integrated Development Environment \(ServiceNow IDE\). It can act as an autonomous AI agent capable of independently generating a complete ServiceNow® scoped or global application.

Using the chat panel within ServiceNow Studio or the ServiceNow IDE, you can interact with Build Agent through an easy-to-use multi-turn conversation interface. You can also ask it general questions about developing on the ServiceNow AI Platform.

All you have to do is describe an application in natural language, and the agent can then automatically create it. Build Agent generates the necessary code, organizes files clearly, and manages both the core logic and user interface components of the application.

Build Agent can understand natural language prompts, autonomously generate full-stack applications, oversee the entire build process, respond to feedback, deploy applications to update sets, and more.

You can also attach images, such as architectural diagrams or UI wireframes, to provide context for prompts in Build Agent. This method enables you to convey the application design and functionality more effectively.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

While creating and updating applications is the primary use case for Build Agent, its capabilities extend beyond that. It can perform various code-related tasks, such as rewriting tables, explaining code, validating and enhancing existing applications, fixing application errors, and more. For instance, Build Agent can use the Run Query tool to query a specific table within your instance and return the top five records or derive specific insights.

Build Agent currently supports the following models:

-   Gemini 3.0 Pro
-   GPT 5.4
-   Opus 4.6
-   Claude Sonnet 4.6

For information on changing the model, see [Manage model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Build Agent is enabled by default to create apps with AI, for example in ServiceNow Studio. To use other Now Assist products, such as the app generation skill, disable Build Agent. For example, using the setting in your ServiceNow Studio preferences. For more information, see [Use the app generation skill to generate apps](../../now-assist-app-gen/task/sns-app-gen-use-app-gen-skill.md).

**Important:** Build Agent only creates metadata supported by ServiceNow® Fluent. For more information, see [ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md). For the latest API reference, see [https://servicenow.github.io/sdk/](https://servicenow.github.io/sdk/)

## Build Agent \(Trial\) app overview

Build Agent is available as a trial app on a freemium model. To install Build Agent \(Trial\), visit the [ServiceNow Store](https://www.servicenow.com/products/vibe-coding.html#benefits).

After you install the Build Agent \(Trial\) app, your instance will receive 100 free user interactions for 30 days at no additional charge, enabling you to explore Build Agent features at no additional cost.

If you exceed the free interaction limit, you must wait 30 days for a reset, or install the paid version of Build Agent. For more information on how to install Build Agent, see [Install Build Agent](../tasks/install-build-agent.md).

## Localization and Build Agent

Build Agent incorporates the ServiceNow AI Platform localization, so you can use it in any supported language. For more information, see [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Build Agent and PDIs

You can access Build Agent on a Personal Development Instance \(PDI\). Developers using PDIs get 25 prompts per instance per 30-day cycle.

PDIs are updated to match the latest Build Agent for a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments. For more information on PDIs, see [Personal developer instance guide](../../applications/concept/personal_developer_instance_guide.md).

## What apps are in ServiceNow

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

## Enhance applications with agentic experiences

You can enhance your applications with agentic experiences by using Build Agent.

Build Agent enables you to create agentic workflows, agents, and skills for your custom applications. Additionally, Build Agent recommends in-app agents tailored to specific use cases.

For more information, see [Create agentic workflows, agents, and skills](../tasks/create-custom-ai-agent.md).

## Build Agent benefits

Build Agent accelerates application development on the ServiceNow AI Platform. It helps automate many repetitive and time-consuming tasks that developers previously had to do manually, enabling:

-   Increased developer productivity
-   Reduced development backlogs
-   Quicker deployment of new business applications
-   Reduction in overall development cost

## What to explore next

To learn more about configuring and using Build Agent, see:

-   [Install Build Agent](../tasks/install-build-agent.md)
-   [Use Build Agent](../tasks/use-build-agent.md)

To learn more about prompting, see this Community article on [The fastest way to learn Build Agent prompting? Ask Build Agent](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544).

-   **[Example Build Agent use cases](additional-build-agent-use-cases.md)**  
There are many use cases for Build Agent beyond application development, including documentation creation, learning assistance, and brainstorming support. Reference these scenarios to identify additional ways to integrate the Build Agent into your development workflow.
-   **[Build Agent workflow](build-agent-workflow.md)**  
The Build Agent workflow automates building applications, testing, and deploying update sets on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.
-   **[Tutorial for Build Agent in ServiceNow Studio](build-agent-tutorial.md)**  
Learn to develop reusable server-side logic and build a ServiceNow® application in Build Agent, from data modeling through testing, using AI-assisted development.
-   **[General guidelines for Build Agent](build-agent-general-guidelines.md)**  
Follow some general guidelines for implementing and managing Build Agent effectively in your development workflow.
-   **[Build Agent tools](build-agent-tools.md)**  
Development tools integrate with Build Agent to automate application building tasks. The tools provide semantic search capabilities, development planning assistance, automated UI validation fixes, database querying, and application navigation support.
-   **[MCP connections and Build Agent](accelerate-design-to-development-with-figma-mcp-server.md)**  
MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.
-   **[Build Agent governance](build-agent-governance.md)**  
Governance controls in Build Agent help with code quality, security, and compliance when generating applications. The Build Agent automated safeguards prevent common development issues and enforce organizational standards.
-   **[Build Agent limitations](build-agent-limitations.md)**  
Plan deployments and troubleshoot issues by learning about Build Agent constraints that affect deployment capabilities and performance.

**Parent Topic:**[Build Agent](build-agent.md)

