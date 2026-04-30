---
title: Create a neighborhood for workplace users
description: Create a neighborhood and assign users to available spaces in a neighborhood. Add or remove users in bulk and allocate available neighborhood spaces to users in a department, cost center, or group.
locale: en-US
release: yokohama
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-01-09"
reading_time_minutes: 2
breadcrumb: [Managing Neighborhoods, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Create a neighborhood for workplace users

Create a neighborhood and assign users to available spaces in a neighborhood. Add or remove users in bulk and allocate available neighborhood spaces to users in a department, cost center, or group.

## Before you begin

**Note:** Verify that Workplace Core is installed to set up and manage neighborhoods.

**Important:** If you’re using Workplace Space Management version1.11.1 or later, to add a user to the neighborhood, refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

**Important:** From Workplace Space Management version 1.11.1, the **Neighbourhood User Assignments** table is no longer available. Instead, the user assignment can be performed on a workplace profile directly using the **Workplace Profile Location Assignment** table \(displayed a related list on the form\) in the Workplace Core application. The **Workplace Profile Location Assignment** in the Workplace Core is now configured with additional fields such as **Profile type**, **Neighborhood**, and **Source** where all the data is saved. This table helps a space manager to perform scenario planning and save any user assignment-related changes performed on a neighborhood directly on the workplace profile.

On a neighborhood, when you configure a user assignment rule, the neighborhood assignment changes on the workplace profile are automatically saved on the user's workplace profile. On the user's workplace profile, you can check the type of assignment from the **Profile type** field.

If you’re an existing customer, upon upgrading, the entities in the **Neighbourhood User assignments** table are automatically migrated to the **Workplace Profile Location Assignment** of the user's workplace profile.

Role required: sn\_wsd\_core.admin, sn\_wsd\_core.workplace\_manager, sn\_wsd\_spcmgmt.space\_planner

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **Create New**.

    You can also create a neighborhood or update an existing neighborhood by navigating to **All** &gt; **Workplace Core** &gt; **Neighborhood.**

2.  On the form, fill in the fields.

<table id="table_zvh_pgg_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the neighborhood.

</td></tr><tr><td>

Active

</td><td>

Status of the neighborhood workplace location.The availability of a workplace location for any workplace-related activities is determined based on the status that is set. For more information, see [Change the status of a workplace location](change-active-status-of-workplace-location.md).

</td></tr><tr><td>

Restricted

</td><td>

A private or restricted neighborhood.If an employee is assigned to the neighborhood by user assignment rule or is added manually \(on-demand basis\), the employee can reserve a space in the neighborhood. Otherwise, employees won’t see the neighborhoods. see [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md).

</td></tr></tbody>
</table>3.  Select **Submit**.

    A neighborhood is created.


