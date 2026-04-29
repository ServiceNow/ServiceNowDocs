---
title: Create an experience for UI Builder
description: Learn how to create a workspace or portal experience for UI Builder in the ServiceNow platform.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create an experience for UI Builder

Learn how to create a workspace or portal experience for UI Builder in the ServiceNow platform.

## Before you begin

Role required: ui\_builder\_admin

## About this task

This task shows you a basic example of how to create a workspace or portal experience for UI Builder. This example creates an experience called Demo Experience to demonstrate the process.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Create** from the UI Builder home page.

    ![UI Builder home page with the Create experience button.](../image/UIB-create-experience-button.png)

3.  Select **Experience**.

4.  In the form, fill in the fields.

    ![Create an experience form.](../image/create-experience.png "Create an experience dialog box")

5.  |Field|Description|
|-----|-----------|
|Name|Add a name to track your experience internally. The experience name is visible to users from the browser tab. For this example, it is `MyApp`.|
|App Shell UI|You must choose an app shell for the experience to work. For example, you could choose a workspace or portal app shell. The app shell is the wrapper of the page contents, which is similar to the functionality of a web page. The app shell can show things like the logo of your company, user preferences, the search icon. For more information, see [Define UI experiences using app shells](../concept/app-shells-uibuilder.md).|
|URL path|Add a path for your experience. The path appends to the end of the URL parameter of your experience. For example, if you used `MyApp` as the title for your experience, you could type `my/app` for the path.|
|Landing path|The landing path is the prefix that people use to reach your experience homepage. To designate a page as the homepage, you must create a page that has a matching path.|
|Roles|Only users with these assigned roles can access the experience. If you leave this field empty, the experience is open to all logged-in users by default.|

6.  Select **Create** to create your experience.

7.  Select **Open experience** to view the main page for your experience.

    ![Main page for your new experience](../image/experience-main-page.png "Main page for your new experience")

    **Note:** In addition to the name of your new experience, the screen includes the URL, application scope, admin panel, and the roles of users who can view the experience. Any pages or variants you create for the experience appear in the **Pages** section.


## What to do next

Now that you have created an experience you can add and customize pages. For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

**Parent Topic:**[Configure how users interact with your applications in UI Builder](../concept/work-experiences.md)

