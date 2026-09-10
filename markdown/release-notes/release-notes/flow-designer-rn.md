---
title: Flows, subflows, and actions release notes
description: The ServiceNow Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.The ServiceNow Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.The ServiceNow Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-09-02"
reading_time_minutes: 3
---

# Flows, subflows, and actions release notes

The ServiceNow® Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.

## About Flows, subflows, and actions

-   Compare two flow histories to see what content was added, removed, and updated.
-   Summarize flow execution details to identify errors and suggest potential fixes.
-   Test conversation-enabled actions and subflows from a conversation.
-   Use an AI agent from a flow.

See , , and  for more information.

## Activation and other requirements

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Workflow Studio is a ServiceNow AI Platform feature that is active by default.

    Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see .

    The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/read-only-option.md).


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/workflow-studio-rn-landing.md)

## Australia General Availability

The ServiceNow® Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.

### What's new


## Australia

The ServiceNow® Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.

### What's new

-   **Business calendar as a scheduled trigger**

    Use the business calendar to trigger flows on existing business schedules. The business calendar trigger helps align automation with shifts, holidays, and operating hours.

-   ****

    Compare two flow history entries in a side-by-side view. Use the step highlighting and change type icons to determine what flow components have been added, removed, and changed.

-   **Flow execution analysis**

    Analyze flow execution details to identify errors and suggest potential fixes.

-   ****

    Test a conversational action to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   ****

    Test a conversational subflow to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   ****

    Use flow data to run an AI agent and configure the expected agent output for use later in the flow.


### What's deprecated or removed

The now.assist.creator role is no longer a required role to use generative AI features with Now Assist.

