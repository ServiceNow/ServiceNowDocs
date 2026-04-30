---
title: Configure eligible users
description: Define the eligible users to show up in the org chart. Admin can create a new eligible user configuration from one of the Users, HR Profile, and Employee Profile tables.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Organization chart in Employee Center Pro, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Configure eligible users

Define the eligible users to show up in the org chart. Admin can create a new eligible user configuration from one of the Users, HR Profile, and Employee Profile tables.

## Before you begin

An active eligible user configuration is a condition that determines who can appear on the org chart. You can have only one active eligible user configuration per domain. Ensure you have only one active configuration.

Role required: sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **Employee Center** &gt; **Organization Chart** &gt; **Eligible users**.

2.  Click **New** or open an existing record.

3.  On the form, fill in the fields.

<table id="table_app_yj5_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the eligible user configuration record.

</td></tr><tr><td>

Order

</td><td>

Enter the order number to determine where the item appears in relation to other items

</td></tr><tr><td>

Application

</td><td>

Application that you want to configure the activity for.

</td></tr><tr><td>

Active

</td><td>

Option to activate the eligible user configuration record for use. Ensure you have only one active configuration for eligible users.

</td></tr><tr><td>

Table

</td><td>

Table that the eligible user configuration record is associated with. You can select from one of the following tables:-   Default: Employee Profile
-   HR Profile: The HR profile table appears only when you install the Human Resources \[com.sn\_hr\_core\] plugin.
-   Users
 **Note:** To display all users in your organization, you can model your eligible users on Users or HR Profile.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that a user must meet to be an eligible user. For example, you can select users who are **Active** or employees joining the organization after a certain start date.

</td></tr></tbody>
</table>4.  Click **Save**.


## Result

Based on this configuration, only the eligible users appear in the Org Chart widget.

**Note:** When you have multiple eligible user configurations, ensure you deactivate the current active definition before activating the other.

## What to do next

A scheduled job populates the direct and otherreport count periodically. You can run the **Populate Manager Reportee Count Using Eligible Users \(Domain separated\)** scheduled job on-demand to update the report count at any time. The counts change based on the eligible users or employee status. For more information on running the job, see [Update the report count based on eligible users](update-report-count.md).

When an employee with direct reports becomes ineligible, the direct reports are tagged to the manager of such ineligible employee.

