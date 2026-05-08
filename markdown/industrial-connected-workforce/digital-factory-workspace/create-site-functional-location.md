---
title: Create a functional location of the type site
description: Create a location for your user to be able to work with the Industrial Connected Workforce \(ICW\).
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prerequisites, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a functional location of the type site

Create a location for your user to be able to work with the Industrial Connected Workforce \(ICW\).

## Before you begin

Role required: sn\_icw.application\_admin

## About this task

The location is the site. Every user must set their location in the user profile to be able to work with ICW. In addition, the filter on task forms works based on the location.

## Procedure

1.  Create a location.

    1.  Navigate to **All** &gt; **User administration** &gt; **Locations**.

    2.  Select **New**.

    3.  On the Location form, enter the location name, address, contact, and other location details.

    4.  Select **Submit**.

2.  Create a functional location for your site.

    1.  Navigate to **All** &gt; **Equipment Model - ISA** &gt; **Equipment Model Entities**.

    2.  Select **New**.

    3.  On the Equipment Model Entity form, enter the details.

        Make sure that you select ISA 95 Default Template for the template and Site for the level.

    4.  Select **Save**.

3.  Create a timezone for the functional location of your site.

    1.  Navigate to the location record associated with the site of the functional location.

    2.  In the **Timezone** field, select the timezone that corresponds to the factory's physical location.

    3.  Save the location record.


## Result

The functional location of the type site is available in the Digital Factory Workspace, from where you can create child functional locations.

**Parent Topic:**[Setting up prerequisites for Digital Factory Workspace](../concept/setting-up-prerequisites-digital-factory-workspace.md)

**Related topics**  


[bundle-optm.equipment-model-workspace]

