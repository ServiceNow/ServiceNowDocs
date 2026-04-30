---
title: Create appearance templates for cards for a mobile campaign
description: Create item card templates that contain information about the appearance of each type of card displayed in a mobile campaign.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Displaying campaigns, Configuring the Mobile Platform, Mobile Platform]
---

# Create appearance templates for cards for a mobile campaign

Create item card templates that contain information about the appearance of each type of card displayed in a mobile campaign.

## Before you begin

Role required: admin

## About this task

When creating cards, you need to assign an item view. Item views provide information about a card's appearance. Therefore, for each card style you want to use, you need a create a separate item view even if the card type is the same. For example, if you want some image cards to have light text on a dark background and other image cards to have dark text on a light background, you would need to create a separate item view for each of those styles.

## Procedure

1.  In the web-based UI, enter `sys_sg_item_view.list` in the filter navigator to open a list of item views.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_psj_wlf_mmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the item view.**Note:** For easy identification, include the card type \(image, text, or video\) in the name.

</td></tr><tr><td>

Short Description

</td><td>

Optional additional details.

</td></tr><tr><td>

Item view JSON

</td><td>

The configuration code you created for the card type. For more information, see [Configure the details for the appearance of cards for a mobile campaign](../reference/mobile-campaign-card-config.md).

</td></tr><tr><td>

Table

</td><td>

The Employee Center table \[`sn_cd_content_mobile`\], which contains the content of the cards.

</td></tr><tr><td>

Dependency fields

</td><td>

Dependency fields taken from data entered in the **Item view JSON** field.

</td></tr><tr><td>

UI Styles

</td><td>

UI styles to apply to text cards. For information about how to configure the font color and background color for text cards, see [Mobile UI styles](../concept/mobile-ui-styles.md).

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

After creating item views for each card style, you need to build and link components to display your mobile campaign. For more information, see [Configure mobile campaign components](mobile-campaign-create.md).

