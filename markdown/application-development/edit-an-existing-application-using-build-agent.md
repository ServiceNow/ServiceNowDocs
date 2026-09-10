---
title: Edit an existing application using Build Agent
description: Use natural language prompts to modify an existing application in Build Agent. You can describe changes in plain language and review, refine, and approve updates before the application is built and installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/edit-an-existing-application-using-build-agent.html
release: zurich
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Edit an existing application using Build Agent

Use natural language prompts to modify an existing application in Build Agent. You can describe changes in plain language and review, refine, and approve updates before the application is built and installed.

## Before you begin

Install and enable Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/install-build-agent.md).

For some prompting guidelines and ideas, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-example-prompts.md).

You can convert existing apps to ServiceNow Fluent and work on them in Build Agent. For more information, see [Convert an application with the ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-sdk/convert-application-now-sdk.md).

Role required: admin

## About this task

You can edit an application with Build Agent in both ServiceNow Studio and the ServiceNow IDE. If you're using the ServiceNow IDE, the application must be open in your workspace. You can add it to the workspace in the following ways:

-   Applications created with Build Agent are automatically added to the workspace in which they were created. They can also be opened in other workspaces in the ServiceNow IDE.
-   For applications that were not developed using the ServiceNow IDE, ServiceNow Studio, or the ServiceNow SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the open app tool to locate the application you want. Alternatively, you can search for an application directly within the Build Agent, and it will automatically use the open app tool. The open app tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.
-   Copy an existing application created with the ServiceNow IDE or ServiceNow SDK from a Git repository. For more information, see [Clone a Git repository with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-ide-family-release/clone-git-repository-servicenow-ide.md).
-   Right-click a record or artifact and select **Configure** to open the metadata editor in ServiceNow Studio.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    ServiceNow Studio opens to a Build Agent chat box.

    \[Omitted image "ba-sns-full-page-chat.png"\] Alt text: ServiceNow Studio home screen with a Build Agent prompt input area, Recents panel, Recent chats panel, and Plans panel listing example plans with statuses.

2.  Display the Build Agent chat panel by selecting the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel.

3.  Select **New conversation**.

    \[Omitted image "ba-sns-new-convo.png"\] Alt text: Build Agent panel with New conversation button highlighted. \[Omitted image ""\] Alt text:

4.  Select **Update an app** in the chat panel.

    \[Omitted image "ba-sns-update-app.png"\] Alt text: New Chat panel with Update an app highlighted.

5.  Select the application that you want to edit and select the **Submit** button.

    Applications converted into ServiceNow Fluent code appear in the Application list.

    \[Omitted image "ba-update-app-2.png"\] Alt text: App selection dialog with Planner Tracker selected from a list of available apps

6.  Describe what you want to change in the application in plain language.

    Build Agent can provide you with some suggestions, such as `Update a table or add/modify fields`.

7.  Select the Send icon \[Omitted image "ba-send-icon.png"\] Alt text:.

    Build Agent starts updating the application.

8.  Review the changes in the Change Log in a tab in ServiceNow Studio and continue iterating to refine the app.

    For more information on the change log, see [Build Agent checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md).

    Review updates to generated tables, flows, and scripts, and preview any user interfaces created in your application. You can interact with the preview to make additional edits, for example, select a button in the **Preview** tab and tell Build Agent to `Change the color of the button to purple`.

9.  Approve the changes:

    1.  If prompted, select **Review all edits** to view the changes.

    2.  If the changes are correct, select **Approve plan**.

10. Prompt and **Approve** Build Agent to build and deploy the application to an update set if it doesn't do so automatically.


## Result

The application is built and installed.

**Note:** Follow the on-screen instructions, as the Build Agent functions interactively.

## What to do next

Review the application and its metadata in ServiceNow Studio using the change log. For more information, see [Build Agent checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md). You can also review the application using the File Navigator in ServiceNow Studio. For more information, see [Find an app or app file using the Navigator panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/qs-find-app-app-file-using-navigator-panel.md).

When you're ready, deploy the app. For more information, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md).

If you want to view source code, open the ServiceNow IDE within ServiceNow Studio and select the **Explorer** view from the Navigator panel. The ServiceNow Fluent application code and other source code in the `src` directory appears.

\[Omitted image "build-agent-file-explorer.png"\] Alt text: File Explorer showing project structure with folders and configuration files

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

