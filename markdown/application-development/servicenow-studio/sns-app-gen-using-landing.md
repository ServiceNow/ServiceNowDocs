---
title: Generate apps with Now Assist for app generation within ServiceNow Studio
description: Have a conversation with the Now Assist for app generation to start building applications.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Generate apps with Now Assist for app generation within ServiceNow Studio

Have a conversation with the Now Assist for app generation to start building applications.

This video shows you how to perform the following procedure.

Generate application with Now Assist for app gen and ServiceNow Studio. 

## Before you begin

To use app generation, you must activate the skill in Now Assist for Creator. For more information, see [Install Now Assist for app generation in ServiceNow Studio](sns-app-gen-install.md).

Role required: a now.assist.creator role and the now\_assist\_panel\_user role

**Note:** If you have users that only need to edit \(not create\) apps, they can be assigned the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles.

## About this task

When app generation is enabled on an instance, the Now Assist icon \(![Now Assist icon.](../../../common/image/icon-ai-sparkle.png)\) appears on the home page banner.

## Procedure

1.  Open the Now Assist panel by navigating to **App Engine** &gt; **ServiceNow Studio** and selecting the Now Assist icon.

    ![Now Assist highlighted in banner.](../images/app-generation-task-initiation-xsr2.png)

2.  In the Now Assist panel, select **Create an app**.

    Now Assist asks you to describe your application.

3.  Summarize your current business process.

    Describe your application's use case so that Now Assist understands the purpose of your application. You can be highly detailed if you have a clear idea of what you want. If you don't, start with a broad description. Now Assist narrows down your application's requirements.

    ![Initial stage in which Now Assist asks user for the purpose of the application.](../images/app-generation-task-initiation.png)

4.  Continue the conversation with Now Assist by providing details about how you want the app to work.

    Now Assist asks you questions to understand the data to be collected, the users involved and their permissions, and the desired interface. Your answers help Now Assist create the correct tables, roles, access control lists \(ACLs\), forms, and record producers for your application.

    If you know exactly how you want your app to work, be specific about its functionality. If you don't, interact with Now Assist to determine the correct application requirements. For more information, see [General guidelines for using Now Assist for app generation in ServiceNow Studio](../concept/sns-app-gen-guidelines.md).

    ![Conversation stage showing the back-and-forth conversation between the user and Now Assist in refining the application requirements.](../images/app-generation-task-conversation.png)

    Beginning in the Yokohama Patch 3 \(May 2025\) release, you can ask Now Assist to create a workspace \(user interface\) and flow \(automation\) for your application. For more information, see [Add a workspace to a custom application with Now Assist for app generation](sns-app-gen-add-workspace.md) and [Add a flow to a custom application with Now Assist for app generation](sns-app-gen-add-flow.md).

5.  Preview, finalize, and then generate the app.

    1.  If necessary, select **Make changes** to continue editing.

        ![Options to preview app, make changes, or discard the app with make changes option highlighted.](../images/app-generation-task-make-changes-ys2.png)

        Continue to interact with Now Assist until the summary it produces matches your application's requirements.

    2.  After you're satisfied with the application requirements, select **Preview app**.

        ![Options to preview app, make changes, or discard the app with preview option highlighted.](../images/app-generation-preview-button-ys2.png)

        The preview opens and displays a list of app files. Filter the app files list and narrow the search as needed. Select any of the app files to view details. For example, select a role to see if it grants users create, read, write, or delete permissions. If your app contains a record producer, select it to see what the form and fields look like. As you continue previewing and requesting updates with Now Assist, changes such as adding a new role are listed as the preview pane loads.

        ![ServiceNow Studio app preview page.](../images/app-generation-preview-in-progress-ys2.png)

        **Note:** Because workspaces and flows rely on tables, these application features are generated after tables and when you save the application.

        ![ServiceNow Studio app preview files list with not generated yet section highlighted.](../images/app-generation-preview-not-generated-ys2.png)

        **Note:** If the Now Assist panel is covering information, select the Now Assist icon ![](../../app-engine-studio/image/now-assist-sparkle-icon-dark.png) to close the panel. Select the icon again to open the panel and continue the conversation.

        When you're finished previewing, select an option:

        ![Now Assist panel showing the options to take after previewing.](../images/app-generation-preview-after-choices.png)

        -   **Save and open app** generates the app and opens it in ServiceNow Studio for you to review and edit as needed. If you included workspaces \(user interface\) or flows \(automation\) in your application, their metadata is generated when you save the application.
        -   **Make changes** enables you to continue the conversation with Now Assist to refine and edit the app. After Now Assist makes any changes you request, the app preview is also updated.
        -   **Discard and start over** deletes the current app and resets the conversation in the Now Assist panel.
        For more information about ServiceNow Studio, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).


## Result

Use the tools in ServiceNow Studio to add more features and enhance your app further. For more information, see [Create an application in ServiceNow Studio](../../servicenow-studio/task/create-an-application-in-servicenow-studio.md) and [Create an app file in ServiceNow Studio](../../servicenow-studio/task/sn-studio-create-app-file.md).

-   **[Add a workspace to a custom application with Now Assist for app generation](sns-app-gen-add-workspace.md)**  
Use Now Assist for app generation to add a workspace to a custom application.
-   **[Add a flow to a custom application with Now Assist for app generation](sns-app-gen-add-flow.md)**  
Use Now Assist for app generation to add a flow to a custom application.
-   **[Review and edit applications using Now Assist for app generation in ServiceNow Studio](sns-app-gen-review-apps.md)**  
Use Now Assist for app generation to review and modify applications in the ServiceNow Studio development environment.

**Parent Topic:**[Now Assist for app generation in ServiceNow Studio](../concept/sns-now-assist-app-gen-landing.md)

