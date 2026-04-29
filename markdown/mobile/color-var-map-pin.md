---
title: Color variable support for map icons
description: Learn how to use color variables to change theming in your mobile map icons
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Color theme considerations, Configure theming, Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for map icons

Learn how to use color variables to change theming in your mobile map icons

<table id="table_q2w_llb_yvb"><tbody><tr><td>

Map screens have a **Pin Color** section with a **Pin color variable** field to control the color map pins using a color variable. A map pin is used on the map template screen, to indicate points of interest on the map.

 Using this field you can define any color variable from the UX Theme Properties \[sys\_ux\_theme\_property\] table. For a list available variables see the color design guide below.

 For details on creating icon UI sections, see [Configure an icon UI section](../task/sg-ui-section-config-navig.md).

</td><td>

![Pin color showing the color labeled as Primary 1.](../image/color-var-example-3.png)

</td></tr></tbody>
</table>## Color design guide for map pins

<table id="table_tkv_qth_cxb"><thead><tr><th>

Color name

</th><th>

Pin example

</th><th>

Color options

</th></tr></thead><tbody><tr><td>

Primary

</td><td>

![Primary mobile pin](../image/icon-colors/icon-map-pin-primary.png)

</td><td>

-   **Mobile variable**

primary

-   **Web variable**

`--now-color--primary-1`


</td></tr><tr><td>

Secondary

</td><td>

![Secondary mobile pin](../image/icon-colors/icon-map-pin-secondary.png)

</td><td>

-   **Mobile variable**

secondary

-   **Web variable**

`--now-color--secondary-3`


</td></tr><tr><td>

Tertiary

</td><td>

![Tertiary mobile pin](../image/icon-colors/icon-map-pin-tertiary.png)

</td><td>

-   **Mobile variable**

tertiary

-   **Web variable**

`--now-color_grouped--gray-4`


</td></tr><tr><td>

Brand

</td><td>

![Brand mobile pin](../image/icon-colors/icon-map-pin-brand.png)

</td><td>

-   **Mobile variable**

brand

-   **Web variable**

`--now-color_brand--secondary`


</td></tr></tbody>
</table>