---
title: Create a custom theme by cloning a Theme Builder theme record
description: Create a custom theme in the Next Experience more efficiently using a published Theme Builder theme record.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Next Experience themes, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a custom theme by cloning a Theme Builder theme record

Create a custom theme in the Next Experience more efficiently using a published Theme Builder theme record.

## Before you begin

In order to clone a Theme Builder theme, the theme must be published. For information on publishing your Theme Builder theme, see [Publish your themes with Theme Builder](tb-apply-theme.md).

Role required: admin

## About this task

To avoid your work from being overwritten, your new cloned theme isn’t editable in Theme Builder.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes**.

    The UX Themes table appears.

2.  Under the Name column, search for the Theme Builder theme you want to clone and select the record.

3.  Clone the five UX Theme style records.

    1.  From the **Compositional: App Theme** tab, select and hold \(or right-click\) the Mobile Colors style record and select **Open link in new tab**.

    2.  In the **Name** field, enter your theme name.

        For example, `ABC Company - Mobile Colors`.

    3.  Select and hold \(or right-click\) the header bar and select **Insert and Stay**.

        This action creates a copy of the style record and redirects the information to the new style record.

        ![Cloned Mobile Colors style record with Insert and Stay option selected.](../image/next-exp-insert-and-stay.png "Cloned Mobile Colors style record")

    4.  Close the open tab.

    5.  Repeat this process for the Shape and Form, Colors, Imagery, and Typography style records.

    **Note:** The cloned style records don’t appear in the current theme record and this behavior is expected.

4.  Clone the UX theme record.

    1.  From the **Name** field, change the name of the theme record.

        For example, `Custom ABC Company`.

    2.  Select and hold \(or right-click\) the header bar and select **Insert and Stay**.

        Your new UX theme record appears. The style records within this theme are empty and this behavior is expected.

        ![Newly created UX Theme record.](../image/next-exp-cloned-theme-record.png "Newly created UX Theme record")

5.  Add the newly created style records to your theme.

    1.  Double-click under the Style column to expose the lookup field.

    2.  Search for and select one of your new style records from the drop-down.

    3.  Save your selection by selecting the green checkmark.

    4.  Double-click under the Type column to expose the drop-down list and select **Core**.

        ![Style Type drop-down list with Core option selected.](../image/next-exp-type-column.png "Style Type drop-down list")

    5.  Save your selection by selecting the green checkmark.

        This action associates your style record to the current theme.

    6.  Repeat this process for the remaining four style records.

    7.  Select and hold \(or right-click\) the header bar and select **Save**.

        If the changes haven't been saved, green bars are displayed next to the style records that you have added.

        ![UX Theme record before the record is saved.](../image/next-exp-custom-theme-green.png "UX Theme record before the record is saved")

6.  Publish your custom theme.

    To publish your custom theme, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

    Now that your custom theme is published, you’re ready to customize your theme. For a step-by-step tutorial for editing your UX Style color record, see Exercise 3, Activity 2 and 3 of the [Next Experience Workshop](https://servicenownextexperience.github.io/labs/CCL1319-K24-Theming-Lab/ex3/activity-2) in the ServiceNow Community.


**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)

