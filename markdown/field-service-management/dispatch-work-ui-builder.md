---
title: Customize Dispatcher Workspace
description: Use UI Builder to build pages for CSM Configurable Workspace or custom web experiences using Next Experience and custom web components.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Customize Dispatcher Workspace

Use UI Builder to build pages for CSM Configurable Workspace or custom web experiences using Next Experience and custom web components.

## UI Builder

UI Builder is a low-code environment. You should be comfortable interacting with code in a visual interface before you start editing any components. Read and become familiar with the UI builder documentation at [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US) before you attempt to use the tool.

**Warning:** Only developers with a high level of experience, sometimes referred to as pro-coders, should perform the procedures that use UI Builder.

## Customizing pages in UI Builder

Next Experience components are the base elements of UI Builder pages like Dispatcher Workspace. Components range from core elements like buttons and labels to more complex components like lists and forms. You can change components to update the Dispatcher Workspace user interface or add new ones. You can also create your own components if the ones that come with UI Builder don't fit your needs.

**Important:** You must use a Script Include when making any customizations to Dispatcher Workspace. For more information, see [Extend a Script Include](https://developer.servicenow.com/dev.do#!/learn/courses/vancouver/app_store_learnv2_scripting_vancouver_scripting_in_servicenow/app_store_learnv2_scripting_vancouver_server_side_scripting/app_store_learnv2_scripting_zurich_extend_a_script_include).

For information on components and how to work with them in UI Builder, see [Customize UI Builder pages using components](https://www.servicenow.com/docs/access?context=work-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US). The components that are available to use are listed on the developer site at [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components).

You can configure nearly any area of Dispatcher Workspace in UI Builder. Three of the most common areas to update are the contextual side panel, the agent card, and the calendar. For more information see the following topics:

-   [Customizing the contextual side panel in Dispatcher Workspace with UI Builder](side-panel-ui-builder.md)
-   [Customizing the agent card in Dispatcher Workspace with UI Builder](agent-card-ui-builder.md)
-   [Customizing the calendar grid in Dispatcher Workspace with UI Builder](calendar-color-ui-builder.md)

