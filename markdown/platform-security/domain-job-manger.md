---
title: Domain Job Management
description: Queue multiple Domain Separation updates sequentially into a single background job using the Domain Job Manager.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Domain Job Management

Queue multiple Domain Separation updates sequentially into a single background job using the Domain Job Manager.

When a Domain record is modified such as reparenting or a change in hierarchy, by default, a job executes to fix all the records in domain separated tables. You can control when this behavior occurs with the **Domain Job Manager** and monitor ongoing job progress with the **View Job Progress** button.

Use the **Domain Job Manager** to pause domain jobs, queue multiple domain table changes and trigger the queued job when ready with all the changes.

|Label|Description|
|-----|-----------|
|Job Type|The current job type|
|Status|The status of the job, see **Job state** in the job manager for more information.|
|Progress|Ongoing job progress|

<table id="table_bmp_5jj_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Job Type

</td><td>

Support job types:Hierarchy change

</td></tr><tr><td>

Job State

</td><td>

-   Active
-   Paused

**Note:** By default paused jobs will auto resume in 1 hour. Check this option to disable this and manually activate the job later


</td></tr></tbody>
</table>