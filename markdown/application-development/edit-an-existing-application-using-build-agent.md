---
title: Edit an existing application using Build Agent
description: Learn to use Build Agent to update or enhance ServiceNow applications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Use, Build Agent, Use AI capabilities in custom applications, Developing your application, Building applications]
---

# Edit an existing application using Build Agent

Learn to use Build Agent to update or enhance ServiceNow applications.

## Before you begin

Install and enable the Build Agent. For more information, see [Install Build Agent](install-build-agent.md).

Role required: admin

## About this task

To edit an application with Build Agent, it must be open in your workspace in the ServiceNow IDE. Here are a few ways to add an application to a workspace:

-   Applications created with Build Agent are automatically added to the workspace in which they were created. They can also be opened in other workspace in the ServiceNow IDE.
-   For applications that were not developed using the ServiceNow IDE or SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the Open App tool to locate the desired application. Alternatively, you can search for an application directly within the Build Agent, and it will automatically utilize the Open App tool. The Open App tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.
-   Clone an existing application created with the ServiceNow IDE or ServiceNow SDK from a Git repository. For more information, see [Clone a Git repository with the ServiceNow IDE](../../servicenow-ide/task/clone-git-repository-servicenow-ide.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

    The Build Agent panel is open by default.

2.  From the Application list, select the application that you want to edit.

    ![Welcome to Build Agent message](../image/build-agent-edit.png)

    If you had converted an application into ServiceNow Fluent code, it would also appear in the Application list.

3.  Describe what you want to change in the application in plain English, and then select **Send**.

    The Build Agent starts updating the application.

4.  Approve the changes:

    1.  If prompted, select **Review all edits** to view the changes.

    2.  If you’re happy with the changes, select **Approve**.

5.  In the chat panel, enter a message to instruct the Build Agent to build and deploy the application.

    You can preview the code files before approval, but to view the actual metadata output, you must build and install the application on the instance.

6.  Build and deploy the application by selecting **Approve**.


## Result

The application is built and installed.

**Note:** Even though this process is standard, be sure to follow the on-screen instructions, as the Build Agent functions interactively.

## What to do next

From the Activity Bar, select the File Explorer view \(![File Explorer](../../servicenow-ide/image/servicenow-ide-file-explorer-icon.png)\) to see the ServiceNow Fluent application code and other source code in the `src` directory, or select the Metadata Explorer view \(![Metadata Explorer](../../servicenow-ide/image/servicenow-ide-metadata-explorer-icon.png)\) to see the application metadata on the instance.

**Parent Topic:**[Use Build Agent](use-build-agent.md)

