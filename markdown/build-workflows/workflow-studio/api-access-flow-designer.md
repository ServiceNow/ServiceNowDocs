---
title: API access to Workflow Studio flows
description: Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions. Flow authors can enable individual flows, subflows, and actions to be client callable during design.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# API access to Workflow Studio flows

Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions. Flow authors can enable individual flows, subflows, and actions to be client callable during design.

## Available Workflow Studio flow APIs

Trigger flows, subflows, and actions using these APIs from server or client scripts.

-   **Server side**

    [FlowAPI](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US): Trigger a flow, subflow, or action using synchronous or asynchronous methods, with or without execution details.

-   **Client side**

    [GlideFlow](https://www.servicenow.com/docs/access?context=GlideFlowAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US): Perform client-side interactions with actions, flows, and subflows. Flow designers must enable a flow, subflow, and action to be called from the client.


## FlowAPI quick methods

Use quick methods in the [FlowAPI](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) class to run an action, flow, or subflow from a server-side script without creating execution details or other related records. Use these methods to increase the speed of high-volume processing in a production environment, and to improve performance by eliminating record-keeping overhead. Methods include:

-   executeActionQuick\(\), executeFlowQuick\(\), executeSubflowQuick\(\): Run an action, flow, or subflow from a server-side script synchronously from the current user session.
-   startActionQuick\(\), startFlowQuick\(\), startSubflowQuick\(\): Run an action, flow, or subflow from a server-side script asynchronously.

## XML and JSON streaming APIs

Builds a large streaming or non-streaming JSON or XML payload to use in a REST or SOAP request to send bulk data to a third-party API. For example, you can use these APIs to create a JSON payload in the Workflow Studio Script step and pass the returned value to the REST step to send the request to a third-party service. For more information, see [JSONStreamingBuilder](https://www.servicenow.com/docs/access?context=JSONStreamingBuilderScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) and [XMLStreamingBuilder](https://www.servicenow.com/docs/access?context=XMLStreamingBuilderScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Client callable APIs

By default, the flows, subflows, and actions can only be called by the FlowAPI within a server script. Flow and action designers can make individual flows, subflows, or actions available to client calls by enabling the **Client callable** option during the design process.

## Run as support

Flows and subflows can run as either the system user or the user who initiates the session. Set this behavior from the [flow properties](../task/create-flow.md). All API quick methods ignore the run as property, and always run as the system user.

Actions always run as the user who initiates the session.

## Code snippets

Application developers can generate a JavaScript function that calls a specific flow, subflow, or action with the **Code Snippet** option. Use the code snippet in scripts such as business rules or the **Scripts - Backgound** module to call specific Workflow Studio elements. The system only generates code snippets for published flows, subflows, and actions. Workflow Studio elements in the draft or modified status do not generate code snippets.

-   **[Create code snippets for flows, subflows, and actions](../task/flow-design-code-snippet.md)**  
Generate a code snippet to call a specific flow, subflow or action.
-   **[Create a client callable flow, subflow, or action](../task/grant-access-flow-apis.md)**  
Enable a client script to trigger a flow, subflow, or action.

**Parent Topic:**[Configuring flows](configuring-flow-designer.md)

