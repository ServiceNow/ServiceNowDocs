---
title: Service Exchange Center
description: The Service Exchange Center enables you to monitor connection health, resolve scan check issues, and add and manage Service Exchange connections from a single dashboard in the Provider Center or Consumer Center applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-se-center.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Service Exchange Center, connection health, health dashboard, scan checks, resolution center]
breadcrumb: [Explore, Service Exchange]
---

# Service Exchange Center

The Service Exchange Center enables you to monitor connection health, resolve scan check issues, and add and manage Service Exchange connections from a single dashboard in the Provider Center or Consumer Center applications.

Using single dashboard, you can manage and monitor Service Exchange connections between provider and consumer instances. It covers the full connection lifecycle, from registering consumers and completing the onboarding to monitoring connection health and resolving issues. Automated scan checks detect configuration issues and errors, and guided resolution steps help you fix each issue.

The Service Exchange Center includes the two tabs:

-   Health: Monitor the health of your connections and identify issues early. Automated scan checks detect configuration issues and errors, and each issue includes troubleshooting steps to resolve it. You can also manage scan suites and their schedules. The Health tab includes the Resolution center, Connection health, and Scan suites tabs. For more information, see [Health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-hd-health.md).
-   Connections: Add, monitor, and manage connections across every stage of onboarding. Each connection appears as a card that shows its company, instance URL, and current state. For more information, see [Connections tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-connections-tab.md).

The health dashboard works the same way in both the provider and consumer views, but some actions are role-specific. A provider creates connection requests and shares the onboarding URL with the consumer. A consumer uses that URL to complete onboarding and connect to the provider. Both can view connection details, configure the settings they control, and offboard a connection. Health monitoring, issues, and scan checks are available in both views, and each view shows the connections for that role.

The dashboard displays the provider or consumer view, depending on which Service Exchange applications are installed on the instance. If both the provider and consumer applications are installed, you can switch between the two views.\[Omitted image "se-center-dashboard.png"\] Alt text: Service Exchange center dashboard showing connection related information.

## Role requirements

The Service Exchange admin \(sb\_admin\) role is required to access the Service Exchange Center.

## How to access

The Service Exchange Center is available from the Administration menu of the **Provider Center** or **Consumer Center** module, depending on which Service Exchange applications are installed on your instance. If both the provider and consumer applications are installed, you can switch between the provider and consumer views.

## Benefits

-   View connection health status
-   Detect configuration issues early with automated scan checks to reduce downtime and troubleshooting effort
-   Resolve known errors using detailed resolution steps
-   Fix known connection errors automatically when a connection goes down
-   Access consolidated health monitoring, connection management, and scan checks in one location
-   View all connections across every onboarding stage, and monitor them without opening individual records
-   Access registration details and connection settings from each connection card
-   Resume an interrupted onboarding from the consumer view

**Related topics**  


[Health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-hd-health.md)

[Connections tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-connections-tab.md)

[Instance scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-scan-checks.md)

