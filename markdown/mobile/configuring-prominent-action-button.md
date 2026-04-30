---
title: Configuring a prominent action button
description: Configure a prominent action button for quick access to Now Assist.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configuring a prominent action button

Configure a prominent action button for quick access to Now Assist.

## Before you begin

Role required: admin

**Note:** You can only have one prominent action button per app type.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

2.  Select **New** to create a new button instance.

3.  Complete the following fields:

<table id="table_g1w_fn3_nhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the button.

</td></tr><tr><td>

Description

</td><td>

Additional information about the button.

</td></tr><tr><td>

Parent

</td><td>

The button's app type.

</td></tr><tr><td>

Application

</td><td>

The application in which your button resides.

 **Note:** This field is auto-populated.

</td></tr><tr><td>

Parent table

</td><td>

Table where the button gets its data.

 Select the Mobile app config \[**sys\_sg\_native\_client**\] table.

</td></tr><tr><td>

Function

</td><td>

Function performed by this button instance.

</td></tr><tr><td>

Label

</td><td>

Label that displays for the button.

</td></tr><tr><td>

Location

</td><td>

The place where the button resides.

 Select **Prominent Action**.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your button.

</td></tr><tr><td>

Order

</td><td>

The order in which the button appears on the screen compared to other buttons.

</td></tr><tr><td>

Active

</td><td>

Select whether the button is active or not.

</td></tr></tbody>
</table>4.  Configure a badge count by navigating to the table and setting your **Location** to **Prominent Action Button**.

5.  Select **Submit** to save your button record.


**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)

