---
title: Playbook release notes
description: The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Playbook release notes

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

## Playbooks highlights for the Australia release

-   Nest playbooks within other playbooks.
-   Enable runtime users to launch a playbook on demand.
-   Test playbooks with the Automated Test Framework.
-   Preview the UI for an activity in when configuring a playbook activity in Workflow Studio.
-   Use AI agents as activities in your playbook to automate tasks.

See  for more information.

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Australia

After you upgrade to Australia, update the Workflow Studio application in the ServiceNow Store.

## New in the Australia release

-   **Nested playbooks**

    Nest playbooks as a step within other playbooks to enable the following scenarios:

    -   Define sets of activities for reuse across multiple playbooks to help avoid duplication.
    -   Break up large playbooks for easy maintenance and fast load time in Playbook Designer.
-   **Simplified end-user playbook experience**

    Implement a wizard experience for guiding your end users through a sequence of steps to achieve an outcome, such as servicing a printer.

-   **Automated Test Framework support for playbooks**

    The Automated Test Framework can be used to create automated tests to confirm your playbooks run as planned.

-   **Use AI agents as a playbook activity**

    Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.


-   **Playbook summarization**

    Generate an AI-powered summary of a playbook from the Workflow Studio canvas. The summary covers the playbook's stages, activities, triggers, and inputs, helping you understand quickly about its purpose and flow without reading through each activity individually.

-   **Use AI skill as an activity**

    Add an existing AI skill as an activity in your playbook to run lightweight, focused AI tasks as part of the playbook flow. When the playbook reaches the activity, the skill executes, produces structured outputs, and passes those outputs to subsequent activities automatically.

-   **Use custom agent in Agentic Playbooks**

    In addition to the default AI Agents, you can add your custom AI Agent for an activity. Choose how you want to use the AI Agents in the activity- Collaborative or Autonomous.


-   **Go back activity**

    Use the Go Back activity to define a conditional return point in a playbook. When placed in a decision branch, the activity directs the playbook to loop back to a specified earlier activity, stage, or the start of the playbook based on the branch outcome. This enables conditional retry and re-evaluation logic without duplicating flow structure.

-   **Playbook generation from a KB article**

    Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.

-   ****

    Preview an activity's runtime UI directly from the diagram canvas, with a real-time side-by-side preview that updates as you edit.

-   **Fluent support for Playbooks**

    Build, edit, and manage playbooks as code with the Fluent domain-specific language \(DSL\) in the ServiceNow IDE or a local SDK.


## Changed in this release

-   **Required role update**

    Any tasks that previously required only the admin role now require the playbook.admin role instead.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Changes in the Now LLM service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## Removed in this release

The now.assist.creator role is no longer a required role to generate a playbook or playbook recommendation when using Now Assist.

## Activation information

The Playbooks application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like Process Automation Content and Process Automation Experience Demo. The Playbooks application can be downloaded for patch fixes.

To use playbook generation features in Workflow Studio, download the  application. To use Agentic Playbooks, enable it through Now Assist.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio consolidates Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, andDecision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **Playbook Experience**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/workflow-studio-rn-landing.md)

