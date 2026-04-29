---
title: Add logic and automation
description: Replace manual work by adding logic and automation to your app in App Engine Studio \(AES\).
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add logic and automation

Replace manual work by adding logic and automation to your app in App Engine Studio \(AES\).

Application templates automatically add logic and automation to your application.

<table id="table_rf3_3cj_3tb"><thead><tr><th>

Automation

</th><th>

Definition

</th><th>

Example

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

Decision

</td><td>

Decisions decouple logic from code by creating decision rules, such as inputs that evaluate data from existing records, external data sources, or data provided at runtime.

</td><td>

Automatically apply cascading discounts to different products based on the increasing number of units ordered.

</td><td>

-   [Add a decision](../task/add-decision.md)
-   [Modify decision table structure in Workflow Studio](https://www.servicenow.com/docs/access?context=format-decision-table-in-decision-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

</td></tr><tr><td>

Email notification

</td><td>

Notifications are emails that are automatically sent when the specified conditions are met.

</td><td>

Automatically send an email when a new support record is created.

</td><td>

-   [Add an email notification](../task/add-notification.md)
-   [Modify an email notification](../task/edit-notification.md)

</td></tr><tr><td>

Flow

</td><td>

A flow is a sequence of reusable actions, initiated by a trigger event, and passing variables between actions.

</td><td>

Automatically generate a Twitter post when an incident is closed or send an email when a record in a specific table is updated or created \(record-based flow\).

</td><td>

-   [Add a flow from scratch](../task/create-scratch-flow.md)
-   [Modify a flow](../task/edit-flow.md)
-   [Work with record-based flows in Table Builder](../../../administer/form-builder/concept/flows-tb.md#)

**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.


</td></tr><tr><td>

Process

</td><td>

Processes are cross-enterprise workflows that enable you to create a single, unified process. Processes can include multiple flows.

</td><td>

Standardize and automate how agents handle chat interactions with VIP users.

</td><td>

-   [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Edit a process](../task/edit-process.md)

</td></tr></tbody>
</table>**Note:** If you’re using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app that’s linked to Git, the new flow won’t be available in the app for other AES users until the admin checks the flow into Git.

-   **[Add a pre-built flow using a template](../task/use-flow-template.md)**  
Use a pre-built flow to quickly automate manual work in the app you're building in App Engine Studio \(AES\).
-   **[Add a flow from scratch](../task/create-scratch-flow.md)**  
If an existing automation template doesn't fit your application goal, define custom automation in App Engine Studio \(AES\) by building a new flow.
-   **[Add a decision](../task/add-decision.md)**  
Create automation for decisions in App Engine Studio \(AES\). The automation decouples decision logic from code by enabling you to create and manage decision rules.
-   **[Add an email notification](../task/add-notification.md)**  
Build notifications in App Engine Studio \(AES\) to create automated emails for events using templates or custom messages.
-   **[Edit a process](../task/edit-process.md)**  
To update or change an existing process for an app built in App Engine Studio \(AES\), edit it in Playbooks.

**Parent Topic:**[Enhance your app](customize-application.md)

