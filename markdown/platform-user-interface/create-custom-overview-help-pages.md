---
title: Create custom overview help
description: You can edit existing overview help pages to display your own custom panels to selected users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview help pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create custom overview help

You can edit existing overview help pages to display your own custom panels to selected users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Overview Help** and edit the help page for your version.

2.  Modify the Overview Help Page form using the fields in the table.

    |Field|Description|
    |-----|-----------|
    |Title|Unique title of this page.|
    |Subtitle|General introduction for the subject of this page. This content appears as the description of the first panel that users see.|
    |Application|Scope of this help page. All overview help pages are created in the global scope, so that they are visible from anywhere in the system. This field is read-only.|

3.  Save the page.

4.  Click **New** in the **Overview Help Panel** related list and complete the form using the fields in the table.

5.  Click **Submit**.

<table id="table_jgv_4qw_hw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Unique name for this panel. This name is the title of the panel shown to users.

</td></tr><tr><td>

Page

</td><td>

Names the overview page to which this panel is connected.

</td></tr><tr><td>

Order

</td><td>

Controls the sequence of the panels in the page. When using icon buttons, the button for the lowest order number appears on the left, and the button for the highest order number appears on the right. When icon buttons are disabled, the lowest order number panel begins the scrolling sequence.

</td></tr><tr><td>

Roles

</td><td>

Names all the user roles that are entitled to see this panel.

</td></tr><tr><td>

Condition

</td><td>

Defines the conditions under which this panel is viewable. For example, you can configure this panel to display only when a specific plugin is activated.

</td></tr><tr><td>

Image

</td><td>

Background image to use when this panel is displayed. Supported image formats are:-   .jpg
-   .png
-   .bmp
-   .gif
-   .jpeg
-   .ico
-   .svg


</td></tr><tr><td>

Icon

</td><td>

Icon used as the access button for this panel from the page. This field is read-only. You cannot specify an icon for your custom panels.

</td></tr><tr><td>

Is title

</td><td>

Controls the display of the title on the initial slide. The field is not used for panels.

</td></tr><tr><td>

Show title

</td><td>

Controls the display of the title on the initial slide. This field is read-only and is not available for panels.

</td></tr><tr><td>

Text

</td><td>

Text describing what is shown in the image for this panel. This content appears below the panel title.

</td></tr></tbody>
</table>
**Parent Topic:**[Overview help pages](../concept/overview-help-pages.md)

