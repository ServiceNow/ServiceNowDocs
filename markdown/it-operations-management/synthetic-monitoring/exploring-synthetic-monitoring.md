---
title: Exploring synthetic monitoring
description: Learn how synthetic monitoring provides proactive, automated testing of service endpoints. By simulating user interactions, it can identify bugs, performance issues, and outages before they impact real users.
locale: en-US
release: xanadu
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Synthetic monitoring, ITOM Health, IT Operations Management]
---

# Exploring synthetic monitoring

Learn how synthetic monitoring provides proactive, automated testing of service endpoints. By simulating user interactions, it can identify bugs, performance issues, and outages before they impact real users.

## Synthetic monitoring overview

Synthetic monitors continually call HTTP endpoints in the Configuration Management Database \(CMDB\) to test availability, response times, or the presence of a defined string in the response body. When a test fails the configured criteria, it can alert you to endpoint issues before your customers do.

For example, you might create a monitor that tests the GET HTTP endpoint of a service. You could configure that monitor to check for a status code of 200 and a response time of under 500 ms. If any code other than `200` is returned or the request takes longer than 500 ms, the test fails. An alert can then be generated and sent through Event Management.

The synthetic monitoring tests can be run by an Agent Client Collector \(ACC\) deployed in your network, on a MID Server, or on the ServiceNow platform.

**Note:** The HTTP endpoints must exist in the HTTP Endpoints \[cmdb\_ci\_endpoint\_http\] table. Endpoints tested from the ServiceNow platform must be publicly accessible.

## Synthetic monitoring users

|User|Description|
|----|-----------|
|Synthetic monitoring administrator \(Admin role\)|Assigns roles, creates and edits monitors, and views monitor tests and their results.|
|Service owner \(Editor role\)|Creates and edits monitors and can also view monitor tests and their results.|
|Network operation center \(NOC\) operator \(Viewer role\)|Monitors tests and their results.|

## Synthetic monitoring customer-hosted workflow

![Workflow between admin and operator](../image/MMASSET0020780_synthetic_monitoring_horizontal.png "Synthetic monitoring workflow")

Admins, service owners, and NOC operators use synthetic monitoring in the following way:

1.  As a service owner, you determine which endpoints to monitor based on business criticality.
2.  As an admin or service owner, you configure locations to run the tests from.

    **Note:** The ServiceNow hosted location is available by default and doesn't need to be configured. However, endpoints tested by that location must be publicly available.

3.  As an admin or service owner, you configure the monitor and then review the results of the tests that the monitor sends. If the results aren't successful, you troubleshoot the configuration. You can also create an alert that fires when a test fails.
4.  Synthetic monitoring runs tests based on the monitor's configuration and reports the results of each test.
5.  As a service owner or operator, you monitor the test results and also respond to any generated alerts. You can view related configuration items \(CIs\) to start triaging the issue when a test fails.

## Synthetic monitoring benefits

<table id="table_odk_l2v_pdc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

View aggregate monitor information.View the synthetic monitoring home page where you can:

-   See an aggregate view of all monitors
-   View the status of all monitors.
-   Drill down into a monitor's details

</td><td>

[View aggregate information about the monitors](identifying-system-issues.md#section_yll_v5k_fdc).

</td><td>

Operators, service owners

</td></tr><tr><td>

Visualize synthetic test results.View the details page for a monitor where you can see:

-   The status and configuration of the monitor.
-   Charts that display test success and response time.
-   Associated CIs that might be the start for investigating failed tests.
-   A historical log of synthetic test runs, including details and the response body.

</td><td>

[View a monitor and its tests](identifying-system-issues.md#section_yx4_2vk_fdc).

</td><td>

Operators, service owners

</td></tr><tr><td>

Get real-time notifications for outages before they impact users.

</td><td>

[Optionally configure alerts when tests don't succeed.](configuring-synthetic-monitoring.md)

</td><td>

Operators, service owners

</td></tr><tr><td>

Share insights with stakeholders.

</td><td>

[View aggregate monitor information](view-aggregat-monitor-information.md).

</td><td>

Operators, service owners

</td></tr><tr><td>

Update monitors to match your business needs.

</td><td>

[Edit existing monitors, including deactivation](../task/manage-synthetic-monitors.md).

</td><td>

Service owner

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using synthetic monitoring, see:

-   [Configuring synthetic monitoring](configuring-synthetic-monitoring.md)
-   [Identifying system issues with synthetic monitoring](identifying-system-issues.md)
-   [Synthetic monitoring reference](../reference/synthetic-monitoring-reference.md)

