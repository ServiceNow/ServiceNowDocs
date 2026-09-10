---
title: Flows, subflows, and actions in Workflow Studio release notes
description: The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-04-21"
reading_time_minutes: 5
---

# Flows, subflows, and actions in Workflow Studio release notes

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.

## About Flows, subflows, and actions in Workflow Studio

-   Create a flow or a subflow from an image by using Now Assist.
-   Debug flows and subflows from a dedicated debugging tab.
-   Pause a flow until it receives a specific message from the flow API.
-   Run a published Now Assist skill from an action.
-   Save flow triggers for reuse in other flows.

See  for more information.

## Activation and other requirements

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Workflow Studio is a ServiceNow AI Platform feature that is active by default.

    Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Accessibility information**
    -   **ARIA label improvements**

        Added and updated ARIA labels to support screen readers.

    -   **Keyboard navigation improvements**

        Improved keyboard navigation with working with actions, flows, and subflows in Workflow Studio.

    -   **Reflow improvements of canvas headers and footers**

        Added support for the reflow of canvas headers and footer content in Workflow Studio actions, flows, and subflows. These components can be zoomed up to 400% through your browser settings without loss of content or functionality.

        This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/workflow-studio-rn.md)

## May 2025

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.

### What's new

-   **Add and edit flows in Now Assist for app generation**

    Create a flow when creating an application in Now Assist for app generation. Enhance an existing application by adding a flow.

-   **Call a Now Assist skill from an action**

    Run a published Now Assist skill from an action. Configure the Now Assist skill inputs and skill outputs from the step inputs and step outputs.

-   ****

    Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.

-   ****

    Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.

-   **Create a flow or subflow from an image**

    Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

-   **Display text descriptions of the data used by actions and flow logic**

    See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.

-   **Generate skill and input descriptions for conversational actions**

    Configure conversational settings for conversational actions by generating skill and input descriptions with generative AI.

-   **Generate skill and input descriptions for conversational subflows**

    Configure conversational settings for conversational subflows by generating skill and input descriptions with generative AI.

-   **Set default values for action inputs**

    Set a default value for a conversational action input. Hide action inputs that have a default value if you don't want users to change the input value in a conversation.

-   **Set default values for subflow inputs**

    Set a default value for a conversational subflow input. Hide subflow inputs that have a default value if you don't want users to change the input value in a conversation.

-   **Summarize a flow or subflow**

    Summarize what a flow or subflow does by using generative AI.

-   **Support additional input data types for conversational actions**

    Support conversational actions that have Dynamic Choice and Array of Objects input types.

-   **Support additional input data types for conversational subflows**

    Support conversational subflows that have Dynamic Choice and Array of Objects input types.

-   **Create the recommended automation type**

    Answer a few questions about your automation and Workflow Studio displays recommendations on whether you should create a playbook, flow, subflow, action, or a data stream.


### What's changed

-   **Display text descriptions of data changes**

    See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.


## Yokohama General Availability

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.

### What's new


### What's changed


## Yokohama Early Availability

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Yokohama release.

### What's new

-   **Configure conversational settings**

    View the subflows and actions that are conversational compatible. Configure conversational settings to make a subflow or action available to conversational interfaces.


-   **Debug flows and subflows**

    Debug flows and subflows from a dedicated Workflow Studio tab. Set breakpoints and step through a paused flow to review configuration and runtime values.

-   **Save a flow trigger for reuse in other flows**

    Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

-   **Use the Flow API to send a message to a paused flow**

    Send a specific message and payload response to a flow that is paused and waiting for a message.

-   **Wait for a specific message from the Flow API**

    Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.


