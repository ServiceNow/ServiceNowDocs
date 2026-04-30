---
title: Change a component's application scope
description: Change a component's application scope if you encounter scope issues when deploying your component to an instance. For example, you may have set an application scope that is already in use or invalid while creating a component in offline mode.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Change a component's application scope

Change a component's application scope if you encounter scope issues when deploying your component to an instance. For example, you may have set an application scope that is already in use or invalid while creating a component in offline mode.

## Before you begin

-   [Set up your environment](set-up-environment.md)
-   [Set up your project](setup-component-project.md)
-   Role required: none

## About this task

## Procedure

1.  In your project directory, open `now-ui.json`.

2.  Update the `scopeName` key with the desired scope name.

    Use the namespace identifier guidelines for application development on the instance. For more information, see [Application scope](../../applications/concept/c_ApplicationScope.md).

    When reserving an application scope, follow these requirements:

    -   Maximum: 18 characters.

    -   Case: snake case.

    ```
    "scopeName": "x_customerprefix_componentname"
    ```

3.  Deploy your component.

    See [Deploy a component to an instance](deploy-to-instance.md).


**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

