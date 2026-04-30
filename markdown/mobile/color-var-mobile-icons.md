---
title: Color variable support for icons
description: Learn how to use color variables to change theming in your mobile map screens
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Color theme considerations for mobile, Configure Next Experience theming for mobile, Next Experience theming for mobile, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for icons

Learn how to use color variables to change theming in your mobile map screens

<table id="table_st2_mtb_yvb"><tbody><tr><td>

Mobile icons have a **Set appearance** section used to define the appearance of your icons. Use the **FontColorVariable** style option to use a color variable a color.

 Using this style you can define any color variable from the UX Theme Properties \[sys\_ux\_theme\_property\] table. For a list available variables see the color design guide below.

 For details on creating map screens, see [Configure an icon UI section](../task/sg-ui-section-config-navig.md).

 For details on creating icons in mobile, see [Mobile icons](sg-mobile-icon.md).

</td><td>

![Color variable used in an icon](../image/color-var-example-4.png)

</td></tr></tbody>
</table>## Mobile icon color guide

Color variables are divided into Use the design guideline to identify the right color variable for your use case.

-   **Alert color palette**

    Alert color palette colors highlight important statuses, states and tasks. Use alert colors to communicate a specific meaning rather than for decoration or organization.

-   **Grouped color palette**

    Grouped color palette colors follow color conventions in a line of industry. Use these colors to show that the colored item is associated with a specific industry or line of business. The meaning of each color depends on context, but should remain consistent within your app.


Each support color has three options, including an assessable option. Consider using the accessible color option for icons that do not contain text to improve navigability for your users.

<table id="table_otd_c1q_1xb"><thead><tr><th>

Color name

</th><th>

Example

</th><th>

Color variables

</th></tr></thead><tbody><tr><td>

Critical

</td><td>

![Critical mobile icons](../image/icon-colors/icons-mobile-critical.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--critical-2`
    -   Option 2: `alert--critical-3`
    -   Option 3 \(Accessible\): `alert--critical-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--critical-2`
    -   Option 2:`--now-color_alert--critical-3`
    -   Option 3 \(Accessible\):`--now-color_alert--critical-4`

</td></tr><tr><td>

High

</td><td>

![High mobile icons](../image/icon-colors/icons-mobile-high.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--high-2`
    -   Option 2: `alert--high-3`
    -   Option 3 \(Accessible\): `alert--high-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--high-2`
    -   Option 2:`--now-color_alert--high-3`
    -   Option 3 \(Accessible\):`--now-color_alert--high-4`

</td></tr><tr><td>

Warning

</td><td>

![Warning mobile icons](../image/icon-colors/icons-mobile-warning.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--warning-2`
    -   Option 2: `alert--warning-3`
    -   Option 3 \(Accessible\): `alert--warning-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--warning-2`
    -   Option 2:`--now-color_alert--warning-3`
    -   Option 3 \(Accessible\):`--now-color_alert--warning-4`

</td></tr><tr><td>

Moderate

</td><td>

![Moderate mobile icons](../image/icon-colors/icons-mobile-moderate.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--moderate-2`
    -   Option 2: `alert--moderate-3`
    -   Option 3 \(Accessible\): `alert--moderate-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--moderate-2`
    -   Option 2:`--now-color_alert--moderate-3`
    -   Option 3 \(Accessible\):`--now-color_alert--moderate-4`

</td></tr><tr><td>

Info

</td><td>

![Info mobile icons](../image/icon-colors/icons-mobile-info.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--info-2`
    -   Option 2: `alert--info-3`
    -   Option 3 \(Accessible\): `alert--info-4`
-   **Web variable**
    -   Option: 1`--now-color_alert--info-2`
    -   Option 2:`--now-color_alert--info-3`
    -   Option 3 \(Accessible\):`--now-color_alert--info-4`

</td></tr><tr><td>

Positive

</td><td>

![Positive mobile icons](../image/icon-colors/icons-mobile-positive.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--positive-2`
    -   Option 2: `alert--positive-3`
    -   Option 3 \(Accessible\): `alert--positive-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--positive-2`
    -   Option 2:`--now-color_alert--positive-3`
    -   Option 3 \(Accessible\):`--now-color_alert--positive-4`

</td></tr><tr><td>

Low

</td><td>

![Low mobile icons](../image/icon-colors/icons-mobile-low.png)

</td><td>

-   **Mobile variables**
    -   Option 1: `alert--low-2`
    -   Option 2: `alert--low-3`
    -   Option 3 \(Accessible\): `alert--low-4`
-   **Web variable**
    -   Option 1:`--now-color_alert--low-2`
    -   Option 2:`--now-color_alert--low-3`
    -   Option 3 \(Accessible\):`--now-color_alert--low-4`

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

![Blue mobile icons](../image/icon-colors/icons-mobile-blue.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--blue-2`
    -   Option 2:`--now-color_grouped--blue-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--blue-4`

</td></tr><tr><td>

Brown

</td><td>

![Brown mobile icons](../image/icon-colors/icons-mobile-brown.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--brown-2`
    -   Option 2:`--now-color_grouped--brown-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--brown-4`

</td></tr><tr><td>

Gray

</td><td>

![Gray mobile icons](../image/icon-colors/icons-mobile-gray.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--gray-2`
    -   Option 2:`--now-color_grouped--gray-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--gray-4`

</td></tr><tr><td>

Green

</td><td>

![Green mobile icons](../image/icon-colors/icons-mobile-green.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--green-2`
    -   Option 2:`--now-color_grouped--green-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--green-4`

</td></tr><tr><td>

Green-Yellow

</td><td>

![Green-yellow mobile icons](../image/icon-colors/icons-mobile-green-yellow.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--green-yelow-2`
    -   Option 2:`--now-color_grouped--green-yelow-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--green-yelow-4`

</td></tr><tr><td>

Magenta

</td><td>

![Magenta mobile icons](../image/icon-colors/icons-mobile-magenta.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--magenta-2`
    -   Option 2:`--now-color_grouped--magenta-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--magenta-4`

</td></tr><tr><td>

Orange

</td><td>

![Orange mobile icons](../image/icon-colors/icons-mobile-orange.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--orange-2`
    -   Option 2"`--now-color_grouped--orange-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--orange-4`

</td></tr><tr><td>

Pink

</td><td>

![Pink mobile icons](../image/icon-colors/icons-mobile-pink.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--pink-2`
    -   Option 2:`--now-color_grouped--pink-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--pink-4`

</td></tr><tr><td>

Purple

</td><td>

![Purple mobile icons](../image/icon-colors/icons-mobile-purple.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--purple-2`
    -   Option 2:`--now-color_grouped--purple-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--purple-4`

</td></tr><tr><td>

Teal

</td><td>

![Teal mobile icons](../image/icon-colors/icons-mobile-teal.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--teal-2`
    -   Option 2:`--now-color_grouped--teal-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--teal-4`

</td></tr><tr><td>

Yellow

</td><td>

![Yellow mobile icons](../image/icon-colors/icons-mobile-yellow.png)

</td><td>

-   **Web variable**
    -   Option 1:`--now-color_grouped--yellow-2`
    -   Option 2:`--now-color_grouped--yellow-3`
    -   Option 3 \(Accessible\):`--now-color_grouped--yellow-4`

</td></tr></tbody>
</table>