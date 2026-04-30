---
title: Create a Next Experience style
description: When you create or modify a Next Experience theme, you create and edit one or more styles. Styles include typefaces, colors, images, and shapes and forms. The style records you create override the default Polaris theme in Next Experience.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Next Experience themes and preferences, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a Next Experience style

When you create or modify a Next Experience theme, you create and edit one or more styles. Styles include typefaces, colors, images, and shapes and forms. The style records you create override the default Polaris theme in Next Experience.

## Before you begin

Role required: admin

## About this task

When you edit Next Experience styles, you work in raw JSON code. Edit with care.

You upload new typefaces or images in a separate process. See [Add Next Experience font and image assets](add-image-asset.md).

## Procedure

1.  In the filter navigator field, enter `sys_ux_style.do` to create a style record.

2.  Name the style and specify whether it’s a Core style or a Variant.

    **Note:** The Dark theme is the only variant shipped with Next Experience.

3.  In the **Style** field, add the base and properties blocks to contain overrides in the style record.

    ```
    {
      "base": {
    },
      "properties":{
      }
     }
    
    ```

4.  To save your work between steps, select the **Additional actions** menu \(![Additional actions icon.](../image/additional-actions.png)\) and choose `Save`.

5.  In the **Style** field, edit the JSON code to reflect the overrides you want the style to contain.

    1.  Add or edit your main colors in the base section of the JSON code.

        Use RGB values.

        The following example shows sample color overrides.

        ![Style block with color overrides](../image/polaris-style-base-colors.png)

    2.  Edit versions of the colors in the properties section of the JSON code.

    3.  Add or edit shapes in the properties section of the JSON code.

        The following example shows sample shape overrides.

        ![Style block with shape overrides](../image/polaris-style-base-shapes.png)

6.  Add fonts, images, and other theme assets.

    For more information, see [Add Next Experience font and image assets](add-image-asset.md).

7.  If you have uploaded fonts, add or edit typefaces in the properties section of the JSON code and select **Update**.

    ![Style block with color, shape, and font overrides](../image/polaris-style-colors-shapes-fonts.png)


## Result

The updated colors, shapes, and typefaces are visible in your theme.

**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)

