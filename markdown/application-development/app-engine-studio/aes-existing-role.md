---
title: Use an existing role for your application
description: Use a previously created role for your application in App Engine Studio \(AES\).
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add application security, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Use an existing role for your application

Use a previously created role for your application in App Engine Studio \(AES\).

## Before you begin

Your application must contain either data or experiences in order to add an existing role. For more information about adding data or experiences to your application, see the following guidance:

-   [Create a data model for your application](../concept/add-data.md)
-   [Add an application experience](../concept/add-experience.md)

Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer

## About this task

App Engine Studio includes default roles that you can use for your application. For more information on the default roles, see [Base system roles](https://www.servicenow.com/docs/access?context=r_BaseSystemRoles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Security, select the add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Use an existing role**, and then select **Continue**.

    **Important:** If your application doesn't contain data or experiences, the **Use an existing role** option will appear, but you cannot select it.

    ![Option to use an existing role](../image/use-existing-role-purple.png "Option to use an existing role")

5.  Select the search field and then select a role from the list.

6.  Select **Edit**.

    A new tab opens to set access controls for the existing role.

7.  In the Experience section, select the experiences that users with the role can access.

8.  In the Data section, set access controls for each available table.

    -   **Create**

        Users with the role can create new records on the data table.

    -   **Read**

        Users with the role can read the data that is stored in the table.

    -   **Write**

        Users with the role can update existing records in the table.

    -   **Delete**

        Users with the role can delete table records.

9.  Select **Save**.


**Parent Topic:**[Add application security](../concept/add-security.md)

