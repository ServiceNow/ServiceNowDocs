---
title: Variables to customize a theme for Desktop Assistant
description: You can modify specific CSS variables to customize themes for Desktop Assistant.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-10-14"
reading_time_minutes: 4
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Variables to customize a theme for Desktop Assistant

You can modify specific CSS variables to customize themes for Desktop Assistant.

|Variable|Description|Order|
|--------|-----------|-----|
|brand-primary-darkest|The darkest shade of the brand's primary color.|1|
|brand-primary-darker|Slightly lighter shade than the darkest shade of the brand's primary color.|2|
|brand-primary|Primary brand color used in the UI.|3|
|brand-primary-lighter|Lighter shade than the primary brand color.|4|

You can apply a gradient to the banner by using the specified colors in the specified order.

<table id="table_fxn_cty_ygc"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

background-secondary

</td><td>

Secondary background color used for UI elements that are not the main focus.

</td><td>

`#ffffff`

</td></tr><tr><td>

background-primary

</td><td>

Primary background color used for main focus areas on the UI.

</td><td>

`#f6f6f8`

</td></tr><tr><td>

font-size-base

</td><td>

Base font size used for UI text.

</td><td>

`16px`

</td></tr><tr><td>

font-weight-base

</td><td>

Base font weight used for UI body text.

</td><td>

`400`

</td></tr><tr><td>

font-family-sans-serif

</td><td>

Default sans serif font family used for UI text.

</td><td>

`Lato`

</td></tr><tr><td>

line-height-base

</td><td>

Default text line height for spacing and readability.

</td><td>

`1.4`

</td></tr><tr><td>

font-size-h5

</td><td>

Font size for heading level 5.

</td><td>

`16px` or value of the *$font-size-base* variable.

</td></tr><tr><td>

font-size-h4

</td><td>

Font size for heading level 4.

</td><td>

`18px`This value is calculated using the ceil \(\) function: `ceil(($font-size-base * 1.125))`.

For example, if the *font-size-base* value is 16 px, the *font-size-h4* value is 18 px: `ceil((16px * 1.125))//18px`.

</td></tr><tr><td>

font-size-h3

</td><td>

Font size for heading level 3.

</td><td>

`20px`This value is calculated using the ceil \(\) function: `ceil(($font-size-base * 1.25))`.

</td></tr><tr><td>

font-size-xl

</td><td>

Extra large font size typically used for titles or large labels.

</td><td>

`24px`This value is calculated using the ceil \(\) function: `ceil(($font-size-base * 1.5))`.

</td></tr><tr><td>

font-size-xs

</td><td>

Extra small font size typically used for minor labels or captions.

</td><td>

`12px`This value is calculated using the ceil \(\) function: `ceil(($font-size-base * 0.75))`.

</td></tr><tr><td>

font-size-small

</td><td>

Smaller font than the base font, used for secondary text.

</td><td>

`14px`This value is calculated using the ceil \(\) function: `ceil(($font-size-base * 0.875))`.

</td></tr><tr><td>

headings-font-family

</td><td>

Font family used for headings.

</td><td>

`Lato`

</td></tr><tr><td>

headings-font-weight

</td><td>

Font weight used for headings.

</td><td>

`600`

</td></tr></tbody>
</table><table id="table_ic1_dsd_zgc"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

text-primary

</td><td>

Main color used for body text.

</td><td>

`#181A1F`

</td></tr><tr><td>

text-color

</td><td>

General text color for the UI, which is the same as *text-primary*.Set a value for this variable only if you have not already defined the value for *text-primary*.

</td><td>

`$text-primary!default`For example, `$text-primary: #000000 !default;`

</td></tr><tr><td>

text-secondary

</td><td>

Color used for less prominent UI text.

</td><td>

`#474D5A`

</td></tr><tr><td>

text-tertiary

</td><td>

Color for tertiary text such as help text and annotations.

</td><td>

