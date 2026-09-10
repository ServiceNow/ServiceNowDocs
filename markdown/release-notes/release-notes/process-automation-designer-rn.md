---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.

## About Playbooks in Workflow Studio

-   Add custom translations for playbooks.
-   Restart playbook activities that have ended in error.
-   Create a checklist directly in the side panel without needing a checklist template.
-   Generate a playbook via API in other ServiceNow applications such as IT Operations Management \(ITOM\).
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.

See  for more information.

## Activation and other requirements

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The application can be downloaded for patch fixes.

    To use the playbook generation feature in Workflow Studio, download the [ServiceNow Otto for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.


## Accessibility and localization

-   **Accessibility information**
-   **Localization information**

    Using OpenAI LLMs for playbook generation is not available in the APAC region.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/workflow-studio-rn.md)

## May 2025

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.

### What's new

-   **Support for Retrieval Augmented Generation \(RAG\) with playbook generation**

    Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions available on your instance in your playbook generation requests.

-   **Generate playbooks with the OpenAI GPT-4o LLM**

    Use the OpenAI GPT-4o LLM to generate a playbook from text.


## Yokohama General Availability

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.

### What's deprecated or removed

-   -   
## Yokohama

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Yokohama release.

### What's new

-   **Translate playbooks content**

    Add custom translations for labels, descriptions, and UI Layout properties in your playbooks.

-   **Restart playbook activities that end in error**

    Configure activities so that end users can restart any activity that ends in an error and variant conditions are automatically re-evaluated when playbooks are restarted.

-   **Add more fields in Create Task activities**

    Add more fields in a more configurable Create Task activity.

-   **Create a checklist directly in Workflow Studio**

    Create a checklist directly in the side panel without needing a checklist template.


### What's changed

-   **Trigger label updated**

    The trigger is now labeled "Start" in Workflow Studio.


-   **Change triggers in any playbook**

    Edit triggers when you duplicate a playbook, in a variant, etc.


### What's deprecated or removed

-   If you have the old Create Task activity in your existing playbooks, it will continue to function. You just can't add the extra fields that are available only in the new Create Task activity.
-   If you have the old Checklist activity in your existing playbooks, it will continue to function. You just won't be able to update the checklist directly in Workflow Studio the way that you can with the new Checklist activity.

