---
title: Playbook release notes
description: The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/process-automation-designer-rn.html
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Workflow Studio release notes, App development and low-code release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Playbook release notes

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

## About Playbook release notes

-   Nest playbooks within other playbooks.
-   Enable runtime users to launch a playbook on demand.
-   Test playbooks with the Automated Test Framework.
-   Preview the UI for an activity in when configuring a playbook activity in Workflow Studio.
-   Use AI agents as activities in your playbook to automate tasks.

See [Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md) for more information.

## Activation and other requirements

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    The Playbooks application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like Process Automation Content and Process Automation Experience Demo. The Playbooks application can be downloaded for patch fixes.

    To use playbook generation features in Workflow Studio, download the  application. To use Agentic Playbooks, enable it through Now Assist.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    After you upgrade to Australia, update the Workflow Studio application in the ServiceNow Store.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/workflow-studio-rn-landing.md)

## August 2026

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

### What's new

-   **[Playbook as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-as-mcp-tool.md)**

    Expose a playbook as a tool in an MCP server, enabling MCP clients to trigger and execute the playbook through the Model Context Protocol \(MCP\).

-   **[AI agents autonomous support configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-activity-definition.md)**

    Configure in the activity definition how you want autonomous support from AI agents for that activity. The additional configurations help you gain more control on the activity in a playbook.


## July 2026

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

### What's new

-   **[Go back activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/go-back-activity.md)**

    Use the Go Back activity to define a conditional return point in a playbook. When placed in a decision branch, the activity directs the playbook to loop back to a specified point. The playbook can look back to an earlier activity, stage, or the start of the playbook based on the branch outcome. This enables conditional retry and re-evaluation logic without duplicating flow structure.

-   **[Playbook generation from a KB article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-generation-from-kb.md)**

    Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.

-   **[Preview an activity's runtime UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/preview-playbook-runtime-ui.md)**

    Preview an activity's runtime UI directly from the diagram canvas, with a real-time side-by-side preview that updates as you edit.

-   **[Fluent support for Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-process-definition.md)**

    Build, edit, and manage playbooks as code with the Fluent domain-specific language \(DSL\) in the ServiceNow IDE or a local SDK.


## June 2026

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

### What's new

-   **[Playbook summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-summarization.md)**

    Generate an AI-powered summary of a playbook from the Workflow Studio canvas. The summary covers the playbook's stages, activities, triggers, and inputs, helping you understand quickly about its purpose and flow without reading through each activity individually.

-   **[Use AI skill as an activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/use-ai-skill-as-activity.md)**

    Add an existing AI skill as an activity in your playbook to run lightweight, focused AI tasks as part of the playbook flow. When the playbook reaches the activity, the skill executes, produces structured outputs, and passes those outputs to subsequent activities automatically.

-   **[Use custom agent in Agentic Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/configure-agentic-playbooks.md)**

    In addition to the default AI Agents, you can add your custom AI Agent for an activity. Choose how you want to use the AI Agents in the activity- Collaborative or Autonomous.


## Australia General Availability

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

### What's new

-   **[Use AI agents as a playbook activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/ai-agent-as-activity.md)**

    Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.


## Australia

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

### What's new

-   **[Nested playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/nested-playbooks.md)**

    Nest playbooks as a step within other playbooks to enable the following scenarios:

    -   Define sets of activities for reuse across multiple playbooks to help avoid duplication.
    -   Break up large playbooks for easy maintenance and fast load time in Playbook Designer.
-   **Simplified end-user playbook experience**

    Implement a wizard experience for guiding your end users through a sequence of steps to achieve an outcome, such as servicing a printer.

-   **[Automated Test Framework support for playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/testing-support-playbooks.md)**

    The Automated Test Framework can be used to create automated tests to confirm your playbooks run as planned.


### What's changed

-   **[Required role update](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/user-access-playbooks.md)**

    Any tasks that previously required only the admin role now require the playbook.admin role instead.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Changes in the Now LLM service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **ServiceNow Otto**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Playbooks. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


### What's deprecated or removed

The now.assist.creator role is no longer a required role to generate a playbook or playbook recommendation when using Now Assist.

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

