---
title: Tutorial part 5: Clone the application on a different instance
description: Clone the application from the remote repository to develop it on another instance.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Getting started: Create your first application in the ServiceNow IDE, Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Tutorial part 5: Clone the application on a different instance

Clone the application from the remote repository to develop it on another instance.

## Before you begin

Complete [Tutorial part 4: Install and use a third-party library](tutorial-install-third-party-library-ide.md).

Role required: admin

## About this task

If you have access to another instance, you can install the application from the remote repository onto the instance to support development across instances.

**Note:** The instance and your user on the instance must meet the same requirements mentioned at the beginning of this tutorial.

Cloning is intended for developing an application on multiple non-production instances and managing it in a single repository. To publish an application and deploy it to a production instance, use the Application Repository. For more information, see [ServiceNow application repository](../../applications/concept/app-repo.md).

## Procedure

1.  Push your changes to the remote repository.

    1.  From the Activity Bar, select the Source Control view \(![Source Control](../image/servicenow-ide-source-control-icon.png)\).

    2.  From the Changes list, select the Stage All Tracked Changes icon \(![Stage all untracked changes](../image/servicenow-ide-stage-icon.png)\).

    3.  From the Untracked Changes list, select the Stage All Untracked Changes icon \(![Stage all untracked changes](../image/servicenow-ide-stage-icon.png)\).

        All of your changes should be in the Staged Changes list.

    4.  In the message box, enter a commit message.

    5.  Select the Commit icon \(![Stage all untracked changes](../image/servicenow-ide-commit-icon.png)\).

    6.  Select the More actions menu icon \(![More actions](../image/servicenow-ide-more-actions-icon.png)\) and select **Push**.

        ![Push the staged changes to the remote repository.](../image/servicenow-ide-push-changes.png)

    All of your changes are available in the remote repository. You or other developers can clone the application onto another instance.

2.  Log in to another ServiceNow instance.

3.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

4.  Create a workspace or open an existing one.

5.  Configure basic authentication in the ServiceNow IDE to connect to the remote repository.

    1.  Use one of the following keyboard shortcuts to open the command palette:

        -   Windows: Ctrl-Shift-P
        -   Mac: Cmd-Shift-P
    2.  Enter `Git: Set IDE Git credentials` and press Enter.

    3.  From the New Git credential form, select **Basic auth**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Git repository URL|The HTTPS URL to the Git repository you created in GitHub. For example: `https://github.com/<owner>/hello-world.git`.|
        |Git username|Your GitHub user name.|
        |Personal access token|The personal access token that you generated from GitHub.|

    5.  Select **Submit**.

6.  Clone the application.

    1.  Use one of the following keyboard shortcuts to open the command palette:

        -   Windows: Ctrl-Shift-P
        -   Mac: Cmd-Shift-P
    2.  Enter `Git: Clone` and press Enter.

    3.  Enter the HTTPS URL to the remote Git repository and press Enter.


## Result

The application is added to the instance with the files from the remote repository.

![The Hello World application files cloned from the remote repository.](../image/servicenow-ide-cloned-app.png)

## What to do next

Continue to [Tutorial part 6: Learn more about the ServiceNow IDE](../reference/tutorial-next-steps-ide.md).

**Parent Topic:**[Getting started: Create your first application in the ServiceNow IDE](../concept/getting-started-create-application-ide.md)

