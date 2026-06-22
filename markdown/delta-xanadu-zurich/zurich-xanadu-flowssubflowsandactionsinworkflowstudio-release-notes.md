---
title: Combined Flows, subflows, and actions in Workflow Studio release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Flows, subflows, and actions in Workflow Studio from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-flowssubflowsandactionsinworkflowstudio-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Flows, subflows, and actions in Workflow Studio release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Flows, subflows, and actions in Workflow Studio from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Flows, subflows, and actions in Workflow Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Flows, subflows, and actions in Workflow Studio to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

After upgrading, users who previously had the fd\_read\_operations role will now see only basic execution details such as the run state and duration. This restriction prevents users with this role from seeing sensitive information in execution details. To provide read access to all execution details such as input configuration and runtime values, grant the user the new role fd\_read\_operations\_all.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://servicenow-staging.fluidtopics.net/access?context=restore-save-as-you-go-functionality&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Flows, subflows, and actions in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Generate data pill values during flow generation](https://servicenow-staging.fluidtopics.net/access?context=flow-generation&family=xanadu&ft:locale=en-US)**

Generate appropriate data pill values for supported flow triggers and action inputs.

-   **[Run an action from a conversation](https://servicenow-staging.fluidtopics.net/access?context=conversational-actions&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://servicenow-staging.fluidtopics.net/access?context=conversational-subflows&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[Reference specific tables with hash tags during flow generation](https://servicenow-staging.fluidtopics.net/access?context=flow-generation&family=xanadu&ft:locale=en-US)**

Enter a hash tag character in the flow directions to refer to a specific table by name. Use auto-complete to select a table name from the options that match your partial entry.


-   **[Show annotations of the text directions used by flow generation](https://servicenow-staging.fluidtopics.net/access?context=create-flow-now-assist&family=xanadu&ft:locale=en-US)**

Show annotations of the text directions used for each item added by flow generation. Receive feedback about how your directions map to specific actions, flow logic, and subflows.


-   **[Control what users with read access can see in execution details](https://servicenow-staging.fluidtopics.net/access?context=user-access-flow-designer&family=xanadu&ft:locale=en-US)**

Grant a user role to control what users with read access can see in execution details. To limit read access to basic execution details only, grant a user the existing fd\_read\_operations role. To allow read access to all execution details, grant a user the new fd\_read\_operations\_all role.

-   **[Sign flows, subflows, and actions](https://servicenow-staging.fluidtopics.net/access?context=cs-fdih&family=xanadu&ft:locale=en-US)**

Sign and validate any flow, subflow, or action.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Add and edit flows in Now Assist for app generation](https://servicenow-staging.fluidtopics.net/access?context=sns-app-gen-add-flow&family=yokohama&ft:locale=en-US)**

Create a flow when creating an application in Now Assist for app generation. Enhance an existing application by adding a flow.

-   **[Call a Now Assist skill from an action](https://servicenow-staging.fluidtopics.net/access?context=call-now-assist-skill-step&family=yokohama&ft:locale=en-US)**

Run a published Now Assist skill from an action. Configure the Now Assist skill inputs and skill outputs from the step inputs and step outputs.

-   **[Check for conversational compatible actions](https://servicenow-staging.fluidtopics.net/access?context=check-for-conversational-compatible-actions&family=yokohama&ft:locale=en-US)**

Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.

-   **[Check for conversational compatible subflows](https://servicenow-staging.fluidtopics.net/access?context=check-for-conversational-compatible-subflows&family=yokohama&ft:locale=en-US)**

Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.

-   **[Create a flow or subflow from an image](https://servicenow-staging.fluidtopics.net/access?context=flow-generation-with-images&family=yokohama&ft:locale=en-US)**

Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

-   **[Display text descriptions of the data used by actions and flow logic](https://servicenow-staging.fluidtopics.net/access?context=exploring-flows&family=yokohama&ft:locale=en-US)**

See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.

-   **[Generate skill and input descriptions for conversational actions](https://servicenow-staging.fluidtopics.net/access?context=configure-action-conversation-settings&family=yokohama&ft:locale=en-US)**

Configure conversational settings for conversational actions by generating skill and input descriptions with generative AI.

-   **[Generate skill and input descriptions for conversational subflows](https://servicenow-staging.fluidtopics.net/access?context=configure-subflow-conversation-settings&family=yokohama&ft:locale=en-US)**

Configure conversational settings for conversational subflows by generating skill and input descriptions with generative AI.

-   **[Set default values for action inputs](https://servicenow-staging.fluidtopics.net/access?context=configure-action-conversation-settings&family=yokohama&ft:locale=en-US)**

Set a default value for a conversational action input. Hide action inputs that have a default value if you don't want users to change the input value in a conversation.

-   **[Set default values for subflow inputs](https://servicenow-staging.fluidtopics.net/access?context=configure-subflow-conversation-settings&family=yokohama&ft:locale=en-US)**

Set a default value for a conversational subflow input. Hide subflow inputs that have a default value if you don't want users to change the input value in a conversation.

-   **[Summarize a flow or subflow](https://servicenow-staging.fluidtopics.net/access?context=flow-summarization&family=yokohama&ft:locale=en-US)**

Summarize what a flow or subflow does by using generative AI.

-   **[Support additional input data types for conversational actions](https://servicenow-staging.fluidtopics.net/access?context=conversational-actions&family=yokohama&ft:locale=en-US)**

Support conversational actions that have Dynamic Choice and Array of Objects input types.

-   **[Support additional input data types for conversational subflows](https://servicenow-staging.fluidtopics.net/access?context=conversational-subflows&family=yokohama&ft:locale=en-US)**

Support conversational subflows that have Dynamic Choice and Array of Objects input types.

-   **[Create the recommended automation type](https://servicenow-staging.fluidtopics.net/access?context=design-considerations-consolidated&family=yokohama&ft:locale=en-US)**

Answer a few questions about your automation and Workflow Studio displays recommendations on whether you should create a playbook, flow, subflow, action, or a data stream.


-   **[Configure conversational settings](https://servicenow-staging.fluidtopics.net/access?context=configure-subflow-conversation-settings&family=yokohama&ft:locale=en-US)**

View the subflows and actions that are conversational compatible. Configure conversational settings to make a subflow or action available to conversational interfaces.


-   **[Debug flows and subflows](https://servicenow-staging.fluidtopics.net/access?context=flow-debugger&family=yokohama&ft:locale=en-US)**

Debug flows and subflows from a dedicated Workflow Studio tab. Set breakpoints and step through a paused flow to review configuration and runtime values.

-   **[Save a flow trigger for reuse in other flows](https://servicenow-staging.fluidtopics.net/access?context=saved-flow-triggers&family=yokohama&ft:locale=en-US)**

Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

-   **[Use the Flow API to send a message to a paused flow](https://servicenow-staging.fluidtopics.net/access?context=FlowAPI-sendMessage_S_S_S&family=yokohama&ft:locale=en-US)**

Send a specific message and payload response to a flow that is paused and waiting for a message.

-   **[Wait for a specific message from the Flow API](https://servicenow-staging.fluidtopics.net/access?context=wait-for-message-action&family=yokohama&ft:locale=en-US)**

Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create and manage external event sources](https://servicenow-staging.fluidtopics.net/access?context=manage-external-event-sources&family=zurich&ft:locale=en-US)**

Create an external event source on your ServiceNow instance that listens to events occurring in an application or system outside of the ServiceNow AI Platform®. Based on the external event source, you can define one or more external trigger definitions in your instance and then associate the external trigger definitions with the external event source. When an event that you specified in the external trigger definition occurs, the external trigger definition executes one or more flows. You can update or remove external event sources that you create.

-   **[Create a domain-separated saved external trigger](https://servicenow-staging.fluidtopics.net/access?context=create-saved-external-trigger&family=zurich&ft:locale=en-US)**

Create a domain-separated saved external trigger. Configurations that you make to the trigger are auto-saved. After the trigger is published, you can edit only the **Label** field values.

-   **[Create a reusable scheduled trigger](https://servicenow-staging.fluidtopics.net/access?context=create-scheduled-trigger&family=zurich&ft:locale=en-US)**

Create a scheduled trigger that starts your flow when you need. Use the trigger across your flows.

-   **[Create a skill for conversational subflows and actions](https://servicenow-staging.fluidtopics.net/access?context=create-conversational-subflow-skill&family=zurich&ft:locale=en-US)**

Create a skill for the conversational subflow and action and make the skill discoverable in conversations. You can have multiple skills for the same subflow or action.

-   **[Enhancements in the subflow and action conversational settings](https://servicenow-staging.fluidtopics.net/access?context=configure-subflow-conversation-settings&family=zurich&ft:locale=en-US)**

To make the error messages more useful in a conversation, you can show specific error messages from the subflow or action rather than showing generic error messages. Additionally, if you override an input with reference, you can apply a filter to limit the number of records in the Reference field.

-   **[Make a flow wait for an email reply](https://servicenow-staging.fluidtopics.net/access?context=wait-for-email-reply-action&family=zurich&ft:locale=en-US)**

Pause a flow until an email reply is received to an outbound email record

-   **[Show subflow stages in a parent flow](https://servicenow-staging.fluidtopics.net/access?context=show-subflow-stages-in-a-parent-flow&family=zurich&ft:locale=en-US)**

Show subflow stages as part of the execution details of a parent flow.

-   **[Save flows, subflows, and actions automatically](https://servicenow-staging.fluidtopics.net/access?context=save-as-you-go-flows&family=zurich&ft:locale=en-US)**

Save flows, subflows, and actions automatically as you work on them.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow generation](https://servicenow-staging.fluidtopics.net/access?context=exploring-flow-generation&family=zurich&ft:locale=en-US)**

Support the Now LLM Long Term Stable models \(LTS\) for Flow generation.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow summarization](https://servicenow-staging.fluidtopics.net/access?context=flow-summarization&family=zurich&ft:locale=en-US)**

Support the Now LLM Long Term Stable models \(LTS\) for Flow summarization.

-   **[Use an AI agent action](https://servicenow-staging.fluidtopics.net/access?context=use-an-ai-agent-action&family=zurich&ft:locale=en-US)**

Use flow data to run an AI agent and configure the expected agent output for use later in the flow.

-   **[Use your preferred LLM to generate descriptions for subflow or action skill, input, and output](https://servicenow-staging.fluidtopics.net/access?context=configure-llm-for-conversational-subflow&family=zurich&ft:locale=en-US)**

Leverage generative AI to generate descriptions for the subflow or action skill, inputs, and outputs. You can configure a default LLM to generate the descriptions.

-   **[View flow history](https://servicenow-staging.fluidtopics.net/access?context=flow-history&family=zurich&ft:locale=en-US)**

View and manage the history of a flow. See past configurations of a flow to copy, restore, or remove them.

-   **[View subflow history](https://servicenow-staging.fluidtopics.net/access?context=subflow-history&family=zurich&ft:locale=en-US)**

View and manage the history of a subflow. See past configurations of a subflow to copy, restore, or remove them.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Flows, subflows, and actions in Workflow Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Flow generation configures action and flow logic inputs](https://servicenow-staging.fluidtopics.net/access?context=create-flow-now-assist&family=xanadu&ft:locale=en-US)**

Use the Now Assist for Creator flow generation skill to create and configure a flow from text directions. Flow generation uses data pills to set input values for actions and flow logic.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Flows, subflows, and actions in Workflow Studio features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Removed the system property com.snc.process\_flow.reporting.iteration.lastn that was used to specify the number of loop iterations that a flow would generate execution details for. To report on all iterations of a loop, create a flow execution settings record for the flow instead. For more information about flow execution settings, see [Flow execution settings](https://servicenow-staging.fluidtopics.net/access?context=flow-execution-settings&family=xanadu&ft:locale=en-US).
-   The user preference for flow authors to include draft actions in the list of available actions has been removed. To see a custom action during flow design, publish the action. For more information, see [Create an action in Workflow Studio](https://servicenow-staging.fluidtopics.net/access?context=create-action&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Flows, subflows, and actions in Workflow Studio features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Flows, subflows, and actions in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

 Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

 Get the latest Workflow Studio features by updating the app from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Flows, subflows, and actions in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Flows, subflows, and actions in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Flows, subflows, and actions in Workflow Studio, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **ARIA label improvements**

Added and updated ARIA labels to support screen readers.

-   **Keyboard navigation improvements**

Improved keyboard navigation with working with actions, flows, and subflows in Workflow Studio.

-   **Reflow improvements of canvas headers and footers**

Added support for the reflow of canvas headers and footer content in Workflow Studio actions, flows, and subflows. These components can be zoomed up to 400% through your browser settings without loss of content or functionality.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.


</td></tr><tr><td>

Zurich

</td><td>

-   **Reflow improvements of canvas headers and footers**
    -   Workflow Studio canvas header
    -   Workflow Studio canvas footer

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Flows, subflows, and actions in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Flows, subflows, and actions in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Protect sensitive data in execution details by using the operations read role.
-   Provide improved support of the variables data type for subflow and action inputs.
-   Show annotations of what text directions were used to generate actions, flow logic, and subflows during flow generation.
-   Sign and validate any flow, subflow, or action.

 See [Workflow Studio](https://servicenow-staging.fluidtopics.net/access?context=workflow-studio&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Create a flow or a subflow from an image by using Now Assist.
-   Debug flows and subflows from a dedicated debugging tab.
-   Pause a flow until it receives a specific message from the flow API.
-   Run a published Now Assist skill from an action.
-   Save flow triggers for reuse in other flows.

 See [Exploring flows](https://servicenow-staging.fluidtopics.net/access?context=exploring-flows&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Create a scheduled trigger that you can use across your flows.
-   Save flows, subflows, and actions automatically as you work on them.
-   View and manage the history of flows and subflows to copy, restore, or remove past configurations.
-   Create multiple skills for conversational subflows and actions from the conversational settings.
-   Configure a default LLM for generating metadata for conversational subflows and actions.

 See [Flows](https://servicenow-staging.fluidtopics.net/access?context=exploring-flows&family=zurich&ft:locale=en-US), [Subflows](https://servicenow-staging.fluidtopics.net/access?context=exploring-subflows&family=zurich&ft:locale=en-US), and [Actions](https://servicenow-staging.fluidtopics.net/access?context=exploring-actions&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

