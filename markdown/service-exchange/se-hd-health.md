---
title: Health tab
description: The Service Exchange Health tab shows connection health, open issues, and scan suites in one view, with resolution steps for each issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-hd-health.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 8
breadcrumb: [Service Exchange Center, Explore, Service Exchange]
---

# Health tab

The Service Exchange Health tab shows connection health, open issues, and scan suites in one view, with resolution steps for each issue.

## Service Exchange Health dashboard layout

The Service Exchange Health dashboard is part of the Service Exchange Center. It offers a single view for monitoring your Service Exchange connections and resolving the issues that affect them. It shows the current status of each connection and lists the configuration issues and errors detected on your instance. Each issue includes resolution steps and, where available, a link to the related knowledge article. The dashboard includes the tabs and elements shown in the following image and described in the table.

\[Omitted image "se-health-dashboard.png"\] Alt text: Service Exchange Health dashboard tab with four callouts highlighted. For descriptions of the numbered callouts, refer to the table that follows.

|Feature|Description|
|-------|-----------|
|1. Tabs|Service Exchange Health dashboard contains three tabs: **Resolution center**, **Connection health**, and **Scan suites**.|
|2. Overview|The overview section shows a high-level summary of the connections.|
|3. Issues|The Issues section lists the unresolved issues detected across connections and the Service Exchange application.|
|4. Provider/Consumer drop-down menu|You can use the Provider/Consumer drop-down menu to switch between the provider and consumer views when the instance supports both roles.|

You can access the **Health** tab from the Administration menu of the **Provider Center** or **Consumer Center** module.

## Resolution center

The **Resolution center** tab is the default tab of the dashboard. It shows the overall health of your connections and the issues detected across connections and the Service Exchange application. The tab contains the following components:

-   **Connection summary**

    Displays a high-level view of the health and status of all your Service Exchange connections in one place. Use it to identify connections that aren't working as expected and that require attention.

-   **Health score**

    The health score is a weighted score, shown as a percentage, that reflects the overall health of your Service Exchange setup. It's calculated from two factors:

    -   Connection health: Displays the status of each connection \(Up, Slow, or Down\).
    -   Issue severity: The priority of the open issues detected by scan checks \(Critical, High, Moderate, or Low\).
-   **Down connections**

    Displays the total number of connections that are currently down, out of all connections. A connection is Down when the Remote Process Sync \(RPS\) connection is down or in an error state. A slow response alone doesn't mark a connection as Down. Payloads can't be exchanged on a Down connection, so work such as case and task updates between the provider and consumer instances stops until the connection is restored. To find the affected connections and their related issues, go to the **Connection health** tab, where Down connections are grouped separately.

-   **Connection status**

    The Connection status donut chart shows how your connections are distributed by status, based on the heartbeat response time and the state of the RPS connection. The center shows the total number of connections, and the legend shows the count for each status.

    -   **Up**: Payloads are exchanged and the ping-pong response time is within the expected limit. The connection is working normally.
    -   **Slow**: Payloads are exchanged, but the ping-pong response time exceeds the slow threshold, which is 15 minutes by default. The connection still works, but data takes longer to reach the connected instance.
    -   **Down**: The RPS connection is down or in an error state. Payloads aren't exchanged.
-   **Issue distribution**

    The Issue distribution chart shows the number of open issues at each priority level: Critical, High, Moderate, and Low. Use it to see how serious the current issues are and where to focus first. Each bar is divided by where the issue occurs:

    -   Platform: Issues at the Service Exchange application level that aren't tied to a specific connection.
    -   Connections: Issues that affect one or more specific connections, for example, when the integration user for a connection doesn't have a required role.
