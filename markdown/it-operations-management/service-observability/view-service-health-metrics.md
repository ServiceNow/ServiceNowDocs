---
title: View service health metrics
description: View detailed metrics for a service, as well as information and metrics from related entities, such as databases and hosts, on the Observability tab in SOW.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Monitoring services and investigating issues, Service Observability, ITOM Health, IT Operations Management]
---

# View service health metrics

View detailed metrics for a service, as well as information and metrics from related entities, such as databases and hosts, on the **Observability** tab in SOW.

## About this task

The **Observability** tab on the Service details page displays metrics for related entities inferred from external application performance management \(APM\) instances, enabling you to view related metrics without having to leave the ServiceNow platform.

The metrics are grouped by the following entity types:

-   Application metrics: Metrics associated with the application services
-   Computer metrics: Metrics associated with the hosts of the service
-   Databases: Metrics associated with databases used by the service

For example, say you have metrics from New Relic used to monitor services, databases, and hosts. Say you also have an issue with the `checkout` service and want to view performance information and metrics related to that service. Service Observability can show you the service, database, and host metrics related to that service that are coming from New Relic, along with related CI information from the ServiceNow platform. Each entity type has its own dashboard and each metric and related CI information has its own chart.

## Before you begin

-   For version 1.5.0, a service must be activated. For more information, see [Activate teams and services](../concept/activate-teams-and-services.md).
-   A data mapping must be configured. For more information, see [Create and manage observability data mappings](create-and-manage-observability-data-mappings.md).

Role required: operator \[snc\_sow\_svcobs.manager\]

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You can access the Service Details page from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../reference/chart-error-states.md).

2.  Select the **Observability** tab.

    The **Observability** tab shows the related metrics and CI information available for the service. Use the navigation pane to view the entity dashboards.

    **Note:** If you don't see navigation options for an entity, then the metrics for that entity haven't been discovered or mapped.

3.  Select an entity to view its dashboard.

    You can do the following with the charts:

    -   Display metrics for a single entity by electing the **All \[entity type\]** drop-down list and choosing an entity.

        **Note:** If more than one entity returned metrics, charts display multiple lines with one line for each entity.

    -   Display metrics from a different time period using the time picker. The default time period is the last hour.
    -   Refresh the charts to the current time period of the last hour by selecting the **Refresh** button.
    -   Hover over a point to view detailed information.
    For detailed information about using this page, refer to the corresponding Observability templates for your APM vendor described in [Observability templates](../reference/observability-templates.md).


