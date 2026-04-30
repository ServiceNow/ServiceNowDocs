---
title: View overall service health
description: View overall service health and related events, like alerts and changes, with the Overview tab on the Service Details page in the SOW.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Monitoring and investigating, Service Observability, ITOM AIOps, IT Operations Management]
---

# View overall service health

View overall service health and related events, like alerts and changes, with the **Overview** tab on the Service Details page in the SOW.

## Before you begin

-   For version 1.5, a service must be activated. For more information, see [Activate teams and services](../concept/activate-teams-and-services.md).
-   A data mapping must be configured. For more information, see [Create and manage data mappings](create-and-manage-observability-data-mappings.md).

Role required: operator \[snc\_sow\_svcobs.manager\]

## About this task

When you have been notified that a service is experiencing performance issues, you can begin your investigation with the **Overview** tab on the Service Details page.

**Note:** Operators can also use the [Analyze a dashboard in Service Observability](../../now-assist-itom/concept/analyze-a-dashboard-in-service-observability.md) and the [Analyze service health in Service Observability](../../now-assist-itom/concept/analyze-service-health-in-service-observability.md) Now Assist AI skills to generate an analysis for them.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and then navigate to a service record.

    You can access a service record from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../reference/chart-error-states.md).

2.  Use the charts in the Overview section to help determine where there might be performance issues.

    The Overview section shows the basic rate, error, and duration \(RED\) metrics along with metrics for key transactions found on the service. Hover over a metric to view more details.

    **Note:** If more than one service is found with the same name, select an individual service using the **All services** drop-down menu.

3.  Change the time period using the time picker.

4.  Use the other charts on the page to view related information about the service, such as recent changes, open incidents, and trends for incidents and alerts.

    These charts help explain whether recurring incidents or alerts might be caused by performance issues on the service. For detailed information about using this page, refer to the corresponding Overview templates for your observability vendor described in [Service Observability templates](../reference/observability-templates.md).


## What to do next

To view more detailed metrics and metrics for related entities, select the **Observability** tab. For more information, see [View service health metrics](view-service-health-metrics.md).

