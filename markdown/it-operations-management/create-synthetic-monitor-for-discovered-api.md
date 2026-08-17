---
title: Create a synthetic monitor for a discovered API
description: Create a synthetic monitor to test the availability of APIs discovered through API Insights.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/create-synthetic-monitor-for-discovered-api.html
release: australia
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 4
keywords: [synthetic monitoring, discovered API, API insights, HTTP endpoint]
breadcrumb: [Configure, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Create a synthetic monitor for a discovered API

Create a synthetic monitor to test the availability of APIs discovered through API Insights.

## Before you begin

-   API Insights
-   CMDB CI Class Models. For more information, see .
-   An existing API component \(cmdb\_ci\_api\_component\) record in the CMDB for the API Insights to discover APIs.
-   One or more locations must be created to host the monitor to test private endpoints or run the monitors from your environment. To create a location, see [Create synthetic monitoring locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitoring-locations.md).

Role required: sn\_sow\_synthetics.synthetics\_editor or sn\_sow\_synthetics.synthetics\_admin

## About this task

When API Insights discovers APIs through Service Graph Connectors, you can proactively monitor their availability and performance by creating synthetic monitors. Synthetic monitors identify issues before they impact users and verify continuous monitoring of critical API endpoints.

For more information about how API discovery integrates with synthetic monitoring, see [API Insights and synthetic monitoring integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/api-discovery-integration.md).

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** and select the synthetic monitoring icon \(\[Omitted image "sys-mon-icon.png"\] Alt text: Synthetic monitoring\).

2.  On the Overview page, create a synthetic monitor by selecting **New**.

3.  In the Monitor details section, enter a name and description for the monitor.

    Use a descriptive name that identifies the discovered API being monitored, such as the API name or endpoint path.

4.  In the **Endpoint settings** section, configure how the monitor interacts with the discovered API.

    1.  For **Endpoint type**, select **Discovered API**.

    2.  In the **API** field, select the discovered API that you want to monitor.

        Each option in the list identifies a discovered API by its HTTP method, path, and URL. The method is part of the selected API component and does not require separate configuration.

        **Note:** The **API** field lists only API components that meet the following criteria:

        -   The endpoint's operational status is **Operational**.
        -   The URL starts with `http`.
        -   The URL does not contain placeholder or template characters \(for example, `/users/{id}`\).
        If a known API does not appear in the list, verify that it meets these criteria.

        To browse the available API component records, select the info icon beside API, and then select **View API components**.

    3.  Verify the service association.

        If the discovered API is related to an application service in the CMDB, the service and its support group are populated automatically and shown as read-only. If no service relationship exists, these fields are hidden and the monitor is created without a service association.

    4.  To configure optional request details, expand **Advanced settings**.

        Under **Advanced settings**, you can configure the following optional details:

        -   **Query parameters**: Query parameters to append to the request URL.

            **Note:** Do not include the leading question mark. For example, use `id=xyz&customer=myco` instead of `?id=xyz&customer=myco`.

        -   **Credentials**: The credential to use if the discovered API requires authentication. OAuth, Basic Auth, and API keys are supported.
        -   Select **Add headers and body** to add custom request headers and, if the API expects a message body, the request body.

            **Note:** For example, enter a JSON snippet for REST APIs that require a request body.

5.  In the Locations section, select one or more locations where the monitor tests run.

    Select a MID Server or Agent Client Collector location, or to run this monitor's test from your ServiceNow instance, select ServiceNow hosted location.

    **Note:** When running tests from your instance, only six tests can be run every minute for performance reasons.

    To create a location, select **Create new location**. For more information, see [Create synthetic monitoring locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitoring-locations.md).

6.  In the Assertion section, define success criteria for the API tests.

    Select one or more criteria, a condition for the criteria, and a value to determine when a test passes.

    **Note:** Multiple criteria use an `AND` phrase, so the test must pass all criteria to be successful.

    Common assertions for discovered APIs include:

    -   **Status code**: Verify the API returns the expected HTTP status code \(for example, 200 for successful requests\).
    -   **Response time**: Verify the API responds within an acceptable time threshold.
    -   **Response body**: Validate that the API returns expected data in the response body.
7.  In the Frequency section, enter the number of minutes between each test run.

    Consider the criticality of the discovered API when setting the frequency. Critical APIs may require more frequent monitoring.

8.  To receive alerts when the discovered API monitor fails, configure alert settings.

    -   In the Alert settings section, activate the toggle switch.
    -   Select an alert severity for test failures.
    -   Add tags to the alert to help with alert management and routing. For more information about using tags in alerts, see [Tag cluster alert grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-clustering-tag-definitions-concept.md).
9.  Select **Save**.


## Result

The synthetic monitor begins testing the discovered API endpoint at the specified frequency. The Overview page displays test results, including availability, response time, and assertion status. See [Identifying system issues with synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/identifying-system-issues.md) for more information about viewing and analyzing test results.

## What to do next

After creating the monitor, verify that tests run successfully and adjust assertions or frequency as needed based on the API's performance characteristics and business requirements.

**Parent Topic:**[Configuring synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configuring-synthetic-monitoring.md)

