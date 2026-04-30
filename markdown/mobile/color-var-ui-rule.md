---
title: Color variable support for UI rules
description: Learn how to use color variables to change theming in your mobile UI rules.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Color theme considerations for mobile, Configure Next Experience theming for mobile, Next Experience theming for mobile, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for UI rules

Learn how to use color variables to change theming in your mobile UI rules.

<table id="table_fbp_nfb_yvb"><tbody><tr><td>

Use the following color variables in the **Value** field of your UI rules with the **Operation** field set to **Set UI Style**

 -   `BackgroundColorVariable`
-   `FontColorVariable` outside or within the `TextDecorator`

 You can define any color variable from the UX Theme Properties \[sys\_ux\_theme\_property\] table. For a list available variables see the color design guide below. For example:

 `{“BackgroundColorVariable”: “--now-color-secondary-3", “BackgroundColor”: “#3f2c11”}`

 For details on creating these UI rule actions, see [Create a mobile UI rule action](../task/create-mobile-ui-rule-action.md).

</td><td>

![Color variable used in a ui action](../image/color-var-example-1.png)

</td></tr></tbody>
</table>## Mobile UI rule color guide

Color variables are divided into Use the design guideline to identify the right color variable for your use case.

-   **Alert color palette**

    Alert color palette colors highlight important statuses, states and tasks. Use alert colors to communicate a specific meaning rather than for decoration or organization.

-   **Grouped color palette**

    Grouped color palette colors follow color conventions in a line of industry. Use these colors to show that the colored item is associated with a specific industry or line of business. The meaning of each color depends on context, but should remain consistent within your app.


<table id="table_otd_c1q_1xb"><thead><tr><th>

Color name

</th><th>

Example

</th><th>

Color variables

</th></tr></thead><tbody><tr><td>

Critical

</td><td>

![Critical alert color scheme](../image/alert-color-palette-critical.png)

</td><td>

-   **Mobile variable**

`alert--critical-0`

-   **Web variable**

`--now-color_alert--critical-0`


</td></tr><tr><td>

High

</td><td>

![High alert color scheme](../image/alert-color-palette-high.png)

</td><td>

-   **Mobile variable**

`alert--high-0`

-   **Web variable**

`--now-color_alert--high-0`


</td></tr><tr><td>

Warning

</td><td>

![Warning alert color scheme](../image/alert-color-palette-warning.png)

</td><td>

-   **Mobile variable**

`alert--warning-0`

-   **Web variable**

`--now-color_alert--warning-0`


</td></tr><tr><td>

Moderate

</td><td>

![Moderate alert color scheme](../image/alert-color-palette-moderate.png)

</td><td>

-   **Mobile variable**

`alert--moderate-0`

-   **Web variable**

`--now-color_alert--moderate-0`


</td></tr><tr><td>

Info

</td><td>

![Info alert color scheme](../image/alert-color-palette-info.png)

</td><td>

-   **Mobile variable**

`alert--info-0`

-   **Web variable**

`--now-color_alert--info-0`


</td></tr><tr><td>

Positive

</td><td>

![Positive alert color scheme](../image/alert-color-palette-positive.png)

</td><td>

-   **Mobile variable**

`alert--positive-0`

-   **Web variable**

`--now-color_alert--positive-0`


</td></tr><tr><td>

Low

</td><td>

![Low alert color scheme](../image/alert-color-palette-low.png)

</td><td>

-   **Mobile variable**

`alert--low-0`

-   **Web variable**

`--now-color_alert--low-0`


</td></tr><tr><td>

Disabled

</td><td>

![Disabled alert color scheme](../image/alert-color-palette-disabled.png)

</td><td>

-   **Mobile variable**

`alert-disabled-background`

-   **Web variable**

`--now-color_background--secondary`


</td></tr><tr><td>

Critical \(Alternate\)

</td><td>

![Critical alert color scheme alternate](../image/alert-color-palette-critical2.png)

</td><td>

-   **Mobile variable**

`alert--critical-4`

-   **Web variable**

`--now-color_alert--critical-4`


</td></tr><tr><td>

High \(Alternate\)

</td><td>

![High alert color scheme alternate](../image/alert-color-palette-high2.png)

</td><td>

-   **Mobile variable**

`alert--high-4`

-   **Web variable**

`--now-color_alert--high-4`


</td></tr><tr><td>

Warning \(Alternate\)

</td><td>

![Warning alert color scheme alternate](../image/alert-color-palette-warning2.png)

</td><td>

-   **Mobile variable**

`alert--warning-4`

-   **Web variable**

`--now-color_alert--warning-4`


</td></tr><tr><td>

Moderate \(Alternate\)

</td><td>

![Moderate alert color scheme alternate](../image/alert-color-palette-moderate2.png)

</td><td>

-   **Mobile variable**

`alert--moderate-4`

-   **Web variable**

`--now-color_alert--moderate-4`


</td></tr><tr><td>

Info \(Alternate\)

</td><td>

![Info alert color scheme alternate](../image/alert-color-palette-info2.png)

</td><td>

-   **Mobile variable**

`alert--info-4`

-   **Web variable**

`--now-color_alert--info-4`


</td></tr><tr><td>

