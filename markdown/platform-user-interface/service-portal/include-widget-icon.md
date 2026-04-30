---
title: Include a font icon in a single widget
description: If you only want one widget to have access to a font icon, include the font icon in a single widget.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a widget dependency, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Include a font icon in a single widget

If you only want one widget to have access to a font icon, include the font icon in a single widget.

## Before you begin

Role required: admin or sp\_admin

## About this task

Adding an icon to a specific widget keeps the icon scoped and prevents it from interfering with other CSS on the page.

## Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **Widgets**, then click the widget you want to add an icon to.

2.  Attach the individual icon file to the widget record.

3.  In the HTML template, include something like the following:

    ```
    <div>
    <i class='font-family'>icon_name</i> you did it!
    </div>
    ```

    Make sure that the class is exactly the same as the font family called out in the CSS. For example, `<i class='material-icons'>` should be the same as the `.material-icons` included in the CSS. The `icon_name` should match the name of the file you attached.

4.  In the CSS field for the widget, add the CSS for the font-icon definition.

    Most font-icon sets include a CSS file similar to the material icons one used below. Use the sys\_id of the attachment as the `src` in the CSS. For example:

    ```css
    /* fallback */
    @font-face {
      font-family: 'Material Icons';
      font-style: normal;
      font-weight: 400;
      src: url('/828b8ca8b7033010897725cbde11a9f7.iix') format('woff2');
    }
    
    .material-icons {
      font-family: 'Material Icons';
      font-weight: normal;
      font-style: normal;
      font-size: 24px;  /* Preferred icon size */
      display: inline-block;
      line-height: 1;
      text-transform: none;
      letter-spacing: normal;
      word-wrap: normal;
      white-space: nowrap;
      direction: ltr;
    
      /* Support for all WebKit browsers. */
      -webkit-font-smoothing: antialiased;
      /* Support for Safari and Chrome. */
      text-rendering: optimizeLegibility;
    
      /* Support for Firefox. */
      -moz-osx-font-smoothing: grayscale;
    
      /* Support for IE. */
      font-feature-settings: 'liga';
    }
    ```


## Result

An icon that you can select in the widget or widget instance. For example:

![Example matches the HTML with a check circle stating,"you did it!"](../image/IconExample.png)

## What to do next

To use custom font-icons across widgets, add the icon to a page or make it a widget dependency.

**Parent Topic:**[Create a widget dependency](widget-dependencies.md)

**Related topics**  


[Include font icons on a page](t_ConfigureAPage.md#)

[Include font icons as a widget dependency](font-icons-dependency.md)

