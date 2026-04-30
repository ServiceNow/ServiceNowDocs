---
title: Adding images to an icon section
description: Upload images or icon-style images to use within your icon sections. Use personalized images to brand your mobile application. This feature is configured in the web-based UI as opposed to the Mobile App Builder.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure an icon UI section, Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Adding images to an icon section

Upload images or icon-style images to use within your icon sections. Use personalized images to brand your mobile application. This feature is configured in the web-based UI as opposed to the Mobile App Builder.

## Before you begin

Role required: admin

## Procedure

1.  Upload an image to the Icon images table and access the sys\_id of the image.

    1.  Navigate to **All**.

    2.  In the filter navigator, enter `sys_sg_icon_image.list`, to open a list of icon images.

    3.  Select **New**.

    4.  Enter a name for your image.

    5.  Select **Click to add** to browse and select an image to upload.

        **Note:** The optimal ratio for images is 1:1.24. Consider a fixed frame size of 74 pixels for the height and 92 pixels for the width.

    6.  Select **Update**.

        Your image is added to the Icon images table.

    7.  Right-click on the element name and select **Copy sys\_id**.

2.  Create an image-type icon from the image you selected.

    1.  Navigate to **All**.

    2.  In the filter navigator, enter `sys_sg_icon.list`, to open the Icons table.

    3.  Select **New**.

    4.  Enter a name for your icon of type image.

    5.  In the **Icon Name** field, enter the attribute name `ImageRef`.

    6.  Right-click in the **Icon Value** field and paste the sys\_id of the element name you selected.

    7.  Select **Image** in the **Type** field.

    8.  Select **Submit**.

3.  Map the defined image to an icon section.

    1.  Navigate to **All**.

    2.  In the filter navigator, enter `sys_sg_navigation_section_destination.list`, to open the Icon section destinations table.

    3.  Do one of the following.

        -   Select a displayed icon section destination from the list.
        -   Select **New** and then from the Select Icon Section Destination Type menu, select either launcher, screen, or function option.
    4.  In the **Image** field, use the reference lookup icon to select the icon type image you created.

        **Note:** For details to complete the rest of the Icon section destination type table, see [Configure an icon UI section](sg-ui-section-config-navig.md).

    5.  Select **Submit**.


