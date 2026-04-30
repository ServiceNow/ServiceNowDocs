---
title: Tutorial part 2: Initialize a repository for your application
description: Initialize a local Git repository for an application in the ServiceNow IDE and push it to a remote Git repository in GitHub to manage the application in source control.
locale: en-US
release: xanadu
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Getting started: Create your first application in the ServiceNow IDE, Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Tutorial part 2: Initialize a repository for your application

Initialize a local Git repository for an application in the ServiceNow IDE and push it to a remote Git repository in GitHub to manage the application in source control.

## Before you begin

Complete [Tutorial part 1: Create an application in the ServiceNow IDE](tutorial-create-application-ide.md).

Role required: admin

## Procedure

1.  From the Activity Bar, select the Source Control view \(![Source Control](../image/servicenow-ide-source-control-icon.png)\).

    ![Source control view with no connected repositories and the option to initialize a local repository.](../image/servicenow-ide-initialize-repo.png)

2.  Initialize a Git repository that's local to the ServiceNow IDE.

    1.  Select **Initialize Repository**.

    2.  Press Enter to use **main** as the default branch name.

    A local repository is initialized for your application, and the application files that are tracked in source control are in the Untracked Changes list. Application files and directories specified in the `.gitignore` file aren’t tracked in source control.

    **Tip:** If you select a file in the list, you can view a comparison of the current and previous version of the file in the Diff editor.

    Before you can push your application to a remote Git repository, you must stage and commit your changes in the local Git repository.

3.  Stage and commit your changes.

    1.  From the Untracked Changes list, select the Stage All Untracked Changes icon \(![Stage all untracked changes](../image/servicenow-ide-stage-icon.png)\).

        ![Source Control view with application files in the Untracked Changes list.](../image/servicenow-ide-stage-changes.png)

        Your changes move to the Staged Changes list.

    2.  In the message box, enter a commit message.

    3.  Select the Commit icon \(![Stage all untracked changes](../image/servicenow-ide-commit-icon.png)\).

        ![Source Control view with application files in the Staged Changes list and a commit message.](../image/servicenow-ide-commit-changes.png)

    Now that you have committed changes, you can expand the Commits section to see your commit history and details about each commit.

    ![Commit history showing an initial commit, including the commit message and author.](../image/servicenow-ide-commit-history.png)

    To push your changes to a remote repository that other developers can access, you need to create a repository with a Git provider like GitHub and generate a personal access token.

    **Note:** The following steps demonstrate using GitHub and basic authentication as an example, but you could use another Git provider of your choosing or OAuth 2.0 authentication. For more information, see [Integrating source control with the ServiceNow IDE](../concept/integrating-source-control-servicenow-ide.md).

4.  Create a remote repository.

    1.  Log in to your GitHub account.

    2.  Select the Create new menu \(![Create new](../image/servicenow-ide-gh-plus-icon.png)\) and select **New repository**.

    3.  On the New repository form, fill in the fields.

        ![Create a new repository form in GitHub.](../image/servicenow-ide-gh-new-repo.png)

    4.  Select **Create repository**.

    5.  From your repository, copy the HTTPS URL and paste it somewhere that you can easily access it again for use in the following steps.

        ![Copy the HTTPS URL for your repository in GitHub.](../image/servicenow-ide-gh-repo-url.png)

5.  Create a personal access token.

    1.  From your user profile in GitHub, select **Settings**.

    2.  From the settings categories, select **Developer Settings**.

    3.  From the Personal access tokens menu, select **Tokens \(classic\)**.

    4.  From the Generate new token menu, select **Generate new token \(classic\)**.

    5.  On the New personal access token \(classic\) form, select the **repo** scope and fill in the remaining required fields.

        The **repo** scope is required to connect to the ServiceNow IDE.

        ![Create a new personal access token (classic) with the repo scope selected in the scopes list.](../image/servicenow-ide-gh-create-token.png)

    6.  Select **Generate token**.

    7.  Copy the token and paste it somewhere that you can easily access it again for use in the following steps so you don't need to regenerate it.

        ![A personal access token that you can copy.](../image/servicenow-ide-gh-token.png)

6.  Configure basic authentication in the ServiceNow IDE to connect to the remote repository.

    1.  Navigate to the ServiceNow IDE.

    2.  Use one of the following keyboard shortcuts to open the command palette:

        -   Windows: Ctrl-Shift-P
        -   Mac: Cmd-Shift-P
    3.  Enter `Git: Set IDE Git credentials` and press Enter.

    4.  From the New Git credential form, select **Basic auth**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Git repository URL|The HTTPS URL of the Git repository you created in GitHub. For example: `https://github.com/<owner>/hello-world.git`.|
        |Git username|Your GitHub user name.|
        |Personal access token|The personal access token that you generated from GitHub.|

    6.  Select **Submit**.

    Now that your authentication credentials are configured, you can push your application to the remote repository.

    **Tip:** If you need to manage existing Git credentials, use the `Git: Manage Git credentials` command from the command palette.

7.  Push your changes to the remote repository.

    1.  Select the More actions menu icon \(![More actions](../image/servicenow-ide-more-actions-icon.png)\) and select **Push**.

        ![Push the staged changes to the remote repository.](../image/servicenow-ide-push-changes.png)

    2.  Enter the HTTPS URL of the remote Git repository and press Enter.

    The application is added to the remote repository in GitHub, and changes to the application across users are tracked remotely.

    ![The hello-world repository in GitHub, which contains the Hello World application from the ServiceNow IDE.](../image/servicenow-ide-gh-repo.png)


## Result

You can check out or create branches in the repository and push changes to the remote repository. For more information, see [Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md).

**Note:** An application on an instance can be connected to only one repository at a time. To update the remote repository an application is connected to, you can use the `Git: Update remote origin` command from the command palette and enter a different remote repository URL.

## What to do next

Continue to [Tutorial part 3: Define a table in ServiceNow Fluent code](tutorial-define-table-fluent-ide.md).

**Parent Topic:**[Getting started: Create your first application in the ServiceNow IDE](../concept/getting-started-create-application-ide.md)

