---
title: Query Generation properties
description: The properties included with Query Generation apply to segments. They define whether the record or indicator that is the basis for a segment has been recently used or changed.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-03"
reading_time_minutes: 3
breadcrumb: [Reference, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Query Generation properties

The properties included with Query Generation apply to segments. They define whether the record or indicator that is the basis for a segment has been recently used or changed.

These properties are available for Query Generation.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_v5w_l2h_23c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_query\_gen.hidden\_insights.groupby.min\_fields

</td><td>

The target number of group-by fields for extended analysis in AI Data Explorer. These group-by fields are taken from the default list view of the relevant table. When this list view contains fewer eligible fields than the property value, the system looks for more eligible fields on the table to try to reach this count.

-   Type: Integer
-   Default value: 5
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Extended analysis](hidden-insights.md)

</td></tr><tr><td>

sn\_query\_gen.segment\_enabled

</td><td>

When set to true, segments are created and used. When false, no segments are created, and all existing segments are excluded from AI Data Explorer search results. During the next Sync Segments Job, all segments are deactivated.-   Type: Boolean \(true/false\)
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.filter

</td><td>

When set to true, excludes all segments from sys\_filter from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.manual\_segment

</td><td>

When set to true, excludes all segments from sn\_query\_gen\_segment\_table\_config \(manual segments\) from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

 **Note:** The ability to disable manual segments is intended for testing and troubleshooting purposes.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.pa\_cubes

</td><td>

When set to true, excludes all segments from indicator sources \(pa\_cubes\) from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.report

</td><td>

When set to true, excludes all segments from sys\_reports from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.report\_sources

</td><td>

When set to true, excludes all segments from sys\_report\_source from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.disable.sys\_app\_module

</td><td>

When set to true, excludes all segments from sys\_app\_module from AI Data Explorer search results. During the next Sync Segments Job, all segments of that type are deactivated in the Segment table.

-   Type: Boolean \(true/false\)
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.indicator.inactivity\_threshold\_multiplier

</td><td>

Applies a multiplier to how long ago an indicator value can have changed for that indicator to be "recently changed." The \[Query Generation\] Sync Segments job deactivates segments based on indicators that have not recently changed. The value that is multiplied differs by indicator frequency \(see \).-   Type: Integer
-   Default value: 1
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr><tr><td>

sn\_query\_gen.segments.reports.last\_viewed\_threshold\_days

</td><td>

Defines how many days ago a report can have run for that report to be considered "recently run." The \[Query Generation\] Sync Segments job deactivates segments based on reports that have not run recently. It also deactivates report sources whose reports have not run recently.-   Type: Integer
-   Default value: 180
-   Location: System Property \[sys\_properties\] table
-   Learn more: 

</td></tr></tbody>
</table>**Parent Topic:**[Query Generation reference](query-generation-reference.md)

