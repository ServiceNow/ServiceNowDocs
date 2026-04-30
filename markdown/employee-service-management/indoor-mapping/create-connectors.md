---
title: Create a connector type
description: Create connectors \(stairs, elevators, escalators, ramps\) and activate the connector type in the View editor. Connector Type contains the style \(icon\) and properties for each connector.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage Directions, Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Create a connector type

Create connectors \(stairs, elevators, escalators, ramps\) and activate the connector type in the View editor. Connector Type contains the style \(icon\) and properties for each connector.

## Before you begin

Indoor Mapping provides Connector Types that are enabled by default. You can create a new connector type depending on your requirement.

Role required: map admin, map editor, map editor limited

## Procedure

1.  To create an icon for your connector type, navigate to **All** &gt; **Indoor Mapping** &gt; **Icons**.

    Indoor Mapping provides a pre-existing icon library. To edit an existing icon, select an icon record and apply your edits. For more information, see [Create Indoor Mapping icons and place types](place-icons-place-type.md).

2.  After creating your icon, navigate to **All** &gt; **Indoor Mapping** &gt; **Connector types**.

    You can edit an existing connector type by selecting the record and applying your edits.

3.  Select **New** to create a new connector type.

    ![Create connectors](../images/manage-directions-2.png)

    On the form, fill in the fields.

<table id="table_wdj_c32_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connector type. For example: ElevatorThe Name will be displayed in the drop-down list when you create a new connector in Map Studio.

</td></tr><tr><td>

Default wait time

</td><td>

Indicate the default wait time. For example: 30

</td></tr><tr><td>

Default time per floor

</td><td>

Default time per floor. For example: 5

</td></tr><tr><td>

Default marker icon

</td><td>

You must search and select the icon type for the connector For example: Elevator

</td></tr><tr><td>

Active

</td><td>

Option to make the connector type active. If you clear the check box, then your connector type will be automatically deactivated on your different maps. **Note:** Turning off the connector type does not remove it. It will be made inactive on your map and there will be no connector display on your maps until it is activated again.

</td></tr><tr><td>

Default order

</td><td>

Specify the default order for the connector type.

</td></tr><tr><td>

Default maximum zoom

</td><td>

Default value is 23.

</td></tr><tr><td>

Default minimum zoom

</td><td>

Default value is 15.

</td></tr><tr><td>

Default marker display

</td><td>

Option to select the default marker display.

</td></tr><tr><td>

Default direction

</td><td>

Select any of the following from the drop-down list:-   Up
-   Down
-   Up and down


</td></tr></tbody>
</table>4.  Click **Submit**.

    The new connector type is available on the Connector types page.

5.  To activate the connector type in the View editor so that it is available for all your buildings, navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

6.  Select a campus, and on the Map Studio menu, select **View Editor**.

7.  From the View Editor content panel on the left pane, select **+Add Connector** to add the newly added connector.

8.  Select the connector type that you added in Step 3.

9.  Click **Apply**.

10. Select **Save this view** to save your changes.


**Parent Topic:**[Manage Directions](enable-interactive-locations.md)

