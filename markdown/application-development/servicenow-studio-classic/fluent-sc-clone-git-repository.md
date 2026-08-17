---
title: Clone a Git repository from ServiceNow Studio
description: Clone a remote Git repository to collaborate on applications in Fluent source control in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/fluent-sc-clone-git-repository.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [Fluent source control, Clone a git repository, servicenow studio]
breadcrumb: [Fluent source control in ServiceNow Studio, Source control integration, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Clone a Git repository from ServiceNow Studio

Clone a remote Git repository to collaborate on applications in Fluent source control in ServiceNow Studio.

## Before you begin

-   Create a workspace for your applications.
-   Set your basic or OAuth 2.0 credentials for ServiceNow Studio to connect to your Git repository. For more information, see [Connect to a Git provider using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-basic-auth.md) and [Connect to a Git provider using OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-oauth-2-0.md).

Role required: admin

## About this task

You can clone a remote Git repository that contains Fluent applications. The repository must contain one or more applications with `now.config.json` and `package.json` files.

**Note:** ServiceNow Studio supports cloning from Git servers on Git version 2.3.2 or later.

Cloning is intended for developing an application on multiple non-production instances and managing it in a single repository. To publish an application and deploy it to a production instance, use the Application Repository. For more information, see [ServiceNow application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/app-repo.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a workspace to which you want to add the application.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Git: Clone` and press Enter.

5.  Enter a remote Git repository URL and press Enter.


## Result

The application is added to the instance and your workspace with the files from the remote repository. Only the default branch is cloned initially. To check out another branch, you must fetch the other branches from the remote repository using the `Git: Fetch` command from the command palette.

## What to do next

You can check out or create branches in the repository and push changes to the remote repository. For more information, see [Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md).

**Parent Topic:**[Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-source-control-sn-studio.md)

