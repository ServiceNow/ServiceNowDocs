---
title: Customizing Virtual Agent with custom controls
description: Custom controls are components that ServiceNow developers can create for use in Virtual Agent topics or topic blocks. Such controls include sliders or video players. Custom controls complement the controls provided in Virtual Agent Designer.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Customizing Virtual Agent with custom controls

Custom controls are components that ServiceNow® developers can create for use in Virtual Agent topics or topic blocks. Such controls include sliders or video players. Custom controls complement the controls provided in Virtual Agent Designer.

Virtual Agent Designer provides a default set of controls that represent [user inputs](../reference/va-user-inputs.md), [bot responses](../reference/va-bot-responses.md), and [utilities](../reference/va-utilities.md) for building a Virtual Agent conversation. As a developer, you can use Virtual Agent Designer to create additional controls \(interface components\) for specific inputs or output responses. For example, a slider is an example of a custom input control that enables end users to select a quantity.

**Note:** Custom controls do not work on Internet Explorer version 11. Custom controls are also not supported for Microsoft Teams.

## Before building a custom control

Custom controls are based on customizable Next Experience Components that you can create by using the Next Experience Design System.

Before building a custom component, you must have the following:

-   Basic knowledge of the ServiceNow AI Platform® and application table structures.
-   General knowledge of web component concepts, development, and design.
-   JavaScript knowledge to define component behavior and that of the custom control.
-   Knowledge of the design process for creating custom components for use in Virtual Agent Designer.

To learn more about developing custom components for Virtual Agent, see [Develop a component for Virtual Agent](https://www.servicenow.com/docs/access?context=va-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## How custom controls work

To add your custom control to Virtual Agent, follow these main steps:

1.  [Create a custom control definition](../task/create-custom-control-definition.md).

    After building the custom component to be used for the control, create a custom control definition that maps an input or response control to the custom component.

2.  [Create a custom control using Virtual Agent Designer.](../task/create-custom-control.md)

    A custom control is an input or response control. Developers build a custom control in Virtual Agent Designer by doing the following:

    -   Selecting a custom control definition.
    -   Defining the input parameters for using the control.
    -   Specifying the output parameters returned by the control.
    An input control has callbacks that use input from the end user. A response control typically presents information to the end user and doesn't have callbacks.

3.  [Add a custom control to a topic or topic block](../task/embed-custom-control.md).

    Topic authors, virtual agent admins, or admins can add a custom control utility to a topic or topic block.


## Secure inputs

Beginning with the San Diego release, you can create custom input controls that can accept secure inputs, such as passwords, to pass through to Integration Hub actions or subflows. To enable this, slide the **Make inputs secure** toggle switch when you create your custom input control. For more information, see [Create a Virtual Agent custom control](../task/create-custom-control.md).

