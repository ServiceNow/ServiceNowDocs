---
title: Override icon illustrations with custom images
description: Modify or override the default icon illustrations with your own custom images to promote visual elements that reflect your company's branding. When you override an icon, Theme Builder updates the icon wherever it is used across the interface.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Icon illustrations, Image styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override icon illustrations with custom images

Modify or override the default icon illustrations with your own custom images to promote visual elements that reflect your company's branding. When you override an icon, Theme Builder updates the icon wherever it is used across the interface.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see Granular admin roles.

## About this task

When you replace the base image, Theme Builder creates the other icon sizes by resizing your new base image automatically. This means that you only need to maintain one source file, and Theme Builder keeps every size in sync for you. If the automatically generated sizes lose sharpness or important details, you can replace any size independently.

You can override an entire icon set via a single base image or provide size‑specific assets for precise control.

Use the base image override when:

-   You want to move quickly with a single source of truth.
-   Minor changes from scaling are acceptable.

Use per‑size overrides when:

-   You need uniform stroke weights across sizes.
-   Fine details get lost at 12×12 or 16×16, and you want simplified small-size art.
-   Your design team maintains a bespoke icon set according to size.

**Important:** Custom images apply to Workspaces and aren’t supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    ![Example view of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel and expand **Icons**.

5.  Use one of the following options to select the icon illustration set that you want to override.

    -   Select the Filter icon ![](../image/tb-filter-icon.png) and expand the icon category to select the specific illustration set that you want to override. Enable **Only show modified images** to display only icons you have changed.
    -   Enter text in the search field to filter the icon library. The results update as you enter and show matching default and custom icons available in the theme’s icon library.
    -   Scroll through the list of icon illustrations in the main stage. Use the records-per-page control to view 10, 20, 50, or 100 icons at a time as you browse.
    Once you have selected an illustration, the property panel opens.

    ![Image styles tab selected with icon illustrations listed on main stage and property panel opened.](../image/tb-icon-property-panel.png "Image styles tab with Icons expanded")

6.  From the property panel, select the file name for the icon size you want to override.

    **Note:** To update all sizes, replace the Base image. Replacing other sizes affects only that size. If you override the base image, all smaller sizes scale automatically and any individual size overrides you've already applied are replaced.

7.  Use one of the following options to upload your custom image:

    -   Select **Browse**, choose your custom image file from your computer's file browser, and select **Open**.
    -   Drag your custom image file from your computer's file browser and drop the image directly into the modal.
    Refer to the upload image modal for size and format limitations or see [Icon illustrations in Theme Builder](../concept/tb-icon-illustrations.md). If your custom image doesn’t meet the required size and format, your image isn’t saved.

8.  Preview your image within the modal and select **Save**.

    Your custom image appears on the main stage within the icon illustration type that you have chosen. The file name for your custom image is now listed in the property panel.

9.  Select the Remove override icon ![](../../../reuse/icons/product-icons/undo-top-outline-24.svg) to restore the default icon illustration.

    **Note:** Removing the base image override resets the icon to its default state and clears all individual size overrides.

10. Preview your edits before publishing your theme to your instance.

    Icon scaling can introduce sharpness or detail issues that are only visible in a live experience.

    1.  Select the **Experiences** tab from the Global styles panel.

    2.  Select the experience that you want to preview from the Experience drop-down list.

    3.  Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab.

        ![Global styles experience preview screen.](../image/tb-experience-preview-1.png "Experience preview")


## Result

If your theme is published, your custom images are visible to users who have your theme applied on refresh. For more information about publishing themes, see [Publish your themes with Theme Builder](tb-apply-theme.md).

**Parent Topic:**[Icon illustrations in Theme Builder](../concept/tb-icon-illustrations.md)

