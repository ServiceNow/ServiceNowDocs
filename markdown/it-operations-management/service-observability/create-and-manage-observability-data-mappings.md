---
title: Create and manage observability data mappings
description: Map your services to the data from a connected external application performance management \(APM\) instance, and view it in charts for the service and its related entities.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring Service Observability, Service Observability, ITOM Health, IT Operations Management]
---

# Create and manage observability data mappings

Map your services to the data from a connected external application performance management \(APM\) instance, and view it in charts for the service and its related entities.

## Before you begin

-   If you are on version 1.5.0, activate the services that have data from an external APM instance. For instructions on how to activate the services, see [Activate teams and services](../concept/activate-teams-and-services.md). For later versions, you don't need to activate services. You can map any of the following service types:
    -   Application
    -   Managed application
    -   Calculated application
    -   Dynamic CI group
    -   Service offerings
    -   Business services
    -   Technical
    -   Tag-based
-   [Connect an observability data source](connect-an-observability-data-source.md)

Role required: sn\_sow\_svcobs.admin

## About this task

When you map the configuration items \(CIs\) of a service to specific tag key/value pairs on the APM metric metadata, Service Observability displays metrics with those tags, in the context of that service and its related CIs. These metrics are grouped by the following entity types:

-   Application metrics: Metrics associated with the application services
-   Compute metrics: Metrics associated with the application's hosts
-   Databases: Metrics associated with databases used by the application

Service Observability supports the following APM vendors:

-   Datadog
-   Dynatrace
-   New Relic

And the following databases:

-   MySQL
-   PostgreSQL

For example, say you have metrics from New Relic that are used to monitor services, databases, and hosts. On those metrics, you have used the tag `service_name`. Say you have also mapped the `checkout` service CI to the APM metadata key/value pair `service_name = checkout`. Service Observability shows you all the database and host metrics tagged with `service_name = checkout` in the context of the `checkout` service CI, along with related CIs.

If some of your metrics on different entities use a different key name or a different key value, you can create exceptions. For example, if your host metrics use `service` instead of `service_name`, you can create an exception to include those metrics.

Each entity type has its own dashboard and each metric and related CI has its own chart.

**Note:** If you are mapping Datadog entities, read [Datadog considerations](datadog-considerations.md) before attempting this procedure.

## Procedure

1.  Navigate to the Data mappings page, following the procedures for your version of Service Observability.

    -   Version 1.5.0: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability Management** &gt; **Manage Observability** &gt; **Data mappings**
    -   Version 1.6.x or later: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability****Data mappings**.
2.  Select **Create your first mapping** or **Create mapping**.

3.  On the Observability data mapping page, enter a name for the mapping.

4.  Choose the services that should use this mapping.

    For version 1.5.0: Enter the names of the activated services that you want to map. For information about activating services, see [Activate teams and services](../concept/activate-teams-and-services.md).

    For version 1.6.x and later:

    1.  Choose **Select services**.
    2.  Use the navigation to narrow down the list to the type of service you're searching for.
    3.  Select the services to add to the mapping. You can add services from any combination of service type.

        **Note:** Use the filter to narrow down the service list.

    4.  Select **Add services** to add them to the mapping.
5.  Create a rule to determine how Service Observability should map services to the APM entities using tag keys and values.

    1.  Select the data source for this map.
    2.  Enter the tag key that you want to map to the activated service.

        **Note:** If you use more than one tag to represent a service, you can create an exception. For example, if most tags use `service_name` except for database metrics, which use `service`, you can create an exception for the database metrics.

    3.  Enter a tag value. Values can be strings or a variable that represents fields on the CI for the service.

        **Note:** You can use variables on your APM data as the value to map multiple entities at once. For example, if your APM data uses the `$service_name` variable and you enter that as the source tag value, all services using that value are mapped.

6.  Select **Save mapping**.

7.  If some of your entities use different key names or values, create exceptions to the default policy by configuring them in the Exceptions card.

    For a description of the field values, see [Observability data mapping form](../reference/observability-data-mapping-form.md).


## Result

On the **Observability** tab of the Service details page, dashboards and charts appear for the entities found from the mapping.

-   **[Datadog considerations](datadog-considerations.md)**  
Read this topic to understand how to correctly configure your data mappings for a Datadog integration with Service Observability.

**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

