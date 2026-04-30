---
title: Add an application experience
description: Use App Engine Studio \(AES\) to add an experience to your app. Experiences are the interface, or wrapper, for how users interact with your app.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add an application experience

Use App Engine Studio \(AES\) to add an experience to your app. Experiences are the interface, or wrapper, for how users interact with your app.

Application templates automatically add experiences to your application.

<table id="table_ky2_f4k_3tb"><thead><tr><th>

Experience

</th><th>

Definition

</th><th>

Example

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

Standard catalog item

</td><td>

A standard catalog item displays a form that users can fill in to create requests, such as a form to request an item or service. Standard catalog items make use of the Request table and produce a request record. In addition, generated request items are linked with a workflow, a catalog task, and any related approvals. Using standard catalog items, users can add multiple items to a cart and generate a request for each requested item. Use a catalog item when you want the service catalog form to generate a request, complete with a workflow, approvals, tasks, etc.

</td><td>

Create a catalog item form, such as a form to request time-off. After submitting the form, a request is created for a manager to approve or reject.

</td><td>

-   [Add a standard catalog item](../task/add-standard-catalog-item.md)
-   [Sample standard catalog item](standard-catalog-item-examples.md)

</td></tr><tr><td>

Record producer

</td><td>

A record producer is a simplified type of catalog item that displays a form for users to fill out. The completed and submitted form inserts a new data record in a selected custom target table that you set up. This type of catalog item enables users to create task-based records, such as an incident record \(without any of the more complex functionality that comes with using a standard catalog item, such as creating requests\). Use a record producer when you want the service catalog form to create a simplified type of record that isn't a request \(for example, a task record such as an incident, change, or enhancement, etc.\).

</td><td>

Create a service catalog form that generates a task record, such as an incident, instead of a request.

</td><td>

-   [Add a record producer](../task/add-a-record-producer.md)
-   [Sample record producer](record-producers-example.md)

</td></tr><tr><td>

Workspace

</td><td>

A workspace is a suite of tools that provides agents, case managers, help desk professionals, and managers with tools to help answer customer questions and resolve customer problems.

</td><td>

Create an equipment fulfillment dashboard where employees can request laptops and other items. Workspaces are similar to portals but smaller in scope.

</td><td>

-   [Add a workspace](../task/add-workspace.md)
-   [Using Workspace Builder](../../workspace-builder/concept/using-workspace-builder.md)
-   [Edit a workspace in Workspace Builder](../task/configure-workspace-builder.md)
-   [Configure workspace settings in Workspace Builder](../task/configure-workspace-settings.md)
-   [Customize a workspace home page in Workspace Builder](../task/edit-workspace-home-page.md)
-   [Add a record page for a workspace in Workspace Builder](../task/configure-record-page-workspace.md)
-   [Create lists for a workspace in Workspace Builder](../task/add-workspace-list.md)
-   [Enable analytics for a workspace in Workspace Builder](../task/configure-analytics-workspace.md)
-   [Sample workspaces you can build](../reference/types-of-workspaces.md)

</td></tr><tr><td>

Portal

</td><td>

A portal is a site where users inside of your organization can find information, submit requests, and complete business tasks.

</td><td>

Create a self-service portal, or entry point for employees to make requests and browse a knowledgebase, which you can then populate with additional workspaces and catalogs.

</td><td>

-   [Add a portal](../task/add-portal.md)
-   [Sample portals you can build](portal-example.md)

</td></tr><tr><td>

Mobile

</td><td>

A mobile experience enables users to access your application from a ServiceNow native mobile app. You must then populate the app with data.

</td><td>

Create a time-off request application for mobile for managers to approve or reject requests in the Now Mobile app on their mobile device.

</td><td>

-   [Add a mobile experience](../task/add-mobile.md)
-   [Sample mobile experience](mobile-experiences-examples.md)

</td></tr></tbody>
</table>-   **[Choosing between record producers and catalog items](record-producer-vs-catalog-item.md)**  
Both the record producer and standard catalog item in App Engine Studio \(AES\) create experiences where users can submit requests through a service portal. However, record producers are more extensible, and enable users to create a record in any table.
-   **[Add a record producer](../task/add-a-record-producer.md)**  
A record producer enables users to create task-based records, such as an incident record, in apps you create in App Engine Studio \(AES\) without creating a request. It enables a better end-user experience by standardizing requests using a simplified form.
-   **[Add a standard catalog item](../task/add-standard-catalog-item.md)**  
Add a standard catalog item to your application in App Engine Studio \(AES\) so users can submit requests for services and offerings.
-   **[Add a workspace](../task/add-workspace.md)**  
Create a workspace using Workspace Builder in App Engine Studio \(AES\). Workspaces provide agents, case managers, help desk professionals, and managers with tools to help answer customer questions and resolve customer problems.
-   **[Add a portal](../task/add-portal.md)**  
Create a portal in App Engine Studio \(AES\) to give your users a site where they can find information, create requests, and complete business tasks.
-   **[Add a mobile experience](../task/add-mobile.md)**  
Add a mobile experience, or interface, to enable users to access your application from a ServiceNow native mobile app.
-   **[Editing an experience in App Engine Studio](edit-experience.md)**  
 Tailor your app's experience to suit your business needs by building interfaces in App Engine Studio \(AES\), such as for mobile apps or catalog items.

**Parent Topic:**[Enhance your app](customize-application.md)

