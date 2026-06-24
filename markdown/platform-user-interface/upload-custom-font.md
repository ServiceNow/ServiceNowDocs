---
title: Upload a custom font to your theme
description: Upload and preview up to 10 custom font families and an unlimited number of associated font faces in your Theme Builder theme.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/upload-custom-font.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [theme builder, custom font, upload custom font, upload font]
breadcrumb: [Global styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Upload a custom font to your theme

Upload and preview up to 10 custom font families and an unlimited number of associated font faces in your Theme Builder theme.

## Before you begin

Role required: admin

## About this task

A font family is a grouping of fonts that share a common design and may include different font faces, like regular, bold, or italic. For example, Ariel is a font family and within the Ariel font family you may find font faces such as Ariel Regular, Ariel Bold, and Ariel Italic.

Upload only one font family at a time. Theme Builder does not yet support variable type fonts.

**Important:** Only upload a font that you’re licensed to use. Depending on their size, custom fonts can inadvertently adjust the amount of text on the page. Always test and preview your fonts before publishing your theme to your instance.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-list.png"\] Alt text: Page drop-down list with Editor selected.

3.  From the Theme drop-down list, select the theme that you want to edit.

    The **Global styles** tab opens automatically with the Overview panel displayed.

    \[Omitted image "tb-editor-page-view.png"\] Alt text: Example view of the Editor page.

4.  From the Overview panel, navigate to the Typography section and select **Add custom font family**.

    \[Omitted image "tb-overview-add-custom-font.png"\] Alt text: Overview panel Topography section with Add custom font family selected.

    **Note:** You can also upload a font directly from the Typography panel.

    \[Omitted image "tb-typography-panel.png"\] Alt text: Global styles Typography panel.

    The Add custom font family modal appears.

5.  Use one of the following options to upload your custom font family:

    -   Select **Browse**, choose your custom font family file from your computer's file browser, and select **Open**.
    -   Drag your custom font file from your computer's file browser and drop the file directly into the modal.
    **Note:** Make sure that the font family file meets the following guidelines or the file isn't saved.

    -   Under 2 MB
    -   WOFF, TTF, or ZIP format
    \[Omitted image "tb-custom-font-modal-browse.png"\] Alt text: Add custom font family modal with Browse selected.

6.  Use the arrow within the modal to view any font faces you have uploaded with your custom font family.

    **Note:** Font faces can be applied individually to components, while the font family is applied globally.

    \[Omitted image "tb-custom-font-family-modal-arrow.png"\] Alt text: Add custom font family modal preview pane with one font face displayed and arrow to view additional font faces highlighted.

7.  Select **Save**.

    Your new font family appears in the Typography section under **Manage custom fonts**, along with the associated font faces.

    \[Omitted image "tb-typography-font-family.png"\] Alt text: Typography section with new custom font family and font faces listed.

8.  Preview how your selected font family or font face appears using any of the following options.

    -   Use the **UI styles preview** or **Experience preview** tabs on the main stage to view how your new font appears globally throughout your theme.
    -   Open the preview modal by selecting the custom font family or font face name that you want to preview listed beneath the **Manage custom fonts** header.

## Result

Once you have uploaded your custom font, you can select it as your default font and apply it to your theme. For information, see [Edit your default font](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/edit-font.md). The most recently added font family appears at the bottom of the **Manage custom fonts** list.

-   **[Add a font face](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/add-font-face.md)**  
Add a new style such as bold or italic to your custom font family in Theme Builder.
-   **[Delete a custom font from your theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/delete-custom-font.md)**  
Delete and remove a custom font family or font face you no longer need from your Theme Builder theme.

**Parent Topic:**[Working with Global styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/working-with-global-styles.md)

