---
title: Theming for AI Search in Service Portal
description: You can customize the look and feel of the AI Search experience in Service Portal by updating the relevant CSS variables.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Override AI Search theming, AI Search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Theming for AI Search in Service Portal

You can customize the look and feel of the AI Search experience in Service Portal by updating the relevant CSS variables.

The following CSS variables control the look and feel of the AI Search features in Service Portal. For more information about AI Search features, see [Using AI Search](https://www.servicenow.com/docs/access?context=use-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

You can edit these variables in the **CSS variables** field of a Theme \[sp\_theme\] record. You can also configure these variables with a CSS Include associated with a portal's theme. For more information, see the following topics:

-   [Create a portal theme](../concept/c_CustomCSS.md)
-   [Create a CSS include to override theming for AI Search in Service Portal](../task/css-override-ais-theming-sp.md)

<table id="table_wcz_tww_knb"><thead><tr><th>

Variable

</th><th>

Default value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

*$now-sp-font-family-sans-serif*

</td><td>

`"SourceSansPro", Helvetica, Arial, sans-serif`

</td><td>

Font family for all texts.

</td></tr><tr><td>

*$now-sp-color--text-primary*

</td><td>

`$gray-dark`

</td><td>

 Color of   unselected tabs, Genius result button text, hit text color, result icons, and  search bar drop down list item text and icon color.

</td></tr><tr><td>

*$now-sp-text-link--primary--color*

</td><td>

`$gray-dark`

</td><td>

The color of the title text in search results.

</td></tr><tr><td>

*$now-sp-display-type--tertiary--color*

</td><td>

`$gray-dark`

</td><td>

The color of the text snippet in search results.

</td></tr><tr><td>

*$now-sp-color--neutral-12*

</td><td>

`$gray-dark`

</td><td>

 Expanded icon color \(chevron\) of the facets in mobile view.

</td></tr><tr><td>

*$now-sp-global-border-radius*

</td><td>

`4px`

</td><td>

 Rounded search results corners affecting the content pane and not search result cards. This variable also affects Genius results, buttons on Genius results, and search bar icon hover background highlights. This variable doesn't affect facets.

</td></tr><tr><td>

*$now-sp-color--focus-ring*

</td><td>

`$brand-primary`

</td><td>

Tabs focus color.

</td></tr><tr><td>

*$now-sp-tabs--selected--color*

</td><td>

`$brand-primary`

</td><td>

Text color of selected tab. Doesn't include on hover.

</td></tr><tr><td>

*$now-sp-tabs--color--hover*

</td><td>

`$brand-primary`

</td><td>

Text color of all tabs when hovered.

</td></tr><tr><td>

*$now-sp-tabs--border-color*

</td><td>

`$sp-b-border-color`

</td><td>

Tabs underline color.

</td></tr><tr><td>

*$now-sp-tabs--selected--background-color*

</td><td>

`$brand-primary`

</td><td>

Selected tab underline color.

</td></tr><tr><td>

*$now-sp-heading--title-primary--color*

</td><td>

`$gray-dark`

</td><td>

Color Filters label.

</td></tr><tr><td>

*$now-sp-checkbox-label--color*

</td><td>

`$gray-dark`

</td><td>

Filter item \(checkbox label\) color.

</td></tr><tr><td>

*$now-sp-button--primary--bare--color*

</td><td>

`$link-color`

</td><td>

**Clear All** and **Clear** link color in facets filter.

</td></tr><tr><td>

*$now-sp-button--primary--bare--color--active*

</td><td>

`$link-color`

</td><td>

**Clear All** and **Clear** link color in facets filter on click.

</td></tr><tr><td>

*$now-sp-button--primary--bare--color--hover*

</td><td>

`$link-hover-color`

</td><td>

 **Clear All** and **Clear** link color in facets filter on hover.

</td></tr><tr><td>

*$now-sp-pill--selected--background-color*

</td><td>

`$brand-primary`

</td><td>

Selected filter pill background.

</td></tr><tr><td>

*$now-sp-pill--selected--border-color*

</td><td>

`$brand-primary`

</td><td>

 Selected filter pill border color.

</td></tr><tr><td>

*$now-sp-button--secondary--background-color*

</td><td>

`$btn-default-bg`

</td><td>

Genius result button background.

</td></tr><tr><td>

*$now-sp-button--secondary--color*

</td><td>

`$btn-default-color`

</td><td>

 Genius result button text color.

</td></tr><tr><td>

*$now-sp-button--secondary--border-color*

</td><td>

`$btn-default-border`

</td><td>

Genius result button border color.

</td></tr><tr><td>

*$now-sp-button--secondary--background-color--hover*

</td><td>

`darken($btn-default-bg, 10%)`

</td><td>

Genius result button background color on hover.

</td></tr><tr><td>

*$now-sp-button--secondary--color--hover*

</td><td>

`$btn-default-color`

</td><td>

 Genius result button text color on hover.

</td></tr><tr><td>

*$now-sp-button--secondary--border-color--hover*

</td><td>

`darken($btn-default-border, 12%)`

</td><td>

 Genius result button border on hover.

</td></tr><tr><td>

*$now-sp-button--secondary--background-color--active*

</td><td>

`darken($btn-default-bg, 10%)`

</td><td>

Genius result button background on click.

</td></tr><tr><td>

*$now-sp-button--secondary--color--active*

</td><td>

`$btn-default-color`

</td><td>

Genius result button text color on click.

</td></tr><tr><td>

*$now-sp-button--secondary--border-color--active*

</td><td>

`darken($btn-default-border, 12%)`

</td><td>

Genius result button border color on click.

</td></tr><tr><td>

*$now-sp-highlighted-value--tertiary--color*

</td><td>

`$gray-dark`

</td><td>

Genius result Top Result tag text color.

</td></tr><tr><td>

*$now-sp-button--border-radius*

</td><td>

`$now-sp-global-border-radius`

</td><td>

Differentiates the radius for button and search bar buttons.

</td></tr><tr><td>

*$now-sp-container--border-radius*

</td><td>

`$now-sp-global-border-radius`

</td><td>

Border radius for search result cards, genius result cards, and the search results container. Doesn't affect the border between individual results.

</td></tr><tr><td>

*$now-sp-button--primary-negative--background-color*

</td><td>

`$btn-primary-bg`

</td><td>

 Genius button background color in the EVAM action confirmation modal.

</td></tr><tr><td>

*$now-sp-button--primary-negative--border-color*

</td><td>

`$btn-primary-border`

</td><td>

Genius button border color in the EVAM action confirmation modal.

</td></tr><tr><td>

*$now-sp-button--primary-negative--background-color--hover*

</td><td>

`darken($btn-primary-bg, 10%)`

</td><td>

Genius button background color on hover in the EVAM action confirmation modal.

</td></tr><tr><td>

*$now-sp-button--primary-negative--border-color--hover*

</td><td>

`darken($btn-primary-border, 12%)`

</td><td>

Genius button border color on hover inside the confirmation.

</td></tr><tr><td>

*$now-sp-button--primary-negative--background-color--active*

</td><td>

`darken($btn-primary-bg, 10%)`

</td><td>

 Genius button background color on click inside the confirmation modal.

</td></tr><tr><td>

*$now-sp-button--primary-negative--border-color--active*

</td><td>

`darken($btn-primary-border, 12%)`

</td><td>

Genius button border color on click inside the confirmation modal.

</td></tr><tr><td>

*$now-sp-button--primary--background-color*

</td><td>

`$btn-primary-bg`

</td><td>

Selected filter \(pill\) background color.

</td></tr><tr><td>

*$now-sp-button--primary--border-color*

</td><td>

`$btn-primary-border`

</td><td>

Selected filter \(pill\) border color

</td></tr><tr><td>

*$now-sp-button--primary--color*

</td><td>

`$btn-primary-color`

</td><td>

Selected filter \(pill\) color.

</td></tr><tr><td>

*$now-sp-button--primary--background-color--hover*

</td><td>

`darken($btn-primary-bg, 10%)`

</td><td>

 Selected filter \(pill\) background color on hover.

</td></tr><tr><td>

*$now-sp-button--primary--border-color--hover*

</td><td>

`darken($btn-primary-border, 12%)`

</td><td>

Selected filter \(pill\) border color on hover.

</td></tr><tr><td>

*$now-sp-button--primary--background-color--active*

</td><td>

`darken($btn-primary-bg, 10%)`

</td><td>

Selected filter \(pill\) background color on click.

</td></tr><tr><td>

*$now-sp-button--primary--border-color--active*

</td><td>

`darken($btn-primary-border, 12%)`

</td><td>

Selected filter \(pill\) border color on click.

</td></tr><tr><td>

*$now-sp-rem-factor*

</td><td>

`5`

</td><td>

The same variable as *--classicsponlydonotuse--rem-multipy*. **Note:** It's not suggested to use this variable.

</td></tr><tr><td>

*$sp-search-result-title-highlight--background-color*

</td><td>

None

</td><td>

Text background color for title highlights in search results.**Note:** For this theme setting to take effect, you must add the static value `removeHitHighlighting` with value `"false"` for the `sn-search-result-evam-card` component in the relevant EVAM view template, as shown in this example:

```json
{
  "component": "sn-search-result-evam-card",
  "staticValues": {
    "removeHitHighlighting": {
      "translatable": true,
      "key": "false"
    }
  },
}
```

To learn about configuring settings in EVAM view templates, see [Define an EVAM view template](https://www.servicenow.com/docs/access?context=define-evam-template&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Create a CSS include to override theming for AI Search in Service Portal](../task/css-override-ais-theming-sp.md)

