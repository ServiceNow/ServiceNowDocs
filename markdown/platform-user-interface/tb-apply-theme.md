---
title: Publish your themes with Theme Builder
description: Publish multiple themes to your web instance or a single theme to your mobile instance to reflect your company's brand.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Publish your themes with Theme Builder

Publish multiple themes to your web instance or a single theme to your mobile instance to reflect your company's brand.

## Before you begin

Role required: admin

## About this task

Currently, mobile instances can only accommodate one published theme at a time.

If you want to publish a theme to specific mobile applications, you can use [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=zurich&pubname=zurich-mobile&ft:locale=en-US). Any themes that are created using Theme Builder are available for publishing in [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

Next Experience Polaris and Coral themes are available for publishing from Theme Builder.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  From the Home page view, select the Manager page view to see the themes that you have created.

3.  Decide which theme you want to publish from the Unpublished section.

    **Note:** When you have selected the theme that you want to publish, verify that you have selected the correct scope for the theme from the application scope picker.![Application scope picker.](../image/tb-scope-picker.png)

4.  To publish your themes, complete any of the following actions.

<table id="choicetable_ahh_ch2_fdc"><thead><tr><th align="left" id="d109387e134">

Option

</th><th align="left" id="d109387e137">

Description

</th></tr></thead><tbody><tr><td id="d109387e143">

**Publish using the List or Grid view More Actions menu**

</td><td>

From the Unpublished section, select the More actions icon ![](../image/tb-more-actions.png)from the theme that you want published, and select **Publish**.![More actions menu opened with Publish selected.](../image/tb-more-actions-publish.png)

</td></tr><tr><td id="d109387e168">

**Publish using the List view drag-and-drop feature**

</td><td>

From the Unpublished section, hover over the theme you want published, and drag the theme into the Published section.

</td></tr></tbody>
</table>5.  Select **Publish** in the confirmation dialog box.

    ![Publish the theme dialog box.](../image/tb-test-theme-dialog-box.png)

    The theme appears in the Published section of the Manager page.

    **Note:** After you have published your theme to your instance, users must [select the theme from their Theme preference](select-a-theme-in-next-experience.md).

6.  Select one theme as the default if you have published multiple themes to your web instance.

    If you have published only one theme to your web instance, that theme is the default theme. The default theme appears first in the user's Theme preference. For more information, see [Set the default theme](set-the-default-theme.md).

7.  Set the presentation order of your themes if you have published multiple themes to your web instance.

    **Note:** The presentation order determines how the themes appear in the user's Theme preference.

    For more information on setting the order of your themes using the List view drag-and-drop feature, see [Set the presentation order of your Theme Builder themes](set-presentation-order-themes.md).

    For information on setting order using the Next Experience, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

8.  Refresh your browser to view the new theme published to your instance.

    **Note:** Only themes that are created in Theme Builder can be edited and published using Theme Builder. Web and mobile themes you may have created outside of Next Experience \(for example, in the mobile legacy UI or Core UI\) can’t be viewed or edited within Theme Builder. To reuse these legacy themes, you must re-create them in Theme Builder.

    Additionally, if you created and published themes outside of Theme Builder, and you want to revert them, you must navigate to the tables that they’re stored in and reapply them. If, however, you want to change themes in individual mobile applications, you can do so using [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=zurich&pubname=zurich-mobile&ft:locale=en-US).


-   **[Set the default theme](set-the-default-theme.md)**  
Set a preferred Theme Builder theme as the default for your web experiences when multiple themes are published.
-   **[Set the presentation order of your Theme Builder themes](set-presentation-order-themes.md)**  
Set the order of your Theme Builder themes to configure how they’re displayed in the user's Theme preferences.

**Parent Topic:**[Configuring Next Experience with Theme Builder](configuring-next-experience-with-theme-builder.md)

