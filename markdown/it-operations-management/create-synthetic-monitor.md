---
title: Create and edit a synthetic monitor
description: Create or edit a synthetic monitor to test the availability and performance of your HTTP endpoints before your customers discover issues.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Create and edit a synthetic monitor

Create or edit a synthetic monitor to test the availability and performance of your HTTP endpoints before your customers discover issues.

## Before you begin

-   A configuration item \(CI\) for the endpoint you want to test.
-   If you're testing private endpoints or want to run the monitors from your environment, one or more locations must be created to host the monitor. To create a location, see [Create synthetic monitoring locations](create-synthetic-monitoring-locations.md).

**Note:** For information about how to bulk create synthetic monitors, see the Synthetic Monitoring Developer Guide.

Role required: sn\_sow\_synthetics.synthetics\_editor or sn\_sow\_synthetics.synthetics\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** and select the synthetic monitoring icon \(![Synthetic monitoring](../image/sys-mon-icon.png)\).

2.  On the Overview page, either create a synthetic monitor or edit an existing one.

    -   To create a synthetic monitor, select **New**.
    -   To edit an existing one, select the link for the monitor you want to edit and then select the **Details** tab.
3.  On the form, fill in the fields.

    1.  In the Monitor details section, enter a unique name for the monitor and a description.

    2.  In the HTTP settings section, fill in the fields.

<table id="table_fyp_s2l_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HTTP method

</td><td>

HTTP method that you want to monitor for the endpoint.**Note:** HEAD and OPTIONS methods aren't supported from a MID Server.

</td></tr><tr><td>

HTTP endpoint CI

</td><td>

CI for the endpoint that you want the monitor to test.If the endpoint doesn't exist, choose **Manage HTTP endpoints in CMDB** to create a CI.

</td></tr><tr><td>

Related service CI

</td><td>

Application service CI related to the HTTP endpoint. The entered value is used to create or update the CI relationship between the HTTP endpoint and the application service.

</td></tr><tr><td>

Support group

</td><td>

Group who is notified and assigned alerts when this monitor fails.**Note:** To view this field in the HTTP Endpoints table, use the Synthetic Monitoring view.

</td></tr><tr><td>

Query parameters

</td><td>

String of query parameters to include in the request URL. **Note:** The string shouldn't include the leading question mark. For example, use `id=xyz&customer=myco` instead of `?id=xyz&customer=myco`.

</td></tr><tr><td>

Credentials

</td><td>

Credential needed if the endpoint requires authentication. OAuth, Basic Auth, and API keys are supported.

</td></tr><tr><td>

Headers

</td><td>

Key-value pairs for the HTTP request headers. You can add multiple pairs.

</td></tr><tr><td>

Body

</td><td>

Text that is used if the API expects a message body, such as a JSON snippet.

</td></tr></tbody>
</table>    3.  In the Locations section, select one or more locations.

        Choose a MID Server or Agent Client Collector location, or to run this monitor's test from your ServiceNow instance, choose ServiceNow hosted location.

        **Note:** When running tests from your instance, only six tests can be run every minute for performance reasons.

        Choose **Create new location** to create a location.

        For more information on how to create a location, see [Create synthetic monitoring locations](create-synthetic-monitoring-locations.md).

    4.  In the Assertion section, define a successful test by selecting one or more criteria, an operator, and a value.

        **Note:** Multiple criteria are joined with an `AND` phrase, so the test must pass all criteria to be successful.

        |Criteria type|Description of success|
        |-------------|----------------------|
        |Status code|Endpoint returns the given status code.|
        |Response time \(in ms\)|Endpoint response time is less than the given value.|
        |Response body|Endpoint sends a string value in the response body that matches the selected operator and given value.|

    5.  In the Frequency section, enter the number of minutes between each test run.

    6.  To have an alert sent through Event Management when a test fails:

        -   In the Alert settings section, activate the toggle switch.
        -   Select an alert severity for a test failure.
        -   Add tags to the alert. For more information about using tags in alerts, see [Tag cluster alert grouping](../../event-management/concept/alert-clustering-tag-definitions-concept.md).
4.  Select **Save**.


## Result

The Overview page for the synthetic monitor displays the results of the tests that the monitor runs. See [Identifying system issues with synthetic monitoring](../concept/identifying-system-issues.md) for more information.

**Parent Topic:**[Configuring synthetic monitoring](../concept/configuring-synthetic-monitoring.md)

