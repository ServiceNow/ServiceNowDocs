---
title: Add a component to Agent Workspace
description: Use custom components to create a custom Workspace interface to fulfill the specific need of your company's agents.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Add a component to Agent Workspace

Use custom components to create a custom Workspace interface to fulfill the specific need of your company's agents.

Communicating with customers through multiple channels can be time consuming. To be efficient in these omni-channel interactions, your agents need a single view of customer information to reduce context switching between multiple tools. By developing custom components for Workspace, your team can bring communications from multiple channels into one interface.

## Adding components to a Workspace

Once deployed to your instance, you can add components to Workspace in these ways.

-   **Add a component to a Workspace modal**

    Use a UI action to launch a custom component in a modal so an agent doesn't have to navigate to a different screen to accomplish a task.

-   **Add a component to a Workspace landing page using UI Builder**

    Use the UI Builder to create custom landing pages for your agents. UI Builder is a drag-and-drop tool that lets you visually arrange workspace components.

    Configure properties in the `now-ui.json` file to use deployed components in the UI Builder. For instructions, see the [ServiceNow Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/ui-builder).

-   **Add a component to a Workspace record view**

    You can add custom or standard components to the component area in the Workspace record view.


**Parent Topic:**[Create custom components using ServiceNow CLI](custom-components.md)

