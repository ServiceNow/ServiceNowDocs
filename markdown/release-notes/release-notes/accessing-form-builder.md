---
title: Accessing
description: You can access in several ways.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Accessing 

You can access  in several ways.

## Launching  from the App Navigator

 is accessible through the application navigator. This feature helps you to interact with  more efficiently.

1.  Navigate to **All** &gt; **Table Builder** and search for the table that you want to open.
2.  Select **Open**. ![image.tb-accessfrmnavigator]

## Launching  from 

 can be currently accessed from within .

See Editing data in App Engine Studio for instructions on editing application data.

1.  Open an application in .

    **Note:** A data table must first be present in the application so that you can access .

2.  From the application home, select the menu icon \(![image.menu-icon]\) next to a table, and then select **Edit**.

     opens with the **Data** tab selected as shown in the following example.

    **Note:** To edit form views for the selected data table, navigate to the **Forms** tab.

    ![image.tables-tab]


## Launching  from 

 can be accessed from within  by selecting **Edit form view** at the bottom of the Config panel, for a selected form object.

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**, and then select a form component on a page.

    See Work with components in UI Builder for more information on adding components.

2.  Select **Edit form view** at the bottom of the Configuration pane.

     opens with the **Forms** tab selected, where you can customize your form views for the selected table. To edit table data, navigate to the **Data** tab as shown in the following example.

    ![image.fb-home]


##  permissions

To use , you must either be an administrator, or have the following role permissions in , or have relevant  user role and delegated developer permissions. For more information, see .

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

 Enables you to configure flows. To work with  flows, you must also have personalize\_form and personalize\_dictionary permissions \(or related delegated developer permissions\).

</td></tr></tbody>
</table>