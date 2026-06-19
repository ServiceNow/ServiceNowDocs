---
title: Edit an existing application using Build Agent
description: Modify existing ServiceNow applications using natural language prompts with Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/edit-an-existing-application-using-build-agent.html
release: australia
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Edit an existing application using Build Agent

Modify existing ServiceNow applications using natural language prompts with Build Agent.

## Before you begin

Install and enable Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/install-build-agent.md).

For some prompting guidelines and ideas, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-example-prompts.md).

Role required: admin

## About this task

You can edit an application with Build Agent in both ServiceNow Studio and the ServiceNow IDE. If you're using the ServiceNow IDE, the application must be open in your workspace. You can add it to the workspace in the following ways:

-   Applications created with Build Agent are automatically added to the workspace in which they were created. They can also be opened in other workspace in the ServiceNow IDE.
-   For applications that were not developed using the ServiceNow IDE, ServiceNow Studio, or the ServiceNow SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the open app tool to locate the application you want. Alternatively, you can search for an application directly within the Build Agent, and it will automatically use the open app tool. The open app tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.
-   Clone an existing application created with the ServiceNow IDE or ServiceNow SDK from a Git repository. For more information, see [Clone a Git repository with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/clone-git-repository-servicenow-ide.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the lower corner of your browser. You can also select the Sparkle icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the application banner.

    \[Omitted image "sn-studio-access-build-agent.png"\] Alt text: If Build Agent isn't open, open it from the status bar in the corner of your browser.

2.  Select **Update an app** in the chat panel.

    \[Omitted image "ba-update-app-1.png"\] Alt text: Chat panel showing four action buttons with Update an app highlighted

3.  Select the application that you want to edit and select the **Submit** button.

    Applications converted into ServiceNow Fluent code appear in the Application list.

    \[Omitted image "ba-update-app-2.png"\] Alt text: App selection dialog with Planner Tracker selected from a list of available apps

4.  Describe what you want to change in the application in plain language.

    Build Agent can provide you with some suggestions, such as `Update a table or add/modify fields`.

5.  Select the Send icon \[Omitted image "ba-send-icon.png"\] Alt text:.

    Build Agent starts updating the application.

6.  Review the changes in the Change Log in a tab in ServiceNow Studio and continue iterating to refine the app.

    For more information on the change log, see [Build Agent conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/ba-conversational-change-log.md).

    Review updates to generated tables, flows, and scripts, and preview any user interfaces created in your application. You can interact with the preview to make additional edits, for example, select a button in the **Preview** tab and tell Build Agent to `Change the color of the button to purple`.

7.  Approve the changes:

    1.  If prompted, select **Review all edits** to view the changes.

    2.  If you’re happy with the changes, select **Approve plan**.

8.  Prompt and **Approve** Build Agent to build and deploy the application to an update set if it doesn't do so automatically.


## Result

The application is built and installed.

**Note:** Even though this process is standard, be sure to follow the on-screen instructions, as the Build Agent functions interactively.

## What to do next

For information on deploying your application, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-deployment.md).

If you want to view source code, open the ServiceNow IDE and select the **File Explorer** view from the Activity bar. The ServiceNow Fluent application code and other source code in the `src` directory appears.

\[Omitted image "build-agent-file-explorer.png"\] Alt text: File Explorer showing project structure with folders and configuration files

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/use-build-agent.md)

