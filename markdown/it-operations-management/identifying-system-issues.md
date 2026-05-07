---
title: Identifying system issues with synthetic monitoring
description: Tests run by synthetic monitors enable service owners and operators to view service endpoint performance at scale.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Identifying system issues with synthetic monitoring

Tests run by synthetic monitors enable service owners and operators to view service endpoint performance at scale.

## Overview of using synthetic monitoring

As a service owner, you can use synthetic monitoring to monitor your service's endpoints, verifying that they're available and performing as expected. You can be notified when synthetic tests fail, enabling you to mitigate issues quickly. You can see trends in HTTP API success rates and response times.

As an operator, you can use synthetic monitoring as part of triaging issues. When you learn a service is reported to have issues, you can view test results for that service's endpoints. If tests are failing or response times are slow, that might be something to investigate.

## View aggregate information about the monitors

The synthetic monitoring landing page shows an overview of all created monitors, including inactive monitors.

From here, you can see the status for all your monitors. Selecting a card at the top filters the list of monitors. For example, you can view only the monitors that have failed or that are in an unknown state.

By default, the list of monitors is sorted by the timestamp in the **Updated** column. You can select a different column header to sort by that category.

Selecting a monitor lets you view details about the monitor's tests, including details, configuration, and associated alerts.

## View a monitor and its tests

To view a monitor's details and the results of its tests, select a monitor from the synthetic monitoring landing page. The Monitor details page provides key information needed to understand how the monitor is performing.

Use the information in the header to understand the basic health of the monitor, including its status and when it last ran a test.

## View individual tests

The Metrics card displays two charts to help you understand the health of each test the monitor has run. The **Failed tests** chart displays each test with a value of `0` when it was successful and a value of `1` when it failed. Hover over a point on the chart to view further details.

The **Response time** chart shows the amount of time in milliseconds that it took to receive a response from the endpoint. Hover over a point on the chart to view details.

**Note:** Test results are retained for 21 days.

The **Monitor result history** table lists each test. By default, the table is sorted from newest to oldest by the timestamp. You can sort by any column to help find issues. For example, you can sort by **Result** to see all failures together or you can sort by **Response time** to view the tests with the highest latency.

If a monitor was configured to generate an alert when it fails, a link to the alert displays in the **Alert** column. Select an alert link to view its details.

When you see a failure or high latency, select a test to view details, including the response body, which might help explain any issues.

![A modal displays information about the test including a response body that states that the request was to a bad gateway.](../image/sys-mon-failed_monitor.png "Response body in the details modal")

