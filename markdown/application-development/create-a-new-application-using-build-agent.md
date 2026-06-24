---
title: Create an application using Build Agent
description: Use Build Agent to develop a new ServiceNow application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/create-a-new-application-using-build-agent.html
release: yokohama
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 3
breadcrumb: [Use, Build Agent, Use AI capabilities in custom applications, Developing your application, Building applications]
---

# Create an application using Build Agent

Use Build Agent to develop a new ServiceNow application.

## Before you begin

Install and enable the Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/install-build-agent.md).

Create a workspace. For more information, see [Create a workspace in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-ide-family-release/create-workspace-servicenow-ide.md).

Build Agent requires ServiceNow SDK version 4.0 at a minimum. If you’re using an older version, Build Agent prompts you to upgrade to ServiceNow SDK 4.0.

**Note:** Build Agent currently doesn't support the Global scope or global applications.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

    The Build Agent panel is open by default.

    \[Omitted image "build-agent-welcome.png"\] Alt text: Build Agent panel is open by default on ServiceNow IDE

    **Tip:** If the Build Agent panel isn’t open, select **Open Build Agent** from the status bar at the bottom-right corner to launch the Build Agent.

2.  In the chat panel, describe the application that you want to create in plain English.

<table id="choicetable_qzh_hj2_lgc"><thead><tr><th align="left" id="d191865e142">

Scenario

</th><th align="left" id="d191865e145">

Actions

</th></tr></thead><tbody><tr><td id="d191865e151">

**First-time use of Build Agent**

</td><td>

Describe the application that you want to create, and then select **Send**. For example:\[Omitted image "build-agent-describe-app.png"\] Alt text: Describe the application in chat input.

You can also attach images, such as architectural diagrams or UI wireframes, to provide context for prompts.

</td></tr><tr><td id="d191865e172">

**Creating another app using Build Agent**

</td><td>

1.  If you have already created applications using Build Agent and want to create another app, select **Create a new app** from the Application list.

\[Omitted image "build-agent-create-second.png"\] Alt text: Welcome to Build Agent message

2.  Describe the application that you want to create, and then select **Send**.

</td></tr></tbody>
</table>    After reviewing your requirements, the Build Agent requests your confirmation to proceed with creating the application.

3.  Instruct the Build Agent to start developing the application by selecting **Approve**.

    \[Omitted image "build-agent-approve-create.png"\] Alt text: Approve the application creation.

    The Build Agent can access ServiceNow knowledge sources and tools, which enable it to learn, analyze, and then create applications.

    After creating the application, the Build Agent builds the application and then asks for your confirmation to deploy it.

    **Note:** You can preview the code files before approval. But to see the actual metadata output, you must build and install the application on the instance.

4.  Instruct the Build Agent to deploy the application by selecting **Approve**.

    **Note:** Even though this process is standard, be sure to follow the on-screen instructions, because the Build Agent functions interactively.

    \[Omitted image "build-agent-approve-build.png"\] Alt text: Approve to build and deploy the application.


## Result

After the application is built and installed, the Build Agent displays a success message. For example:

\[Omitted image "build-agent-success.png"\] Alt text: Build Agent success message

From the Activity Bar, select the **File Explorer** view \(\[Omitted image "servicenow-ide-file-explorer-icon.png"\] Alt text: File Explorer\) to see the ServiceNow Fluent application code and other source code in the `src` directory. For example:

\[Omitted image "build-agent-file-explorer.png"\] Alt text: File Explorer

From the Activity Bar, select the **Metadata Explorer** view \(\[Omitted image "servicenow-ide-metadata-explorer-icon.png"\] Alt text: Metadata Explorer\) to see the application metadata on the instance. For example:

\[Omitted image "build-agent-metadata-explorer.png"\] Alt text: Metadata Explorer

|Issues|Description|Solution|
|------|-----------|--------|
|Build not deployed|The Build Agent only deploys the latest successful build. If your updates aren’t available after deployment, it may indicate that the build failed, even though the deployment was successful.|Check the build status and note any error messages. Paste those error messages into the chat panel and ask the Build Agent to resolve the build issues and redeploy the application.|
|Empty UI page|When working on complex UI pages, the Build Agent may occasionally display an empty page.|Open the browser console, copy the error messages, and paste them into the chat panel. Then, ask the Build Agent to fix the UI page. The Build Agent assists you in both creating and debugging your applications.|
|Context limit exceeded|If something goes wrong while creating or updating your application, you have the option to retry. The Build Agent maintains a history of your session and can resume from the point of failure. However, if your chat window exceeds the context limit, you receive a 'Context Window Exceeded' error.|Open a new chat window and describe the application you want to create once again. Although the Build Agent doesn’t retain the context from the previous chat session, it reviews the work already done and continues from where it stopped.|
|Rate limit error|Another error you might encounter is the 'Rate limit error', which happens when the LLM provider receives too many requests to handle.|Wait for a minute or two before trying again.|

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/use-build-agent.md)

