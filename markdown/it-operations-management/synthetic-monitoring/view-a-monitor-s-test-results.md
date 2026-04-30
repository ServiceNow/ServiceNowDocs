---
title: View a monitor's test results
description: View the results of tests run by a monitor, along with configuration details, and related configuration items \(CIs\).
locale: en-US
release: xanadu
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2025-02-07"
reading_time_minutes: 1
breadcrumb: [Identifying system issues with synthetic monitoring, Synthetic monitoring, ITOM Health, IT Operations Management]
---

# View a monitor's test results

View the results of tests run by a monitor, along with configuration details, and related configuration items \(CIs\).

## Before you begin

Role required: sn\_sow\_synthetics.synthetics\_viewer, sn\_sow\_synthetics.synthetics\_editor, sn\_sow\_synthetics.synthetics\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** and select the synthetic monitoring icon \(![Synthetic monitoring](../image/sys-mon-icon.png)\).

2.  Select a monitor from the list of all monitors.

3.  View the overall health of the monitor in the header, which shows its status, and when it was last run and updated.

4.  View an overview of the monitor's configuration in the **Configuration** card.

    -   To view the full configuration, use the **Details** tab. See [Create and edit a synthetic monitor](../task/create-synthetic-monitor.md) for more information.
    -   To view the health of the associated CI, select the link.
5.  View health metrics for the monitor from the **Metrics** card.

    The **Failed tests** chart displays each test with a value of `0` when successful and a value of `1` when it failed. The **Response time** chart shows the amount of time in milliseconds that it took to receive a response from the endpoint. Hover over a point on the charts to view details.

    -   To change the time period, use the drop-down menu.
    -   To refresh the chars, use the context menu.
6.  View the status of each test in the **Monitor result history** card.

    To view the details for a test, select its timestamp. For more information about the test details, see [View test details](view-test-details.md).

    **Note:** Filtering the list affects the data displayed in the metric charts.


