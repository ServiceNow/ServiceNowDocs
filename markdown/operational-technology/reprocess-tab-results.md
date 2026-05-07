---
title: Reprocess Auto Query results
description: On the Settings page, the Reprocess tab is available to reprocess Auto Query results.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Reprocess Auto Query results

On the Settings page, the Reprocess tab is available to reprocess Auto Query results.

## Reprocess feature

The Reprocess feature allows the system to reevaluate previously collected Auto Query scan results using the latest query driver logic. This is useful when a query driver\(s\) is updated. Instead of rescanning devices, the system reuses existing stored scan results and processes them again. The results display on the Results page.

The Reprocess feature runs based on the configured schedule. As displayed in this table, you can schedule your configuration.

<table id="table_n5r_2z5_33c"><thead><tr><th>

Setting

</th><th>

Options

</th></tr></thead><tbody><tr><td>

Start time

</td><td>

Default: 12:00 AM UTC

</td></tr><tr><td>

Run Mode

</td><td>

-   Always
-   Only when the Query Driver version changes \(default setting\)

</td></tr><tr><td>

Scope

</td><td>

-   Results only
-   Results + Archived Results

</td></tr><tr><td>

Time range

</td><td>

Last 17 days, Last 30 days, or Custom. Default is the last 14 days.

</td></tr><tr><td>

Duration

</td><td>

Until completed or time-limited

</td></tr><tr><td>

Batch size

</td><td>

No default.

</td></tr><tr><td>

Enable?

</td><td>

Yes / No

</td></tr></tbody>
</table>After upgrading to a new query driver version, enable the Reprocess schedule to reevaluate recent scan results using improved logic.

![Settings>Reprocess tab](../images/reprocess-tab-edit.png)

