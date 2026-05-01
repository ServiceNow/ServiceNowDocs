---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Zurich release.

## Playbooks highlights for the Zurich release

-   Add permissions for playbook authors and runtime users.
-   Activate a playbook without a trigger. Set multiple potential triggers for a playbook, or trigger a playbook on a schedule.
-   Enable AI agents to complete activities without human intervention during runtime.
-   Set child variants to evaluate later in a playbook.
-   Create decision branches for stages.

See [Exploring Playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Zurich

After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

## New in the Zurich release

-   **[Set child variants to evaluate later in a playbook](https://www.servicenow.com/docs/access?context=set-evaluation-point&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Instead of evaluating immediately after the trigger, set a playbook's child variants to be evaluated after a specific activity in the playbook.

-   **[Agentic Playbooks](https://www.servicenow.com/docs/access?context=agentic-playbooks&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Enable AI agents to assist users with activities during runtime.

-   **[Add permissions for playbook authors](https://www.servicenow.com/docs/access?context=user-access-playbooks&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Control which playbook authors can create, edit, and view playbooks in Workflow Studio

-   **[Add permissions for runtime users](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Control whether runtime users can [view a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [add optional activities](https://www.servicenow.com/docs/access?context=optional-activities&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [restart a playbook](https://www.servicenow.com/docs/access?context=restart&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), and [complete work within specific stages](https://www.servicenow.com/docs/access?context=add-configure-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

-   **[Create decision branches for stages](https://www.servicenow.com/docs/access?context=create-decision-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Add a decision node between stages to determine which stage to run next, based on runtime conditions.

-   **[Set multiple triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Configure a playbook to run based on any one of multiple triggers.

-   **[Schedule when a playbook should trigger](https://www.servicenow.com/docs/access?context=create-scheduled-trigger-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Configure a playbook to run based on a schedule.

-   **[Choose your LLM for playbook generation and recommendations](https://www.servicenow.com/docs/access?context=change-default-llm-playbook-generation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Choose between NowLLM, OpenAI ChatGPT4-o, Gemini, Claude for playbook generation and recommendations.

-   **[Route users to stages based on decisions](https://www.servicenow.com/docs/access?context=add-configure-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Send runtime users to a stage based off of the trigger record or input that users provide.

-   **[Yokohama 27.2 and 27.3 releases](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

    See 27.2 and 27.3 features in the [Yokohama Playbooks release notes](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   [Generate a playbook with the OpenAI GPT-4o LLM](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
    -   [Retrieval Augmented Generation \(RAG\) for playbooks](https://www.servicenow.com/docs/access?context=playbook-assist&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

## Changed in this release

-   **[Activate playbooks without a trigger](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **[Implement playbooks that are callable by a scriptable API](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **[Decision activity enhancements](https://www.servicenow.com/docs/access?context=create-a-decision-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    User experience improvements to decision activities:

    -   In the Board view, select the branch or Start rule icon on a decision activity card to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://www.servicenow.com/docs/access?context=add-configure-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.


## Deprecations

-   now.assist.creator role

## Activation information

The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The application can be downloaded for patch fixes.

To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

Download the latest Workflow Studio app in the ServiceNow Store to access the newest features.

## Accessibility information

-   In Diagram view, navigate between and configure stages and activities [via keyboard](https://www.servicenow.com/docs/access?context=keyboard-navigation-in-playbook-diagram-view&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).
-   Set the action bar to always show in Diagram view. To learn more, see [View all buttons without hover](https://www.servicenow.com/docs/access?context=view-all-buttons-without-hover&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Localization information

Using OpenAI LLMs for playbook generation is not available in the APAC region.

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio consolidates , Workflow Studio, Action Designer, Integration Hub integrations, and ServiceNow® Decision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=exploring-flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results they produce.

-   **[Playbook Experiences](https://www.servicenow.com/docs/access?context=playbook-ui&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn-landing.md)

