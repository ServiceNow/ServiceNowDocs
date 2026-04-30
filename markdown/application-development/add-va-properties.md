---
title: Add properties to communicate with Virtual Agent
description: To develop a component for Virtual Agent, add specific properties and actions to interact with the Virtual Agent client interface. The properties required depend on the type of component you are creating.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Develop a component for Virtual Agent, Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Add properties to communicate with Virtual Agent

To develop a component for Virtual Agent, add specific properties and actions to interact with the Virtual Agent client interface. The properties required depend on the type of component you are creating.

## Before you begin

-   [Set up your environment](set-up-environment.md)
-   [Set up your project](setup-component-project.md)
-   [Develop a component](develop-component.md)

## Procedure

1.  In your component code, add the Virtual Agent properties to interact with the Virtual Agent client interface.

<table id="table_k3t_nqd_lmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

controlData

</td><td>

Initial data that the Virtual Agent server sends to your component as the topic runs. Data type: JSON Object

</td></tr><tr><td>

responseValue

</td><td>

Data sent to the component from the user's response, either from the client directly, or from the server if there is a refresh. Only use in components that require user input. Data type: JSON Object

</td></tr><tr><td>

forceCloseControl

</td><td>

Flag that indicates whether the component can accept input. When true, the control closes and the user cannot interact with it. Monitor changes on the client to update this value. Only use in components that require user input.Data type: Boolean

</td></tr></tbody>
</table>2.  If creating an input component, use the `VA_CONTROL#VALUE_SENT` action to send user values to the server.

<table id="table_pdz_frd_lmb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

VA\_CONTROL\#VALUE\_SENT

</td><td>

Response data from the client to send to the server. Only use in components that require user input. Data type: JSON Object

</td></tr></tbody>
</table>
## What to do next

[Test a component for Virtual Agent](test-va-component.md) and [Deploy a component to an instance](deploy-to-instance.md).

**Parent Topic:**[Develop a component for Virtual Agent](../concept/va-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

