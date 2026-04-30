---
title: Synthetic monitoring release notes
description: The ServiceNow synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Synthetic monitoring release notes

The ServiceNow® synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring is a new application in the Yokohama release.

## Synthetic monitoring highlights for the Yokohama release

-   View real-world performance data from your services without needing actual users, catching issues before they're released to production.
-   Get real-time notifications for performance degradations or outages before they impact users.
-   Visualize synthetic test results and share insights with stakeholders.

See [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** Synthetic monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Synthetic monitoring features

-   **[Create and edit a synthetic monitor](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Create and manage synthetic tests to replicate end-user transactions for critical service endpoints. Configure an alert to activate when a test fails, enabling you to address issues before they impact users.

    As of version 1.2, you can:

    -   Test for response code: Confirm that your endpoints are returning success codes and know when they aren’t.
    -   Test for response time: Confirm that your services are meeting performance expectations by setting thresholds for response times.
    -   Test for response text: Validate whether specific content exists in the response body, enabling accurate end-to-end checks.
    -   Run tests from your local Glide instance: Enable closer integration with your instance and reduce the need for external test runners.
    -   Run tests from multiple locations.
-   **[Identifying system issues with synthetic monitoring](https://www.servicenow.com/docs/access?context=identifying-system-issues&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    View the Overview page for a monitor where you can:

    -   View the status of the monitor.
    -   View charts that display test failures and response times.
    -   Visit related configuration items \(CIs\) that might be the start to investigating failed tests.
    -   View a historical log of synthetic test runs, including details and the response body text.
    -   Share results by exporting a list of tests for a monitor.

## UI changes

-   **Overview and detail pages in SOW.**

    Create view and manage your synthetic monitors on the overview and detail pages.

    As of version 1.2, the following UI enhancements are available:

    -   Improved filtering for finding your endpoints.
    -   Bulk editing of monitors.
    -   Charts on the Overview page now display failures instead of successes.

## Activation information

Install synthetic monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

You must do the following before you can use synthetic monitoring:

-   If you have version 1.0, configure at least one proxy agent on the Agent Client Collector. These agents should be the ones you use to monitor the health and performance of the services to be monitored. For more information about proxy agents, see [Using proxy agents in Agent Client Collector](https://www.servicenow.com/docs/access?context=proxy-agent&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

    Starting with version 1.2, you can run tests from your local Glide instance instead of a proxy agent.

-   Add CIs in the CMDB for the endpoints that you want to monitor.
-   If your endpoints require authentication, configure credentials in the Credentials \[discovery\_credentials\] table.

## Related ServiceNow applications and features

-   **[Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Synthetic monitoring can use a proxy agent on the Agent Client Collector to monitor the health of service endpoints.

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Access and use synthetic monitoring in Service Operations Workspace, a configurable workspace that provides a unified experience for multiple IT Operations Management workflows.


