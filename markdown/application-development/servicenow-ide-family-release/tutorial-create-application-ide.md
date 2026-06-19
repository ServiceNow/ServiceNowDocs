---
title: Tutorial part 1: Create an application in the ServiceNow IDE
description: Create an application that you can develop in source code in the ServiceNow IDE.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-ide-family-release/tutorial-create-application-ide.html
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Getting started: Create your first application in the ServiceNow IDE, Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Tutorial part 1: Create an application in the ServiceNow IDE

Create an application that you can develop in source code in the ServiceNow IDE.

## Before you begin

Role required: admin

## About this task

In the ServiceNow IDE, you can develop scoped applications in source code using ServiceNow Fluent to define application metadata \[sys\_metadata\]. You can also create JavaScript modules and use third-party libraries to organize and reuse code within scoped applications. For an application to support development in source code, you must create a scoped application or convert an existing scoped application using the ServiceNow IDE or ServiceNow SDK. In this tutorial, you create a scoped application from the ServiceNow IDE.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

    Before you can create an application, you must create a workspace in which you can add applications and navigate through them from one place.

    \[Omitted image "servicenow-ide-empty-state.png"\] Alt text: ServiceNow IDE home page before creating a workspace or application

    Workspaces are specific to a user, and you can create multiple workspaces to group different sets of applications. Applications can be added or removed from a workspace at any time. Workspaces in the ServiceNow IDE are based on workspaces in Visual Studio Code.

2.  Create a workspace.

    1.  Select **Create a workspace**.

    2.  Enter a name for the workspace and press Enter.

    3.  Enter a description for the workspace and press Enter.

        The workspace becomes the active workspace but doesn't contain any applications yet.

        \[Omitted image "servicenow-ide-new-workspace.png"\] Alt text: The empty state of an active workspace.

        **Tip:** To switch the active workspace, you can browse and select other workspaces from the ServiceNow IDE home page or from the command palette with the `Workspaces: Browse Workspaces` command.

3.  Create an application in the workspace.

    1.  Select **Create an app**.

    2.  Enter a name, such as `Hello World`, and press Enter.

    3.  Enter a description for the application and press Enter.

    4.  Enter a scope, such as `x_snc_hello_world`, and press Enter.

        **Important:** The scope name must be unique on the instance, begin with x\_&lt;prefix&gt;, and be 18 characters or fewer. For more information, see [Namespace identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_NamespaceIdentifier.md).

    5.  Enter a package name, such as `x-snc-hello-world`, and press Enter.

        The package name must adhere to Node Package Manager \(npm\) package naming standards.

    6.  Select the **A basic application using NowSDK and TypeScript** template to use TypeScript to create JavaScript modules.

        The application templates define the default application structure.

        **Note:** TypeScript uses static typing and type annotations to support developers catching errors earlier while writing code. If you'd prefer to get started with JavaScript instead, select **JavaScript**.

        Your application is added to your workspace. From the File Explorer view \(\[Omitted image "servicenow-ide-file-explorer-icon.png"\] Alt text: File Explorer\), you can navigate through the application files.

        \[Omitted image "servicenow-ide-create-app-pre-build.png"\] Alt text: Files in the Hello World application.

        The `package.json` and `now.config.json` files define the application structure, which is similar to that of Node.js applications or Node Package Manager \(npm\) packages. A sample ServiceNow Fluent file \(`index.now.ts`\) and JavaScript module \(`script.js` or `script.ts`\) were created in the `src` directory, and dependencies were installed into the `node_modules` directory. The application is also added to the Custom Application \[sys\_app\] table.

        Next, build and install the application to make it available for development across the instance.

    7.  From the Status Bar at the bottom of the ServiceNow IDE, select **Build and Install**.

        \[Omitted image "servicenow-ide-build-status-bar.png"\] Alt text: Theinstall button in the Status Bar at the bottom of the ServiceNow IDE user interface.

        Building and installing the application compiles its ServiceNow Fluent code and JavaScript or TypeScript module code into Application Files \[sys\_metadata\] and EcmaScript Modules \[sys\_module\] on the instance, respectively. Build artifacts in the `dist/app` directory are packaged into an installable `.zip` file in the `target` directory.

        Logs in the Output panel indicate the status of the build and if the application is installed successfully. If either process fails, review the logs to identify any issues.

        \[Omitted image "servicenow-ide-deploy-logs.png"\] Alt text: Logs in the Output panel indicating that the application built and installed successfully.

        For information about the application structure, see the [Application structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/building-applications-source-code.md) section of the Building applications in source code topic.


## What to do next

Continue to [Tutorial part 2: Initialize a repository for your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-ide-family-release/tutorial-initialize-repository-ide.md).

**Parent Topic:**[Getting started: Create your first application in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-ide-family-release/getting-started-create-application-ide.md)

