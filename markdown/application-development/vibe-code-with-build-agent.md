---
title: Get started with agentic development using Build Agent
description: Use Build Agent on the ServiceNow AI Platform to build apps agentically by executing complex configuration and development tasks through conversational prompts. This approach simplifies editing and creating ServiceNow applications and metadata such as tables, relationships, and access controls, without manual navigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/vibe-code-with-build-agent.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build Agent overview, Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Get started with agentic development using Build Agent

Use Build Agent on the ServiceNow AI Platform to build apps agentically by executing complex configuration and development tasks through conversational prompts. This approach simplifies editing and creating ServiceNow applications and metadata such as tables, relationships, and access controls, without manual navigation.

**Note:** Review any AI-generated code before deploying it.

For more information on Build Agent, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent.md).

## Build Agent and agentic app development

Build Agent is an autonomous AI agent native to ServiceNow that translates plain language instructions into ready-to-deploy applications and metadata, using the platform’s domain language and guardrails. It's purpose-built for full-stack creation and editing across tables, flows, UI, and scripts, and it operates as the core engine for vibe coding and AI-assisted development on the ServiceNow AI Platform.

Available in the ServiceNow IDE and ServiceNow Studio, Build Agent appears as a chat panel with a multi-turn conversation interface. Build Agent processes natural language prompts, autonomously generates full-stack applications, manages the entire build process, and responds to feedback. The agent generates all necessary code, organizes files clearly, and manages both the core logic and user interface components of applications.

Build Agent supports the following development tasks:

-   Generate and edit enterprise-grade applications: Create full-stack ServiceNow applications from natural language prompts with enterprise-grade governance.
-   Accelerate development workflows: Support flow design, catalog item creation, and Automated Test Framework \(ATF\) test creation.
-   Enhance understanding: Explain how to best perform tasks on the ServiceNow AI Platform.
-   Perform diverse code tasks: Refactor tables, explain and document code, validate and enhance existing applications, fix errors, run queries, and more.
-   Support governance: Work inside platform scopes, roles, and testing workflows rather than as a detached external bot.
-   Enable developer learning: Answer ServiceNow development questions, summarize documents, and provide practical examples.

For more information on Build Agent, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent.md).

## General guidelines for agentic development with Build Agent

To maximize Build Agent effectiveness, use the following practices:

-   Design before coding: Think through and document the requirements for your application across the data and UI layers, for example using Workflow Studio or Figma.
-   Start with a clear plan: Collaborate with Build Agent to define scope, required tables, and metadata types.
-   Instruct with context: Write instructions for what you want to achieve with your application using Markdown in your file system, and ask Build Agent to use the file as context for its work.
-   Use specific terminology: Treat Build Agent as your development partner. Provide specific, clear instructions using ServiceNow platform terminology such as table names, field names, roles, and artifact types.
-   Test early and often: Add sample records, test on the instance, and build ATF tests throughout development.
-   Use version control: Use Git for tracking changes and maintaining a clean workspace structure.
-   Provide visual context: Give screenshots to Build Agent to troubleshoot UI issues and request changes.
-   Extend with third-party libraries: Integrate third-party Node Package Manager \(NPM\) libraries, such as React JS, for enhanced interfaces.
-   Maintain documentation: Keep clear rules and documentation in project folders; use Build Agent to create knowledge base articles.
-   Iterate and experiment: Prototype freely, then ask Build Agent for an ideal prompt to recreate the result once your vision is complete.

## Where to use Build Agent

Access Build Agent through either of the following options:

-   Customer instance: Upgrade to a minimum of Zurich and activate Build Agent \(Trial\) with a 25 calls per month limit.
-   Personal developer instance: Request a Zurich or above Personal Development Instance \(PDI\) on the [Developer site](https://developer.servicenow.com/) with a 10 calls per month limit.

## Tools for using Build Agent

You can access Build Agent within both ServiceNow Studio and ServiceNow IDE. Both products offer different experiences for different levels of agentic app development.

## Limitations of Build Agent

Use Build Agent for creating standalone apps that have limited interaction with flows, deployment, etc. on the ServiceNow AI Platform. For details, see [Limitations of agentic app generation with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vc-build-agent-limitations.md).

## Helpful resources

ServiceNow resources for AI-assisted development:

-   **\[Omitted image "dcx-icon-community.svg"\] App Engine Academy: Practical Build Agent - Add Gen AI to your existing dev methodology**

    [App Engine Academy on YouTube](https://www.youtube.com/watch?v=37msFk6xukM)

-   **Install a trial version of Build Agent**

    [Get Build Agent on the ServiceNow Store](https://store.servicenow.com/store/app/0b1eae7ec3a4b690bc9a989f0501316c)

-   **Community article on learning prompting from Build Agent**

    [The fastest way to learn Build Agent prompting? Ask Build Agent.](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544)

-   **Vibe coding with ServiceNow Build Agent: The future of AI-powered app development**

    [Community blog on getting started with Build Agent](https://www.servicenow.com/community/now-assist-for-creator-articles/zurich-release-vibe-coding-with-servicenow-build-agent-the/ta-p/3408806)

-   **Build Agent enablement guide**

    [\#BuildWithBuildAgent Guidebook on Community](https://www.servicenow.com/community/developer-advocate-blog/your-buildwithbuildagent-guidebook-is-here/ba-p/3419535)


**Parent Topic:**[AI-assisted ServiceNow AI Platform development with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vc-build-agent-landing.md)

