---
title: Create an application in ServiceNow Studio
description: Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an application in ServiceNow Studio

Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.

## Before you begin

As of the version 27.1.2, both admins and users with Guided Application Creator \(GAC\) roles can create apps in ServiceNow Studio. To create a custom global app, the GAC user must have the Global role.

Role required: adminor Guided Application Creator roles

## About this task

You can create apps using the following procedure, or you can use Now Assist tools to get a head start creating your app. For more information about using a conversational interface to create an app, see [Now Assist for app generation in ServiceNow Studio](../../now-assist-app-gen/concept/sns-now-assist-app-gen-landing.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon \(![create icon](../image/sn-studio-add-icon.png)\) next to the Navigator panel or the **Create** button.

    ![There are two create buttons, one on either side of the screen. Click either Create button to start developing an app.](../image/sn-studio-create-button-zs1.png)

3.  Select **App** from the options that appear.

4.  You can begin creating your app on your own by using Now Assist or Creator Studio.

    -   Create the application on your own, adding content and files of your choosing. If you're beginning on your own, select **On your own** &gt; **Continue**, and continue with step 5 in this procedure.
    -   Begin a chat with Now Assist, which uses AI to help you create an app based on your conversation. Select **With Now Assist** &gt; **Start a chat**, and begin the conversation to create your app.

        For more information, see [Generate apps with Now Assist for app generation within ServiceNow Studio](../../now-assist-app-gen/task/sns-app-gen-using-landing.md).

    -   Use Creator Studio to create a simple request and fulfill application, which you can then add to in ServiceNow Studio. Select **With Creator Studio** &gt; **Continue in Creator Studio**, and Creator Studio opens, where you can start working.

        For more information, see [Building apps with Creator Studio](../../creator-studio/concept/building-apps-with-creator-studio.md).

    **Note:** If you need some inspiration for your app, select **Explore the App Gallery**. After signing in with your ServiceNow credentials, you have access to a library of apps and app files that can help you create your application.

    ![Begin creating your app on your own or using some assistance. You can also explore the app gallery to find inspiration from completed applications.](../image/sn-studio-app-gallery.png)

5.  Enter the basic information for the app on the form.

    ![Enter basic app details](../image/sn-studio-create-scoped-app.png "Create an app basic details")

    1.  Enter a **Name** and **Description** for your application.

    2.  Add a logo by either dragging the image to the **Browse or drag to upload** field or selecting the field, selecting the image from your file directory, and selecting **Open**.

    3.  Specify the **Scope**.

        -   **Scoped** means that the app doesn't interact with any other data on the instance. By default, the app can access and change its own tables and business logic, but other apps can't unless you give them explicit permission.
        -   **Global** means that all tables and business logic on the instance can interact with the app.
        For more information about working with scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

    4.  Select **Continue**.

6.  Define user access to the app by adding roles.

    ServiceNow Studio automatically defines default admin and user roles. You can remove the predefined roles or add more roles. For more information about roles, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    1.  Select **Add a role**.

    2.  Enter the **Role name** and **Description**.

    3.  Repeat this process for as many roles that you need to add.

    4.  Select **Continue**.

    ![Define roles for the app](../image/sn-studio-add-roles.png "Roles create user access to the app")

7.  Continue building your app by creating a new file or viewing the app details page.

    -   Select **Create file** to begin adding files to your application right away.
    -   Select **View app details** to go to the app details page for your new app.

## Result

Now that your app is created, you can add other content, such as application files, dependencies, and cross-scope privileges. For more information, see [Create an app file in ServiceNow Studio](sn-studio-create-app-file.md), [Working with metadata app file categories in the ServiceNow Studio Navigator](../concept/sn-studio-working-with-metadata.md), and [Access integrated development tools and builders in ServiceNow Studio](../concept/open-and-switch-between-integrated-development-tools.md).

**Parent Topic:**[Working with applications in ServiceNow Studio](../concept/working-with-apps-in-servicenow-studio.md)

