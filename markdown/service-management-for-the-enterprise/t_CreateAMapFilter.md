---
title: Create a map filter in Facilities Service Management
description: Create a custom filter to highlight spaces on a map for fast and easy recognition. You can create custom filters for any mappable space \(fm\_space\), asset, associated user, CI, or task with a location defined.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Map filters, Interactive facility maps, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Create a map filter in Facilities Service Management

Create a custom filter to highlight spaces on a map for fast and easy recognition. You can create custom filters for any mappable space \(fm\_space\), asset, associated user, CI, or task with a location defined.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space Management** &gt; **Map Configuration** &gt; **Filters**.

2.  Click **New** or an existing map filter.

3.  Complete or edit the form.

    Map Filter form

<table id="table_zvv_lgq_hbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the map filter.

</td></tr><tr><td>

Table

</td><td>

Table that the map filter is accessing information from.

</td></tr><tr><td>

Location field

</td><td>

Fields from the table selected when the table is not associated with a location. **Note:** The table selected determines which fields show. You can dot-walk to any field from the selected table.

</td></tr><tr><td>

Group by

</td><td>

Field that the map filter groups by. You can color each matching space based on this group.For example, you can group by availability status from the Facility Space \[fm\_space\] table.

 **Note:** The table selected determines which fields show. You can dot-walk to any field from the selected table.

</td></tr><tr><td>

Condition

</td><td>

Conditions that define the map filter. The table selected determines what conditions are available.

</td></tr><tr><td>

Public

</td><td>

Filter is available to others.

</td></tr><tr><td>

Roles

</td><td>

Roles required to view this filter on the workbench.

</td></tr><tr><td>

Description

</td><td>

Description of the map filter.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## What to do next

After you create a filter, click the **Show on Floor Plan** related link to view the map filter on a map.

**Parent Topic:**[Map filters](../reference/r_MapFilters.md)

**Related topics**  


[Simple filters](../reference/r_SimpleFilters.md)

[Saved filters](../reference/r_SavedFilters.md)

