---
title: Initialize a Git repository with the ServiceNow IDE
description: Initialize a local Git repository for an application and push it to a remote Git repository to manage an application in source control.
locale: en-US
release: xanadu
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate source control, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Initialize a Git repository with the ServiceNow IDE

Initialize a local Git repository for an application and push it to a remote Git repository to manage an application in source control.

## Before you begin

-   Create or convertan application with the ServiceNow IDE. For more information, see [Create an application with the ServiceNow IDE](create-application-servicenow-ide.md)or [Convert an application with the ServiceNow IDE](convert-application-servicenow-ide.md).
-   Create a dedicated Git repository for the application from your Git provider.
-   Set your basic or OAuth 2.0 credentials for the ServiceNow IDE to connect to your Git repository. For more information, see [Connect to a Git provider using basic authentication with the ServiceNow IDE](connect-git-provider-basic-auth.md) or [Configure OAuth 2.0 credentials to connect to a Git provider with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#).

Role required: admin

## About this task

An application on an instance can be connected to only one repository at a time. To clone an application that exists in a remote Git repository, see [Clone a Git repository with the ServiceNow IDE](clone-git-repository-servicenow-ide.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace with an application that isn't connected to a Git repository.

3.  From the Activity Bar, select the Source Control view \(![Source Control](../image/servicenow-ide-source-control-icon.png)\).

4.  Select **Initialize Repository** or use the `Git: Initialize Repository` command from the command palette.

5.  Select the application for which you want to initialize a Git repository and press Enter.

6.  Select **main** as the default branch name or enter another name and press Enter.

7.  Select the Stage All Untracked Changes icon \(![Stage all untracked changes](../image/servicenow-ide-stage-icon.png)\).

8.  Enter a commit message and select the Commit icon \(![Stage all untracked changes](../image/servicenow-ide-commit-icon.png)\).

9.  Select the More actions menu icon \(![More actions](../image/servicenow-ide-more-actions-icon.png)\) and select **Push**.

10. Enter a remote repository URL and press Enter.


## Result

The application is available in the remote repository.

If your Git credentials aren't configured or are inactive, the application isn't pushed to the remote repository. When prompted to configure your credentials, select **Configure** to configure your Git credentials and then try again.

## What to do next

You can check out or create branches in the repository and push changes to the remote repository. For more information, see [Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md).

**Parent Topic:**[Integrating source control with the ServiceNow IDE](../concept/integrating-source-control-servicenow-ide.md)

**Related topics**  


[Connect to a Git provider using basic authentication with the ServiceNow IDE](connect-git-provider-basic-auth.md)

[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#)

[Configure a MID Server to use source control with the ServiceNow IDE](configure-mid-server-source-control.md)

[Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md)

