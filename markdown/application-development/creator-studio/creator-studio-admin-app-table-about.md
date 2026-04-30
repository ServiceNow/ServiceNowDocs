---
title: Changing the table for an app
description: Admins can change the underlying table for an app built in Creator Studio. That is, you can change the table that the app saves its requests to.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Administering an app's underlying table, Administering Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Changing the table for an app

Admins can change the underlying table for an app built in Creator Studio. That is, you can change the table that the app saves its requests to.

View the current table for the app by selecting the **Data management** tab in the App settings. For more information, see [Edit an app's settings in Creator Studio](../task/creator-studio-edit-app-settings.md).

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
-   The request\_type field for the new table should have the label **Request type**, and it should be a reference to the Record Producer table.
-   If the new table isn’t in the same scope as the app, the scope of the table must allow updates from other scopes.

For more information on the Task table, see [Working with the Task table](https://www.servicenow.com/docs/access?context=c_TaskTable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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
</table>**Parent Topic:**[Administering an app's underlying table](creator-studio-admin-app-table.md)

