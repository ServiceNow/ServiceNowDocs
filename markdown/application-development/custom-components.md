---
title: Create custom components using ServiceNow CLI
description: Develop custom components using the Next Experience UI Framework and the ui-component extension.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Builder library, Developing your application, Building applications]
---

# Create custom components using ServiceNow CLI

Develop custom components using the Next Experience UI Framework and the ui-component extension.

Components are reusable building blocks that you use to create a custom user interface. The Next Experience Design System comes with a set of customizable components that you can drag into your custom UI. Develop your own components if you can't find what you need in the Next Experience Design System library.

To see the Next Experience Design System library, visit the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3F%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).

## Benefits of creating custom components

Developing custom components lets you:

-   Personalize a UI according to your agent, customer, and company needs.
-   Make your employees more effective and reduce context switching with quick access to important data and information.
-   Accommodate your company's unique omni-channel environment using APIs to consolidate your data.

For example, you might want to create a component that displays the cases associated with an SLA, or that tracks the active chats in a particular queue. You can use the Next Experience UI Framework and the ui-component extension to develop the component you need, and access data from your platform using the [Http Effect API](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/ui-framework/api-reference/effect-http). You can also query platform data using GraphQL by creating a custom schema. For more information, see [Scripted GraphQL](https://www.servicenow.com/docs/access?context=scripted-graph-ql&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## What to know before you begin

Before you start designing and building your component, make sure you have:

-   Some general knowledge of web component concepts, development, and design.
-   JavaScript knowledge to define the component behavior.
-   Knowledge of Node Package Manager \(npm\).
-   The most recent version of Node.js installed on your local machine. For more information, see, [Node.js](https://nodejs.org).
-   The ServiceNow CLI installed on your machine.

## Next Experience UI Framework

The Next Experience UI Framework is a JavaScript framework that lets you extend your apps and build web components that are reusable throughout your applications. Using the Next Experience UI Framework lets you:

-   Create a single component to use in multiple places across your applications.
-   Encapsulate the component's scope to prevent conflicts with other code.
-   Add properties, slots, and actions to your component, allowing users to customize the component every time they use it in a Workspace.

For more information, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/ui-framework/getting-started/introduction).

## ui-component extension and development flow

The ui-component extension is an extension to the ServiceNow CLI that lets you develop custom components using the Next Experience UI Framework. With the ui-component extension, you can:

-   Create the set of files required to develop a component, or project scaffolding.
-   Start a local development server to test your component.
-   Build a component project and deploy it to a ServiceNow instance.

For more information, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/getting-started).

## Application scope

When you deploy a Next Experience UI Framework component, it deploys into a scoped application on the instance. You can provide an application scope for the component to use as a namespace identifier. Use the namespace identifier guidelines for application development on the instance. For more information, see [Application scope](../../applications/concept/c_ApplicationScope.md).

When reserving an application scope, follow these requirements:

-   Maximum: 18 characters.

-   Case: snake case.

-   Format: `x_customerprefix_componentname`, where:
    -   `customerprefix` is the value in the **glide.appcreator.company.code** system property on your instance.
    -   `componentname` is the value provided in the component's `name` parameter when you created the project.

If you do not provide an application scope when creating your component project, the Now CLI creates one for you.

Alternatively, you can add a value to the `scopeName` parameter in the `now-ui.json` file.

## Reference guide

To see the Now CLI reference guide, visit the [Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/getting-started).

-   **[Develop a component for Virtual Agent](va-components.md)**  
Create a custom Virtual Agent component to gather input or display information in the Virtual Agent client interface.
-   **[Add a component to Agent Workspace](workspace-component.md#)**  
Use custom components to create a custom Workspace interface to fulfill the specific need of your company's agents.

**Parent Topic:**[Builder library](../../custom-application/concept/builder-library-table.md)

