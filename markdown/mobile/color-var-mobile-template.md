---
title: Color variable support for card view templates
description: Learn how to use color variables to change theming in your mobile card views.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Color theme considerations, Configure theming, Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Color variable support for card view templates

Learn how to use color variables to change theming in your mobile card views.

<table id="table_zbt_vzd_zvb"><tbody><tr><td>

Card view templates use the values in the **Template JSON** field to determine the appearance of a card. Use the following properties to include color variables in your cards.

 -   Text: TextColorVariable
-   Background: ColorVariable
-   HTMLText: TextColorVariable
-   Standalone Icons: TextColorVariable
-   Viewgroup: BackgroundColorVariable
-   Onselect \(defined in root-view attribute JSON\): TextColorVariable and BackgroundColorVariable

 Use these properties to assign a color using color variables from the UX Theme Properties \[sys\_ux\_theme\_property\] table.

 For details creating card templates, see [Create a card template with Mobile Card Builder](../task/mcb-create-template.md).

</td><td>

![Color variable used in a card view template](../image/color-var-example-5.png)

</td></tr></tbody>
</table>