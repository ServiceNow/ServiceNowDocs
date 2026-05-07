---
title: Flows, Subflows, and Actions release notes
description: The ServiceNow Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Flows, Subflows, and Actions release notes

The ServiceNow® Workflow Studio flows, subflows, and actions application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Australia release.

## Workflow Studio flows, subflows, and actions highlights for the Australia release

-   Compare two flow histories to see what content was added, removed, and updated.
-   Summarize flow execution details to identify errors and suggest potential fixes.
-   Test conversation-enabled actions and subflows from a conversation.
-   Use an AI agent from a flow.

See [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US), [Exploring subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US), and [Exploring actions](https://www.servicenow.com/docs/access?context=exploring-actions&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for more information.

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Workflow Studio flows, subflows, and actions to Australia

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://www.servicenow.com/docs/access?context=restore-save-as-you-go-functionality&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## New in the Australia release

-   **[Business calendar as a scheduled trigger](https://www.servicenow.com/docs/access?context=create-trigger-business-calendar&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Use the business calendar to trigger flows on existing business schedules. The business calendar trigger helps align automation with shifts, holidays, and operating hours.

-   **[Flow history compare view](https://www.servicenow.com/docs/access?context=flow-history-compare-view&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Compare two flow history entries in a side-by-side view. Use the step highlighting and change type icons to determine what flow components have been added, removed, and changed.

-   **[Flow execution analysis](https://www.servicenow.com/docs/access?context=flow-execution-analysis-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Analyze flow execution details to identify errors and suggest potential fixes.

-   **[Test conversational action](https://www.servicenow.com/docs/access?context=test-conversational-action&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Test a conversational action to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   **[Test conversational subflow](https://www.servicenow.com/docs/access?context=test-conversational-subflow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Test a conversational subflow to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   **[Use an AI agent action](https://www.servicenow.com/docs/access?context=use-an-ai-agent-action&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Use flow data to run an AI agent and configure the expected agent output for use later in the flow.


## Removed in this release

The now.assist.creator role is no longer a required role to use generative AI features with Now Assist.

## Activation information

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Exploring Playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Playbook enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.

-   **[Data Stream actions and pagination](https://www.servicenow.com/docs/access?context=data-stream-actions&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.

-   **[Exploring Decision Tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Decision tables in Workflow Studio enable developers to decouple decision logic from their code by creating and maintaining decision rules.

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Automate integration tasks using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn-landing.md)

