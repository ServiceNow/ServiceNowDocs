---
title: Configure additional capabilities in a record section
description: Define additional record section capabilities like the number of rows, specifying the card size, and the type of card-swiping action. These features are configured in the web-based UI as opposed to the Mobile App Builder.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure a record UI section, Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure additional capabilities in a record section

Define additional record section capabilities like the number of rows, specifying the card size, and the type of card-swiping action. These features are configured in the web-based UI as opposed to the Mobile App Builder.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_sg_item_section.list`, to open a list of record sections.

3.  Select a displayed record section.

4.  On the form, fill in the fields.

    **Note:** This table lists all features that are not yet available for configuration in the Mobile App Builder. For configurations available within Mobile App Builder, see [Configure a record UI section](sg-ui-section-config-item.md).

<table id="table_oqd_tzg_rrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scrolling type

</td><td>

Method by which users scroll through the mobile cards displayed in a row. The options are:-   **Free scroll** - Allows the user to scroll multiple cards with a single swipe.
-   **Snap to Start** - Causes the user to scroll one card at a time.
This field is available when you select **Horizontal** in the **Orientation** field.

</td></tr><tr><td>

Is custom size

</td><td>

Enables you to define the specific dimensions of cards within the record section. If this field is selected the **Card size** field does not display, instead the **Custom height** and **Custom width** fields display.

</td></tr><tr><td>

Custom height

</td><td>

The height of cards in the record section. The range is from 42 through 296 pixels. This field is available when you select the field **Is custom size**.

</td></tr><tr><td>

Custom width

</td><td>

The width of cards in the record section. The range is from 64 through 304 pixels. This field is available when you select the field **Is custom size**.

</td></tr><tr><td>

Card size

</td><td>

Size of card displayed in all rows. The following card sizes, in pixels, are available:-   **Small**: \(width 304 x height 108\)
-   **XSmall**: \(width 148 x height 184\)
-   **Medium**: \(width 304 x height 148\)
-   **Large**: \(width 304 x height 243\)
-   **XLarge**: \(width 304 x height 314\)
If the listed card sizes do not meet your requirements, you can customize a card size. For more information, see [Customize a card size for a record section](sg-ui-section-config-custom-card.md).This field is not available if you select the field **Is custom size**.

</td></tr><tr><td>

Row count

</td><td>

The number of rows displayed in each record section. You can have from 1 through 3 rows. Selecting **None** displays 1 row.This field is available when you select **Horizontal** in the **Orientation** field.

</td></tr><tr><td>

Column count

</td><td>

The number of columns displayed in each record section. You can display from 1 through 3 columns. Selecting **None** displays 1 column.This field is available when you select **Vertical** in the **Orientation** field.

</td></tr><tr><td>

Wide column count

</td><td>

This number of columns displayed in each record section for either larger devices like tablets or in landscape mode. You can display from 1 through 4 columns. Selecting **None** displays 1 column.This field is available when you select **Vertical** in the **Orientation** field.

 **Note:** The selection made in the **Wide column count** field must be greater than the number in the **Column count** field.

</td></tr></tbody>
</table>5.  Right-click in the header and select **Save**.


