---
title: Create an application using Build Agent
description: Build custom ServiceNow applications by describing your requirements in plain language to Build Agent. The AI agent generates and builds the application code automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-a-new-application-using-build-agent.html
release: zurich
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Create an application using Build Agent

Build custom ServiceNow applications by describing your requirements in plain language to Build Agent. The AI agent generates and builds the application code automatically.

## Before you begin

You can watch a short video on how to create an application in Build Agent.

Create an application in Build Agent 

Install and enable Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/install-build-agent.md).

If you prefer to access in the ServiceNow IDE instead of ServiceNow Studio, you must first create a workspace. For more information, see [Create a workspace in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-ide-family-release/create-workspace-servicenow-ide.md).

**Note:** Build Agent requires ServiceNow SDK version 4.0 at a minimum. If you’re using an older version, Build Agent prompts you to upgrade to ServiceNow SDK 4.0.

For some prompting guidelines and ideas, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-example-prompts.md).

Role required: admin

## About this task

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the lower corner of your browser. You can also select the Sparkle icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the application banner.\[Omitted image "sn-studio-access-build-agent.png"\] Alt text: If Build Agent isn't open, open it from the status bar in the corner of your browser.

2.  In the chat panel, describe the application that you want to create in plain language or select a prompt.

<table id="choicetable_qzh_hj2_lgc"><thead><tr><th align="left" id="d178421e223">

Scenario

</th><th align="left" id="d178421e226">

Actions

</th></tr></thead><tbody><tr><td id="d178421e232">

**Describe the app you want to create**

</td><td>

Describe the application that you want to create, and then select the Send icon\[Omitted image "ba-send-icon.png"\] Alt text:. For example:\[Omitted image "build-agent-describe-app.png"\] Alt text: Describe the application in a chat panel

You can also attach images, such as architectural diagrams or UI wireframes, to provide context for prompts.

</td></tr><tr><td id="d178421e253">

**Select a predetermined prompt**

</td><td>

1.  Select **Create an app** from the Application list. \[Omitted image "ba-create-app-1.png"\] Alt text: Welcome to Build Agent message
2.  Describe the application that you want to create, including as much context as possible, and then select the Send icon \[Omitted image "ba-send-icon.png"\]. For example, include roles, data requirements, and success criteria.


</td></tr></tbody>
</table>    After reviewing your requirements, Build Agent requests confirmation to proceed with creating the application.

3.  Instruct Build Agent to start developing the application by selecting **Approve plan**.

    Or, if you're not satisfied with the plan, tell Build Agent what you change, and continue to prompt until you have a plan you like.

    \[Omitted image "ba-create-app-2.png"\] Alt text: Implementation plan for Planner Tracker application

    Build Agent can access ServiceNow knowledge sources and tools, which enable it to learn, analyze, and then create applications.

    After creating the application, Build Agent builds the application.

    **Note:** You can preview the code files before approval. But to see the actual metadata output, you must build and install the application on the instance.

4.  If your application has a user interface, you can preview the app in a tab in ServiceNow Studio to inspect how it looks.

    You can keep prompting to refine the app, its appearance, and functionality. For more information, see [Edit an existing application using Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/edit-an-existing-application-using-build-agent.md).


## Result

Review the application and its metadata in ServiceNow Studio using the change log. For more information, see [Build Agent conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-conversational-change-log.md). You can also review the application using the File Navigator in ServiceNow Studio. For more information, see [Find an app or app file using the Navigator panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/qs-find-app-app-file-using-navigator-panel.md).

\[Omitted image "ba-create-app-4.png"\] Alt text: App details panel showing the Planner Tracker application metadata organized in a hierarchical tree structure

When you're ready, deploy the app. For more information, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md).

For information on troubleshooting issues, see [Common issues and solutions in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-troubleshooting.md).

After the application is built, Build Agent displays a success message. For example:

\[Omitted image "build-agent-success.png"\] Alt text: Build Agent success message

Build Agent displays the details of your app in the chat panel.

\[Omitted image "ba-create-app-3.png"\] Alt text: Planner Tracker application build summary

You can prompt Build Agent for details on how to access your new app.

\[Omitted image "ba-access-app.png"\] Alt text: Response with multiple methods to access the Planner Tracker app

If you want to view source code, open the ServiceNow IDE and select the **File Explorer** view from the Activity bar. The ServiceNow Fluent application code and other source code in the `src` directory appears.

\[Omitted image "build-agent-file-explorer.png"\] Alt text: File Explorer showing project structure with folders and configuration files

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

