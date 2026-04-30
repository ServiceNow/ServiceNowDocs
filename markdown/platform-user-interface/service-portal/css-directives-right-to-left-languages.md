---
title: CSS for right-to-left languages in portals
description: You can control the generation of CSS for right-to-left languages using a variety of methods.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Styling for right-to-left languages in portals, Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# CSS for right-to-left languages in portals

You can control the generation of CSS for right-to-left languages using a variety of methods.

Base system portals besides Service Portal \(/sp\) and custom portals might need additional CSS customization to mirror the direction of a portal for right-to-left languages completely.

Custom widgets might need some manual conversion for right-to-left languages.

-   For inline styles in a widget's HTML template, move these styles to the widget's CSS so they’ll be automatically converted.
-   For internal styles in a widget's HTML template, you can use the `[dir=”rtl”]` attribute selector or `.rtl` class selector to provide CSS that is specific to right-to-left languages.
-   To include CSS that is specific to right-to-left languages, you can call the isRTLEnabled\(\) method in the [GlideSPScriptable - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) class in a widget’s server script or use the g\_portal\_isrtl global flag in the widget’s client script.

Also, in the theme, page, widget, or widget instance CSS, you can add right-to-left directives to CSS properties only using a Sass interpolation string \(`#{""}`\).

|Right-to-left CSS directive|Description|
|---------------------------|-----------|
|`/*rtl:ignore*/`|Ignores the property when converting portal CSS for right-to-left languages.|
|`/*rtl:prepend:10px*/`|Adds a value to the beginning of the property value for right-to-left languages. This example prepends `10px`.|
|`/*rtl:append:3rem*/`|Adds a value to the end of the property value for right-to-left languages. This example appends `3rem`.|
|`/*rtl:replace:`30px`*/` or `/*rtl:`30px`*/`|Replaces the property value with the specified value for right-to-left languages. This example replaces the property value with `30px`.|
|`/*rtl:insert:25px*/`|Inserts the specified value in place of the directive for right-to-left languages. This example inserts `25px`.|

## Ignore the transform property in the converted right-to-left CSS

```css
.fl {
transform: rotate(45deg) translateY(5px) #{"/*rtl:ignore*/"};
}
```

**Parent Topic:**[Styling for right-to-left languages in portals](styling-right-to-left-languages.md)

