---
title: Create a smartphone map page module
description: You can create a custom smartphone module that links directly to a map page.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a smartphone map page module

You can create a custom smartphone module that links directly to a map page.

## Before you begin

Role required: admin

## Procedure

1.  Obtain the sys\_id of the map page.

    The sys\_id is required when you create the module.

2.  Navigate to **System Mobile UI** &gt; **Navigator Apps**.

3.  Open the application menu where you want the new module to appear.

4.  In the **Modules** related list, click **New**.

5.  Complete the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the module.|
    |Order|Enter a number to specify the order of the module within the application menu. For example, an entry of `100` would place this module before one with an **Order** entry of `200`.|
    |Application menu|Select the application menu where you want this module to appear. By default, this field displays the application menu that you opened to create the module.|
    |Table|Do not select a table.|
    |Updated|Displays the date and time when the module record is updated.|
    |Roles|Select the roles that are permitted to access this module. If this field is blank, all roles can access the module.|
    |Active|Select the check box to activate this module. Only active modules appear in the application menu.|
    |Filter|Do not add a filter condition.|
    |Path|Enter `map/` followed by the sys\_id of the map page. For example: `map/c86c5feac0a80a6600706f0102968196`|

6.  Click **Submit**.


**Parent Topic:**[Map pages](../concept/c_MapPages.md)

**Related topics**  


[Set up Google Maps API](set-up-google-maps-api.md)

[Create a map page](t_CreateAMapPage.md)

[Create a map page module](create-map-page-module.md)

[Create an advanced Map Page](create-advanced-map-page.md)

[Set map application scope](set-map-application-scope.md)

[Scripting for map pages](../reference/scripting-for-map-pages.md)

