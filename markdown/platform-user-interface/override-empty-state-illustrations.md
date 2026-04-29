---
title: Override empty state illustrations with custom images
description: Modify or override the default empty state illustrations with your own custom images to promote visual elements that reflect your company's branding.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [override empty state, empty state illustrations, custom images]
breadcrumb: [Empty state illustrations, Image styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override empty state illustrations with custom images

Modify or override the default empty state illustrations with your own custom images to promote visual elements that reflect your company's branding.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Verify that your custom images use the desired colors and meet your branding requirements before uploading to Theme Builder.

Role required: admin

## About this task

**Important:** Custom images apply to Workspaces and aren’t supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    ![Example view of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel.

    The empty state illustrations are displayed on the main stage and grouped by type.

    ![Image styles tab selected with empty state illustrations listed on main stage and property panel opened.](../image/tb-image-styles-opened.png "Image styles tab selected")

5.  Use one of the following options to select the empty state illustration that you want to override.

    -   Select the Filter icon ![](../image/tb-filter-icon.png) icon and expand the empty states category to select the specific empty state illustration that you want to override.
    -   Scroll through the list of empty state illustrations within the main stage.
    The property panel opens automatically.

6.  From the property panel, select the **Images** tab.

    ![Property panel with Images tab selected.](../image/tb-property-panel-images.png "Property panel Images tab")

7.  Select either the large, medium, or small image file of the illustration you want to override.

    **Note:** You can only override one image size at a time.

    The upload images modal appears.

    ![Upload image modal.](../image/tb-image-upload-modal.png "Upload images modal")

8.  Use one of the following options to upload your custom image:

    -   Select **Browse**, choose your custom image file from your computer's file browser, and select **Open**.
    -   Drag your custom image file from your computer's file browser and drop the image directly into the modal.
    Refer to the upload image modal for size and format limitations. If your custom image doesn’t meet the required size and format, your image isn’t saved.

    ![Upload image modal with Browse selected and file limitations expanded.](../image/tb-image-upload-modal-browse.png "Upload image modal with size and format limitations")

9.  Select **Save**.

    Your custom image appears on the main stage within the empty state category that you have chosen.

    ![Add data empty state illustration category with custom image displayed.](../image/tb-add-data-image-modal.png "Add data empty state category with custom image displayed")

10. Select the Remove override symbol if you want to restore the default empty state illustration.

    ![Images tab with Remove override selected.](../image/tb-custom-image-override.png "Image Remove override")

11. Preview your edits before publishing your theme to your instance.

    1.  Select the **Experience preview** tab from the Global styles panel.

    2.  Select the experience that you want to preview from the Experience drop-down list.

    3.  Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab.

        ![Global styles experience preview screen with Admin Center experience selected.](../image/tb-experience-preview-1.png "Experience preview")


## Result

If your theme is published, your custom images are visible to users who have your theme applied on refresh. For more information about publishing themes, see [Publish your themes with Theme Builder](tb-apply-theme.md).

**Parent Topic:**[Empty state illustrations in Theme Builder](../concept/empty-state-illustrations.md)

