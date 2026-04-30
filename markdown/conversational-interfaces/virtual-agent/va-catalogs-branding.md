---
title: Set up Catalog branding
description: Customize the appearance of Catalogs in Virtual Agent to match your business' branding.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-09-06"
reading_time_minutes: 2
keywords: [Virtual, Theme, Builder, Agent, Catalogs, branding, web, client]
breadcrumb: [Catalogs for Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Set up Catalog branding

Customize the appearance of Catalogs in Virtual Agent to match your business' branding.

## Before you begin

Role required: admin, virtual\_agent\_admin

Download Theme Builder from the ServiceNow Store and activate the plugin \(sn\_theme\_builder\). For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## About this task

Virtual Agent uses the Branding Setup \[sys\_cs\_branding\_setup\] table to define branding colors, but Catalogs don't inherit branding colors. Instead, Catalogs use cascading style sheets \(CSS\) variables defined in the UX Themes \[sys\_ux\_theme\] record on the instance.

## Procedure

1.  Navigate to **All** &gt; **Themes** &gt; **Theme Builder**.

2.  Create a new theme by providing primary and secondary colors.

    **Note:** You can match your colors to the Chat Header Background and Chat Background colors in the branding record of your choice. For more information creating themes, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

3.  Save your theme.

4.  Add your theme to the portal configuration.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes**.

    2.  Select the record for the theme you want to import.

    3.  Under the Additional Actions icon ![Additional actions icon.](../images/additional-actions-icon.png), select **Copy sys\_id**.

    4.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.

    5.  Select the portal configuration where you want to add your branding theme, and add the following line to the server script, including the sys\_id from Step 4c.

    For example, if your sys\_id is `0be48eb1eba0011090fa99602a522843`, you add:

    ```
    macroponent_theme: '0be48eb1eba0011090fa99602a522843'
    ```

5.  Add a variant theme to the portal configuration if desired.

    1.  Repeat Steps 4a and 4b.

    2.  Under the **Compositional: App theme** tab, open your desired **Style** whose **Type** is `Variant`.

    3.  Repeat Steps 4c and 4d.

    4.  Select the portal configuration where you added your branding theme, and add the following line to the server script, including the sys\_id from Step 5c.

    For example, if your variant theme's sys\_id is `1df59fc2fcb1122101gb00713b633954`, you add:

    ```
    macroponent_theme_variant: '1df59fc2fcb1122101gb00713b633954'
    ```

6.  Select **Update** to save the configuration.

7.  Navigate to the portal where the configuration is used.

    For example, if you updated the **ESC Chat** portal configuration, navigate to Employee Service Center.

8.  Run the catalog topic in the portal chat to load its configuration and reveal any elements that need branding.

    ![Virtual Agent chat window, with highlighted links and buttons to be updated.](../images/catalog-branding-01.png)

9.  Navigate to **All** &gt; **Now Experience framework** &gt; **Themes** &gt; **Theme Builder**.

10. From the drop-down menu, select **Manager**, then select your created theme.

11. Under the **Component styles** tab, select **Edit**.

    ![Update the color hex codes in Theme Builder to match your branding colors.](../images/catalog-branding-02.png)

12. Select one of the elements needing branding found in Step 8.

13. In the palette sidebar, set the element's hex code color to match the color from your branding record.

14. Repeat Steps 12 and 13 until you update all elements.

    ![Virtual Agent chat window, with highlighted links and buttons updated after changing hex color codes in Theme Builder.](../images/catalog-branding-03.png)


## Result

Catalog color themes now match your branding.

**Parent Topic:**[Catalogs for Virtual Agent](../concept/va-catalogs.md)

