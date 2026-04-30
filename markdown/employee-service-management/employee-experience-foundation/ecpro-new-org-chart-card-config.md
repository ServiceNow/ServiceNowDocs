---
title: Configure card settings for org chart
description: Define the lines and information to show on the Employee Center Pro org chart card.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Org Chart Configuration]
breadcrumb: [Organization chart in Employee Center Pro, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure card settings for org chart

Define the lines and information to show on the Employee Center Pro org chart card.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

Use **Org Chart Card Configuration** to define information to display on the chart. Define one user card configuration on the same table as the one used in the eligible user configuration.

**Note:** New hires appear in an org chart during the onboarding and when a sys\_user record is created. You may configure the conditions to suit your business requirements.

You can configure two primary and six secondary slots of information on the card of an employee. Information is configured by selection or dot-walking the fields from the Employee Profile \[sn\_employee\_profile\], HR Profile \[sn\_hr\_core\_profile\], or User \[sys\_user\] tables.

## Procedure

1.  Navigate to **Employee Center** &gt; **Organization Chart** &gt; **User display** &gt; **Org Chart Configurations Card**.

2.  On the form, fill in the fields.

<table id="table_app_yj5_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user display configuration record.

</td></tr><tr><td>

Application

</td><td>

Application that you want to configure the activity for.

</td></tr><tr><td>

Table

</td><td>

Table that the user display configuration record is associated with.

</td></tr><tr><td>

Show preferred pronoun

</td><td>

Option to show the preferred pronoun from the employee profile of the user on the org chart. Pronouns field appears only when you select the employee profile table.

</td></tr><tr><td>

Primary display fields

</td><td>

Primary fields to display on the org chart card. For Employee profile, defaults are user.name and user.title. Primary display fields appear on all user cards that includes the manager hierarchy, selected user card and direct reports, if any. User search results also display the information as per the primary display fields.**Note:** Configure two primary display fields.

</td></tr><tr><td>

Action group

</td><td>

Group of quick actions defined for org chart. For **Org Chart Group**, you can use actions such as view profile, email, or call. For more information, see

</td></tr><tr><td>

Order

</td><td>

Enter the order number to determine where the item appears in relation to other items

</td></tr></tbody>
</table>3.  Click **Save**.

4.  On the secondary field form, specify the required org chart fields configuration such as **icon** and **display field** to display as secondary fields on the selected employee card.

    **Note:** Configure upto six secondary display fields.

5.  Click **Submit** or **Update**.


## What to do next

For more information on widget instance options, see [Modify the org chart widget display](config-orgchart-instanceoptions.md).

