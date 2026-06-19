---
title: Exploring Build Agent
description: Build Agent enables developers to create, edit, and deploy full-stack ServiceNow applications to update sets that encompass both user interface and back-end components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/exploring-build-agent.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 7
keywords: [AI agent, application development, natural language, full-stack applications, conversational interface, autonomous AI, code generation, Now Assist, AI Agents, generative AI, agentic AI]
audience: developer
breadcrumb: [Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Exploring Build Agent

Build Agent enables developers to create, edit, and deploy full-stack ServiceNow® applications to update sets that encompass both user interface and back-end components.

## How to use Build Agent

**Note:** Starting with the Australia release, you can use Build Agent in ServiceNow Studio. This document provides guidance on using Build Agent in the ServiceNow IDE. For detailed instructions on using Build Agent in ServiceNow Studio, see [Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-agent-in-servicenow-studio.md).

Build Agent is an AI tool designed for developers within ServiceNow Studio the ServiceNow Integrated Development Environment \(ServiceNow IDE\). Build Agent acts as an autonomous AI agent capable of independently generating a complete ServiceNow® scoped or global application. For example, a global scope app that uses tables such as incident, problem, and change.

Using the chat panel within ServiceNow Studio or the ServiceNow IDE, you can interact with Build Agent through an easy-to-use multi-turn conversation interface. You can also ask it general questions about developing on the ServiceNow AI Platform.

All you have to do is describe an application in natural language, and the agent can then automatically create it. Build Agent generates the necessary code, organizes files clearly, and manages both the core logic and user interface components of the application.

Build Agent can understand natural language prompts, autonomously generate full-stack applications, oversee the entire build process, respond to feedback, deploy applications to update sets, and more.

You can also upload supported file types, such as images, code, and documents, to provide more context about application design and functionality. For more information, see [Supported file types for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/ba-supported-file-types.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

While creating and updating applications is the primary use case for Build Agent, its capabilities extend beyond that. It can perform various code-related tasks, such as rewriting tables, explaining code, validating and enhancing existing applications, fixing application errors, and more. For instance, Build Agent can use the Run Query tool to query a specific table within your instance and return the top five records or derive specific insights.

Build Agent currently supports the following models:

-   Gemini 2.5 Pro
-   Azure OpenAI 5.4
-   Opus 4.6

For information on changing the model, see .

Build Agent is enabled by default to create apps with AI, for example in ServiceNow Studio. To use other Now Assist products, such as the app generation skill, disable Build Agent. For example, using the setting in your ServiceNow Studio preferences. For more information, see [Use the app generation skill to generate apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/sns-app-gen-use-app-gen-skill.md).

## Fluent and modern web frameworks

Build Agent generates code in ServiceNow Fluent, the domain-specific language for developing on the ServiceNow AI Platform. Build Agent can also incorporate modern web frameworks, such as React, when building custom user experiences.

**Important:** Build Agent only creates metadata supported by ServiceNow® Fluent. For more information, see [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/servicenow-fluent.md). For the latest API reference, see [https://servicenow.github.io/sdk/](https://servicenow.github.io/sdk/)

## Build Agent \(Trial\) app overview

Build Agent is available as a trial app on a freemium model. To install Build Agent \(Trial\), visit the [ServiceNow Store](https://www.servicenow.com/products/vibe-coding.html#benefits).

After you install the Build Agent \(Trial\) app, your instance will receive 100 free user interactions for 30 days at no additional charge, enabling you to explore Build Agent features at no additional cost.

If you exceed the free interaction limit, you must wait 30 days for a reset, or install the paid version of Build Agent. For more information on how to install Build Agent, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/install-build-agent.md).

## Localization and Build Agent

Build Agent incorporates the ServiceNow AI Platform localization, so you can use it in any supported language. For more information, see .

## How prompts are counted

Prompts are counted each time you submit a message to Build Agent. If Build Agent asks a clarifying question and you respond, that response counts as a prompt. Approving a plan that Build Agent presents does not count as a prompt. To get the most value from each prompt, draft your message in a text editor before you submit it.

For more information on prompting, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-example-prompts.md).

## What apps are in ServiceNow

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

## Enhance applications with agentic experiences

You can enhance your applications with agentic experiences by using Build Agent.

Build Agent enables you to create agentic workflows, agents, and skills for your custom applications. Additionally, Build Agent recommends in-app agents tailored to specific use cases.

For more information, see [Create agentic workflows, agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/create-custom-ai-agent.md).

## Build Agent benefits

Build Agent accelerates application development on the ServiceNow AI Platform. It helps automate many repetitive and time-consuming tasks that developers previously had to do manually, enabling:

-   Increased developer productivity
-   Reduced development backlogs
-   Quicker deployment of new business applications
-   Reduction in overall development cost

## What to explore next

To learn more about configuring and using Build Agent, see:

-   [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/install-build-agent.md)
-   [Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/use-build-agent.md)

To learn more about prompting, see this Community article on [The fastest way to learn Build Agent prompting? Ask Build Agent.](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544)

-   **[Example Build Agent use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/additional-build-agent-use-cases.md)**  
Use Build Agent for a wide range of development scenarios beyond application creation, including app analysis, modernization, documentation, governance, and learning assistance. Reference these scenarios to identify ways to apply Build Agent across your development workflow.
-   **[Build Agent workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-workflow.md)**  
The Build Agent workflow automates building applications, testing, and deploying update sets on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.
-   **[Tutorial for Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-tutorial.md)**  
Learn to develop reusable server-side logic and build a ServiceNow® application in Build Agent, from data modeling through testing, using AI-assisted development.
-   **[General guidelines for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-general-guidelines.md)**  
Use these guidelines to get the most out of Build Agent in your development workflow.
-   **[Build Agent tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-tools.md)**  
Build Agent tools support application development tasks such as semantic search, schema inspection, code search, planning, UI validation, database querying, and app navigation. Each tool extends what Build Agent can do during a build session.
-   **[MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/accelerate-design-to-development-with-figma-mcp-server.md)**  
MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.
-   **[Build Agent governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-governance.md)**  
Governance controls in Build Agent help with code quality, security, and compliance when generating applications. The Build Agent automated safeguards prevent common development issues and enforce organizational standards.
-   **[Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-limitations.md)**  
Plan deployments and troubleshoot issues by learning about Build Agent constraints that affect deployment capabilities and performance.

**Parent Topic:**[Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent.md)

