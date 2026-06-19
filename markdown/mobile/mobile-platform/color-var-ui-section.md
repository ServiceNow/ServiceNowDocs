---
title: Color variable support for icon UI sections
description: Learn how to use color variables to change theming in your mobile icon UI sections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/color-var-ui-section.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2025-07-31"
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

 For details on creating these actions, see [Configure an icon UI section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-ui-section-config-navig.md).

 You can define any color variable from the UX Theme Properties \[sys\_ux\_theme\_property\] table. For a list available variables see the color design guide below.

</td><td>

\[Omitted image "color-var-example-2.png"\] Alt text: Color variable used in an icon UI section

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

\[Omitted image "icon-color-primary.png"\] Alt text: Primary icon color

</td><td>

\[Omitted image "icon-example-primary.png"\] Alt text: Primary icon example

</td><td>

-   **Mobile variable**

`primary`

-   **Web variable**

`--now-color--primary-1`


</td></tr><tr><td>

Critical

</td><td>

\[Omitted image "icon-color-alert.png"\] Alt text: Critical icon color

</td><td>

\[Omitted image "icon-example-critical.png"\] Alt text: Critical icon example

</td><td>

-   **Mobile variable**

`alert--critical-2`

-   **Web variable**

`--now-color_alert--critical-2`


</td></tr><tr><td>

High

</td><td>

\[Omitted image "icon-color-high.png"\] Alt text: High icon color

</td><td>

\[Omitted image "icon-example-high.png"\] Alt text: High icon example

</td><td>

-   **Mobile variable**

`alert--high-2`

-   **Web variable**

`--now-color_alert--high-2`


</td></tr><tr><td>

Warning

</td><td>

\[Omitted image "icon-color-warning.png"\] Alt text: Warning icon color

</td><td>

\[Omitted image "icon-example-warning.png"\] Alt text: Warning icon example

</td><td>

-   **Mobile variable**

`alert--warning-2`

-   **Web variable**

`--now-color_alert--warning-2`


</td></tr><tr><td>

Moderate

</td><td>

\[Omitted image "icon-color-moderate.png"\] Alt text: Moderate icon color

</td><td>

\[Omitted image "icon-example-moderate.png"\] Alt text: Moderate icon example

</td><td>

-   **Mobile variable**

`alert--moderate-2`

-   **Web variable**

`--now-color_alert--moderate-2`


</td></tr><tr><td>

Info

</td><td>

\[Omitted image "icon-color-info.png"\] Alt text: Info icon color

</td><td>

\[Omitted image "icon-example-info.png"\] Alt text: Info icon example

</td><td>

-   **Mobile variable**

`alert--info-2`

-   **Web variable**

`--now-color_alert--info-2`


</td></tr><tr><td>

Positive

</td><td>

\[Omitted image "icon-color-positive.png"\] Alt text: Positive icon color

</td><td>

\[Omitted image "icon-example-positive.png"\] Alt text: Positive icon example

</td><td>

-   **Mobile variable**

`alert--positive-2`

-   **Web variable**

`--now-color_alert--positive-2`


</td></tr><tr><td>

Low

</td><td>

\[Omitted image "icon-color-low.png"\] Alt text: Low icon color

</td><td>

\[Omitted image "icon-example-low.png"\] Alt text: Low icon example

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

\[Omitted image "icon-color-blue.png"\] Alt text: Blue icon color

</td><td>

\[Omitted image "icon-example-blue.png"\] Alt text: Blue icon example

</td><td>

-   **Web variable**

`--now-color_grouped--blue-2`


</td></tr><tr><td>

Brown

</td><td>

\[Omitted image "icon-color-brown.png"\] Alt text: Brown icon color

</td><td>

\[Omitted image "icon-example-brown.png"\]

</td><td>

-   **Web variable**

`--now-color_grouped--brown-2`


</td></tr><tr><td>

Gray

</td><td>

\[Omitted image "icon-color-gray.png"\] Alt text: Gray icon color

</td><td>

\[Omitted image "icon-example-gray.png"\] Alt text: Gray icon example

</td><td>

-   **Web variable**

`--now-color_grouped--gray-2`


</td></tr><tr><td>

Green

</td><td>

\[Omitted image "icon-color-green.png"\] Alt text: Green icon color

</td><td>

\[Omitted image "icon-example-green.png"\] Alt text: Green icon example

</td><td>

-   **Web variable**

`--now-color_grouped--green-2`


</td></tr><tr><td>

Green-Yellow

</td><td>

\[Omitted image "icon-color-green-yellow.png"\] Alt text: Green-yellow icon color

</td><td>

\[Omitted image "icon-example-green-yellow.png"\] Alt text: Green-yellow icon example

</td><td>

-   **Web variable**

`--now-color_grouped--green-yellow-2`


</td></tr><tr><td>

Magenta

</td><td>

\[Omitted image "icon-color-magenta.png"\] Alt text: Magenta icon color

</td><td>

\[Omitted image "icon-example-magenta.png"\] Alt text: Magenta icon example

</td><td>

-   **Web variable**

`--now-color_grouped--magenta-2`


</td></tr><tr><td>

Orange

</td><td>

\[Omitted image "icon-color-orange.png"\] Alt text: Orange icon color

</td><td>

\[Omitted image "icon-example-orange.png"\] Alt text: Orange icon example

</td><td>

-   **Web variable**

`--now-color_grouped--orange-2`


</td></tr><tr><td>

Pink

</td><td>

\[Omitted image "icon-color-pink.png"\] Alt text: Pink icon color

</td><td>

\[Omitted image "icon-example-pink.png"\] Alt text: Pink icon example

</td><td>

-   **Web variable**

`--now-color_grouped--pink-2`


</td></tr><tr><td>

Purple

</td><td>

\[Omitted image "icon-color-purple.png"\] Alt text: Purple icon color

</td><td>

\[Omitted image "icon-example-purple.png"\] Alt text: Purple icon example

</td><td>

-   **Web variable**

`--now-color_grouped--purple-2`


</td></tr><tr><td>

Teal

</td><td>

\[Omitted image "icon-color-teal.png"\] Alt text: Teal icon color

</td><td>

\[Omitted image "icon-example-teal.png"\] Alt text: Teal icon example

</td><td>

-   **Web variable**

`--now-color_grouped--teal-2`


</td></tr><tr><td>

Yellow

</td><td>

\[Omitted image "icon-color-yellow.png"\] Alt text: Yellow icon color

</td><td>

\[Omitted image "icon-example-yellow.png"\] Alt text: Yellow icon example

</td><td>

-   **Web variable**

`--now-color_grouped--yellow-2`


</td></tr></tbody>
</table>