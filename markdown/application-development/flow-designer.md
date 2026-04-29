---
title: Flow Designer
description: Flow Designer is a ServiceNow AI Platform feature that enables rich process automation capabilities in a consolidated design environment. Flow Designer enables process owners to use natural language to automate approvals, tasks, notifications, and record operations without having to code.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build form and business logic, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Flow Designer

Flow Designer is a ServiceNow AI Platform feature that enables rich process automation capabilities in a consolidated design environment. Flow Designer enables process owners to use natural language to automate approvals, tasks, notifications, and record operations without having to code.

## Flow Designer and IntegrationHub

For any new process flow requirements, ServiceNow recommends using Flow Designer over the legacy workflow for almost all circumstances.

## Flow Designer and Business Rules

You should use Flow Designer instead of Business Rules unless:

-   Business logic needs to run in a specific sequence with other Business Rules. For example, new business logic needs to run after one Business Rule but before another.
-   Logic needs to execute immediately before or after writing to the database in the same thread.
-   The logic only calls a Script Include.

When designing a flow, follow these design principles:

-   Single Purpose: Each flow should have a singular goal.
-   Reusability: Design with reusable sub-flows in mind \(approval is a great example\).
-   Clarity: The language and layout of a flow should make each action’s purpose clear.

Start with a white board design of a business flow. Then build the flow action by action to align with the process. More than one flow may be required for a for a single process to keep to the design principles.

Use the following practices when working with Flow Designer:

-   Use records, not SysIDs. Provide a guided experience with inline documentation.
-   Learn how to use template objects to work with both static and dynamic inputs.
-   Avoid passing around blobs of data unless absolutely necessary.
-   Only pass information to a flow that the flow is going to use.

Use the following practices when working with Flow Designer Actions:

-   Always create actions under the scope of the application’s spoke, if applicable.
-   Set access to Accessible from all scopes in actions to be able to reuse actions across other apps and scopes in the future.
-   Set **Protection** to Read-only to avoid any unwanted edits to the actions by users.
-   Make sure inputs have a specific type.
-   Ensure that **Mandatory** is selected where required.
-   If using a **choice** input type, use a default value.

Use the following practices when working with IntegrationHub:

-   Create one spoke per integration system. Only put actions for a single system in a spoke.
-   When creating the scoped app for the spoke, use a version naming convention that makes sense.
-   Use a connection alias instead of an inline connection. The Base URL will be automatically extracted.
-   Use connection attributes under the Alias to pass the version in a REST step giving future flexibility for versioning in the resource path.
-   Use Save as Attachment to save the content in the response instead of creating another step to save the data.
-   If the Alias is dynamic, make Alias one of the inputs and use the data pill to provide the Alias.

Use the following practices in Flow Designer and IntegrationHub for Error Handling:

-   Create a Script Include to handle errors.
-   Write short and understandable error messages.
-   Incorporate all of the possible error messages the API returns.
-   Ensure that the outputs from the integration step are validated before using them.
-   Fail Early: If the inputs are not available, do not call the integration.

Self-Paced Training: [Flow Designer](https://developer.servicenow.com/dev.do#!/learn/courses/paris/app_store_learnv2_flowdesigner_paris_flow_designer)

Self-Paced Training: [IntegrationHub](https://developer.servicenow.com/dev.do#!/learn/courses/paris/app_store_learnv2_rest_paris_rest_integrations/app_store_learnv2_rest_paris_rest_in_integrationhub/app_store_learnv2_rest_paris_rest_in_integrationhub_objectives)

**Parent Topic:**[Build form and business logic](build-form-and-business-logic.md)

