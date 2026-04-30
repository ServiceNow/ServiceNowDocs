---
title: Create and edit a synthetic monitor
description: Create or edit a synthetic monitor to test the availability and performance of your HTTP endpoints before your customers discover issues.
locale: en-US
release: xanadu
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring synthetic monitoring, Synthetic monitoring, ITOM Health, IT Operations Management]
---

# Create and edit a synthetic monitor

Create or edit a synthetic monitor to test the availability and performance of your HTTP endpoints before your customers discover issues.

## Before you begin

If you're testing private endpoints or want to run the monitors from your environment, one or more locations must be created to host the monitor. To create a location, see [Create synthetic monitoring locations](create-synthetic-monitoring-locations.md).

Role required: sn\_sow\_synthetics.synthetics\_editor or sn\_sow\_synthetics.synthetics\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** and select the synthetic monitoring icon \(![Synthetic monitoring](../image/sys-mon-icon.png)\).

2.  On the Overview page, either create a synthetic monitor or edit an existing one.

    -   To create a synthetic monitor, select **New**.
    -   To edit an existing one, select the monitor you want to edit and then select the **Details** tab.
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

HTTP method that you want to monitor for the endpoint.

</td></tr><tr><td>

HTTP endpoint CI

</td><td>

CI that you want the monitor to test.If the endpoint doesn't exist, choose **Create new endpoint** and enter the endpoint URL.

</td></tr><tr><td>

Related service CI

</td><td>

Application service CI related to the HTTP endpoint. The entered value is used to create or update the CI relationship between the HTTP endpoint and the application service.

</td></tr><tr><td>

Support group

</td><td>

Group who is notified and assigned alerts when this monitor fails.

</td></tr><tr><td>

Query parameters

</td><td>

String of query parameters to include in the request URL. **Note:** The string shouldn't include the leading question mark. For example, use `id=xyz&customer=myco` instead of `?id=xyz&customer=myco`.

</td></tr><tr><td>

Credentials

</td><td>

Credential needed if the endpoint requires authentication. Supported credentials are basic auth and access tokens.

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

        -   To run this monitor's test from your ServiceNow instance, select **Current Instance**.

            **Note:** When running tests from the platform, only six tests can be run every minute for performance reasons.

            The endpoint for the monitor must be publicly available.

        -   Choose any of the locations you previously created.
        For more information on how to create a location, see [Create synthetic monitoring locations](create-synthetic-monitoring-locations.md).

    4.  In the Assertion section, define a successful test by selecting one or more criteria, an operator, and a value.

        **Note:** Multiple criteria are joined with an `AND` phrase, so the test must pass all criteria to be successful.

        |Criteria type|Description of success|
        |-------------|----------------------|
        |Status code|Endpoint returns the given status code.|
        |Response time \(in ms\)|Endpoint sends a response in a faster time period than the given value.|
        |Response body|Endpoint sends a string value in the response body that matches the selected operator and given value.|

    5.  In the Frequency section, enter the number of minutes between each test run.

    6.  In the Alert settings section, activate the toggle switch and select an alert severity to create an alert if the test fails.

4.  Select **Save**.


## Result

The Overview page for the synthetic monitor displays the results of the tests that the monitor runs. See [Identifying system issues with synthetic monitoring](../concept/identifying-system-issues.md) for more information.

**Parent Topic:**[Configuring synthetic monitoring](../concept/configuring-synthetic-monitoring.md)

