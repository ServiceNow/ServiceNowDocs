---
title: Set the location type in Location table
description: Set the location type of a location by creating a dictionary override of the table.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Location migration, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Set the location type in Location table

Set the location type of a location by creating a dictionary override of the table.

## Before you begin

Role required: admin

## About this task

When you create a location in the Workplace Core application, that location is automatically added in the ServiceNow® Location \[cmn\_location\] table. The Location type of that location is set based on the Dictionary Overrides. The Dictionary Overrides are configured for all location tables such as Site, Region, Campus, Building, Floor, Area, and Room, except for the Space table. To set the Location type of the Space table, you can add a choice in the Location type and use it in the Space table’s Location type dictionary override.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the **Location \[cmn\_location\]** table.

3.  In the Columns related list, select **Location type**.

4.  In the Location type Dictionary Entry form, scroll down to the Dictionary Overrides related list.

5.  Select the Dictionary Entry Override that you want to view or edit.

6.  Edit the override by changing the **Default value**.

    The Location type of the locations that are created in the Workplace Core are set as per the specified default value. For example, if you have changed the default value of the Region Dictionary Entry Override to Zone, then the new locations created as a Region are set with the Location type as Zone.

7.  If there is no default value that suits the location type, add a default value.

    1.  In the Location type Dictionary Entry form, select the Choices related list.

    2.  Click **New**.

    3.  Specify the choice details.

        The choice is added. The choice is displayed while specifying a default value.


## Result

The location type is set for the selected location table.

**Parent Topic:**[Location migration](../concept/location-migration.md)

