---
title: Create an application in ServiceNow Studio
description: Create a custom application in ServiceNow Studio, then add data, automation, or other app files using integrated development tools and builders.Add a file to your application immediately after creating it in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 5
breadcrumb: [Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an application in ServiceNow Studio

Create a custom application in ServiceNow Studio, then add data, automation, or other app files using integrated development tools and builders.

## Before you begin

As of version 27.1.2, both admins and users with Guided Application Creator \(GAC\) roles can create apps in ServiceNow Studio. To create a custom global app, the GAC user must have the Global role.

Role required: adminor Guided Application Creator roles

## About this task

Use the following steps to create an app manually, or use Build Agent to create your app through conversational interaction. For more information, see [Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-agent-in-servicenow-studio.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon \[Omitted image "sn-studio-add-icon.png"\] Alt text: create icon next to the Navigator panel or the **Create** button.

    \[Omitted image "sn-studio-create-button-zs1.png"\] Alt text: There are two create buttons, one on either side of the screen. Select either Create button to start developing an app.

3.  Select **App** from the options that appear.

4.  Select how to create your app from the available options.

    \[Omitted image "sn-studio-create-app-as2.png"\] Alt text: Create your app independently, using Now Assist, or using Creator Studio. Select Explore the App Gallery to browse completed applications for reference.

    **Note:** To browse completed apps for reference, select **Explore the App Gallery**. After signing in with your ServiceNow credentials, you can access a library of apps and app files.

<table id="choicetable_tgq_ryl_m3c"><thead><tr><th align="left" id="d156920e193">

How to create

</th><th align="left" id="d156920e196">

Description

</th></tr></thead><tbody><tr><td id="d156920e202">

**On your own**

</td><td>

Create the application independently, adding content and files of your choosing.Select **On your own** &gt; **Continue** and continue with step 5 in this procedure.

</td></tr><tr><td id="d156920e222">

**With Now Assist, which opens Build Agent**

</td><td>

Begin a conversation with Build Agent to create your application.Select **With Now Assist** &gt; **Start a chat**. The Build Agent chat panel opens. Select **Create an application** or describe what you want to build.

For more information, see [Create an application using Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/create-a-new-application-using-build-agent.md).

</td></tr><tr><td id="d156920e273">

**With Creator Studio**

</td><td>

Use Creator Studio to create a simple request and fulfill application.Select **With Creator Studio** &gt; **Continue in Creator Studio** to begin creating your application.

For more information, see [Building apps with Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/building-apps-with-creator-studio.md).

</td></tr></tbody>
</table>5.  Enter the basic information for the app.

    \[Omitted image "sn-studio-create-scoped-app.png"\] Alt text: Enter basic app details including name, description, logo, and scope.

    1.  Enter a **Name** and **Description** for the application.

    2.  Add a logo by dragging an image to the **Browse or drag to upload** field, or select the field, choose the image from your file directory, and select **Open**.

    3.  Specify the **Scope**.

        -   **Scoped**: The app does not interact with other data on the instance by default. The app can access and change its own tables and business logic, but other apps cannot unless you grant them explicit permission.
        -   **Global**: All tables and business logic on the instance can interact with the app.
        For more information about working with scopes, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/c_ApplicationScope.md).

    4.  Select **Continue**.

6.  Define user access to the app by adding roles.

    ServiceNow Studio automatically defines default admin and user roles. Remove the predefined roles or add more roles as needed. For more information about roles, see [Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-roles.md).

    1.  Select **Add a role**.

    2.  Enter the **Role name** and **Description**.

    3.  Repeat for each additional role you need to add.

    4.  Select **Continue**.

    **Note:** At least one role is required to continue making updates to the application.

    \[Omitted image "sn-studio-add-roles.png"\] Alt text: Define roles to control user access to the app.

7.  Continue building your app by creating a file or viewing the App details page.

    -   Select **Create file** to add files to your application immediately.
    -   Select **View app details** to open the App details page for your new app.
    Your new application is created and ready to develop further.


## What to do next

Add application files, dependencies, and cross-scope privileges to your new application.

**Parent Topic:**[Applications in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-apps-in-servicenow-studio.md)

## Add a file to your app in ServiceNow Studio

Add a file to your application immediately after creating it in ServiceNow Studio.

### Before you begin

Role required: admin or delegated\_developer

### About this task

Use this procedure to add files immediately after creating an app. To create files from anywhere else in ServiceNow Studio, see [Create an app file in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-create-app-file.md).

### Procedure

1.  On the app creation confirmation page, select **Create file**.

    \[Omitted image "sn-studio-create-file-from-app.png"\] Alt text: Create a file directly after creating your application.

2.  Search for and select the file type you want to create.

    **Note:** Available file types depend on your permissions. If you do not see a file type you expect, contact your administrator.

    For more information about each available file type and category, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md).

3.  Select **Continue**.

4.  Enter the details for the new app file in the form.

    The form fields vary depending on the file type.

5.  Select **Submit**.

    The new file is created and associated with your application.


