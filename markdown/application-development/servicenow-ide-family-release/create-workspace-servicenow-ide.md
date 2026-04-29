---
title: Create a workspace in the ServiceNow IDE
description: Create a workspace to view and organize the applications you're working on in the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Create a workspace in the ServiceNow IDE

Create a workspace to view and organize the applications you're working on in the ServiceNow IDE.

## Before you begin

Role required: admin

## About this task

In a workspace in the ServiceNow IDE, you can add any applications that you're working on to navigate through multiple applications from one place. You can create multiple workspaces to group different sets of applications. Workspaces are specific to a user, and applications can be added or removed from a workspace at any time. When you open the ServiceNow IDE, the workspace in which you were most recently working opens. Workspaces in the ServiceNow IDE are based on workspaces in Visual Studio Code. For general information about workspaces, see the [Visual Studio Code documentation](https://code.visualstudio.com/docs) website.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  From the ServiceNow IDE home page, select **Create a workspace**.

    **Tip:** You can also use the `Workspaces: Create a Workspace` command from the command palette.

3.  Enter a name for the workspace and press Enter.

4.  Enter a description for the workspace and press Enter.

    The workspace becomes the active workspace.

    ![A workspace on the homepage.](../image/servicenow-ide-empty-workspace.png)

5.  Add existing applications to the workspace.

    1.  Select **Open apps**.

    2.  Select an application.

        Only applications created or converted with the ServiceNow IDE or ServiceNow SDK can be added. You can add additional applications to a workspace from the main menu or the command palette with the `Workspaces: Add Application to Workspace` command.


## What to do next

Create, convert, or clone an application and add it to your workspace. For more information, see [Adding applications in ServiceNow IDE](../concept/creating-applications-servicenow-ide.md).

To switch the active workspace, you can browse and select other workspaces from the ServiceNow IDE home page or from the command palette with the `Workspaces: Browse Workspaces` command.

