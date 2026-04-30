---
title: Details page of a synthetic monitor
description: Read the following to understand how to use the Details page of a synthetic monitor to view the results of its tests.
locale: en-US
release: xanadu
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM Health, IT Operations Management]
---

# Details page of a synthetic monitor

Read the following to understand how to use the Details page of a synthetic monitor to view the results of its tests.

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
-   Unknown: The test failed to run, likely due to an issue with the related Agent Client Collector \(ACC\) proxy.
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

-   Configuration card: Basic current configuration of the monitor.
-   Metrics card: Charts that provide performance of each test for the time period selected in the time picker.
-   Monitor result history: All tests run by the monitor and its results.

## Details tab

You can use the **Details** tab to create a monitor or edit an existing one. See [Create and edit a synthetic monitor](../task/create-synthetic-monitor.md) for more information.

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

