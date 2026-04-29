---
title: Set up notifications in workspace utility settings
description: Set up the advanced notification and search settings in your workspace experience so that you can control how your users see notifications and search options.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure UI Builder workspace experiences, Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Set up notifications in workspace utility settings

Set up the advanced notification and search settings in your workspace experience so that you can control how your users see notifications and search options.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Set up the advanced notification and search settings in your workspace experience. You can turn notifications on or off to control how people see notifications in your workspace experience.

![Workspace experience utility settings.](../image/experience-utilities-settings.png "Workplace experience settings")

You can also control whether the search functionality is visible to the users of your workspace experience. If you choose to display a search option, you can define what search results are returned by choosing a source for the search.

Before you can edit the experience settings, you must be in the correct application scope. If you're in a different scope, the experience settings are read-only. To change your application scope, go to the main header, select the application picker \(![Application picker.](../image/application-picker.png)\), and then select the application scope that you want. For more information about the application scope, see [Learn about security and roles](security-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Open or create a page in your workspace experience.

4.  Select **Experience settings** in the upper-right.

    ![Arrow pointing to the Experience settings link on the experience view page.](../image/experience-settings-navigation.png)

5.  Scroll down to **Notifications**.

    ![Notifications settings for workspace experiences.](../image/uib-settings-notification.png)

6.  Select the **Turn on notifications** option.

7.  Click **Save**.

8.  Click **Advanced settings** to go to the ServiceNow AI Platform® and edit the JSON values of the record.

    **Note:** If you have the Record component on a page, you can have a record open in the workspace experience when a notification is selected. Follow the instructions in [Record UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/record/uib-setup) on the ServiceNow developer site and define a featureRoutes page property.


**Parent Topic:**[Configure UI Builder workspace experiences](../concept/ui-builder-workspace-settings.md)

