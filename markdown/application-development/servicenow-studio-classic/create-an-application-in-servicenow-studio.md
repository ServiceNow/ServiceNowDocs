---
title: Create an application in ServiceNow Studio
description: Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.html
release: yokohama
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Create an application in ServiceNow Studio

Create a custom application in ServiceNow Studio. After creating the foundations of your app, you can add data, automation, or many other types of app files using integrated development tools and builders in ServiceNow Studio.

## Before you begin

As of the February 2025 release, both admins and users with Guided Application Creator \(GAC\) roles can create apps in ServiceNow Studio. To create a custom global app, the GAC user must have the Global role.

Role required: adminor Guided Application Creator roles

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the Create icon \(\[Omitted image "sn-studio-add-icon.png"\] Alt text: create icon\) next to the Navigator panel or the **Create** button.

    \[Omitted image "sn-studio-create-button-ys2.png"\] Alt text: There are two create buttons, one on either side of the screen. Click either Create button to start developing an app.

3.  Select **App** from the options that appear.

4.  Enter the basic information for the app on the form.

    \[Omitted image "sn-studio-create-scoped-app.png"\] Alt text: Enter basic app details

    1.  Enter a **Name** and **Description** for your application.

    2.  Add a logo by either dragging the image to the **Browse or drag to upload** field or selecting the field, selecting the image from your file directory, and selecting **Open**.

    3.  Specify the **Scope**.

        -   **Scoped** means that the app doesn't interact with any other data on the instance. By default, the app can access and change its own tables and business logic, but other apps can't unless you give them explicit permission.
        -   **Global** means that all tables and business logic on the instance can interact with the app.
        For more information about working with scopes, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/c_ApplicationScope.md).

    4.  Select **Continue**.

5.  Define user access to the app by adding roles.

    ServiceNow Studio automatically defines default admin and user roles. You can remove the predefined roles or add more roles. For more information about roles, see [Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/user-administration/ua-creating-roles.md).

    1.  Select **Add a role**.

    2.  Enter the **Role name** and **Description**.

    3.  Repeat this process for as many roles that you need to add.

    4.  Select **Continue**.

    \[Omitted image "sn-studio-add-roles.png"\] Alt text: Define roles for the app

6.  Select one of the following options.

    -   Select **Create file** to begin adding files to your application right away.
    -   Select **View app details** to go to the app details page for your new app.

## Result

Now that your app is created, you can add other content, such as application files, dependencies, and cross-scope privileges. For more information, see [Create an app file in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/sn-studio-create-app-file.md), [Working with metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md), and [Access integrated development tools and builders in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/open-and-switch-between-integrated-development-tools.md).

**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/using-servicenow-studio.md)

