---
title: Get started vibe coding with Build Agent
description: Use Build Agent on the ServiceNow AI Platform to vibe code and create apps by executing complex configuration and development tasks through conversational prompts. This approach simplifies editing and creating ServiceNow applications and metadata such as tables, relationships, and access controls, without manual navigation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build Agent overview, Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Get started vibe coding with Build Agent

Use Build Agent on the ServiceNow AI Platform to vibe code and create apps by executing complex configuration and development tasks through conversational prompts. This approach simplifies editing and creating ServiceNow applications and metadata such as tables, relationships, and access controls, without manual navigation.

**Note:** Though vibe coding doesn't usually include reviewing code, review any AI-generated code before deploying it.

## Build Agent and developing apps with AI

Build Agent is an autonomous AI agent native to ServiceNow that translates plain language instructions into ready-to-deploy applications and metadata, using the platform’s domain language and guardrails. It's purpose-built for full-stack creation and editing across tables, flows, UI, and scripts, and it operates as the core engine for vibe coding and AI-assisted development on the ServiceNow AI Platform.

Available in the ServiceNow IDE and ServiceNow Studio, Build Agent appears as a chat panel with a multi-turn conversation interface. Build Agent processes natural language prompts, autonomously generates full-stack applications, manages the entire build process, and responds to feedback. The agent generates all necessary code, organizes files clearly, and manages both the core logic and user interface components of applications.

Build Agent supports the following development tasks:

-   Generate and edit enterprise-grade applications: Create full-stack ServiceNow applications from natural language prompts with enterprise-grade governance.
-   Accelerate development workflows: Support flow design, catalog item creation, and Automated Test Framework \(ATF\) test creation.
-   Enhance understanding: Explain how to best perform tasks on the ServiceNow AI Platform.
-   Perform diverse code tasks: Refactor tables, explain and document code, validate and enhance existing applications, fix errors, run queries, and more.
-   Support governance: Work inside platform scopes, roles, and testing workflows rather than as a detached external bot.
-   Enable developer learning: Answer ServiceNow development questions, summarize documents, and provide practical examples.

For more information on Build Agent, see [Build Agent](../../build-agent/concept/build-agent.md).

## General guidelines for AI-assisted development with Build Agent

To maximize Build Agent effectiveness, use the following practices:

-   Design before coding: Think through and document the requirements for your application across the data and UI layers, for example using Workflow Studio or Figma.
-   Start with a clear plan: Collaborate with Build Agent to define scope, required tables, and metadata types.
-   Instruct with context: Write instructions for what you want to achieve with your application to give context using Markdown in your file system.
-   Communicate clearly: Treat Build Agent as your development partner with specific, clear instructions.
-   Test early and often: Use the agent to add sample records, test on the instance, and build ATF tests.
-   Use version control: Use Git for tracking changes and maintaining a clean workspace structure.
-   Provide visual context: If you want an enhanced UI, give screenshots to Build Agent to troubleshoot and request changes.
-   Maximize UI and integration: Integrate third-party Node Package Manager \(NPM\) libraries like React JS for enhanced interfaces.
-   Maintain documentation: Keep clear rules and documentation in project folders; use Build Agent to create Knowledge Base articles.
-   Iterate and experiment: Prototype freely and ask Build Agent for optimal prompts once your vision is complete.

## Where to use Build Agent

Access Build Agent through either of the following options:

-   Customer instance: Upgrade to a minimum of Zurich and activate Build Agent \(Trial\) with a 25 calls per month limit.
-   Personal developer instance: Request a Zurich or above Personal Development Instance \(PDI\) on the [Developer site](https://developer.servicenow.com/) with a 10 calls per month limit.

## Tools for using Build Agent

You can access Build Agent within both ServiceNow Studio and ServiceNow IDE. Both products offer different experiences for different levels of AI-assisted app development.

## Limitations of Build Agent

Use Build Agent for creating standalone apps that have limited interaction with flows, deployment, etc. on the ServiceNow AI Platform. For details, see [Limitations of AI-assisted app generation with Build Agent](vc-build-agent-limitations.md).

## Helpful resources

ServiceNow resources for AI-assisted development:

-   **![](../../../reuse/icons/dcx-icons/dcx-icon-community.svg) App Engine Academy: Practical Build Agent - Add Gen AI to your existing dev methodology**

    [App Engine Academy on YouTube](https://www.youtube.com/watch?v=37msFk6xukM)

-   **Install a trial version of Build Agent**

    [Get Build Agent on the ServiceNow Store](https://store.servicenow.com/store/app/0b1eae7ec3a4b690bc9a989f0501316c)

-   **Community article on learning prompting from Build Agent**

    [The fastest way to learn Build Agent prompting? Ask Build Agent.](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544)

-   **Vibe coding with ServiceNow Build Agent: The future of AI-powered app development**

    [Community blog on getting started with Build Agent](https://www.servicenow.com/community/now-assist-for-creator-articles/zurich-release-vibe-coding-with-servicenow-build-agent-the/ta-p/3408806)

-   **Build Agent enablement guide**

    [\#BuildWithBuildAgent Guidebook on Community](https://www.servicenow.com/community/developer-advocate-blog/your-buildwithbuildagent-guidebook-is-here/ba-p/3419535)


**Parent Topic:**[AI-assisted ServiceNow AI Platform development with Build Agent](vc-build-agent-landing.md)

