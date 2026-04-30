---
title: Create or customize a theme
description: You can create themes or customize existing themes.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSS theme support, Customizing instance appearance, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create or customize a theme

You can create themes or customize existing themes.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Themes**.

2.  Choose from the following options.

    -   To create a new theme, click **New**.
    -   To customize an existing theme, click the theme name.
3.  Enter a name for the theme in the **Name** field.

4.  Add any of the [default CSS styles](../reference/r_DefaultCSSStyle.md) in the **CSS** field.

    Sometimes the default style is not the only style definition for an object. In such cases, you can use the CSS [important rule](http://www.w3.org/TR/CSS2/cascade.html#important-rules) format to override any other style definitions with the default definition. For example, this definition overrides the text color in the main navigation: `$navpage-nav-color-sub: #fff !important`.

5.  Select the **Active** check box.

6.  Select one of the following from the **Device** choice list to identify the user interface version for the theme.

    |Option|Description|
    |------|-----------|
    |**Browser**|Identifies a Legacy UI11 theme.|
    |**Doctype**|Identifies a Legacy UI15 theme.|
    |**Concourse**|Identifies a Core UI theme.|

7.  Click **Submit**.


## What to do next

Refresh the page to see the new theme in the theme picker. The theme picker displays only themes that are compatible with the current version of the UI.

**Parent Topic:**[CSS theme support](../concept/c_CSSThemeSupport.md)

**Related topics**  


[Activating CSS theme support](../reference/r_ActivatingCSSThemeSupport.md)

[Default CSS styles](../reference/r_DefaultCSSStyle.md)

