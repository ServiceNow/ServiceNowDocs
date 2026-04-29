---
title: Color variable support for icon UI sections
description: Learn how to use color variables to change theming in your mobile icon UI sections.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Color theme considerations, Configure theming, Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for icon UI sections

Learn how to use color variables to change theming in your mobile icon UI sections.

<table id="table_nvp_tkb_yvb"><tbody><tr><td>

Icon UI sections have a **Color** section with two fields to control the foreground and background colors for the element.

 -   **Background color Variable**
-   **Foreground color variable**

 These two fields can be found on the following tables:

-   Icon section destination launcher \[sys\_sg\_navigation\_section\_destination\_applet\_launcher\]
-   Icon section destination function \[sys\_sg\_navigation\_section\_destination\_button\]
-   Icon section destination screen \[sys\_sg\_navigation\_section\_destination\_screen\]

 For details on creating these actions, see [Configure an icon UI section](../task/sg-ui-section-config-navig.md).

 You can define any color variable from the UX Theme Properties \[sys\_ux\_theme\_property\] table. For a list available variables see the color design guide below.

</td><td>

![Color variable used in an icon UI section](../image/color-var-example-2.png)

</td></tr></tbody>
</table>## Mobile icon UI section color guide

Color variables are divided into Use the design guideline to identify the right color variable for your use case.

-   **Alert color palette**

    Alert color palette colors highlight important statuses, states and tasks. Use alert colors to communicate a specific meaning rather than for decoration or organization.

-   **Grouped color palette**

    Grouped color palette colors follow color conventions in a line of industry. Use these colors to show that the colored item is associated with a specific industry or line of business. The meaning of each color depends on context, but should remain consistent within your app.


## Alert color palette

<table id="table_otd_c1q_1xb"><thead><tr><th>

Color name

</th><th>

Color

</th><th>

Example

</th><th>

Color options

</th></tr></thead><tbody><tr><td>

Primary

</td><td>

![Primary icon color](../image/icon-colors/icon-color-primary.png)

</td><td>

![Primary icon example](../image/icon-colors/icon-example-primary.png)

</td><td>

-   **Mobile variable**

`primary`

-   **Web variable**

`--now-color--primary-1`


</td></tr><tr><td>

Critical

</td><td>

![Critical icon color](../image/icon-colors/icon-color-alert.png)

</td><td>

![Critical icon example](../image/icon-colors/icon-example-critical.png)

</td><td>

-   **Mobile variable**

`alert--critical-2`

-   **Web variable**

`--now-color_alert--critical-2`


</td></tr><tr><td>

High

</td><td>

![High icon color](../image/icon-colors/icon-color-high.png)

</td><td>

![High icon example](../image/icon-colors/icon-example-high.png)

</td><td>

-   **Mobile variable**

`alert--high-2`

-   **Web variable**

`--now-color_alert--high-2`


</td></tr><tr><td>

Warning

</td><td>

![Warning icon color](../image/icon-colors/icon-color-warning.png)

</td><td>

![Warning icon example](../image/icon-colors/icon-example-warning.png)

</td><td>

-   **Mobile variable**

`alert--warning-2`

-   **Web variable**

`--now-color_alert--warning-2`


</td></tr><tr><td>

Moderate

</td><td>

![Moderate icon color](../image/icon-colors/icon-color-moderate.png)

</td><td>

![Moderate icon example](../image/icon-colors/icon-example-moderate.png)

</td><td>

-   **Mobile variable**

`alert--moderate-2`

-   **Web variable**

`--now-color_alert--moderate-2`


</td></tr><tr><td>

Info

</td><td>

![Info icon color](../image/icon-colors/icon-color-info.png)

</td><td>

![Info icon example](../image/icon-colors/icon-example-info.png)

</td><td>

-   **Mobile variable**

`alert--info-2`

-   **Web variable**

`--now-color_alert--info-2`


</td></tr><tr><td>

Positive

</td><td>

![Positive icon color](../image/icon-colors/icon-color-positive.png)

