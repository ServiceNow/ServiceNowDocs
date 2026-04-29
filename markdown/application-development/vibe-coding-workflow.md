---
title: Workflow for vibe coding and AI-assisted development
description: The vibe coding and using AI to develop apps workflow begins with developers providing conversational prompts to the Build Agent tool, which then creates tables, forms, workflows, and automation rules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [vibe coding, AI-assisted development, workflow, conversational prompts, text-to-code generation, code explanations, optimization suggestions, governance, security, enterprise compliance, scalability, natural language, blueprint, tables, roles, UI components, workflows, full-stack components, JavaScript, metadata, business rules, integration points, automated tests, self-heal, iterative development, deployment, audit trails]
breadcrumb: [Explore, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Workflow for vibe coding and AI-assisted development

The vibe coding and using AI to develop apps workflow begins with developers providing conversational prompts to the Build Agent tool, which then creates tables, forms, workflows, and automation rules.

Integrated tools like Build Agent and Now Assist for Creator enhance the experience by offering text-to-code generation, code explanations, and optimization suggestions. Governance and security are embedded throughout the process, ensuring enterprise-grade compliance and scalability.

**Note:** The term "vibe coding" can be anything between two distinct philosophies:

-   One definition of vibe coding state that developers don't review or touch generated code before checking it in; simply provide an idea, get code back, no review needed.
-   Another definition of vibe coding is an umbrella term that encompasses AI-assisted, agentic-assisted development, where developers still need to understand and support the generated code.

ServiceNow has tools to help you review, refine, and test apps for both vibe coding, like Build Agent, and AI-assisted development, such as Now Assist for Creator.

## Step-by-Step general workflow

1.  Describe your goal: Provide a clear natural language prompt \(for example, `Create an application that handles several types of issues related to cash management. Create a custom data model with tables for each type of request. Add fields that are typical for these types of issues to each table. Request tables should extend the Task table. Create custom states for each request type to track issue resolution.`\).

    Tip:

    -   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
    -   You can craft a prompt and then feed it to an LLM, such as Claude, and ask for it to be made more specific for ServiceNow.
    For more information on example prompts, see [Example prompts for vibe coding and AI-assisted development](../reference/vibe-coding-example-prompts.md).

2.  Generate the plan: Build Agent interprets your prompt and creates a blueprint, including tables, roles, UI components, and workflows.

    Benefit: Architectural clarity before coding begins. For more information, see [Vibe coding: Chatting your way to a new app with ServiceNow Build Agent](https://www.servicenow.com/community/developer-advocate-blog/vibe-coding-chatting-your-way-to-a-new-app-with-servicenow-build/ba-p/3383952).

3.  Build and generate code: The ServiceNow AI Platform autonomously creates full-stack components using ServiceNow Fluent, JavaScript, and ServiceNow metadata.

    Includes: UI pages, data models, business rules, and integration points. For more information, see [Vibe coding with ServiceNow Build Agent: The future of AI-powered app development](https://www.servicenow.com/community/now-assist-for-creator-articles/zurich-release-vibe-coding-with-servicenow-build-agent-the/ta-p/3408806).

4.  Validate and self-heal: If you're using Build Agent, it generates automated tests and fixes errors without manual intervention.

    Governance: Compliance and security checks are applied automatically. For more information, see [Governance for vibe coding and AI-assisted app development](vc-governance.md).

5.  Refine through prompts: Add features or adjust design iteratively \(for example, `Add a Kanban board` or `Improve UI layout for accessibility`\).

    For more information, see [Vibe Coding: Chatting your way to a new app with ServiceNow Build Agent on Community](https://www.servicenow.com/community/developer-advocate-blog/vibe-coding-chatting-your-way-to-a-new-app-with-servicenow-build/ba-p/3383952).

6.  Run tests: Run Automated Test Framework to test that the app is working as expected.

    For more information, see [Testing vibe-coded and AI-developed apps](vc-and-atf.md).

7.  Deploy securely: Push from a sandbox in Developer Sandboxes with audit trails and enterprise-grade security via Vault Console and Machine Identity Console.

    For more information, see [Vibe coding, AI-assisted development, and deployment](vc-and-deployment.md).


