---
title: Override tile icon illustrations with custom images
description: Modify or override the default tile icon illustrations with your own custom images to promote visual elements that reflect your company's branding.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tile icon illustrations, Image styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override tile icon illustrations with custom images

Modify or override the default tile icon illustrations with your own custom images to promote visual elements that reflect your company's branding.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Verify that your custom images use the desired colors and meet your branding requirements before uploading to Theme Builder.

## About this task

**Important:** Custom images apply to Workspaces and aren’t supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    ![Example view of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel and expand **Tile icons**.

5.  Use one of the following options to select the tile icon illustration that you want to override.

    -   Select the Filter icon ![](../image/tb-filter-icon.png) icon and expand the tile icon category to select the specific illustration that you want to override.
    -   Scroll through the list of tile icon illustrations within the main stage.
    Once you have selected an illustration, the property panel opens.

    ![Image styles tab selected with tile icon illustrations listed on main stage and property panel opened.](../image/tb-tile-icon-property-panel.png "Image styles tab with Tile icons expanded")

6.  From the property panel, select the **Images** tab.

7.  Select the default tile icon illustration file name.

    The upload images modal appears.

8.  Use one of the following options to upload your custom image:

    -   Select **Browse**, choose your custom image file from your computer's file browser, and select **Open**.
    -   Drag your custom image file from your computer's file browser and drop the image directly into the modal.
    Refer to the upload image modal for size and format limitations. If your custom image doesn’t meet the required size and format, your image isn’t saved.

9.  Preview your image in the modal and select **Save**.

    ![Upload image modal with custom image displayed and Save selected.](../image/tb-tile-icon-custom.png "Upload image modal with custom image displayed")

    Once saved, your custom image appears on the main stage within the card category you have chosen. The file name for your custom image is now listed in the property panel.

10. Select the Remove override symbol if you want to restore the default tile icon illustration.

    ![Remove custom image override symbol.](../image/tb-remove-custom-image-symbol.png "Remove override")

11. Preview your edits before publishing your theme to your instance.

    1.  Select the **Experience preview** tab from the Global styles panel.

    2.  Select the experience that you want to preview from the Experience drop-down list.

    3.  Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab.

        ![Global styles experience preview screen with Admin Center experience selected.](../image/tb-experience-preview-1.png "Experience preview")


## Result

If your theme is published, your custom images are visible to users who have your theme applied on refresh. For more information about publishing themes, see [Publish your themes with Theme Builder](tb-apply-theme.md).

**Parent Topic:**[Tile icon illustrations in Theme Builder](../concept/tile-icons-in-tb.md)

