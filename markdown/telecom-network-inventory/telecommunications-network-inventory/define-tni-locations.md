---
title: Define a location hierarchy
description: Define a location hierarchy for your Telecommunications Network Inventory forms so that you can track and manage your network assets. By defining a location hierarchy, you can see where all your network equipment is located.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Telecommunications Network Inventory]
---

# Define a location hierarchy

Define a location hierarchy for your Telecommunications Network Inventory forms so that you can track and manage your network assets. By defining a location hierarchy, you can see where all your network equipment is located.

## Before you begin

-   Role required: admin, sn\_ni\_core.inventory\_admin
-   To establish locations hierarchy, ensure to:
    1.  Create the top-level locations that contain the subordinate locations. For example, in the locations hierarchy, create `Americas` first. Leave the **Parent** field empty.
    2.  Create a regional location and in the **Parent** field, select the top-level location as its parent. For example, in the locations hierarchy, create `North America` and then select `Americas` as its parent.
    3.  In the Locations section at the bottom of the form, click **New** and create the location records for each lower-level child location that are subordinate to that regional location.

## About this task

A location record must contain at least one of the following properties or sets of properties:

-   Address
-   Country
-   Region
-   Latitude and Longitude

By using this form, you can construct a location hierarchy. For example, the following example shows a typical location hierarchy that appears when you search for a location in the **Location** field in the Network Site form.

![Locations hierarchy view with the list of locations.](../image/locations-hierarchy.png "Locations hierarchy")

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Locations**.

2.  Select **New**.

3.  On the Location form, fill in the fields, with address and contact information for the location record.

    **Note:** To learn more about the fields on the Locations form, see [Location form](../reference/tni-location-forms.md#).

4.  Click **Submit**.


**Parent Topic:**[Configuring Telecommunications Network Inventory](../concept/configuring-telecom-network-inventory.md)

