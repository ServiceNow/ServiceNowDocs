---
title: Customize segment button colors in the segmented control area
description: Customize the color of segment buttons to help users identify a tapped segment button. For example, use a darker color to indicate that it is a selected button.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using dynamic segments to display data, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Customize segment button colors in the segmented control area

Customize the color of segment buttons to help users identify a tapped segment button. For example, use a darker color to indicate that it is a selected button.

## Before you begin

Role required: admin

## Procedure

1.  Access the Card Template form.

    1.  In the web-based UI, enter `sys_sg_form_screen.list` in the filter navigator.

    2.  Select the record screen that contains the dynamic screen segment you want to configure.

    3.  Select the **Record Screen Segments** tab and select the information icon \(![Information icon.](../image/gac-info-icon.png)\) next to the embedded screen that contains a dynamic record screen segment.

    4.  Select **Open Record** from the menu.

    5.  From the **Dynamic segment list stream** field, select the information icon \(![Information icon.](../image/gac-info-icon.png)\) and select **Open Record**.

    6.  Select the List Stream M2M Item Configuration to use for the dynamic section.

    7.  In the **Card** field of the List Item Configuration form, select the information icon \(![Information icon.](../image/gac-info-icon.png)\) and select **Open Record**.

2.  In the Card Template form, select the menu icon \(![Menu icon.](../image/context-menu-icon.png)\) and select **Configure** &gt; **Form Layout**.

3.  In the Configuring Card Template form, select **Root-view attribute JSON** and move it to the selected area.

    The **Root-view attribute JSON** displays in the Card Template form.

4.  Select **Save**.

5.  Define the appearance of a tapped segment in the segmented control by pasting the following JSON code in the **Root-view attribute JSON** field of the Card Template form.

    ```
    {
    "OnSelect":
       {
         "BackgroundColor" : "Primary",
         "TextColor": "#FFFFFF"
       }
    }
    ```

6.  If the standard primary, secondary, or destructive values do not fit your color scheme, modify the default values for the background color and text color by providing hexadecimal color values.

7.  Right-click in the header and select **Save**,