Positive \(Alternate\)

</td><td>

![Positive alert color scheme alternate](../image/alert-color-palette-positive2.png)

</td><td>

-   **Mobile variable**

`alert--positive-4`

-   **Web variable**

`--now-color_alert--positive-4`


</td></tr><tr><td>

Low \(Alternate\)

</td><td>

![Low alert color scheme alternate](../image/alert-color-palette-low2.png)

</td><td>

-   **Mobile variable**

`alert--low-4`

-   **Web variable**

`--now-color_alert--low-4`


</td></tr><tr><td>

Disabled \(Alternate\)

</td><td>

![Disabled alert color scheme alternate](../image/alert-color-palette-disabled2.png)

</td><td>

-   **Mobile variable**

`alert-disabled-text`

-   **Web variable**

`--now-color_text--tertiary`


</td></tr></tbody>
</table><table id="table_f5d_c1q_1xb"><thead><tr><th>

Color name

</th><th>

Example

</th><th>

Color options

</th></tr></thead><tbody><tr><td>

Blue

</td><td>

![Blue grouped color scheme](../image/grouped-color-palette-blue.png)

</td><td>

-   **Web variable**

`--now-color_grouped--blue-0`


</td></tr><tr><td>

Brown

</td><td>

![Brown grouped color scheme](../image/grouped-color-palette-brown.png)

</td><td>

-   **Web variable**

`--now-color_grouped--brown-0`


</td></tr><tr><td>

Gray

</td><td>

![Gray grouped color scheme](../image/grouped-color-palette-gray.png)

</td><td>

-   **Web variable**

`--now-color_grouped--gray-0`


</td></tr><tr><td>

Green

</td><td>

![Green grouped color scheme](../image/grouped-color-palette-green.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-0`


</td></tr><tr><td>

Green-Yellow

</td><td>

![Green-yellow grouped color scheme](../image/grouped-color-palette-green-yellow.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-yellow-0`


</td></tr><tr><td>

Magenta

</td><td>

![Magenta grouped color scheme](../image/grouped-color-palette-magenta.png)

</td><td>

-   **Web variable**

`--now-color_grouped--magenta-0`


</td></tr><tr><td>

Orange

</td><td>

![Orange grouped color scheme](../image/grouped-color-palette-orange.png)

</td><td>

-   **Web variable**

`--now-color_grouped--orange-0`


</td></tr><tr><td>

Pink

</td><td>

![Pink grouped color scheme](../image/grouped-color-palette-pink.png)

</td><td>

-   **Web variable**

`--now-color_grouped--pink-0`


</td></tr><tr><td>

Purple

</td><td>

![Purple grouped color scheme](../image/grouped-color-palette-purple.png)

</td><td>

-   **Web variable**

`--now-color_grouped--purple-0`


</td></tr><tr><td>

Teal

</td><td>

![Teal grouped color scheme](../image/grouped-color-palette-teal.png)

</td><td>

-   **Web variable**

`--now-color_grouped--teal-0`


</td></tr><tr><td>

Yellow

</td><td>

![Yellow grouped color scheme](../image/grouped-color-palette-yellow.png)

</td><td>

-   **Web variable**

`--now-color_grouped--yellow-0`


</td></tr><tr><td>

Blue \(Alternate\)

</td><td>

![Blue grouped color scheme alternate](../image/grouped-color-palette-blue2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--blue-4`


</td></tr><tr><td>

Brown \(Alternate\)

</td><td>

![Brown grouped color scheme alternate](../image/grouped-color-palette-brown2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--brown-4`


</td></tr><tr><td>

Gray \(Alternate\)

</td><td>

![Gray grouped color scheme alternate](../image/grouped-color-palette-gray2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--gray-4`


</td></tr><tr><td>

Green \(Alternate\)

</td><td>

![Green grouped color scheme alternate](../image/grouped-color-palette-green2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-4`


</td></tr><tr><td>

Green-Yellow \(Alternate\)

</td><td>

![Green-yellow grouped color scheme alternate](../image/grouped-color-palette-green-yellow2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-yellow-4`


</td></tr><tr><td>

Magenta \(Alternate\)

</td><td>

![Magenta grouped color scheme alternate](../image/grouped-color-palette-magenta2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--magenta-4`


</td></tr><tr><td>

Orange \(Alternate\)

</td><td>

![Orange grouped color scheme alternate](../image/grouped-color-palette-orange2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--orange-4`


</td></tr><tr><td>

Pink \(Alternate\)

</td><td>

![Pink grouped color scheme alternate](../image/grouped-color-palette-pink2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--pink-4`


</td></tr><tr><td>

Purple \(Alternate\)

</td><td>

![Purple grouped color scheme alternate](../image/grouped-color-palette-purple2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--purple-4`


</td></tr><tr><td>

Teal \(Alternate\)

</td><td>

![Teal grouped color scheme alternate](../image/grouped-color-palette-teal2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--teal-4`


</td></tr><tr><td>

Yellow \(Alternate\)

</td><td>

![Yellow grouped color scheme alternate](../image/grouped-color-palette-yellow2.png)

</td><td>

-   **Web variable**

`--now-color_grouped--yellow-4`


</td></tr></tbody>
</table>