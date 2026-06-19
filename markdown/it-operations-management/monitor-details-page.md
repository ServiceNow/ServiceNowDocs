---
title: Details page of a synthetic monitor
description: Use the details page of a synthetic monitor to view test results, monitor status, and configuration settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/monitor-details-page.html
release: australia
topic_type: reference
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Details page of a synthetic monitor

Use the details page of a synthetic monitor to view test results, monitor status, and configuration settings.

## Header

The header provides an overview of the monitor.

<table id="table_tts_tjt_ydc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Monitor name

</td><td>

Name given to the monitor when it was created.

</td></tr><tr><td>

Enabled

</td><td>

Indication of whether the monitor is active.

</td></tr><tr><td>

Status

</td><td>

Status of the latest test run. Values can be one of the following:-   Pending: The monitor is waiting for the first test to run, based on the configured frequency.
-   Success: The test ran and passed the assertion criteria that you set.
-   Failure: The test ran but didn't pass the assertion criteria. Select a timestamp link to view the response body for more information about the test.

</td></tr><tr><td>

Last test ran

</td><td>

Timestamp for when the latest test finished running.

</td></tr><tr><td>

Last updated

</td><td>

Timestamp for when the monitor was most recently edited and saved.

</td></tr></tbody>
</table>## Overview tab

The **Overview** tab provides an aggregated view of all the tests that the monitor has run. This tab shows the following:

-   Metrics card: Charts that provide performance of each test for the time period selected in the time picker.
-   Monitor result history: All tests run by the monitor and its results.

## Details tab

You can use the **Details** tab to create a monitor or edit an existing one. See [Create and edit a synthetic monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitor.md) for more information.

**Parent Topic:**[Synthetic monitoring reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/synthetic-monitoring-reference.md)