-   **Issues**

    The Issues list shows all unresolved issues detected across your connections and the Service Exchange application. Issues come from scan check results and from errors recorded in the Service Exchange Error table. Automatic mitigation also creates Health issue records. When a connection goes down, the system checks for known connection errors that it can fix automatically and creates an issue for each error it detects.

    The table includes the **Issue summary**, **Status**, **Priority**, **Connection**, **Assigned to**, **Last detected**, and **Category** columns. The **Category** column shows the category of the related known error: Onboarding, Data, Configuration, Installation, Entitlements, Connection, Attachments, or Unknown. The column is empty for issues without a known error. The Connection column is empty for issues that aren't specific to a connection. By default, issues are sorted by priority, with the most recently detected first. The list has a locked filter, **State is not Resolved**, so resolved issues don't appear in the list. Issues that automatic mitigation fixes are resolved when the system creates them, so these issues don't appear in the list either. You can add filters from the column headers to narrow the list. The list shows all issues in both provider and consumer views. If no issues are found, an empty state message appears instead of the table. If an error recurs with the same known error, source record, connection, and error message, the existing unresolved issue is updated instead of a new issue being created. The finding count increases, and the **Last detected** date and issue details are updated. Issues for unknown errors show `[Unknown]` followed by the error message as the issue summary.

    Select an issue in the **Issue summary** column to open the issue details panel, which shows the resolution steps and guidance for the issue. The panel provides options such as **Assign to me**, **Follow**, and **Mute**. Select the **Source record** link to open the record that caused the issue. Select the Navigate to Issue Report icon \(\[Omitted image "icon-se-center-Issue-report.svg"\] Alt text: Navigate to Issue Report record\) to open the issue report with more details and resolution steps. The issue details panel has two tabs:

    -   The **Details** tab shows the resolution steps, which can include links to knowledge articles.
    -   The **Activity** tab shows comments and work notes. Add updates using the **Comments** and **Work notes** tabs. For issues created by automatic mitigation, the work notes show each fix that the system ran and its result.
    After you complete the resolution steps, select **Validate &amp; Resolve**. If the issue no longer exists, it's resolved and removed from the list. If the issue still exists, a message confirms that the issue is still detected. If automatic mitigation fails or returns an error, the issue stays open. Complete the resolution steps, and then select **Validate &amp; Resolve**. To download a log of the issues, select **Generate diagnostic report**. The report downloads as a Microsoft Excel file.


## Connection health

The **Connection health** tab displays a list of connections grouped by status: Down, Slow, and Up. Use it to monitor the performance of individual connections and to verify that data is exchanged between instances. The tab shows the total number of established provider or consumer connections on the instance.

Connections are grouped by status with Down connections appear first, so you can see at a glance which connections need attention. It also provides detailed information for each Service Exchange connection through individual connection cards. You can search connections by name, number, status, and other details.

Use **Sort by** and **Show all** to arrange the list, and the refresh button to update the data.

-   **Connection card**

    Each connection is displayed as a card that contains the following information.

    |Element|Description|
    |-------|-----------|
    |Company and status|Name and logo of the connected company, and the connection status. The status is color-coded: green for Up, purple for Slow, and red for Down.|
    |Heartbeat|Round-trip time for a payload to travel to the connected instance and return, and the time since the last check.|
    |Outbound|Status of payloads sent to the connected instance, number of payloads sent in the last 24 hours, and date and time of the last sent payload.|
    |Inbound|Status of payloads received from the connected instance, number of payloads received in the last 24 hours, and date and time of the last received payload.|
    |Queue counts|Number of inbound and outbound queue records in the Ready or Running state, which are waiting to be processed. Heartbeat ping and pong records aren't counted.|
    |Issues|Open issues for the connection, with links to the issue records. If the connection has no open issues, `No issues found` appears.|
    |Created date and version|Date the connection was created and the Service Exchange application version.|

    The system checks for connection responses every minute. Heartbeat pings are sent to the connected instance every hour by default.


## Scan suites

The **Scan suites** tab lists the scan suites available on your instance. A scan suite is a group of scan checks that detect Service Exchange configuration issues, such as missing roles, invalid settings, or incomplete configurations. When a scan check detects a problem, it creates an issue that appears in the Issues list on the **Resolution center** tab. For information about instance scan checks, see [Instance scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-scan-checks.md).

Scan suites are organized into two categories:

-   Service Exchange On-Demand: Suites that run only when you execute them manually or triggered systematically such as the Post-Clone, Pre-Onboarding, Post-Upgrade, and Post-Onboarding suites.
-   Service Exchange Scheduled: Suites that run automatically at a configured time or frequency.

Each scan suite contains multiple scan checks. When you select a scan suite, you can view all scan checks included in that suite. Scan results appear as issues. Each issue is assigned a priority level: critical, high, moderate, or low, based on its severity. You can run any scan suite by selecting **Execute scan suite**. The button is available on both the Scan suites tab and the scan check page.

The scan check page lists the checks in a suite with the **Name**, **Category**, **Priority**, **Short Description**, **Active**, and **Class** columns, sorted by the Updated date by default. To add a scan check to a suite, select **Create check** on the scan check page and select one of the following check types:

-   Table: Checks records in a table against defined conditions.
-   Column: Checks the values in a specific column.
-   Script: Runs a script that performs the check and creates findings.
-   Linter: Runs a linter check on code.

