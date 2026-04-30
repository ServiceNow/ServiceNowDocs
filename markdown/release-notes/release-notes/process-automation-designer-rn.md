---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.

## Playbooks highlights for the Yokohama release

-   Add custom translations for playbooks.
-   Restart playbook activities that have ended in error.
-   Create a checklist directly in the side panel without needing a checklist template.
-   Generate a playbook via API in other ServiceNow applications such as IT Operations Management \(ITOM\).
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.

See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Yokohama

After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.

## New in the Yokohama release

-   **[Translate playbooks content](https://www.servicenow.com/docs/access?context=add-translations-playbooks&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Add custom translations for labels, descriptions, and UI Layout properties in your playbooks.

-   **[Restart playbook activities that end in error](https://www.servicenow.com/docs/access?context=restart&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Configure activities so that end users can restart any activity that ends in an error and variant conditions are automatically re-evaluated when playbooks are restarted.

-   **[Support for Retrieval Augmented Generation \(RAG\) with playbook generation](https://www.servicenow.com/docs/access?context=playbook-assist&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions available on your instance in your playbook generation requests.

-   **Generate playbooks with the OpenAI GPT-4o LLM**

    Use the OpenAI GPT-4o LLM to generate a playbook from text.

-   **[Add more fields in Create Task activities](https://www.servicenow.com/docs/access?context=create-task-activity&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Add more fields in a more configurable Create Task activity.

-   **[Create a checklist directly in Workflow Studio](https://www.servicenow.com/docs/access?context=checklist-task-activity&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Create a checklist directly in the side panel without needing a checklist template.


## UI changes

-   **Trigger label updated**

    The trigger is now labeled "Start" in Workflow Studio.


## Changed in this release

-   **Change triggers in any playbook**

    Edit triggers when you duplicate a playbook, in a variant, etc.


## Deprecations

-   If you have the old Create Task activity in your existing playbooks, it will continue to function. You just can't add the extra fields that are available only in the new Create Task activity.
-   If you have the old Checklist activity in your existing playbooks, it will continue to function. You just won't be able to update the checklist directly in Workflow Studio the way that you can with the new Checklist activity.

## Activation information

The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The application can be downloaded for patch fixes.

To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Using OpenAI LLMs for playbook generation is not available in the APAC region.

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio consolidates , Workflow Studio, Action Designer, Integration Hub integrations, and ServiceNow® Decision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=exploring-flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results they produce.

-   **Playbook Experiences**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn.md)

