---
title: Create a map page module
description: You can create a new application module for desktop or smartphone users to display a Google map page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a map page module

You can create a new application module for desktop or smartphone users to display a Google map page.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Modules** and click **New**.

2.  Select the appropriate application for the module.

    For example, if you are planning to display critical incidents, add a module to the Incident application menu.

3.  Point to the application menu you want to add the module to and click the edit application \(pencil\) icon.

4.  Select the **Link Type** tab and select the type of link you want for the module.

    For example, you can create a module that opens a map page directly, or one that links through a URL.

5.  Complete the form, as appropriate.

<table id="table_el5_rj5_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Enter a name for the module in the application navigator.

</td></tr><tr><td>

Order

</td><td>

Enter a number to define the sequence this condition should be evaluated if more than one matching condition exists. The order is evaluated from the lowest value to the highest value.

</td></tr><tr><td>

Application menu

</td><td>

Select the application menu where you want this module to appear. By default, this field displays the application menu that you opened to create the module.

</td></tr><tr><td>

Hint

</td><td>

Enter a brief description to display when a user points to the module name in the application navigator.

</td></tr><tr><td>

Active

</td><td>

Select the check box to activate this module. Only active modules appear in the application menu.

</td></tr><tr><td>

Image

</td><td>

Select an icon to display with this module in the application navigator. If this field is blank, a default icon is used.

</td></tr><tr><td>

Link type

</td><td>

Select the desired link type from the list. This selection changes the available fields in the form.

</td></tr><tr><td>

Map page

</td><td>

Select the pre-configured map page to use for this module. For example, **Critical Incidents**.

</td></tr><tr><td>

Roles

</td><td>

Select the roles that are permitted to access this module. If this field is blank, all roles can access the module.

</td></tr><tr><td>

Arguments

</td><td>

Define the URL for this module in the format `map_page.do?sysparm_name=<map page name>`. This field is available when the **Link type** is **URL \(from Arguments\)**.**Note:** If the map page title has a space in it, replace the space with `%20` for the correct syntax. For example, a map page called Critical Incidents becomes `Critical%20Incidents%20` in a URL.

</td></tr></tbody>
</table>6.  Click **Submit**.


**Parent Topic:**[Map pages](../concept/c_MapPages.md)

**Related topics**  


[Set up Google Maps API](set-up-google-maps-api.md)

[Create a map page](t_CreateAMapPage.md)

[Create an advanced Map Page](create-advanced-map-page.md)

[Set map application scope](set-map-application-scope.md)

[Create a smartphone map page module](t_CreateASmartphoneMapPageModule.md)

[Scripting for map pages](../reference/scripting-for-map-pages.md)

