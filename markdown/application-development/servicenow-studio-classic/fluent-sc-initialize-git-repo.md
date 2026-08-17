---
title: Initialize a Git repository
description: Initialize a local Git repository for an application in ServiceNow Studio and push it to a remote Git repository to manage an application in source control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/fluent-sc-initialize-git-repo.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 2
keywords: [Fluent source control, ServiceNow Studio, Fluent, Git repository]
breadcrumb: [Fluent source control in ServiceNow Studio, Source control integration, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Initialize a Git repository

Initialize a local Git repository for an application in ServiceNow Studio and push it to a remote Git repository to manage an application in source control.

## Before you begin

-   Create or convert an application with ServiceNow Studio. For more information, see [Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md) or [Convert an application to Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/convert-app-to-fluent.md).
-   Create a dedicated Git repository for the application from your Git provider.
-   Set your basic or OAuth 2.0 credentials for ServiceNow Studio to connect to your Git repository. For more information, see [Connect to a Git provider using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-basic-auth.md) and [Connect to a Git provider using OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-oauth-2-0.md).

Role required: admin

## About this task

An application on an instance can be connected to only one repository at a time. To clone an application that exists in a remote Git repository, see [Clone a Git repository from ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-clone-git-repository.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a workspace with an application that isn't connected to a Git repository.

3.  Select the **Changes** tab in the Navigator panel.

4.  Select **Initialize Repository** or use the `Git: Initialize Repository` command from the command palette.

5.  Select the application for which you want to initialize a Git repository and press Enter.

6.  Select **main** as the default branch name or enter another name and press Enter.

7.  Select the stage all untracked changes icon \[Omitted image "servicenow-ide-stage-icon.png"\] Alt text:.

8.  Enter a commit message and select the commit icon \[Omitted image "servicenow-ide-commit-icon.png"\] Alt text:.

9.  Select the more actions menu icon \[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: and select **Push**.

10. Enter a remote repository URL and press Enter.


## Result

The application is available in the remote repository.

If your Git credentials aren't configured or are inactive, the application isn't pushed to the remote repository. When prompted to configure your credentials, select **Configure** to configure your Git credentials and then try again.

## What to do next

Check out or create branches in the repository and push changes to the remote repository. For more information, see [Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md).

**Parent Topic:**[Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-source-control-sn-studio.md)

