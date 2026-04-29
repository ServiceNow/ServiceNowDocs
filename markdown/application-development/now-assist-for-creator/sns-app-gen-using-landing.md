---
title: Generate apps in ServiceNow Studio
description: Use the app generation skill to build an application in ServiceNow Studio by describing your business process in a conversation with Now Assist.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [App generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate apps in ServiceNow Studio

Use the app generation skill to build an application in ServiceNow Studio by describing your business process in a conversation with Now Assist.

This video shows you how to perform the following procedure.

Generate application with the Now Assist for Creator app generation skill in ServiceNow Studio. 

## Before you begin

To use app generation, enable the skill in the Now Assist Admin console. For more information, see [Turn on the app generation skill](sns-app-gen-install.md).

Role required: now\_assist\_panel\_user

**Note:** To edit \(not create\) apps, assign users the delegated\_developer or now\_assist\_panel\_user role.

## About this task

When the app generation skill is turned on, the Now Assist icon \(![Now Assist icon.](../../../common/image/icon-ai-sparkle.png)\) appears on the home page banner.

## Procedure

1.  Open the Now Assist panel by navigating to **App Engine** &gt; **ServiceNow Studio** and selecting the Now Assist icon.

    ![Now Assist highlighted in banner.](../images/app-generation-task-initiation-xsr2.png)

2.  In the Now Assist panel, select **Create an app**.

    Now Assist asks you to describe your application.

3.  Describe your current business process.

    Include your application's use case so that Now Assist understands the purpose of your application. Provide detailed requirements if you have them, or start with a broad description so that Now Assist can help narrow down your application's requirements.

    ![Initial stage in which Now Assist asks user for the purpose of the application.](../images/app-generation-task-initiation.png)

4.  Provide details about how you want the app to work.

    Now Assist asks questions to understand the data to be collected, the users involved and their permissions, and the desired interface. Your answers help Now Assist create the correct tables, roles, access control lists \(ACLs\), forms, and record producers for your application. You can also ask Now Assist to create a workspace \(user interface\) and flow \(automation\) for your application.

    If you know exactly how you want your app to work, be specific about its functionality. If you do not, describe what you know and collaborate with Now Assist to determine the correct application requirements. For more information, see [General guidelines for using app generation](../concept/sns-app-gen-guidelines.md).

    ![Conversation stage showing the back-and-forth conversation between the user and Now Assist in refining the application requirements.](../images/app-generation-task-conversation.png)

5.  Preview, finalize, and then generate the app.

    1.  If necessary, select **Make changes** to continue editing.

        ![Options to preview app, make changes, or discard the app with make changes option highlighted.](../images/app-generation-task-make-changes-ys2.png)

        Continue the conversation with Now Assist until the summary matches your application's requirements.

    2.  When the application requirements are accurate, select **Preview app**.

        ![Options to preview app, make changes, or discard the app with preview option highlighted.](../images/app-generation-preview-button-ys2.png)

        The preview opens and displays a list of app files. Filter the app files list and narrow the search as needed. Select any app file to view details. For example, select a role to see if it grants users create, read, write, or delete permissions. If your app contains a record producer, select it to see the form and fields. As you continue previewing and requesting updates with Now Assist, changes such as adding a new role appear as the preview pane loads.

        ![ServiceNow Studio app preview page.](../images/app-generation-preview-in-progress-ys2.png)

        **Note:** Workspaces and flows depend on tables, so these application features are generated after tables and when you save the application.

        ![ServiceNow Studio app preview files list with not generated yet section highlighted.](../images/app-generation-preview-not-generated-ys2.png)

        **Note:** If the Now Assist panel is covering information, select the Now Assist icon ![](../../app-engine-studio/image/now-assist-sparkle-icon-dark.png) to close the panel. Select the icon again to open the panel and continue the conversation.

        When you finish previewing, select an option:

        ![Now Assist panel showing the options to take after previewing.](../images/app-generation-preview-after-choices.png)

        -   **Save files and open app** generates the app and opens it in ServiceNow Studio for you to review and edit. If you included workspaces \(user interface\) or flows \(automation\) in your application, their metadata is generated when you save the application.
        -   **Make changes** continues the conversation with Now Assist so you can refine and edit the app. The app preview updates after Now Assist applies your changes.
        -   **Discard and start over** deletes the current app and resets the conversation in the Now Assist panel.
        For more information about ServiceNow Studio, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).


## Result

Use the tools in ServiceNow Studio to add more features and enhance your app. For more information, see [Create an application in ServiceNow Studio](../../servicenow-studio/task/create-an-application-in-servicenow-studio.md#) and [Create an app file in ServiceNow Studio](../../servicenow-studio/task/sn-studio-create-app-file.md).

-   **[Add a workspace to a custom application with app generation](sns-app-gen-add-workspace.md)**  
Add a workspace to a custom application by asking Now Assist. Describe what you want in the workspace, or ask Now Assist for recommendations.
-   **[Add a flow to a custom application with app generation](sns-app-gen-add-flow.md)**  
Add a flow to a custom application by asking Now Assist. Describe what you want the flow to do, or ask Now Assist for suggestions.
-   **[Review and edit applications built using app generation](sns-app-gen-review-apps.md)**  
After app generation creates an application, review and modify it in ServiceNow Studio to verify accuracy and extend functionality.

**Parent Topic:**[App generation](../concept/sns-now-assist-app-gen-landing.md)

