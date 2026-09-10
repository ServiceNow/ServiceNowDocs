---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

## About Playbooks in Workflow Studio

-   Add permissions for playbook authors and runtime users.
-   Activate a playbook without a trigger. Set multiple potential triggers for a playbook, or trigger a playbook on a schedule.
-   Enable AI agents to complete activities without human intervention during runtime.
-   Set child variants to evaluate later in a playbook.
-   Create decision branches for stages.

See  for more information.

## Activation and other requirements

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The application can be downloaded for patch fixes.

    To use the playbook generation feature in Workflow Studio, download the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

-   **Additional requirements**

    Download the latest Workflow Studio app in the ServiceNow Store to access the newest features.


## Accessibility and localization

-   **Accessibility information**
    -   In Diagram view, navigate between and configure stages and activities via keyboard.
    -   Set the action bar to always show in Diagram view. To learn more, see .
    -   In Diagram view, use a screen reader to help navigate the designer.
    -   Updated color contrast for activities to meet WCAG standards.
-   **Localization information**

    Using OpenAI LLMs for playbook generation is not available in the APAC region.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/workflow-studio-rn-landing.md)

## August 2026

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **Playbook as an MCP tool**

    Expose a playbook as a tool in an MCP server, enabling MCP clients to trigger and execute the playbook through the Model Context Protocol \(MCP\).

-   **AI agents autonomous support configurations**

    Configure in the activity definition how you want autonomous support from AI agents for that activity. The additional configurations help you gain more control on the activity in a playbook.


## July 2026

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **Playbook generation from a KB article**

    Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.


## June 2026

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **Playbook summarization**

    Generate an AI-powered summary of a playbook from the Workflow Studio canvas. The summary covers the playbook's stages, activities, triggers, and inputs, helping you understand quickly about its purpose and flow without reading through each activity individually.

-   **Use AI skill as an activity**

    Add an existing AI skill as an activity in your playbook to run lightweight, focused AI tasks as part of the playbook flow. When the playbook reaches the activity, the skill executes, produces structured outputs, and passes those outputs to subsequent activities automatically.

-   **Use custom agent in Agentic Playbooks**

    In addition to the default AI Agents, you can add your custom AI Agent for an activity. Choose how you want to use the AI Agents in the activity- Collaborative or Autonomous.


## December 2025

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **Set child variants to evaluate later in a playbook**

    Instead of evaluating immediately after the trigger, set a playbook's child variants to be evaluated after a specific activity in the playbook.

-   **Create decision branches for stages**

    Add a decision node between stages to determine which stage to run next, based on runtime conditions.


### What's deprecated or removed

-   now.assist.creator role

## November 2025

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **[Route users to stages based on decisions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-stage.md)**

    Send runtime users to a stage based off of the trigger record or input that users provide.


## Zurich General Availability

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new


### What's deprecated or removed


## Zurich

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

### What's new

-   **Agentic Playbooks**

    Enable AI agents to assist users with activities during runtime.

-   **Add permissions for playbook authors**

    Control which playbook authors can create, edit, and view playbooks in Workflow Studio

-   **Add permissions for runtime users**

    Control whether runtime users can view a playbook, add optional activities, restart a playbook, and [complete work within specific stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-stage.md).

-   **Set multiple triggers**

    Configure a playbook to run based on any one of multiple triggers.

-   **Schedule when a playbook should trigger**

    Configure a playbook to run based on a schedule.

-   **Choose your LLM for playbook generation and recommendations**

    Choose between NowLLM, OpenAI ChatGPT4-o, Gemini, Claude for playbook generation and recommendations.

-   **Generate a playbook with a trigger**

    Generate a playbook with both a trigger and activities.


### What's changed

-   **Activate playbooks without a trigger**

    Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **Implement playbooks that are callable by a scriptable API**

    Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **Decision activity enhancements**

    User experience improvements to decision activities:

    -   In the Board view, select the branch to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-activity.md)**

    Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.

-   **ServiceNow Otto**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Playbooks. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


