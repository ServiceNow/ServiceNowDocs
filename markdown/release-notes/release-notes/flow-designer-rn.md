---
title: Flows, subflows, and actions in Workflow Studio release notes
description: The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 6
---

# Flows, subflows, and actions in Workflow Studio release notes

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multiple-step flows from reusable components. Workflow Studio flows, subflows, and actions were enhanced and updated in the Zurich release.

## Workflow Studio flows, subflows, and actions highlights for the Zurich release

-   Create a scheduled trigger that you can use across your flows.
-   Save flows, subflows, and actions automatically as you work on them.
-   View and manage the history of flows and subflows to copy, restore, or remove past configurations.
-   Create multiple skills for conversational subflows and actions from the conversational settings.
-   Configure a default LLM for generating metadata for conversational subflows and actions.

See [Exploring flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-flows.md), [Exploring subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-subflows.md), and [Exploring actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-actions.md) for more information.

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading flows, subflows, and actions to Zurich

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/restore-save-as-you-go-functionality.md).

## New in the Zurich release

-   **[Create and manage external event sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/manage-external-event-sources.md)**

    Create an external event source on your ServiceNow instance that listens to events occurring in an application or system outside of the ServiceNow AI Platform®. Based on the external event source, you can define one or more external trigger definitions in your instance and then associate the external trigger definitions with the external event source. When an event that you specified in the external trigger definition occurs, the external trigger definition executes one or more flows. You can update or remove external event sources that you create.

-   **[Create a domain-separated saved external trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-saved-external-trigger.md)**

    Create a domain-separated saved external trigger. Configurations that you make to the trigger are auto-saved. After the trigger is published, you can edit only the **Label** field values.

-   **[Create a reusable scheduled trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-scheduled-trigger.md)**

    Create a scheduled trigger that starts your flow when you need. Use the trigger across your flows.

-   **[Create a skill for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-conversational-subflow-skill.md)**

    Create a skill for the conversational subflow and action and make the skill discoverable in conversations. You can have multiple skills for the same subflow or action.

-   **[Enhancements in the subflow and action conversational settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-subflow-conversation-settings.md)**

    To make the error messages more useful in a conversation, you can show specific error messages from the subflow or action rather than showing generic error messages. Additionally, if you override an input with reference, you can apply a filter to limit the number of records in the Reference field.

-   **[Make a flow wait for an email reply](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/wait-for-email-reply-action.md)**

    Pause a flow until an email reply is received to an outbound email record

-   **[Show subflow stages in a parent flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/show-subflow-stages-in-a-parent-flow.md)**

    Show subflow stages as part of the execution details of a parent flow.

-   **[Save flows, subflows, and actions automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/save-as-you-go-flows.md)**

    Save flows, subflows, and actions automatically as you work on them.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-flow-generation.md)**

    Support the Now LLM Long Term Stable models \(LTS\) for Flow generation.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/flow-summarization.md)**

    Support the Now LLM Long Term Stable models \(LTS\) for Flow summarization.

-   **[Use an AI agent action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/use-an-ai-agent-action.md)**

    Use flow data to run an AI agent and configure the expected agent output for use later in the flow.

-   **[Use conversational subflows and actions by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/conversational-subflows.md)**

    Use conversational subflows and actions when you install any Now Assist product. This skill is active by default.

-   **[Use your preferred LLM to generate descriptions for subflow or action skill, input, and output](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-llm-for-conversational-subflow.md)**

    Leverage generative AI to generate descriptions for the subflow or action skill, inputs, and outputs. You can configure a default LLM to generate the descriptions.

-   **[View flow history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/flow-history.md)**

    View and manage the history of a flow. See past configurations of a flow to copy, restore, or remove them.

-   **[View subflow history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/subflow-history.md)**

    View and manage the history of a subflow. See past configurations of a subflow to copy, restore, or remove them.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Display flow recommendations in flow diagramming view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/exploring-flow-recommendations.md)**

    Get a list of recommendations for the next item in your flow while in a flow diagramming view.

-   **[Launch the flow debugger from an updated button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/flow-debugger.md)**

    Start the flow debugger from an updated button.

-   **[Open conversational subflow settings from an updated button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-subflow-conversation-settings.md)**

    The option to open subflow conversational settings has moved from the more action menu to the sidebar.

-   **[Open conversational action settings from an updated button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-action-conversation-settings.md)**

    The option to open action conversational settings has moved from the more action menu to the sidebar.

-   **[See event sources from a new menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/manage-external-event-sources.md)**

    Create, read, update, or delete external event sources with the Event sources menu. An Event sources menu has been added to a panel of the spokes page that appears after you select a spoke under the **Integrations** tab.

-   **[Open conversational action settings from an updated button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/configure-action-conversation-settings.md)**

    The option to open action conversational settings has moved from the more action menu to the sidebar.

-   **[Event sources menu added to spokes page under the __Integrations__ tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/manage-external-event-sources.md)**

    Create, read, update, or delete external event sources with the Event sources menu. An Event sources menu has been added to the left panel of the spokes page that appears after you select a spoke under the **Integrations** tab.


## Activation information

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Accessibility information

-   **Reflow improvements of canvas headers and footers**

    The following components were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

    -   Workflow Studio canvas header
    -   Workflow Studio canvas footer
    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See  for details.


## Related ServiceNow applications and features

-   **[Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer.md)**

    Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.

-   **[Data Stream actions and pagination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/data-stream-actions.md)**

    Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.

-   **[Exploring Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/decision-designer-overview.md)**

    Decision tables in Workflow Studio enable developers to decouple decision logic from their code by creating and maintaining decision rules.

-   **[Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integrationhub.md)**

    Automate integration tasks using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/workflow-studio-rn-landing.md)

