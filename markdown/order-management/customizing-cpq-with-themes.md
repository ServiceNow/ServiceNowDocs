---
title: Customizing CPQ with themes
description: Custom themes let you customize your layout. You can enable custom themes by submitting a feature enablement request.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Customizing CPQ with themes

Custom themes let you customize your layout. You can enable custom themes by submitting a feature enablement request.

CPQ admin users can edit a custom theme to customize the look and feel of their layout.

To access the custom theme options in the layout editor, submit a CPQ Feature Enablement Request to enable themes.

## Getting started

From the blueprint page, select a layout, and then click the Customize Theme tab at the top of the page.

**Note:** This tab appears only if the theme feature is enabled for your tenant.

![Customize theme](../images/cpq-themes-customize.png)

On the Customize Theme tab, click to turn on **Enable Theme**. \(By default, this option is off.\)

![Theme test](../images/cpq-themes-enable-theme.png)

When this option is turned on, you see the full Theme Editor screen.

## The visual editor

The visual editor includes five sets of options and an interactive preview. The standard CPQ theme is applied by default, but you can modify any fields to start customizing your theme.

![Visual editor showing default options on the interactive preview screen](../images/cpq-themes-visual-editor.png)

The following options are available in the visual editor.

|Option|Description|
|------|-----------|
|Root Text Color|Default font color used in the layout|
|Primary Color|Color used most often for buttons and selections|
|Primary Background Color|Default color used for the background and containers|
|Secondary Background Color|Default color used for tier items such as expandable section backgrounds|
|Neutral Color|Secondary color used for fields such as hint text|
|Success Color|Background color for success message banners|
|Info Color|Background color for neutral message banners|
|Warning Color|Background color for warning message banners|
|Error Color|Color for error messaging and field validation|
|Font Size|Default font size; small, medium, large|
|Border Radius|Determines border shape for fields where 0 = Square and 16 = Round|
|Border Width|Determines overall size of the border for fields; none, normal, thick|
|Spacing|Determines overall padding for the layout; tight, normal, loose|

## The JSON editor

The JSON editor provides additional control by using overrides for any element included in the theme.

By default, the values for the current theme are shown, but a user can manually enter new key value pairs to modify the theme. The structure of the theme JSON is already provided in the editor. Clicking in the editor lets the user type in the code block. Any changes made in the visual editor are represented in the JSON editor, and vice versa.

![Theme details](../images/cpq-themes-json-editor-default-theme.png)

A toggle hides or shows the standard CPQ theme as a reference for fields you may want to revert without discarding the entire theme.

If you want to overwrite a layout element that is not included in the sample data, you can inspect the layout to determine the field to change. Fields that begin with `--lgk-` are customizable in a theme.

The following example demonstrates inspecting a toggle.

![Code for toggle button](../images/cpq-themes-constructed-stylesheet.png)

To overwrite an element, add the field name and the modified value in the properties section of the theme override. The format should not include the `--lgk-` but should just be `“fieldname” : “value”`.

The following are example theme overrides.

![Custom Themes](../images/cpq-themes-custom-theme-override.png)

## Using a custom font

A theme can support a custom font through a hosted URL entered in either the visual editor or the JSON editor. This font file needs to be hosted so that it is accessible to the theme. For a custom font, you need to provide a name and the font source URL.

![Custom font links user interface](../images/cpq-themes-custom-font.png)

