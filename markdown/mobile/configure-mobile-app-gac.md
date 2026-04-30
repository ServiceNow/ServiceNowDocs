---
title: Create a mobile application using Guided Application Creator
description: Use the Guided Application Creator in Studio to create a base scoped application and mobile app components. These components can be used in any of the ServiceNow mobile apps.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile app building tools, Building mobile apps, Mobile Platform]
---

# Create a mobile application using Guided Application Creator

Use the Guided Application Creator in Studio to create a base scoped application and mobile app components. These components can be used in any of the ServiceNow mobile apps.

## Before you begin

Role required: admin

## About this task

Studio is a development environment where your application developers can work on custom applications in one centralized location. Much of the configuration for mobile apps in this section take place in Studio \(**System Applications** &gt; **Studio**\). For more information about Studio, see [Legacy - ServiceNow Studio](https://www.servicenow.com/docs/access?context=c_ServiceNowStudio&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **System Applications** &gt; **Studio**.

2.  In Studio, click **Create Application** or select an existing application from the list.

    The application that you create here is a new scoped application which will contain your app. Scoped applications help restrict data and application files to just this one application. For more information on scoped applications, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

    You can also access the Guided Application Creator outside Studio by navigating to **System Applications** &gt; **My Company Applications**, and then click **Create new**.

    Studio opens a Guided Application Creator window where you create your application.

3.  If you are launching Guided Application Creator for the first time, click **Let's get started** on the welcome screen.

4.  Follow the steps on the screen to create a name, description, and logo for your application, and then click **Create**.

5.  In the **Roles** field, select the roles to associate with your app.

    Users with the selected roles can access your application. If you have selected no roles, users with any role will have access to the application.

6.  Click **Create new role** to create a new role to associate to the application.

7.  Click **Continue** when you are finished defining roles for your application.

8.  Select **Mobile** as the format for this application, and then click **Continue**.

9.  Select or create tables that you want to use in your mobile app.

    The Guided Application Creator can create list screens for these tables. If you create new screens later, you will not be limited to the tables you select here.

10. Click **Done with Tables** when you are finished adding tables to your application.

11. Click the **Start** button to create screens for your selected tables using the Guided Application Creator.

    If you do not want to create screens at this point, you can click **X** in the upper right corner of the window to close the Guided Application Creator and return to Studio.

12. Fill in the fields in the Guided Application Creator form as needed:

    |Field|Description|
    |-----|-----------|
    |Name|Name for the app. The launcher screen created in this process will use this name.|
    |Description|Description for the app.|
    |Tables|Tables for which Guided Application Creator will create screens.|
    |Roles|Roles for your screens. Users with the selected roles can access the created screens.|

13. Click **Create**.

    The Guided Application Creator will create a list and form for each of the selected table, including **New**, **Edit**, and **Delete** functions for each table.

14. Click the **Done with apps** button, and then the **Done** button to return to Studio


## Result

You now have a new application that you can access in Studio.

## What to do next

Create apps to add functionality to your mobile app using Guided Application Creator, or close Guided Application Creator and create apps using Studio.

To create mobile apps, use [Mobile App Builder](../concept/mab-concept.md).

