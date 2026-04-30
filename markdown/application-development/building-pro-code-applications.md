---
title: Building pro-code applications
description: Create and manage custom applications from scratch using classic pro-code tools.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Developing your application, Building applications]
---

# Building pro-code applications

Create and manage custom applications from scratch using classic pro-code tools.

-   **[ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md)**

    Use ServiceNow Studio to build apps and app files with integrated tools, access and edit metadata in scoped and global apps, and package app changes for deployment, all in one powerful development tool.

-   **[ServiceNow IDE](../../servicenow-ide/concept/servicenow-ide-landing.md)**

    ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. With the ServiceNow IDE, you can create and develop scoped applications in source code, create JavaScript modules, and use third-party libraries.

-   **[ServiceNow SDK](../../servicenow-sdk/concept/servicenow-sdk-landing.md)**

    ServiceNow SDK enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. You can also use the ServiceNow SDK to create JavaScript modules and use third-party libraries.

-   **[ServiceNow Extensions for Visual Studio Code](../../applications/concept/vs-code.md)**

    The ServiceNow extensions for VS Code editor enables you to edit applications offline and within ServiceNow instances.


## Which app builder should I use?

Use the following table to choose the app building experience that matches your role and technical background.

<table id="app-builders-table"><thead><tr><th>

Tool

</th><th>

Users

</th><th>

Features

</th></tr></thead><tbody><tr><td>

Creator Studio: Build an app without code.

</td><td>

Process owners, line of business owners

</td><td>

Build request-fulfillment apps without writing code. For example, create an application to request office supplies: a user fills out a form, and an approver accepts or denies the request. For more information, see [Exploring Creator Studio](../../creator-studio/concept/exploring-creator-studio.md).

</td></tr><tr><td>

App Engine Studio: Build a range of apps using low-code tools.

</td><td>

Citizen developers

</td><td>

Build a broader range of apps than Creator Studio without writing code.For more information, see [Exploring App Engine Studio](../../app-engine-studio/concept/exploring-aes.md).

</td></tr><tr><td>

ServiceNow Studio: Build and deliver apps in a unified environment.

</td><td>

Citizen developers, Platform developers

</td><td>

Build apps in a unified development environment.ServiceNow Studio provides streamlined navigation, integrated low-code tools, and built-in tracking and packaging so you can develop and ship apps faster.

For more information, see [Exploring ServiceNow Studio](../../servicenow-studio/concept/exploring-servicenow-studio.md).

</td></tr><tr><td>

ServiceNow IDE and ServiceNow SDK: Build apps in source code.

</td><td>

Source code developers

</td><td>

Develop applications in source code with ServiceNow Fluent, create JavaScript modules, and use third-party libraries. ServiceNow Fluent is a domain-specific programming language for creating application metadata in code. Use Build Agent in ServiceNow IDE to create and update apps in source code with a conversational interaction.The ServiceNow IDE runs Visual Studio Code for the Web on the ServiceNow AI Platform. The ServiceNow SDK runs Visual Studio Code Desktop locally. For more information, see [Building applications in source code](../concept/building-applications-source-code.md).

</td></tr></tbody>
</table>## Scripting

-   **[Action Designer](https://www.servicenow.com/docs/access?context=actions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Use Workflow Studio to automate a repeatable task within a flow as a sequence of related steps. Enable flow authors to add actions to multiple flows with minimal configuration.

-   **[Client-side scripting](https://www.servicenow.com/docs/access?context=client-side-scripting-overview&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Client scripts enable the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

-   **[Now Assist for Code](https://www.servicenow.com/docs/access?context=now-assist-code-landing&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Now Assist for code generation allows developers to write scripts quickly with AI-generated code suggestions based on text or code prompts.

-   **[Now Code Editor](../../../administer/now-code-editor/concept/now-code-editor.md)**

    Now Code Editor provides a rich-text editor interface that supports Cascading Style Sheets \(CSS\), Hypertext Markup Language \(HTML\), JavaScript, Extensible Markup Language \(XML\), and JavaScript Object Notation \(JSON\). Use Now Code Editor to modify UI configuration, data resource configuration, styles, events, client-side and server-side scripts in Next Experience UI Builder components.

-   **[Server-side scripting](https://www.servicenow.com/docs/access?context=c_ServerScripting&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Server scripts run on the server or database. They can change the appearance or behavior of the ServiceNow AI Platform or run as business rules when records and tables are accessed or modified.


## Core functionality

-   **[Groups](https://www.servicenow.com/docs/access?context=ua-creating-groups&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Simplify user administration by assigning roles to groups. Any business rules, assignment rules, system roles, or attributes that refer to the group apply to all group members automatically.

-   **[Notifications](https://www.servicenow.com/docs/access?context=notifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Use ServiceNow Notifications to manage system email, create system notifications, and configure how your system responds to inbound email.

-   **[Roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Roles control access to features and capabilities in applications and modules. The admin role provides access to all features and capabilities.

-   **[ServiceNow plugins](https://www.servicenow.com/docs/access?context=c_ServiceNowPlugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Plugins are software components that provide specific features and functionalities within a ServiceNow instance.

-   **[UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    UI policies dynamically change the behavior of information on a form and control custom process flows for tasks.

-   **[Users](https://www.servicenow.com/docs/access?context=user&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    User records establish a relationship between an individual and your ServiceNow instance. User records consist of a user name, a password, and information relating to the individual, such as contact information, location, and job title.


## Related applications and features

-   **[JavaScript APIs](https://www.servicenow.com/docs/access?context=api-reference&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Use JavaScript APIs in scripts that you write to change the functionality of applications, or when you create new applications.

-   **[UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md)**

    Use UI Builder to build web user interfaces for CSM Configurable Workspace, App Engine Studio generated workspaces and portals, or custom web experiences using Next Experience Components and custom web components.


