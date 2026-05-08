---
title: Changing the table for an app
description: Admins can change the associated table for an app built in Creator Studio. That is, you can change the table that the app saves its requests to.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [An app's table, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Changing the table for an app

Admins can change the associated table for an app built in Creator Studio. That is, you can change the table that the app saves its requests to.

View the current table for the app by selecting the **Data management** tab in the App settings. For more information, see [Edit an app's settings in Creator Studio](../task/creator-studio-edit-app-settings.md).

**Note:** There are two ways to change an app's associated table:

-   You can use Guided Setup, which is an easier, more streamlined process. For more information, see [Configure the table for Creator Studio apps](../task/config-creator-studio-guided-setup.md#).
-   You can update several tables on the ServiceNow AI Platform. For more information, see [Change a Creator Studio app's table](../task/creator-studio-change-app-table.md).

## Reasons to change the table for an app

Some reasons that you may want to change the table for an app include:

-   You have an existing table that has business logic or handling of specific fields, you can have the app write to that table to use the existing logic.
-   You can't extensively modify the Request App table, so you may want to make more complex modifications and use a different table.
-   You want to use a table that inherits components from a federated app.
-   You already have a large federated application and want to put data from the new Creator Studio into that federated app table.

## Requirements for changing the table for an app

The app must already be created before you can change the table for it.

A general guideline is to use a table that extends the Request Task table.

-   If you change an app's table to one that doesn't extend a Request Task-extended table, it could affect automations.
-   If the new table doesn't have the **request\_type** field, the app's automations won't be correctly triggered.

    **Note:** You can change the **Request type** field, which specifies the form, on the Request Task table or a table that extends Request Task. To do so, you must be an admin or have the sn\_creatorstudio.configuration\_admin or sn\_creatorstudio.task\_admin role.

-   The request\_type field for the new table should have the label **Request type**, and it should be a reference to the Record Producer table.
-   If the new table isn’t in the same scope as the app, the scope of the table must allow updates from other scopes.

For more information on the Task table, see Working with the Task table.

## Role for changing the table for an app

To change the associated table for an app, you must have either the admin role, the sn\_creatorstudio.app\_configurator role, or sn\_creatorstudio.configuration\_admin, which are granular admin roles. For more information, see Granular admin roles.

## Repercussions of changing an app's table

The following table describes how different parts of building an app in Creator Studio are affected by changing the app's table.

<table id="table_l5g_w31_s2c"><thead><tr><th>

Part of building an app

</th><th>

Effect

</th></tr></thead><tbody><tr><td>

Forms

</td><td>

If you change the table for an app after a form is created, users get an error when they view a form that was created against a table that's different from the app's current table. In that case, you should change the table back to the original table, or users should create new forms that use the new table.

</td></tr><tr><td>

Automations

</td><td>

If you change the table to one without the **request\_type** field, users can't add a playbook to the app.

</td></tr><tr><td>

Workspace list configurations

</td><td>

If you change the table after a user created a filtered list, the filtered list retains the original table.If multiple filtered lists use different tables, users will get errors based on those discrepancies. For example, they can't manage columns for a table that they don't have edit access to.

</td></tr></tbody>
</table>**Parent Topic:**[Administering an app's associated table](creator-studio-admin-app-table.md)

