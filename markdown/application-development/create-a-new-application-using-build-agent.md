---
title: Create an application using Build Agent
description: Build custom ServiceNow applications by describing your requirements in plain language to Build Agent. The AI agent generates and builds the application code automatically.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Create an application using Build Agent

Build custom ServiceNow applications by describing your requirements in plain language to Build Agent. The AI agent generates and builds the application code automatically.

## Before you begin

Install and enable Build Agent. For more information, see [Install Build Agent](install-build-agent.md).

If you prefer to access in the ServiceNow IDE instead of ServiceNow Studio, you must first create a workspace. For more information, see [Create a workspace in the ServiceNow IDE](../../servicenow-ide/task/create-workspace-servicenow-ide.md).

**Note:** Build Agent requires ServiceNow SDK version 4.0 at a minimum. If you’re using an older version, Build Agent prompts you to upgrade to ServiceNow SDK 4.0.

For some prompting guidelines and ideas, see [Example prompts](../reference/build-agent-example-prompts.md).

Role required: admin

## About this task

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser. ![If Build Agent isn't open, open it from the status bar in the corner of your browser.](../../servicenow-studio/image/sn-studio-access-build-agent.png)

2.  In the chat panel, describe the application that you want to create in plain language or select a prompt.

<table id="choicetable_qzh_hj2_lgc"><thead><tr><th align="left" id="d251873e209">

Scenario

</th><th align="left" id="d251873e212">

Actions

</th></tr></thead><tbody><tr><td id="d251873e218">

**Describe the app you want to create**

</td><td>

Describe the application that you want to create, and then select the Send icon![](../image/ba-send-icon.png). For example:![Describe the application in a chat panel](../image/build-agent-describe-app.png)

You can also attach images, such as architectural diagrams or UI wireframes, to provide context for prompts.

</td></tr><tr><td id="d251873e239">

**Select a predetermined prompt**

</td><td>

1.  Select **Create an app** from the Application list. ![Welcome to Build Agent message](../image/ba-create-app-1.png)
2.  Describe the application that you want to create, including as much context as possible, and then select the Send icon ![](../image/ba-send-icon.png). For example, include roles, data requirements, and success criteria.


</td></tr></tbody>
</table>    After reviewing your requirements, Build Agent requests confirmation to proceed with creating the application.

3.  Instruct Build Agent to start developing the application by selecting **Approve plan**.

    Or, if you're not satisfied with the plan, tell Build Agent what you change, and continue to prompt until you have a plan you like.

    ![Implementation plan for Planner Tracker application](../image/ba-create-app-2.png "Approving the plan")

    Build Agent can access ServiceNow knowledge sources and tools, which enable it to learn, analyze, and then create applications.

    After creating the application, Build Agent builds the application.

    **Note:** You can preview the code files before approval. But to see the actual metadata output, you must build and install the application on the instance.

4.  If your application has a user interface, you can preview the app in a tab in ServiceNow Studio to inspect how it looks.

    You can keep prompting to refine the app, its appearance, and functionality. For more information, see [Edit an existing application using Build Agent](edit-an-existing-application-using-build-agent.md).


## Result

Review the application and its metadata in ServiceNow Studio using the change log. For more information, see [Build Agent conversation change log](../concept/ba-conversational-change-log.md). You can also review the application using the File Navigator in ServiceNow Studio. For more information, see [Find an app or app file using the Navigator panel](../../servicenow-studio/task/qs-find-app-app-file-using-navigator-panel.md).

For information on deploying your application, see [Vibe coding, AI-assisted development, and deployment](../../vibe-coding/concept/vc-and-deployment.md).

For information on troubleshooting issues, see [Troubleshooting in Build Agent](../reference/build-agent-troubleshooting.md).

After the application is built, Build Agent displays a success message. For example:

![Build Agent success message](../image/build-agent-success.png "Success message")

Build Agent displays the details of your app in the chat panel.

![Planner Tracker application build summary](../image/ba-create-app-3.png "Planner tracker app build summary")

You can prompt Build Agent for details on how to access your new app.

![Response with multiple methods to access the Planner Tracker app](../image/ba-access-app.png "Details on accessing your app")

If you want to view source code, open the ServiceNow IDE and select the **File Explorer** view from the Activity bar. The ServiceNow Fluent application code and other source code in the `src` directory appears.

![File Explorer showing project structure with folders and configuration files](../image/build-agent-file-explorer.png "App code in the ServiceNow IDE")

**Parent Topic:**[Use Build Agent](use-build-agent.md)

