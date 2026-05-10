---
title: Override banner illustrations with custom images
description: Modify or override the default banner illustrations with your own custom images to promote visual elements that reflect your company's branding.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Banner illustrations, Image styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override banner illustrations with custom images

Modify or override the default banner illustrations with your own custom images to promote visual elements that reflect your company's branding.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

Verify that your custom images use the desired colors and meet your branding requirements before uploading to Theme Builder.

## About this task

**Important:** Custom images apply to Workspaces and aren’t supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    ![Example view of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel and expand **Banners**.

5.  Use one of the following options to select the banner illustration that you want to override.

    -   Select the Filter icon ![](../image/tb-filter-icon.png) icon and expand the banner category to select the specific banner illustration that you want to override.
    -   Scroll through the list of banner illustrations within the main stage.
    Once you have selected an illustration, the property panel opens.

    ![Image styles tab selected with banner illustrations listed on main stage and property panel opened.](../image/tb-banner-property-panel.png "Image styles tab with Banners selected")

6.  From the property panel, select the **Images** tab.

7.  Select the default banner illustration file name.

    For example, the file name listed for this illustration is **banner\_customer\_general.svg**.

    The upload images modal appears.

8.  Use one of the following options to upload your custom image:

    -   Select **Browse**, choose your custom image file from your computer's file browser, and select **Open**.
    -   Drag your custom image file from your computer's file browser and drop the image directly into the modal.
    Refer to the upload image modal for size and format limitations. If your custom image doesn’t meet the required size and format, your image isn’t saved.

9.  Preview your image in the modal and select **Save**.

    Your custom image appears on the main stage within the banner type that you have chosen. The file name for your custom image is now listed in the property panel.

    ![Customer general banner illustration type with custom image displayed on main stage.](../image/tb-banner-customer-general.png "Customer general banner type with custom image displayed")

10. Select the Remove override symbol if you want to restore the default banner illustration.

    ![Remove custom image override symbol.](../image/tb-remove-custom-image-symbol.png "Remove override")

11. Preview your edits before publishing your theme to your instance.

    1.  Select the **Experience preview** tab from the Global styles panel.

    2.  Select the experience that you want to preview from the Experience drop-down list.

    3.  Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab.

        ![Global styles experience preview screen with Admin Center experience selected.](../image/tb-experience-preview-1.png "Experience preview")


## Result

If your theme is published, your custom images are visible to users who have your theme applied on refresh. For more information about publishing themes, see [Publish your themes with Theme Builder](tb-apply-theme.md).

**Parent Topic:**[Banner illustrations in Theme Builder](../concept/banners-in-tb.md)

