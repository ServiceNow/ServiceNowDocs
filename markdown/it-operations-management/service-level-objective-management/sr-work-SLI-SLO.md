---
title: Working with reliability metrics
description: Learn about the reliability metrics and features that can help you track service health, respond to issues, and support business goals.
locale: en-US
release: yokohama
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Working with reliability metrics

Learn about the reliability metrics and features that can help you track service health, respond to issues, and support business goals.

## Service reliability dashboard

The Service reliability dashboard displays a customizable, high-level view of service performance. It helps you monitor and manage reliability using visualizations that track service states, error budgets, and service level objectives \(SLOs\) over time.

The dashboard displays information about all services in Service Reliability Management \(SRM\). You can access the dashboard in Service Operations Workspace in the following ways:

-   Navigate to **Services \(![Services icon](../../service-reliability/image/icon-sr-services.png)\)** &gt; **Service reliability**.
-   Navigate to **Home \(![Home icon](../../service-reliability/image/icon-sr-homepage.png)\)** &gt; **Service reliability**

For more details, see [Visualizations in the Service reliability dashboard](../../service-reliability/reference/sr-service-dashboard-visualizations.md).

**Note:** You can also view SLO information for all services on the Services Overview tab. See [Working with SRM services](../../service-reliability/concept/sr-work-services.md) for more information.

## Notification destinations

Notification destinations help keep teams informed about service reliability. Attach them to error budget policies to send notifications when a policy is breached.

To view and manage notification destinations in Service Operations Workspace, navigate to **Teams** &gt; **\[Your team\]** &gt; **SLO Notification destinations**.

Visit the following links to learn more about creating and working with notification destinations:

-   [Create a notification destination in SRM](../task/create-notification-destination.md)
-   [Create SLOs, SLIs, and error budget policies](../task/sr-create-slo-sli.md)
-   [Notifications for breached error budgets](../reference/srm-notifications-messages.md)

## Reliability metrics tab

The Reliability metrics tab shows how well a specific service is meeting its reliability goals. Use it to track SLOs, service level indicators \(SLIs\), and error budgets for a service.

To view the Reliability metrics tab in Service Operations Workspace, navigate to **Services \(![Services icon](../../service-reliability/image/icon-sr-services.png)\)** &gt; **\[Your service\]** &gt; **Reliability Metrics**.

![The Reliability metrics tab shows a list of SLOs for the User Authentication service.](../../service-reliability/image/sr-slo-list-view.png "SRM Reliability metrics tab")

See these links to learn more about what you can do in the Reliability metrics tab:

-   [Create SLOs, SLIs, and error budget policies](../task/sr-create-slo-sli.md)
-   [Edit a reliability metric](../task/sr-edit-sli-slo.md)
-   [View SRM reliability metrics](../../service-reliability/task/sr-view-slo.md)

## Service level objectives table

On the Reliability metrics tab, the Service level objectives table includes the following details about the selected service:

-   **Service level objective**: Name of the SLO. The SLO is a target value or the objective that your team must reach to meet your service level agreement \(SLA\).
-   **SLI type**: Performance category being measured:
    -   Availability: Percentage of time your service or configuration item is available, also known as uptime.
    -   Errors: Frequency of your service errors.
    -   Latency: Time that it takes to service a request.
    -   Saturation: Fullness of your system, focusing on resource usage.
-   **Compliance period**: Time window used to calculate performance:
    -   Month: Current month, for example, if the current date is January 26, the month is January 1 through January 31.
    -   Rolling 7, 30, or 90 days: Number of days from the current date. For example, for rolling 7 days, the duration is 7 days back from the current date.
-   **State**: Status of the SLO, such as draft, running, or retired.
-   **Objective \(percentage\)**: Target percentage of SLI performance.
-   **Limit occurrences**: Number of limit breaches that have occurred. Used by count-based SLOs only.
-   **Service level indicator**: SLI associated with the SLO.
-   **Error budget**: Allowable failure time for the compliance period, calculated using the compliance period and objective \(percentage\).
-   **Remaining error budget**: Error budget still available.
-   **Remaining breach occurrences**: Number of breaches still available before the limit is reached.

**Note:** For performance purposes, SLO and SLI records \(\[sn\_sow\_srm\_slo\_history\] and \[sn\_sow\_srm\_sli\_metric\]\) are archived after one year and deleted five years later. Archived data is omitted from tables and visualizations.

