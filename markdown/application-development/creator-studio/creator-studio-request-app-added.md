---
title: Ask an admin to create an app for you in Creator Studio
description: Don't have permission to build an app? Ask your admin to get you started by creating a basic app for you. Just give them a name and tell them what you want the app to do. Once they start it, you’ll take over and modify it.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [App creation, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Ask an admin to create an app for you in Creator Studio

Don't have permission to build an app? Ask your admin to get you started by creating a basic app for you. Just give them a name and tell them what you want the app to do. Once they start it, you’ll take over and modify it.

## Before you begin

To request an app to be created for you, the admin needs to assign you the role of sn\_creatorstudio.restricted\_user.

## About this task

When you ask an admin to create an app for you, you automatically become the owner of it. For more information, see [Collaborating with others to build apps in Creator Studio](../reference/creator-studio-collaboration-roles.md).

Here’s how to ask an admin to create an app for you.

## Procedure

1.  Let's open Creator Studio. On your instance, select the **All** tab.

    ![Interface showing All, Favorites, and History tabs with a Filter field.](../image/cs-all-menu.png "All tab")

    This tab lets you see all the apps installed on your instance.

2.  In the white text field, enter `App Engine`.

    The list of apps displayed underneath the text box now pertains only to App Engine.

3.  In the list, select **Creator Studio**.

    That's how you open Creator Studio! You've landed on its home page. Under **Apps**, you see all the apps that people already created.

4.  Select **Create app** to get started with your request.

5.  Fill in the fields on the modal that pops up.

    1.  Give your app a **Name**, which should be descriptive and intuitive.

    2.  Describe what your app will do in the **Description**.

        For example, `App to request office equipment`

    3.  Enter any additional comments that you want the admin to know when approving your request.

    ![Request an admin to create your app for you](../image/cs-request-app-creation.png "Request to have an app created")

6.  Select the **Submit request** button.


## Result

After you ask your admin to create the app, they'll review and approve the request. They might need more details about the app from you. You'll get an email notification once they approve and create it. At that point, you’re the owner of the app. You can find your app in Creator Studio and start building out the app's forms, automation, and workspace category.

To learn all the things you can do as the app owner when building the app, see [Application collaboration](../../applications/concept/application-collaboration.md).

**For admins:**

-   Every app built in Creator Studio adds a record in the Request App Config table. The table’s name follows the format of scope\_request, for example, x\_snc\_02\_03\_request.However, your admin can change the table for an app after you create it. For more details, check out [Administering an app's associated table](../concept/creator-studio-admin-app-table.md).
-   You’ll review and approve app requests in the Application Tasks table of the Request App Administration app.

**Parent Topic:**[App creation in Creator Studio](../concept/creator-studio-creating-apps.md)

