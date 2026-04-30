---
title: Create an application in ServiceNow Studio
description: Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automations, or many other types of app files using integrated development tools and builders in ServiceNow Studio.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Create an application in ServiceNow Studio

Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automations, or many other types of app files using integrated development tools and builders in ServiceNow Studio.

## Before you begin

Only admins can create an app in ServiceNow Studio. If you need an app created for you, contact your admin.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the Create icon \(![create icon](../image/sn-studio-add-icon.png)\) next to the Navigator panel or the **Create** button.

    ![Create an app using either the Navigator icon or the Create button](../image/sn-studio-create-app.png "Select either Create button")

3.  Select **App** from the options that appear.

4.  Enter the basic information for the app on the form.

    ![Enter basic app details](../image/sn-studio-create-scoped-app.png "Create an app basic details")

    1.  Enter a **Name** and **Description** for your application.

    2.  Add a logo by either dragging the image to the **Browse or drag to upload** field or selecting the field, selecting the image from your file directory, and selecting **Open**.

    3.  Specify the **Scope**.

        -   **Scoped** means that the app doesn't interact with any other data on the instance. By default, the app can access and change its own tables and business logic, but other apps can't unless you give them explicit permission.
        -   **Global** means that all tables and business logic on the instance can interact with the app.
        For more information about working with scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

    4.  Select **Continue**.

5.  Define user access to the app by adding roles.

    ServiceNow Studio automatically defines default admin and user roles. You can remove the pre-defined roles or add more roles. For more information about roles, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    1.  Select **Add a role**.

    2.  Enter the **Role name** and **Description**.

    3.  Repeat this process for as many roles that you need to add.

    4.  Select **Continue**.

    ![Define roles for the app](../image/sn-studio-add-roles.png "Roles create user access to the app")

6.  Open the app dashboard when ServiceNow Studio is done creating the foundation of the app by selecting **Go to app dashboard**.


## Result

The app dashboard opens within ServiceNow Studio. From there, you can add other content, such as application files, dependencies, and cross-scope privileges. For more information, see [Create an app file in ServiceNow Studio](sn-studio-create-app-file.md), [Working with metadata app file categories in the ServiceNow Studio Navigator](../concept/sn-studio-working-with-metadata.md), and [Access integrated development tools and builders in ServiceNow Studio](../concept/open-and-switch-between-integrated-development-tools.md).

**Parent Topic:**[Using ServiceNow Studio](../concept/using-servicenow-studio.md)

