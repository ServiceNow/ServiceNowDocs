---
title: Create a workspace
description: Create a workspace to view and organize the applications you're working on in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/create-a-workspace.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 1
keywords: [Create a workspace, pro-code development, ServiceNow Studio]
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create a workspace

Create a workspace to view and organize the applications you're working on in ServiceNow Studio.

## Before you begin

Role required: admin

## About this task

Add applications you're working on to a workspace so you can access multiple applications. You can create multiple workspaces to group different sets of applications. Workspaces are specific to a user, and applications can be added or removed from a workspace at any time. When you open ServiceNow Studio, the workspace you most recently used opens in the Explorer tab. Workspaces in ServiceNow Studio are based on workspaces in Visual Studio Code. For general information about workspaces, see the [Visual Studio Code documentation](https://code.visualstudio.com/docs) website.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  On the Explorer tab, select **Create a workspace**.

    **Tip:** You can also use the `Workspaces: Create a Workspace` command from the command palette.

3.  Enter a name for the workspace and press Enter.

4.  Enter a description for the workspace and press Enter.

    The workspace becomes the active workspace.

5.  Add existing applications to the workspace.

    1.  Select **Open apps**.

    2.  Select an application.

        Only applications created in or converted to Fluent can be added. You can add additional applications to a workspace from the main menu or the command palette with the `Workspaces: Add Application to Workspace` command.


## What to do next

To switch the active workspace, you can browse and select other workspaces from the ServiceNow Studio home page or from the command palette with the `Workspaces: Browse Workspaces` command.

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

