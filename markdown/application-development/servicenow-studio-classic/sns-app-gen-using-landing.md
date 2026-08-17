---
title: Generate apps in ServiceNow Studio
description: Use the app generation skill to build an application in ServiceNow Studio by describing your business process in a conversation with ServiceNow Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-app-gen-using-landing.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 4
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [App generation, AI tools and files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Generate apps in ServiceNow Studio

Use the app generation skill to build an application in ServiceNow Studio by describing your business process in a conversation with ServiceNow Otto®.

## Before you begin

To use app generation, enable the skill in the AI Admin Hub. For more information, see [Turn on the app generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-app-gen-install.md).

Role required: now\_assist\_panel\_user

**Note:** To edit \(not create\) apps, assign users the delegated\_developer or now\_assist\_panel\_user role.

## About this task

When the app generation skill is turned on, the ServiceNow Otto® icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist icon.\) appears on the home page banner.

## Procedure

1.  Open the ServiceNow Otto® panel by navigating to **App Engine** &gt; **ServiceNow Studio** and selecting the ServiceNow Otto® icon.

    \[Omitted image "app-generation-task-initiation-xsr2.png"\] Alt text: ServiceNow Otto icon highlighted in banner.

2.  In the ServiceNow Otto® panel, select **Create an app**.

    ServiceNow Otto® asks you to describe your application.

3.  Describe your current business process.

    Include your application's use case so that ServiceNow Otto® understands the purpose of your application. Provide detailed requirements if you have them, or start with a broad description so that ServiceNow Otto® can help narrow down your application's requirements.

4.  Provide details about how you want the app to work.

    ServiceNow Otto® asks questions to understand the data to be collected, the users involved and their permissions, and the desired interface. Your answers help ServiceNow Otto® create the correct tables, roles, access control lists \(ACLs\), forms, and record producers for your application. You can also ask ServiceNow Otto® to create a workspace \(user interface\) and flow \(automation\) for your application.

    If you know exactly how you want your app to work, be specific about its functionality. If you do not, describe what you know and collaborate with ServiceNow Otto® to determine the correct application requirements. For more information, see [General guidelines for using app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-app-gen-guidelines.md).

5.  Preview, finalize, and then generate the app.

    1.  If necessary, select **Make changes** to continue editing.

        \[Omitted image "app-generation-task-make-changes-ys2.png"\] Alt text: Options to preview app, make changes, or discard the app with make changes option highlighted.

        Continue the conversation with ServiceNow Otto® until the summary matches your application's requirements.

    2.  When the application requirements are accurate, select **Preview app**.

        \[Omitted image "app-generation-preview-button-ys2.png"\] Alt text: Options to preview app, make changes, or discard the app with preview option highlighted.

        The preview opens and displays a list of app files. Filter the app files list and narrow the search as needed. Select any app file to view details. For example, select a role to see if it grants users create, read, write, or delete permissions. If your app contains a record producer, select it to see the form and fields. As you continue previewing and requesting updates with ServiceNow Otto®, changes such as adding a new role appear as the preview pane loads.

        **Note:** Workspaces and flows depend on tables, so these application features are generated after tables and when you save the application.

        \[Omitted image "app-generation-preview-not-generated-ys2.png"\] Alt text: ServiceNow Studio app preview files list with not generated yet section highlighted.

        **Note:** If the ServiceNow Otto® panel is covering information, select the ServiceNow Otto® icon \[Omitted image "now-assist-sparkle-icon-dark.png"\] Alt text: to close the panel. Select the icon again to open the panel and continue the conversation.

        When you finish previewing, select an option:

        -   **Save files and open app** generates the app and opens it in ServiceNow Studio for you to review and edit. If you included workspaces \(user interface\) or flows \(automation\) in your application, their metadata is generated when you save the application.
        -   **Make changes** continues the conversation with ServiceNow Otto® so you can refine and edit the app. The app preview updates after ServiceNow Otto® applies your changes.
        -   **Discard and start over** deletes the current app and resets the conversation in the ServiceNow Otto® panel.
        For more information about ServiceNow Studio, see [ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-landing.md).


## Result

Use the tools in ServiceNow Studio to add more features and enhance your app. For more information, see [Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md) and [Create an app file in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-create-app-file.md).

-   **[Add a workspace to a custom application with app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-app-gen-add-workspace.md)**  
Add a workspace to a custom application by asking ServiceNow Otto®. Describe what you want in the workspace, or ask ServiceNow Otto® for recommendations.
-   **[Add a flow to a custom application with app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-app-gen-add-flow.md)**  
Add a flow to a custom application by asking ServiceNow Otto®. Describe what you want the flow to do, or ask ServiceNow Otto® for suggestions.
-   **[Review and edit applications built using app generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-app-gen-review-apps.md)**  
After app generation creates an application, review and modify it in ServiceNow Studio to verify accuracy and extend functionality.

**Parent Topic:**[App generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-now-assist-app-gen-landing.md)

