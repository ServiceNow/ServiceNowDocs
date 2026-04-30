---
title: Mirror the portal direction for right-to-left languages
description: Mirror the direction of a portal's user interface for right-to-left languages by enabling the necessary CSS.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Styling for right-to-left languages in portals, Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Mirror the portal direction for right-to-left languages

Mirror the direction of a portal's user interface for right-to-left languages by enabling the necessary CSS.

## Before you begin

Active a right-to-left language, such as Hebrew. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select a portal.

3.  Select the **Support right-to-left languages** option.

4.  Select **Update**.

    CSS that mirrors the direction of a portal's user interface for right-to-left languages is generated.

5.  If you use an external CSS library for your portal theme, provide your own CSS that mirrors the direction of a portal's user interface to override the automatically generated CSS.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Themes**.

    2.  Select the theme for the portal.

    3.  In the **CSS Includes** related list, select the CSS Include that links to an external CSS library URL.

        If you need to create a new CSS Include, see [Create a portal theme](c_CustomCSS.md).

    4.  In the **RTL CSS file URL** field, enter the URL to an external style sheet for mirroring the direction of a portal for right-to-left languages.

    5.  Select **Update**.


## Result

When the session language is a right-to-left language, the direction of the portal user interface is mirrored to display from right to left.

If any content in your portal isn’t automatically mirrored for right-to-left languages, see [CSS for right-to-left languages in portals](css-directives-right-to-left-languages.md) for information about how to resolve these issues.

**Parent Topic:**[Styling for right-to-left languages in portals](styling-right-to-left-languages.md)

