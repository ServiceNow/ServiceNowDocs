---
title: Accessing Table Builder
description: You can access Table Builder in several ways.
locale: en-US
release: xanadu
product: Form Builder
classification: form-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Accessing Table Builder

You can access Table Builder in several ways.

## Launching Table Builder from App Engine Studio

Table Builder can be currently accessed from within App Engine Studio.

See [Editing data in App Engine Studio](../../../build/app-engine-studio/concept/edit-data.md) for instructions on editing application data.

1.  Open an application in App Engine Studio.

    **Note:** A data table must first be present in the application so that you can access Table Builder.

2.  From the application home, select the menu icon \(![Menu icon.](../../../build/app-engine-studio/image/menu-icon.png)\) next to a table, and then select **Edit**.

    Table Builder opens with the **Data** tab selected as shown in the following example.

    **Note:** To edit form views for the selected data table, navigate to the **Forms** tab.

    ![Data tab.](../image/tables-tab.png "Data tab")


## Launching Table Builder from UI Builder

Table Builder can be accessed from within UI Builder by clicking **Edit form view** at the bottom of the Config panel, for a selected form object.

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**, and then select a form component on a page.

    See [Work with components in UI Builder](../../ui-builder/concept/work-components.md) for more information on adding components.

2.  Click **Edit form view** at the bottom of the Configuration pane.

    Table Builder opens with the **Forms** tab selected, where you can customize your form views for the selected table. To edit table data, navigate to the **Data** tab as shown in the following example.

    ![Forms tab.](../image/fb-home.png "Forms tab")


## Table Builder permissions

To use Table Builder, you must either be an administrator, or have the following role permissions in ServiceNow AI Platform, or have relevant AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

<table id="table_opn_xkl_lsb"><thead><tr><th>

Permission

</th><th>

Access

</th></tr></thead><tbody><tr><td>

Personalize Form

 \(personalize\_form\)

</td><td>

-   Required to access **Forms** tab.
-   Required to customize fields on the form.
-   Does not grant dictionary access.
-   Does not grant Policies and Rules access.
-   Does not grant Tables access.

</td></tr><tr><td>

Personalize Dictionary

 \(personalize\_dictionary\)

</td><td>

-   Required to access **Data** tab.
-   Required to access field configuration.
-   Required to change dictionary fields.
-   Does not grant Policies and Rules access.

</td></tr><tr><td>

Personalize Rules

 \(personalize\_rules\)

</td><td>

Enables access to the **Policies and Rules** tab.

</td></tr><tr><td>

Personalize Choice

 \(personalize\_choices\)

</td><td>

Allows a user to configure choices for a field.

</td></tr><tr><td>

Flow Designer

 \(flow\_designer\)

</td><td>

Required to access the **Flows** tab.

 Allows a user to configure flows. To work with Table Builder flows, you must also have personalize\_form and personalize\_dictionary permissions \(or related delegated developer permissions\).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Table Builder](exploring-fb.md)

