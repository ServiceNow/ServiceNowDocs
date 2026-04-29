---
title: Customize fields for mapping location
description: Customize ad-hoc fields for setting location appropriate location for work orders pr work order tasks when you add location using map interface.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Locations, Set up workforce, Configure, Field Service Management]
---

# Customize fields for mapping location

Customize ad-hoc fields for setting location appropriate location for work orders pr work order tasks when you add location using map interface.

## Before you begin

Role required: wm\_admin

## About this task

You can customize the fields for a location that is added through map interface. This allows you to create and use locations more accurately for work orders.

For example, you can customize the location to add additional fields like **Sub-locality** or **Street 2** and map them appropriately with the location returned by map interface like Google map interface.

## Procedure

1.  Navigate to **All**, type `sys_ux_client_script_include.list`, and press Enter.

2.  From the UX Client Script Includes list, select `ResponseHandlerServiceLocation` client script include.

3.  On the UX Client Script Include form, edit the **Script** field to modify the script.

4.  Select **Update**.


## Result

The location table and records will be updated as per the customized location.

**Related topics**  


[Field Service with Service Locations Support components](../concept/service-locations-components.md)

[Assign ad-hoc Service Locations](../concept/field-service-with-service-locations.md)

