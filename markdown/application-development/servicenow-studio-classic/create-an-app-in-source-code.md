---
title: Create an app in source code
description: Create an application to develop in source code in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/create-an-app-in-source-code.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [Create app in source code, ServiceNow Studio]
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an app in source code

Create an application to develop in source code in ServiceNow Studio.

## Before you begin

Create a workspace for your application. For more information, see [Create a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-a-workspace.md).

**Note:** You can use Build Agent to help you create and edit applications in ServiceNow Studio. For more information, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a workspace.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Fluent: Create Fluent App` and press Enter.

5.  Select the type of application.

    -   Scoped: Create a scoped application that is protected by identifying and restricting access to application files and data.
    -   Global: Create an application in the global scope to allow it to be accessible to other global applications.
6.  Enter a name for the application and press Enter.

7.  Enter a description for the application and press Enter.

8.  For scoped applications, enter a scope name and press Enter.

    The scope name must be unique on the instance, begin with x\_&lt;prefix&gt;, and be 18 characters or fewer. For more information, see [Namespace identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_NamespaceIdentifier.md).

9.  Enter a package name for the application and press Enter.

    The package name must adhere to Node Package Manager \(npm\) package naming standards.

10. Select a template that defines the default application structure.


## Result

An application with the default application structure is added to the instance and open in your workspace. For information about the application structure, see the Application Structure section of the [Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md) topic.

\[Omitted image "servicenow-ide-create-app.png"\] Alt text: An application open in the File Explorer view.

In the status bar, a message confirms whether the application was created. If the application creation fails, review the output logs in the panel.

**Note:** For ServiceNow Studio to install the required dependencies in an application, the public npm registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## What to do next

From your Git provider, create a dedicated Git repository for the application. Initialize a local Git repository for your application and push it to the remote repository. For more information, see [Initialize a Git repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-initialize-git-repo.md).

In ServiceNow Studio, start developing your application in source code with ServiceNow Fluent, writing custom JavaScript modules, or adding third-party libraries.

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