`#656E81`

</td></tr><tr><td>

text-muted

</td><td>

Muted text color that is generally the same as *text-tertiary*.Set a value for this variable only if you have not already defined the value for *text-tertiary*.

</td><td>

`$text-tertiary!default`For example, `$text-tertiary: #999999 !default;`

</td></tr><tr><td>

color-grey

</td><td>

Neutral grey color used for elements such as borders and backgrounds.

</td><td>

`#C6CBCB`

</td></tr><tr><td>

link-color

</td><td>

Color for hyperlinks.

</td><td>

`#3c59e7`

</td></tr></tbody>
</table>|Variable|Description|Default|
|--------|-----------|-------|
|btn-default-color|Default color for button text.|`$brand-primary`|
|btn-primary-color|Text color for primary buttons.|`$text-white`|
|btn-primary-bg|Background color for primary buttons.|`$brand-primary`|
|brand-primary|Primary brand color used across the UI.|`#4f52bd!default;`|
|brand-primary-darker|A darker shade of the primary brand color.|`#333579`|
|brand-primary-darkest|Darkest shade of the primary brand color.|`#1D1E46`|
|brand-primary-lighter|A lighter shade of the primary brand color.|`#8789D2`|
|brand-primary-lightest|Lightest shade of the primary brand color.|`#D1D2EE`|

|Variable|Description|Default|
|--------|-----------|-------|
|brand-warning-darker|Darker shade of UI warning state color.|`#AFA400`|
|brand-success-darker|Darker shade of color used for success states on the UI.|`#3B7F00`|
|brand-danger-darker|Darker shade of color used for danger states on the UI.|`#CC293C`|
|alert-warning-bg|Background color used for alerts and warnings.|`$state-warning-bg`|
|badge-color|Text color for badges on the UI.|`$text-white`|

|Variable|Description|Default value|
|--------|-----------|-------------|
|border-primary|Primary border color used for main UI elements.|`#8790A1`|
|border-secondary|Secondary border color used for less prominent UI elements.|`#ACB2BE`|
|border-tertiary|Tertiary border color used for background borders.|`#DADDE2`|
|border-width-xs|Extra-small border width used for UI elements like thin lines or light dividers.|`1px`|
|border-style-solid|Sets the border style to solid.|`solid`|
|border-radius-base|Base border radius for rounding corners of UI elements.|`4px`|
|input-border|Border style for input fields.|`$border-primary`|

|Variable|Description|Default value|
|--------|-----------|-------------|
|sp-space--xxl|Extra-extra-large spacing for wide gaps or larger layouts.|`32px`|
|sp-space--xl|Extra-large spacing for major sections.|`24px`|
|sp-space--lg|Large spacing for padding or margins.|`16px`|
|sp-space--md|Medium or standard spacing for most UI elements.|`12px`|
|sp-space--sm|Small spacing for compact layouts.|`8px`|
|sp-space--xs|Extra-small spacing for minimal gaps.|`4px`|
|sp-space--xxs|Extra-extra-small spacing for minimal UI gaps.|`2px`|
|panel-heading-padding|Padding applied to the heading section of a panel or card.|`$sp-space--xl`|

<table id="table_npr_kg2_zgc"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td colspan="3">

Font weight variable

</td></tr><tr><td>

font-weight-lg

</td><td>

Font weight used for large or bold text.

</td><td>

`600`This value is calculated using the ceil \(\) function: `ceil(($font-weight-base * 1.5))`.

</td></tr><tr><td colspan="3">

Shadow and effects variables

</td></tr><tr><td>

sp-panel-box-shadow

</td><td>

Shadow styling for panel components.

</td><td>

`0 4px 8px 0 rgba(23, 40, 52, 0.08)`

</td></tr><tr><td>

sp-box-shadow--md

</td><td>

Medium box shadow effects for UI components.

</td><td>

``

</td></tr></tbody>
</table>**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)

