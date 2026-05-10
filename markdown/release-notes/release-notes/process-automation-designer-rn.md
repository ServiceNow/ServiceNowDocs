---
title: Playbook release notes
description: The Playbook builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Playbook release notes

The Playbook builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbook builder was enhanced and updated in the Australia release.

## Playbooks highlights for the Australia release

-   Nest playbooks within other playbooks.
-   Enable runtime users to launch a playbook on demand.
-   Test playbooks with the Automated Test Framework.
-   Preview the UI for an activity in when configuring a playbook activity in Workflow Studio.
-   Use AI agents as activities in your playbook to automate tasks.

See [Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer.md) for more information.

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Australia

After you upgrade to Australia, update the Workflow Studio application in the ServiceNow Store.

## New in the Australia release

-   **[Nested playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/nested-playbooks.md)**

    Nest playbooks as a step within other playbooks to enable the following scenarios:

    -   Define sets of activities for reuse across multiple playbooks to help avoid duplication.
    -   Break up large playbooks for easy maintenance and fast load time in Playbook Designer.
-   **[Simplified end-user playbook experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/wizard-layouts-playbooks.md)**

    Implement a wizard experience for guiding your end users through a sequence of steps to achieve an outcome, such as servicing a printer.

-   **[Automated Test Framework support for playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/testing-support-playbooks.md)**

    The Automated Test Framework can be used to create automated tests to confirm your playbooks run as planned.

-   **[Use AI agents as a playbook activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/ai-agent-as-activity.md)**

    Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.


## Changed in this release

-   **[Required role update](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-playbooks.md)**

    Any tasks that previously required only the admin role now require the playbook.admin role instead.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

The Playbooks application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like Process Automation Content and Process Automation Experience Demo. The Playbooks application can be downloaded for patch fixes.

To use playbook generation features in Workflow Studio, download the [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md) application. To use Agentic Playbooks, enable it through Now Assist.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio.md)**

    ServiceNow® Workflow Studio consolidates Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, andDecision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **[Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-architecture-overview.md)**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn-landing.md)

