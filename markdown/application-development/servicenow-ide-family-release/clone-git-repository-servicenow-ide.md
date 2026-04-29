---
title: Clone a Git repository with the ServiceNow IDE
description: Clone a remote Git repository to collaborate on applications in source control with the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Clone a Git repository with the ServiceNow IDE

Clone a remote Git repository to collaborate on applications in source control with the ServiceNow IDE.

## Before you begin

-   Create a workspace for your applications. For more information, see [Create a workspace in the ServiceNow IDE](create-workspace-servicenow-ide.md).
-   Set your basic or OAuth 2.0 credentials for the ServiceNow IDE to connect to your Git repository. For more information, see [Connect to a Git provider using basic authentication with the ServiceNow IDE](connect-git-provider-basic-auth.md) or [Configure OAuth 2.0 credentials to connect to a Git provider with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#).

Role required: admin

## About this task

You can clone a remote Git repository that contains applications created or converted with the ServiceNow IDE or ServiceNow SDK. The repository must contain one or more applications with `now.config.json` and `package.json` files.

**Note:** ServiceNow IDE supports cloning from Git servers on Git version 2.3.2 or later.

Cloning is intended for developing an application on multiple non-production instances and managing it in a single repository. To publish an application and deploy it to a production instance, use the Application Repository. For more information, see [ServiceNow application repository](../../applications/concept/app-repo.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace to which you want to add the application.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Git: Clone` and press Enter.

5.  Enter a remote Git repository URL and press Enter.


## Result

The application is added to the instance and your workspace with the files from the remote repository. Only the default branch is cloned initially. To check out another branch, you must fetch the other branches from the remote repository using the `Git: Fetch` command from the command palette.

## What to do next

You can check out or create branches in the repository and push changes to the remote repository. For more information, see [Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md).

