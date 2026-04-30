---
title: Business rules installed with Facilities Service Management
description: A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Installed with Facilities Service Management, Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Business rules installed with Facilities Service Management

A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.

Facilities Service Management adds the following business rules.

<table id="table_ngl_zwx_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Building Utilization

</td><td>

Building\[alm\_building\]

</td><td>

Ensures that utilization thresholds are set to numbers from 0 through 100.

</td></tr><tr><td>

Update User Primary Location

</td><td>

Associated User\[fm\_m2m\_user\_to\_space\]

</td><td>

Updates the sys user records location to the current primary location for the user in the fm\_m2m\_user\_to\_space table.

</td></tr><tr><td>

Reference Area

</td><td>

Facility Space\[fm\_space\]

</td><td>

Calculates the area in common units for the space.

</td></tr><tr><td>

Prevent ancestry loop

</td><td>

Facility Space\[fm\_space\]

</td><td>

Prevents circular space definitions where a space is both a parent and child at the same time.

</td></tr><tr><td>

Rollup

</td><td>

Facility Space\[fm\_space\]

</td><td>

Rolls up the space information to level as info is changed on the space.

</td></tr><tr><td>

Rollup

</td><td>

Level\[fm\_level\]

</td><td>

Rolls up level information to the building.

</td></tr><tr><td>

Floor Utilization

</td><td>

Level\[fm\_level\]

</td><td>

Ensures that utilization thresholds are set to numbers from 0 through 100.

</td></tr><tr><td>

Rollup

</td><td>

Associated User\[fm\_m2m\_user\_to\_space\]

</td><td>

Updates the space utilization on a space as users are added and removed from spaces.

</td></tr><tr><td>

Reference area

</td><td>

Campus\[fm\_campus\]

</td><td>

Calculates the area in common units for the space.

</td></tr><tr><td>

update space display name

</td><td>

Building\[alm\_building\]

</td><td>

Generates the full display name for the space.

</td></tr><tr><td>

Max Occupancy

</td><td>

Building\[alm\_building\]

</td><td>

Max occupancy cannot be less than 0.

</td></tr><tr><td>

Rollup

</td><td>

Building\[alm\_building\]

</td><td>

Rolls up building data to the campus.

</td></tr><tr><td>

Request Autoclose

</td><td>

Facilities Request\[facilities\_request\]

</td><td>

Automatically closes requests that are resolved and have not been updated in the 1 day. This number is a property in System Properties.

</td></tr><tr><td>

Facilities Primary Location Change

</td><td>

User\[sys\_user\]

</td><td>

Updates the fm\_m2m\_user\_to\_space table when the location on the sys\_user records changes.

</td></tr><tr><td>

Max Occupancy

</td><td>

Facility Space\[fm\_space\]

</td><td>

Max occupancy cannot be less than 0.

</td></tr><tr><td>

Prevent duplicates

</td><td>

Facility Zone \[fm\_zone\]

</td><td>

Do not allow the same space to be added to a single zone more than once.

</td></tr><tr><td>

Prevent duplicates

</td><td>

Associated User\[fm\_m2m\_user\_to\_space\]

</td><td>

Do not allow the same user to be added to the same space more than once.

</td></tr><tr><td>

Prevent multiple main level for building

</td><td>

Level\[fm\_level\]

</td><td>

Do not allow there to be more than one main level set for levels in a building.

</td></tr><tr><td>

Update primary location

</td><td>

Associated User\[fm\_m2m\_user\_to\_space\]

</td><td>

Helps keep the sys user and fm\_m2m\_users\_to\_space tables in synchronization when primary location changes.

</td></tr><tr><td>

Facilities area unit option changed

</td><td>

Facility Space\[fm\_space\]

</td><td>

Converts\` square feet to square meters

</td></tr><tr><td>

update space display name

</td><td>

Level\[fm\_level\]

</td><td>

Updates display name as building and level name changes

</td></tr><tr><td>

Reference Area

</td><td>

Facility Space\[fm\_space\]

</td><td>

Calculates the area in common units for the spaces.

</td></tr><tr><td>

Max Occupancy

</td><td>

Facility Space\[fm\_space\]

</td><td>

Max occupancy cannot be less than 0.

</td></tr><tr><td>

Reference Area

</td><td>

Facility Space\[fm\_space\]

</td><td>

Calculates the area in common units for the space.

</td></tr><tr><td>

Space - generate full name

</td><td>

Facility Space\[fm\_space\]

</td><td>

Generates the full display name for the space.

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Service Management](r_InstallWFacServMgmnt.md)

