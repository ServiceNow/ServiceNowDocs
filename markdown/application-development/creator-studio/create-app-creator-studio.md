---
title: Create an app in Creator Studio
description: Get started creating an app by specifying basic info for the app that you're building in Creator Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/creator-studio/create-app-creator-studio.html
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [App creation, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Create an app in Creator Studio

Get started creating an app by specifying basic info for the app that you're building in Creator Studio.

## Before you begin

If you don't have permission to create an app, you can request that a teammate create one for you. For more information, see [Ask an admin to create an app for you in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-request-app-added.md).

You can also watch a short video on how to create an app.

Video on how to create an app 

Your administrator must add you to the Creator Studio Users group.

## Procedure

1.  Let's open Creator Studio. On your instance, select the **All** tab.

    \[Omitted image "cs-all-menu.png"\] Alt text: Interface showing All, Favorites, and History tabs with a Filter field.

    This tab lets you see all the apps installed on your instance.

2.  In the white text field, enter `Creator Studio`.

    The list of apps you see underneath the text box now pertains only to App Engine.

3.  In the list, select **Creator Studio**.

    That's how you open Creator Studio! You've landed on its home page. Under **Apps**, you see all the apps that people already created.

4.  Select **Create app** to begin your journey.

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-request-app-added.md).
5.  Select the type of app you want to build, such as **Service Desk**.

    Service Desk apps enable users to submit requests, report issues, and access support related to services within your company.

    **Note:** Your admin may have hidden this page.

    \[Omitted image "crs-interstitial-sd.png"\] Alt text: Within the Creator Studio interface, select the "Service Desk" app option. This type of app is designed to streamline the management of incoming requests or support tickets.

6.  Select the **Continue** button.

7.  Fill in the fields on the Create app page that appears.

    \[Omitted image "crs-create-app-ys2.png"\] Alt text: Enter details to create the app

    1.  Give your app a **Name**, which should be descriptive and intuitive.

    2.  Describe what your app does in the **Description**.

        For example, `This app enables a person to request office equipment.`

    3.  Select **Advanced settings** and confirm that your app's name and tables are unique by specifying the **Scope**.

        For more advanced information about scopes, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_ApplicationScope.md).

    4.  Select **Create app**.


## Result

**Congrats:** Hooray, you've created your app! Next, we will use a template to add a form that people will use to fill out requests in your app. Check out [Add a form to an app in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-add-form.md) for how to do that.

To learn all the things you can do as the app owner when building the app, see [Application collaboration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/application-collaboration.md).

For sys admin eyes only: Every app built in Creator Studio adds a record in the Request App Config table, which contains the table that the app uses. Your admin can change the table for an app, see [Administering an app's associated table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-admin-app-table.md) for more information. The name of the table follows the format of scope\_request, for example, x\_snc\_02\_03\_request.

**Parent Topic:**[App creation in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-creating-apps.md)

