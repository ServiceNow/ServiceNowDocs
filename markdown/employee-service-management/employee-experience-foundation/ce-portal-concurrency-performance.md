---
title: Portal Concurrency
description: Discover ways to improve performance and enhance portal concurrency content.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-04-25"
reading_time_minutes: 2
breadcrumb: [Managing portal performance, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Portal Concurrency

Discover ways to improve performance and enhance portal concurrency content.

Portal performance features seamlessly improve high concurrency content without sacrificing user functionality, and creates greater availability and flexibility to a larger number of users accessing content simultaneously.

**Note:** This feature only works for **Company Events**, and when **Optimize performance for high traffic volume** is selected.

![](../images/pc-optimize-performance-htv.png)

For more information on managing portal performance, see [Managing portal performance](improve-manage.md).

|sn\_cd\_precomputed\_audience-list|
|Column name|Column type|Description|
|----------------------------------|
|-----------|-----------|-----------|
|User|Reference \(sys\_user\)|The user associated to this precompute record|
|Content|Reference \(sn\_cd\_content\_base\)|The content the user has access to|
|Domain|Sys Domain|Domain separation field|

**Note:** The data in the table should only be added through the Sync flow and should not be manually changed.

## Precompute Flow for Automatic Sync Trigger

1.  New Scheduled Job exists titled **Content Publishing: Precompute Audiences for Company Events** that is scheduled to run every 24 hours at 00:30.
2.  When job triggers, check all high traffic company events from the current hour to the next 30 hours.
3.  For each event that is found, precompute the audience to record the user and the content in the precompute table.
4.  Check the Scheduled Job titled **Content Publishing: Precompute Audiences for Company Events** for the precompute flow cleanup.
5.  When job triggers, calculate unique events among existing precompute audience records.
6.  For each company event calculated, check if it has ended. If ended, delete all precompute records associated to it.

<table id="table_ktn_r2z_cfc"><thead><tr><th colspan="2">

Precompute Flow Examples

</th></tr></thead><tbody><tr><td>

Full manual sync

</td><td>

A system admin can manually run the Scheduled Job **Content Publishing: Precompute Audiences for Company Events** to fully sync the precomputed audience table.

</td></tr><tr><td>

Partial manual sync

</td><td>

A Content Admin can browse to the **sn\_cd\_company\_event** table, find a specific event, and select the **Precompute Audiences for this Content** UI Action.

 **Note:** This only removes users who don’t belong in a content audience anymore and is used in last minute cases to ensure only users who should have access can view content.

</td></tr></tbody>
</table>## Precomputed Audience Check Flow

1.  User accesses a Company Event with high traffic performance optimization enabled.
2.  Performance optimization check is initiated.
    1.  Queries precompute audience table with content ID and current user ID.
    2.  If a user is found, start loading the article.
    3.  If no user is found, initiate standard access check.

## Standard Audience Check Flow

**Note:** The standard audience check is the current state and is still used in cases when precompute is not in use.

1.  User accesses a Company Event.
2.  Access check is initiated.
    1.  Queries schedule content table for each schedule associated to the content being viewed.
    2.  For each schedule content record, iterate each associated audience.
    3.  For each audience, run**.isUserInAudience\(\)**. This evaluates if the current user is in the audience.
    4.  If a user is found, start loading the article.
    5.  If no user is found, iterate each audience associated for each schedule content record.
    6.  If a user is never found, show the empty state article detail page.

**Parent Topic:**[Managing portal performance](improve-manage.md)

