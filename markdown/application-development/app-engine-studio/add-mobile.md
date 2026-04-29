---
title: Add a mobile experience
description: Add a mobile experience, or interface, to enable users to access your application from a ServiceNow native mobile app.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Add an experience, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a mobile experience

Add a mobile experience, or interface, to enable users to access your application from a ServiceNow native mobile app.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

When you add a mobile experience, you're creating a basic version of the mobile app, which you must then continue editing in Mobile App Builder before it's ready to deploy.

Use Mobile App Builder to build and manage screens and records that make up workflows within the mobile apps that you build with AES. For example, you can add a webpage or a list that appears as a tab on a phone app.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Experience, select **Add**.

4.  Select **Mobile experience**, and then select **Get started**.

5.  Select the kind of mobile experience that you want to add and select **Continue.**

    -   Mobile Agent
    -   Now Mobile
    For more information about the mobile experience options and important considerations when choosing a mobile experience, see [Design considerations for mobile apps](https://www.servicenow.com/docs/access?context=mobile-design-consideration&version=australia&pubname=australia-mobile&ft:locale=en-US).

6.  On the form, fill in the fields.

<table id="table_t2b_lcv_jsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add an icon

</td><td>

Icon that best reflects the content of the screen.

</td></tr><tr><td>

Label for experience

</td><td>

Description for the screen.

</td></tr><tr><td>

Roles

</td><td>

Roles that have access to the screen. You can specify multiple roles, but you must select them one at a time from the list that appears when you start typing in the **Roles** field.**Note:** If you do not specify a role, all users will have access to the mobile experience.

</td></tr><tr><td>

Available offline

</td><td>

Option to make the experience available offline. **Note:** Offline experiences are available only in Mobile Agent apps.

</td></tr></tbody>
</table>7.  Select **Continue**.

8.  Select the type of screen to add and select **Continue**.

<table id="table_xdz_vb1_vsb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List

</td><td>

Screen that lists information retrieved from an existing data table, which you choose in the next step. **Note:** Creating a List screen adds all of the data table's values to the mobile experience.

</td></tr><tr><td>

Webpage

</td><td>

Screen that displays an existing webpage, which you specify the URL for in the next step.

</td></tr></tbody>
</table>9.  To add a list page to the mobile experience, do the following:

    1.  Select the table that will appear as a list on the screen.

        After you select a data table, some of its contents appear on the page.

    2.  To make the table conditional, select **Set conditions for this table** and define the conditions that must be met for the data to appear using the condition builder.

        For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    3.  Select **Continue**.

    4.  Specify attributes for the data extracted from the table and select **Continue**.

        |Field|Description|
        |-----|-----------|
        |Add an icon|Icon that reflects the data in the table.|
        |Screen label|Brief label to describe the list screen.|

10. To add a webpage to the mobile experience, do the following:

    1.  Specify the attributes for the table data and select **Continue**.

        |Field|Description|
        |-----|-----------|
        |Add an icon|Icon that reflects webpage.|
        |Screen label|Brief label to describe the webpage.|
        |URL|Absolute or relative URL for the webpage.|

11. Depending on if you are done or not, do one of the following:

    -   If you are done adding screens to the mobile experience, select **Done adding screens**.
    -   To add more screens to the mobile experience, select **Add more screens**.
12. To finish creating the mobile experience, select **Done**.

    After you create the mobile experience in AES, you must edit it in Mobile App Builder.

13. Next to the mobile experience you created, select the menu icon \(![Menu icon](../image/menu-icon-purple.png)\) and then select **Edit**.

14. Edit the mobile experience in Mobile App Builder.

    For more information, see [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=australia&pubname=australia-mobile&ft:locale=en-US).


## What to do next

Scan or copy the QR code for your mobile experience using the **Select app** and **Select platform** fields.

![Scan QR code for the mobile experience.](../image/mobile-experience-qr-code.jpg)

For more information on modifying mobile experiences, see [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=australia&pubname=australia-mobile&ft:locale=en-US).

-   **[Sample mobile experience](../concept/mobile-experiences-examples.md)**  
A mobile experience enables users to access your application from a ServiceNow native mobile app.

**Parent Topic:**[Add an application experience](../concept/add-experience.md)

