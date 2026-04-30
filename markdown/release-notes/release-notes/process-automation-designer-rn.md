---
title: Playbooks in Workflow Studio release notes
description: The ServiceNow Playbooks builder within the ServiceNow Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Playbooks in Workflow Studio release notes

The ServiceNow® Playbooks builder within the ServiceNow® Workflow Studio application enables playbook owners to create multiple-flow processes in a diagram or task board interface. The Playbooks builder was enhanced and updated in the Xanadu release.

## Playbooks highlights for the Xanadu release

-   Use one playbook for multiple scenarios with variants.
-   Get recommendations on which activities to replace placeholder activities with.
-   Preview and modify your text directions before generating your playbook outline with Now Assist.
-   Generate a playbook with out-of-the-box activities from text, an image or both.
-   Collect custom responses from an end user, without requiring an existing table or fields.
-   Better manage access to your playbooks and playbook components.

See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for more information.

**Important:** Playbooks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Playbooks to Xanadu

After you upgrade to Xanadu, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

## New in the Xanadu release

-   **[Variants](https://www.servicenow.com/docs/access?context=playbook-variants&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Use one playbook for multiple scenarios with variants.

-   **[Playbook recommendations](https://www.servicenow.com/docs/access?context=playbook-recommendations&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Get suggestions on which activities to replace placeholder activities with.

-   **[Re-prompt and preview](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Preview and modify your prompt before building your playbook.

-   **[Image to playbook generation](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Generate a playbook with out-of-the-box activities from text, an image, or both.

-   **[Questionnaire activity](https://www.servicenow.com/docs/access?context=questionnaire-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Reference flow glide variable input and output values in an activity's condition builders to collect up to 10 pieces of information from an agent or fulfiller to use later during a playbook run, without requiring an existing table or fields.

-   **[Greater access controls](https://www.servicenow.com/docs/access?context=user-access-playbooks&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Better manage access to your playbooks and playbook components.

-   **[Archived data enhancements](https://www.servicenow.com/docs/access?context=archive-process-executions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Schedule process execution data to be archived, and view the JSON files for your archived data.

-   **[Script support for activate, restart, deactivate, and duplicate](https://servicenow.com/docs/bundle/xanadu-release-notes/page/release-notes/now-platform-app-engine/api-rn.html)**

    Use a script include or business rule that calls the activate, deactivate, restart, or duplicate playbook APIs.

-   **[Washington 25.2 release](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

    See 25.2 features in the [Washington DC Playbooks release notes](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   Playbook Assist

## Changed in this release

-   **[Updated Roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    The pd\_admin role is now playbook.admin.

-   **Activities trigger asynchronously**

    To avoid slowing down the playbook runs, the first activities are triggered asynchronously.


## Removed in this release

Use the Questionnaire activity instead of the Collect User Data activity.

## Activation information

The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the app in the ServiceNow Store, as well as related applications like the Process Automation Experience Demo application.

To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The following features are part of the ServiceNow AI Platform® and are active by default:

-   Archived data enhancements
-   Script support for activate, restart, and deactivate
-   Updated roles
-   Greater access controls

Download the app in the ServiceNow Store to access the following features:

-   Variants
-   Questionnaire activity
-   Playbook Recommendations
-   Re-prompt and preview

For access to all Xanadu features, download the latest app in the store.

## Localization information

Playbook generation with images is not available in the APAC region.

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio consolidates , Workflow Studio, Action Designer, Integration Hub integrations, and ServiceNow® Decision Builder into one design environment. Author, configure, and monitor all of your workflows in a streamlined experience.

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=exploring-flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results they produce.

-   **Playbook Experiences**

    ServiceNow® Playbook experiences enable you to customize the default playbook user experience for your agents.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn.md)

