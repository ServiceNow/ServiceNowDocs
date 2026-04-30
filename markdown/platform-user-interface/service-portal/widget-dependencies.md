---
title: Create a widget dependency
description: In Service Portal, you can link JavaScript and CSS files to widgets to create dependencies between widgets and third-party libraries, external style sheets, and angular modules.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a widget dependency

In Service Portal, you can link JavaScript and CSS files to widgets to create dependencies between widgets and third-party libraries, external style sheets, and angular modules.

## Before you begin

Role required: sp\_admin or admin

## About this task

Dependencies are loaded asynchronously from the server when needed.

Widgets can have as many or as few dependencies as needed. However, the more you add, the more content a widget must download to render on the page. Keep dependencies as small as possible for more efficient load times.

## Procedure

1.  Create a dependency package.

    A dependency package is a collection of JavaScript and CSS files that can be connected to a widget.

    1.  Navigate to **Service Portal** &gt; **Dependencies**.

    2.  In the dependency record, define the following fields.

        |Field|Description|
        |-----|-----------|
        |Name|The name of your dependency. \(Useful for selecting a dependency from a dropdown list.\)|
        |Application|Application scope for the dependency record.|
        |Include on page load|Select if you want your dependency to be loaded onto the page on the initial page load of Service Portal, or leave unchecked to load the dependency only when the linked widget is loaded onto a page.|
        |Angular module name|Optional. Define the value if the linked JavaScript is an Angular module. Provide the name of the Angular module being loaded, so that it can be injected into the Service Portal Angular application.|

2.  Add files to the dependency package.

    After you save the information for your dependency package, use the related lists to add JS and CSS Include files. For each related list, include the following information:

<table id="table_sjx_vgl_3w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the script include.

</td></tr><tr><td>

Source

</td><td>

Depending on whether you add a JS Include or a CSS Include, select one of these options from the list:-   URL
-   UI script \(for a JS Include\) or Style Sheet \(for a CSS Include\)
 For a JS Include, use the UI Script field to reference a UI Script found in **System UI** &gt; **UI Scripts**.

 For the CSS Include, use the Style Sheet field to reference a record in the `sp_css` table.

</td></tr></tbody>
</table>3.  Add a dependency package to a widget.

    After you have created a dependency package and added files, create a relationship between the dependency and a widget.

    1.  Navigate to **Service Portal** &gt; **Widgets** and find the widget record you want to add the dependency to.

    2.  From the Dependencies related list, click **Edit**.

    3.  In the slushbucket, find the dependency you created and double-click to add it to the selected items column on the right.

    4.  Save the page to return to the widget record.


-   **[Include a font icon in a single widget](include-widget-icon.md)**  
If you only want one widget to have access to a font icon, include the font icon in a single widget.
-   **[Include font icons as a widget dependency](font-icons-dependency.md)**  
You can include font icons wherever a widget is loaded by including them as a widget dependency.

**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

