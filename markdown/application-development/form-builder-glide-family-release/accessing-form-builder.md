---
title: Accessing Table Builder
description: You can access Table Builder in several ways.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Accessing Table Builder

You can access Table Builder in several ways.

## Launching Table Builder using naming shortcuts

You can use naming shortcuts to open tables from the app navigator.

Enter `tablename.builder`, `tablename.view`, `tablename.sheet`, or `tablename.flow` in the search to access the table directly. For example, searching `incident.builder` in the search opens field view of the incident table in the Data tab.

![naming shortcut navigation screen](../image/tb-shortcut-example.png)

|User Input|Behavior|
|----------|--------|
|&lt;tablename&gt;.builder|Opens the table in the Table Builder with the **Field** option selected in **Data** tab.|
|&lt;tablename&gt;.view|Opens table in Table Builder in the **Form** tab.|
|&lt;tablename&gt;.sheet|Opens a table in Table Builder with the **Sheet** option selected in **Data** tab.|
|&lt;tablename&gt;.flow|Opens a table in Table Builder in the **Flow** tab.|

## Launching Table Builder from the App Navigator

Table Builder is accessible through the application navigator. This feature helps you to interact with Table Builder more efficiently.

1.  Navigate to **All** &gt; **Table Builder**.
2.  Search for the table that you want to open.
3.  Select **Open**.

    ![Access table from the App navigator](../image/tb-accessfrmnavigator.png)


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

Table Builder can be accessed from within UI Builder by selecting **Edit form view** at the bottom of the Config panel, for a selected form object.

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**, and then select a form component on a page.

    See [Work with components in UI Builder](../../ui-builder/concept/work-components.md) for more information on adding components.

2.  Select **Edit form view** at the bottom of the Configuration pane.

    Table Builder opens with the **Forms** tab selected, where you can customize your form views for the selected table. To edit table data, navigate to the **Data** tab as shown in the following example.

    ![Forms tab.](../image/fb-home.png "Forms tab")


## Table Builder permissions

To use Table Builder, you must either:

-   be an administrator, or
-   have the following role permissions in ServiceNow AI Platform, or
-   have the relevant AES user role and delegated developer permissions.

For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

**Note:** When creating a table, assign at least one role with **Read** permission. Setting read permission helps you to preview and access the table.

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
-   Doesn’t grant dictionary access.
-   Doesn’t grant Policies and Rules access.
-   Doesn’t grant Tables access.

</td></tr><tr><td>

Personalize Dictionary

 \(personalize\_dictionary\)

</td><td>

-   Required to access **Data** tab.
-   Required to access field configuration.
-   Required to change dictionary fields.
-   Doesn’t grant Policies and Rules access.

</td></tr><tr><td>

Personalize Rules

 \(personalize\_rules\)

</td><td>

Enables access to the **Policies and Rules** tab.

</td></tr><tr><td>

Personalize Choice

 \(personalize\_choices\)

</td><td>

Enables you to configure choices for a field.

</td></tr><tr><td>

Flow Designer

 \(flow\_designer\)

</td><td>

Required to access the **Flows** tab.

 Enables you to configure flows. To work with Table Builder flows, you must also have personalize\_form and personalize\_dictionary permissions \(or related delegated developer permissions\).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Table Builder](exploring-fb.md)

