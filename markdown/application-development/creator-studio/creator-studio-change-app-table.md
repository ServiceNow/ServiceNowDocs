---
title: Change a Creator Studio app's table
description: Change the table associated with an app if you want one that differs from the default.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [An app's table, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Change a Creator Studio app's table

Change the table associated with an app if you want one that differs from the default.

## Before you begin

**Note:** You should perform this task only if you did not change the table during Guided Setup. For more information, see [Configure the table for Creator Studio apps](config-creator-studio-guided-setup.md#).

The app must already be created before you can change the table for it.

Some general guidelines for changing the table are:

-   If you change an app's table to one that doesn't extend a Request Task-extended table, it could affect automations.
-   If the new table doesn't have the **request\_type** field, the app's automations won't be correctly triggered.

    **Note:** You can change the **Request type** field, which specifies the form, on the Request Task table or a table that extends Request Task. To do so, you must be an admin or have the sn\_creatorstudio.configuration\_admin or sn\_creatorstudio.task\_admin role.

-   The request\_type field for the new table should have the label **Request type**, and it should be a reference to the Record Producer table.
-   If the new table isn’t in the same scope as the app, the scope of the table must allow updates from other scopes.

See [Changing the table for an app](../concept/creator-studio-admin-app-table-about.md) for more information.

Role required: admin, app configurator \(sn\_creatorstudio.app\_configurator\), or Creator Studio configuration admin \(sn\_creatorstudio.configuration\_admin\). For more information on working with granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## About this task

To ensure that forms and automations work, a general guideline is to change the table to a table that extends the Request Task table.

## Procedure

1.  Open the **All** menu and enter `sn_creatorstudio_request_app_config.list`.

2.  Enter the app name in the search box for the **Name** column and press Enter.

    **Note:** You must enter the first word of the app name, not subsequent words in the app name.

3.  Select the app from the list.

    ![Request App Configs list filtered to show names starting with doc, displaying Doc Review 1 and Travel request app entries.](../image/crs-change-app-table1.png "List of apps to configure")

4.  Change the scope to the app's scope or a global scope if you're not in the correct scope.

    You can change the scope in one of the following ways:

    -   Selecting the **here** in the message "To edit the record click here."
    -   Selecting the application scope icon ![](../../applications/image/icon-scope-changed.png) and choosing the appropriate scope.
    For more information on scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

5.  Enter the name of the table you want the app to write to in the **Request table** field.

    The table should extend the Request Task table and have the **request\_type** field. For more details on what table you can use, see [Requirements for changing the table for an app](../concept/creator-studio-admin-app-table-about.md#crs-requirements-change-table).

    ![Request App Config form with Color field showing dropdown list of table options.](../image/crs-change-app-table2.png "List of apps to configure")

6.  Select **Update** to save your changes.


**Parent Topic:**[Administering an app's associated table](../concept/creator-studio-admin-app-table.md)