</td><td>

![Positive icon example](../image/icon-colors/icon-example-positive.png)

</td><td>

-   **Mobile variable**

`alert--positive-2`

-   **Web variable**

`--now-color_alert--positive-2`


</td></tr><tr><td>

Low

</td><td>

![Low icon color](../image/icon-colors/icon-color-low.png)

</td><td>

![Low icon example](../image/icon-colors/icon-example-low.png)

</td><td>

-   **Mobile variable**

`alert--low-2`

-   **Web variable**

`--now-color_alert--low-2`


</td></tr></tbody>
</table>## Grouped color palette

<table id="table_eff_pbh_cxb"><thead><tr><th>

Color name

</th><th>

Color

</th><th>

Example

</th><th>

Color options

</th></tr></thead><tbody><tr><td>

Blue

</td><td>

![Blue icon color](../image/icon-colors/icon-color-blue.png)

</td><td>

![Blue icon example](../image/icon-colors/icon-example-blue.png)

</td><td>

-   **Web variable**

`--now-color_grouped--blue-2`


</td></tr><tr><td>

Brown

</td><td>

![Brown icon color](../image/icon-colors/icon-color-brown.png)

</td><td>

![](../image/icon-colors/icon-example-brown.png)

</td><td>

-   **Web variable**

`--now-color_grouped--brown-2`


</td></tr><tr><td>

Gray

</td><td>

![Gray icon color](../image/icon-colors/icon-color-gray.png)

</td><td>

![Gray icon example](../image/icon-colors/icon-example-gray.png)

</td><td>

-   **Web variable**

`--now-color_grouped--gray-2`


</td></tr><tr><td>

Green

</td><td>

![Green icon color](../image/icon-colors/icon-color-green.png)

</td><td>

![Green icon example](../image/icon-colors/icon-example-green.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-2`


</td></tr><tr><td>

Green-Yellow

</td><td>

![Green-yellow icon color](../image/icon-colors/icon-color-green-yellow.png)

</td><td>

![Green-yellow icon example](../image/icon-colors/icon-example-green-yellow.png)

</td><td>

-   **Web variable**

`--now-color_grouped--green-yellow-2`


</td></tr><tr><td>

Magenta

</td><td>

![Magenta icon color](../image/icon-colors/icon-color-magenta.png)

</td><td>

![Magenta icon example](../image/icon-colors/icon-example-magenta.png)

</td><td>

-   **Web variable**

`--now-color_grouped--magenta-2`


</td></tr><tr><td>

Orange

</td><td>

![Orange icon color](../image/icon-colors/icon-color-orange.png)

</td><td>

![Orange icon example](../image/icon-colors/icon-example-orange.png)

</td><td>

-   **Web variable**

`--now-color_grouped--orange-2`


</td></tr><tr><td>

Pink

</td><td>

![Pink icon color](../image/icon-colors/icon-color-pink.png)

</td><td>

![Pink icon example](../image/icon-colors/icon-example-pink.png)

</td><td>

-   **Web variable**

`--now-color_grouped--pink-2`


</td></tr><tr><td>

Purple

</td><td>

![Purple icon color](../image/icon-colors/icon-color-purple.png)

</td><td>

![Purple icon example](../image/icon-colors/icon-example-purple.png)

</td><td>

-   **Web variable**

`--now-color_grouped--purple-2`


</td></tr><tr><td>

Teal

</td><td>

![Teal icon color](../image/icon-colors/icon-color-teal.png)

</td><td>

![Teal icon example](../image/icon-colors/icon-example-teal.png)

</td><td>

-   **Web variable**

`--now-color_grouped--teal-2`


</td></tr><tr><td>

Yellow

</td><td>

![Yellow icon color](../image/icon-colors/icon-color-yellow.png)

</td><td>

![Yellow icon example](../image/icon-colors/icon-example-yellow.png)

</td><td>

-   **Web variable**

`--now-color_grouped--yellow-2`


</td></tr></tbody>
</table>