---
title: Create discovery job
description: Create and schedule a new Data Discovery Store job.
locale: en-US
release: zurich
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Discovery scheduled discovery, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Create discovery job

Create and schedule a new Data Discovery Store job.

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Scheduled Discovery**.

2.  Select **Discovery Jobs** in the right side navigation pane.

3.  Fill in the form.

<table id="table_qqp_lgg_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the job.

</td></tr><tr><td>

Description

</td><td>

Description of the job.

</td></tr><tr><td>

Scan Type

</td><td>

Number of entries to be scanned. Possible states are as follows:-   **Sample**: Scans 10,000 entries.
-   **Full**: Scans all entries.


</td></tr><tr><td>

Select policy

</td><td>

The policy to use for the scheduled job.

</td></tr><tr><td>

Start Date

</td><td>

Sets the start date for the job.

</td></tr><tr><td>

Time window start

</td><td>

The start of the time window to run this job. The job will run after the time entered in this field. The time entered in the **Time window start** field must happen before the time entered in the **Time window end** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr><tr><td>

Time window end

</td><td>

The end of the time window to run this job. The job runs until the time entered in this field. If the job hasn't complete this time, the job pauses and resumes at the next time window start. The time entered in the **Time window end** field must happen after the time entered in the **Time window start** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr></tbody>
</table>4.  Select the **Schedule** button.


