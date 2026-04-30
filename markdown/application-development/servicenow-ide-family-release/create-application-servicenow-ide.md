---
title: Create an application with the ServiceNow IDE
description: Create a scoped application to develop in source code with the ServiceNow IDE.
locale: en-US
release: xanadu
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Add applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Create an application with the ServiceNow IDE

Create a scoped application to develop in source code with the ServiceNow IDE.

## Before you begin

Create a workspace for your applications. For more information, see [Create a workspace in the ServiceNow IDE](create-workspace-servicenow-ide.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Fluent: Create Fluent App` and press Enter.

5.  Enter a name for the application and press Enter.

6.  Enter a description for the application and press Enter.

7.  Enter a scope for the application and press Enter.

    The scope name must be unique on the instance, begin with x\_&lt;prefix&gt;, and be 18 characters or fewer. For more information, see [Namespace identifier](../../applications/concept/c_NamespaceIdentifier.md).

8.  Enter a package name for the application and press Enter.

    The package name must adhere to Node Package Manager \(npm\) package naming standards.

9.  Select a template that defines the default application structure.

10. Build and install your application to compile source code into application metadata and make your changes available across the instance. For more information, see [Build and install an application in the ServiceNow IDE](build-applications-servicenow-ide.md).


## Result

A scoped application with the default application structure is added to the instance and open in your workspace. For information about the application structure, see the [Application structure](../../custom-application/concept/building-applications-source-code.md#application-structure) section of the Building applications in source code topic.

![An application open in the File Explorer view.](../image/servicenow-ide-create-app.png)

In the status bar, a message confirms whether the application was created. If the application creation fails, review the output logs in the panel.

**Note:** For the ServiceNow IDE to install the required dependencies in an application, the public npm registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## What to do next

From your Git provider, create a dedicated Git repository for the application. Initialize a local Git repository for your application and push it to the remote repository. For more information, see [Initialize a Git repository with the ServiceNow IDE](initialize-git-repository-servicenow-ide.md).

In the ServiceNow IDE, start developing your application in source code with ServiceNow Fluent, writing custom JavaScript modules, or adding third-party libraries.

