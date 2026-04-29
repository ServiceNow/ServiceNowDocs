---
title: Service Exchange Center
description: Service Exchange center is a unified dashboard that consolidates connection health monitoring, issue resolution, and scan check management into a single interface.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Service Exchange]
---

# Service Exchange Center

Service Exchange center is a unified dashboard that consolidates connection health monitoring, issue resolution, and scan check management into a single interface.

Service Exchange Center provides administrators with a centralized location to monitor Service Exchange connections, track instance performance, and identify critical issues generated from scan suites.

## Role requirements

The Service Exchange Admin \(sb\_admin\) role is required to access the Service Exchange Center.

## How to access

The Service Exchange Center is accessible from the Administration menu under either the **Provider Center** or **Consumer Center** modules in the application menu, depending on your instance role. The dashboard displays data relevant to your entry point, with the option to switch between provider and consumer views when your instance supports both roles.

## Benefits

-   Quick visibility into connection health status.
-   Reduced downtime and troubleshooting efforts through early issue identification.
-   Known errors with detailed solutions for faster resolution.
-   Improved productivity through automation and visibility.
-   Consolidated health monitoring, connection management, and scan checks in one location.

## Service Exchange health

Service Exchange health dashboard is the part of Service Exchange Center and provides unified views of connection health. It also consolidates functionality that was previously available across multiple interfaces, including the Health Dashboard, and scan checks. Service Exchange Health includes the following tabs and elements:

![View of Service Exchange Health dashboard with four callouts highlighted. For descriptions of the numbered callouts, refer to the table that follows.](../image/se-health-dashboard.png)

|Feature|Description|
|-------|-----------|
|1. Tabs|Service Exchange Health dashboard contains three tabs: Resolution center, Connection health, and Scan suites.|
|2. Overview|The overview section shows a high-level summary of the connections.|
|3. Issue|The issue section lists all issues found during scan checks.|
|4. Provider/Consumer drop-down menu|The Provider/Consumer drop-down menu enables switching between provider and consumer views when the instance supports both roles.|

-   **Resolution center**

    The Resolution Center is the default landing page that provides an at-a-glance view of integration health. This tab contains the following components:

    -   **Connection Summary**

        Displays the overall health score calculated from connection statuses \(Up, Down, or Slow\), the down connections count indicates connections requiring attention. A donut chart visualizes the distribution of connection states.

    -   **Issue Distribution**

        A bar chart that categorizes issues by severity \(critical, high, moderate, low\) from scan checks.

    -   **Issues List**

        A comprehensive table listing all detected unresolved issues generated from scan checks and the Service Exchange Error table, with columns for issue summary, associated connection, count, assigned user, and other information.

        Selecting an issue summary, shows details about the issue, known errors include resolution steps and guidance. The issue dialog includes options to mute, assign, or follow the issue, and a **Validate &amp; Resolve** button to revalidate the issue status and resolve if no longer applicable. You can select the Navigate to Issue Report icon ![](../image/icon-se-center-Issue-report.svg) next to **Validate &amp; Resolve** button to get more details about the issue.

        Post comments or work notes using the Activity tab.

-   **Connection health**

    The Connection heath tab displays a list of connections grouped by their status, down, slow, or up. It also provides detailed information for each Service Exchange connection through individual connection cards. Each card contains:

    -   Connection name and status \(color-coded: green for Up, red for Down, purple for Slow\)
    -   Outbound and inbound status indicators
    -   Payload statistics \(sent and received\)
    -   App version
    -   Connection creation date
    -   Related issues associated with the connection
    You can also search, sort, and filter connections based on name, number, status, and so on.

-   **Scan suites**

    The Scan Suites tab provides access to automated health checks that detect issues and inconsistencies. To learn more about instance scan checks, see [Instance scan checks](service-bridge-v2-scan-checks.md).

    Scan suites are organized into two categories:

    -   **On-demand suites**

        Suites that are available for manual execution as needed. On-demand suites include suites for post-clone, pre-onboarding, post-upgrade, and post-onboarding scenarios.

    -   **Scheduled suites**

        Suites that run automatically at configured times.

    Each scan suite contains multiple scan checks. When you select a scan suite, you can view all scan checks included in that suite.

    Scan results appear as issues. Each issue is assigned a priority level: critical, high, medium, or low, based on its severity. You can run any scan suite as needed using **Execute scan suite** button.

-   **Provider/Consumer drop-down menu**

    Provides options for switching between provider and consumer views when the instance supports both roles.


**Related topics**  


[Execute a scan suite as a provider](../task/se-execute-scan-check.md#)

[Execute a scan suite as a consumer](../task/se-con-execute-scan-check.md#)

