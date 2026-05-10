---
title: Create an application in ServiceNow Studio
description: Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.Add files to your application right after you create it in ServiceNow Studio.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an application in ServiceNow Studio

Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.

## Before you begin

As of the version 27.1.2, both admins and users with Guided Application Creator \(GAC\) roles can create apps in ServiceNow Studio. To create a custom global app, the GAC user must have the Global role.

Role required: adminor Guided Application Creator roles

## About this task

You can create apps using the following procedure, or you can use Build Agent to get a head start creating your app. For more information about using a conversational interface to create an app, see [Build Agent in ServiceNow Studio](../concept/build-agent-in-servicenow-studio.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon ![create icon](../image/sn-studio-add-icon.png) next to the Navigator panel or the **Create** button.

    ![There are two create buttons, one on either side of the screen. Select either Create button to start developing an app.](../image/sn-studio-create-button-zs1.png)

3.  Select **App** from the options that appear.

4.  Choose how to create your app from the available options.

    ![Begin creating your app on your own, using Now Assist, or using Creator Studio. You can also explore the app gallery to find inspiration from completed applications.](../image/sn-studio-create-app-as2.png)

    **Note:** If you need some inspiration for your app, select **Explore the App Gallery**. After signing in with your ServiceNow credentials, you have access to a library of apps and app files that can help you create your application.

<table id="choicetable_tgq_ryl_m3c"><thead><tr><th align="left" id="d296548e200">

How to create

</th><th align="left" id="d296548e203">

Description

</th></tr></thead><tbody><tr><td id="d296548e209">

**On your own**

</td><td>

Create the application on your own, adding content and files of your choosing.Select **On your own** &gt; **Continue**, and continue with step 5 in this procedure.

</td></tr><tr><td id="d296548e229">

**With Now Assist, which opens Build Agent**

</td><td>

Begin a conversation with Build Agent to create your application.Select **With Now Assist** &gt; **Start a chat**. The Build Agent chat panel opens, where you can select **Create an application** or begin describing what you want to build.

For more information, see [Create an application using Build Agent](../../build-agent/tasks/create-a-new-application-using-build-agent.md).

</td></tr><tr><td id="d296548e280">

**With Creator Studio**

</td><td>

Use Creator Studio to create a simple request and fulfill application.Select **With Creator Studio** &gt; **Continue in Creator Studio** to begin creating your application.

For more information, see [Building apps with Creator Studio](../../creator-studio/concept/building-apps-with-creator-studio.md).

</td></tr></tbody>
</table>5.  Enter the basic information for the app on the form.

    ![Enter basic app details](../image/sn-studio-create-scoped-app.png "Create an app basic details")

    1.  Enter a **Name** and **Description** for your application.

    2.  Add a logo by either dragging the image to the **Browse or drag to upload** field or selecting the field, selecting the image from your file directory, and selecting **Open**.

    3.  Specify the **Scope**.

        -   **Scoped** means that the app doesn't interact with any other data on the instance. By default, the app can access and change its own tables and business logic, but other apps can't unless you give them explicit permission.
        -   **Global** means that all tables and business logic on the instance can interact with the app.
        For more information about working with scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

    4.  Select **Continue**.

6.  Define user access to the app by adding roles.

    ServiceNow Studio automatically defines default admin and user roles. You can remove the predefined roles or add more roles. For more information about roles, see [Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-roles.md).

    1.  Select **Add a role**.

    2.  Enter the **Role name** and **Description**.

    3.  Repeat this process for as many roles as you need to add.

    4.  Select **Continue**.

    **Note:** You must have at least one role in the application to be able to continue making updates.

    ![Define roles for the app](../image/sn-studio-add-roles.png "Roles create user access to the app")

7.  Continue building your app by creating a new file or viewing the app details page.

    -   Select **Create file** to begin adding files to your application right away.
    -   Select **View app details** to go to the app details page for your new app.

## What to do next

Add content such as application files, dependencies, and cross-scope privileges to your new application.

**Parent Topic:**[Working with applications in ServiceNow Studio](../concept/working-with-apps-in-servicenow-studio.md)

## Add a file to your app in ServiceNow Studio

Add files to your application right after you create it in ServiceNow Studio.

### Before you begin

Role required: admin or delegated\_developer

### About this task

This procedure details how to add files to an app right after creating it. For more information on how to create files from anywhere else in ServiceNow Studio, see [Create an app file in ServiceNow Studio](sn-studio-create-app-file.md).

### Procedure

1.  On the app creation confirmation page, select **Create file**.

    ![Create a file directly after creating your application.](../image/sn-studio-create-file-from-app.png)

2.  Search for and select the type of file you'd like to create.

    **Note:** The types of available files you see depends on your permissions. If you're expecting to see a certain file type but don't see it, contact your administrator.

    For more information about each available file type and category, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md).

3.  Select **Continue**.

4.  Fill in the form with the details for the new app file.

    The form fields vary depending on the type of file you created.

5.  Select **Submit**.


