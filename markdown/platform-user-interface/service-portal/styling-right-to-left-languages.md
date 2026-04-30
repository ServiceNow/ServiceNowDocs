---
title: Styling for right-to-left languages in portals
description: Localizing a portal for right-to-left languages requires CSS that mirrors the direction of portal pages.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Styling for right-to-left languages in portals

Localizing a portal for right-to-left languages requires CSS that mirrors the direction of portal pages.

Service Portal can generate the CSS required to mirror the user interface direction of the portal when the session language is a right-to-left language. The entire hierarchy of existing infrastructure for styling left-to-right languages—the theme, page, widget, and widget instance SCSS—is converted to CSS for right-to-left languages. All directional properties supported by [RTLCSS](https://rtlcss.com/learn/getting-started/why-rtlcss/) are converted. However, plain CSS files included in any of the theme or widget dependency records, internal CSS, and inline CSS aren’t automatically converted.

You can also provide your own CSS for right-to-left languages to override the automatically generated CSS if you use an external CSS library and you can control the conversion of CSS for right-to-left languages using a variety of methods.

**Note:** Base system portals besides Service Portal \(/sp\) and custom portals might need additional CSS customization to mirror the direction of a portal for right-to-left languages completely.

To track how many users view a portal in a right-to-left language, see the PortalPageLoad event in User Experience Analytics for Service Portal. For more information about available events, see [Service Portal events](../reference/sp-analytics-events.md).

-   **[Mirror the portal direction for right-to-left languages](mirror-portal-direction-right-to-left-languages.md)**  
Mirror the direction of a portal's user interface for right-to-left languages by enabling the necessary CSS.
-   **[CSS for right-to-left languages in portals](css-directives-right-to-left-languages.md)**  
You can control the generation of CSS for right-to-left languages using a variety of methods.

**Parent Topic:**[Defining portal styles](portal-css.md)

