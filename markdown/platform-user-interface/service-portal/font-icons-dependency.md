---
title: Include font icons as a widget dependency
description: You can include font icons wherever a widget is loaded by including them as a widget dependency.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a widget dependency, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Include font icons as a widget dependency

You can include font icons wherever a widget is loaded by including them as a widget dependency.

## Before you begin

Role required: admin or sp\_admin

## About this task

**Note:** CSS included as a widget dependency is not scoped and can disrupt other CSS on a page.

## Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **CSS** and create a new style sheet.

2.  Attach the font-icon set to the sp\_css record you created, and use the sys\_id of the attachment as the `src` for the font icon.

    For example:

    ```css
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

3.  Navigate to **Service Portal** &gt; **Dependencies** and create a new dependency.

4.  Attach the CSS record you created to the new dependency using the **CSS Includes** related list.


**Parent Topic:**[Create a widget dependency](widget-dependencies.md)

