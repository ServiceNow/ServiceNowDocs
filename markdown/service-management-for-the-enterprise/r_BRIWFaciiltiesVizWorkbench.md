---
title: Business rules installed with Facilities Visualization Workbench
description: A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installed with Facilities Visualization Workbench, Activate Facilities Visualization Workbench, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Business rules installed with Facilities Visualization Workbench

A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.

Facilities visualization workbench adds the following business rules.

<table id="table_ngl_zwx_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update default campus

</td><td>

Campus\[fm\_campus\]

</td><td>

Ensures one default campus

</td></tr><tr><td>

Prevent duplicates

</td><td>

Facility Map Option\[fm\_map\_option\]

</td><td>

Prevents duplicate map options

</td></tr><tr><td>

Max search results per campus &lt; 50

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the maximum search results to less than 50

</td></tr><tr><td>

Max spaces per zone &lt; 1000

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the number of spaces per zone to 1000

</td></tr><tr><td>

Build Scratchpad

</td><td>

Facilities Map Filter\[fm\_map\_filter\]

</td><td>

Provides a list of tables that are extended from fm\_spaces. Used by the Hide field for space tables client script.

</td></tr><tr><td>

Prevent duplicates

</td><td>

Facility Map Color\[fm\_map\_color\]

</td><td>

Prevents duplicate map colors

</td></tr><tr><td>

Prevent duplicates

</td><td>

Facility Map Task Option\[fm\_map\_task\]

</td><td>

Prevents duplicate map task options

</td></tr><tr><td>

Facility map highlight color validation

</td><td>

System Property\[sys\_properties\]

</td><td>

Validates the highlight colors on the floor plan map

</td></tr><tr><td>

Facility map color validation

</td><td>

Facility Map Color\[fm\_map\_color\]

</td><td>

Validates the colors on the floor plan map

</td></tr><tr><td>

Max facilities/move search results&lt; 5000

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the maximum facilities move search results to less than 5000

</td></tr><tr><td>

Prevent duplicate

</td><td>

Facility Feature\[fm\_facility\_feature\]

</td><td>

Prevents duplicate facility features

</td></tr><tr><td>

Create spaces requires default class

</td><td>

Facility Feature\[fm\_facility\_feature\]

</td><td>

Prevents empty class by default on a space

</td></tr><tr><td>

Facility map outline color validation

</td><td>

System Property\[sys\_properties\]

</td><td>

Validates the outline colors on the floor plan map

</td></tr><tr><td>

Max requests per level should be &lt; 5000

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the number of requests per level to 5000

</td></tr><tr><td>

Prevent duplicate

</td><td>

Facility Icon\[fm\_icon\]

</td><td>

Prevents duplicate facility icons

</td></tr><tr><td>

Max search results for other campuses

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the maximum search results for other campuses

</td></tr><tr><td>

Max search results per level &lt; 50

</td><td>

System Property\[sys\_properties\]

</td><td>

Limits the maximum search results per level to less than 50

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Visualization Workbench](r_InstallWFacVisWorkbench.md)

