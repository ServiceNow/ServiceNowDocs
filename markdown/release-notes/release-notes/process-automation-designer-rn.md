---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

## Playbooks highlights for the Zurich release

-   Add permissions for playbook authors and runtime users.
-   Activate a playbook without a trigger. Set multiple potential triggers for a playbook, or trigger a playbook on a schedule.
-   Enable AI agents to complete activities without human intervention during runtime.
-   Set child variants to evaluate later in a playbook.
-   Create decision branches for stages.

See [Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer.md) for more information.

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Zurich

After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

## New in the Zurich release

-   **[Set child variants to evaluate later in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/set-evaluation-point.md)**

    Instead of evaluating immediately after the trigger, set a playbook's child variants to be evaluated after a specific activity in the playbook.

-   **[Agentic Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/agentic-playbooks.md)**

    Enable AI agents to assist users with activities during runtime.

-   **[Add permissions for playbook authors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/user-access-playbooks.md)**

    Control which playbook authors can create, edit, and view playbooks in Workflow Studio

-   **[Add permissions for runtime users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-process-definition.md)**

    Control whether runtime users can [view a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-process-definition.md), [add optional activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/optional-activities.md), [restart a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/restart.md), and [complete work within specific stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-stage.md).

-   **[Create decision branches for stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-decision-stage.md)**

    Add a decision node between stages to determine which stage to run next, based on runtime conditions.

-   **[Set multiple triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer-triggers.md)**

    Configure a playbook to run based on any one of multiple triggers.

-   **[Schedule when a playbook should trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-scheduled-trigger-definition.md)**

    Configure a playbook to run based on a schedule.

-   **[Choose your LLM for playbook generation and recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/change-default-llm-playbook-generation.md)**

    Choose between NowLLM, OpenAI ChatGPT4-o, Gemini, Claude for playbook generation and recommendations.

-   **[Route users to stages based on decisions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-stage.md)**

    Send runtime users to a stage based off of the trigger record or input that users provide.

-   **[Generate a playbook with a trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/playbook-assist.md)**

    Generate a playbook with both a trigger and activities.


-   **[Playbook summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/playbook-summarization.md)**

    Generate an AI-powered summary of a playbook from the Workflow Studio canvas. The summary covers the playbook's stages, activities, triggers, and inputs, helping you understand quickly about its purpose and flow without reading through each activity individually.

-   **[Use AI skill as an activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/use-ai-skill-as-activity.md)**

    Add an existing AI skill as an activity in your playbook to run lightweight, focused AI tasks as part of the playbook flow. When the playbook reaches the activity, the skill executes, produces structured outputs, and passes those outputs to subsequent activities automatically.

-   **[Use custom agent in Agentic Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-agentic-playbooks.md)**

    In addition to the default AI Agents, you can add your custom AI Agent for an activity. Choose how you want to use the AI Agents in the activity- Collaborative or Autonomous.


-   **[Playbook generation from a KB article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/playbook-generation-from-kb.md)**

    Generate a playbook directly from an existing knowledge base article to reduce manual effort when creating playbooks for documented processes.


## Changed in this release

-   **[Activate playbooks without a trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer-triggers.md)**

    Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **[Implement playbooks that are callable by a scriptable API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer-triggers.md)**

    Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **[Decision activity enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-a-decision-activity.md)**

    User experience improvements to decision activities:

    -   In the Board view, select the branch or Start rule icon on a decision activity card to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-activity.md)**

    Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.


## Deprecations

-   now.assist.creator role

## Activation information

The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The application can be downloaded for patch fixes.

To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

Download the latest Workflow Studio app in the ServiceNow Store to access the newest features.

## Accessibility information

-   In Diagram view, navigate between and configure stages and activities [via keyboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/keyboard-navigation-in-playbook-diagram-view.md).
-   Set the action bar to always show in Diagram view. To learn more, see [View all buttons without hover](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/view-all-buttons-without-hover.md).
-   In Diagram view, use a screen reader to help navigate the designer.
-   Updated color contrast for activities to meet WCAG standards.

## Localization information

Using OpenAI LLMs for playbook generation is not available in the APAC region.

## Related ServiceNow applications and features

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio consolidates , Workflow Studio, Action Designer, Integration Hub integrations, and ServiceNow® Decision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-flows.md)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results they produce.

-   **[Playbook Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/playbook-ui.md)**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/workflow-studio-rn-landing.md)

