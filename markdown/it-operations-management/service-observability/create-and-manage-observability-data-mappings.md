---
title: Create and manage data mappings
description: Map your services to the data from a connected external application performance management \(APM\) instance, and view it in charts for the service.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Create and manage data mappings

Map your services to the data from a connected external application performance management \(APM\) instance, and view it in charts for the service.

## Before you begin

-   If you are on version 1.5.0, activate the services that have data from an external APM instance. For instructions on how to activate the services, see [Activate teams and services](../concept/activate-teams-and-services.md). For later versions, you don't need to activate services. You can map any of the following service types:
    -   Application
    -   Mapped application
    -   Calculated application
    -   Dynamic CI group
    -   Technical
    -   Tag-based
    -   Service offerings
    -   Business services
-   [Connect a Service Observability data source](connect-an-observability-data-source.md)

Role required: sn\_sow\_svcobs.admin

## About this task

When a service CI is mapped to specific APM metric tag key/value pairs, Service Observability displays metrics containing those tags for that service. These metrics are grouped by the following entity types:

-   Application metrics: Metrics associated with the selected service
-   Compute metrics: Metrics associated with the hosts the service is run on
-   Databases: Metrics associated with databases used by the service

For example, say you have metrics from New Relic that are used to monitor services, databases, and hosts. On those metrics, you have used the tag `service_name`. Say you have also mapped the `checkout` service CI to the APM metadata key/value pair `service_name = checkout`. Service Observability shows you all the database and host metrics tagged with `service_name = checkout` in the context of the `checkout` service CI.

If some of your metrics on different entities use a different key name or a different key value, you can create exceptions. For example, if your host metrics use `service` instead of `service_name`, you can create an exception to include those metrics.

Each entity type has its own dashboard and each metric or related CI has its own default chart. You can customize the templates used for the dashboards and charts. See [Customize Service Observability dashboard templates](customize-service-observability-dashboard-templates.md) for more information.

**Note:** To understand how Service Observability creates these mappings, see [APM vendor entity mappings for Service Observability](../reference/apm-vendor-entity-mappings.md).

For a description of the field values, see [Service Observability data mapping form](../reference/observability-data-mapping-form.md).

## Procedure

1.  Navigate to the Data mappings page, following the procedures for your version of Service Observability.

    -   Version 1.5.0: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability Management** &gt; **Manage Observability** &gt; **Data mappings**
    -   Version 1.6.x or later: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability** &gt; **Data mappings**.
2.  Select **Create your first mapping** or **Create mapping**.

3.  On the Observability data mapping page, enter a name for the mapping.

4.  Choose the services that should use this mapping.

    -   For version 1.5.0: Enter the names of the activated services that you want to map. For information about activating services, see [Activate teams and services](../concept/activate-teams-and-services.md)
    -   For version 1.6.x and later:
        1.  Choose **Select services**.
        2.  Use the navigation to narrow down the list to the type of service you're searching for.
        3.  Select the services to add to the mapping. You can add services from any combination of service type.

            **Note:** Use the filter to narrow down the service list.

        4.  Select **Add services** to add them to the mapping.
    The Mapping preview pane updates to show the selected service, or the first service in a list of services.

5.  Create a rule to determine how Service Observability should map internal services to the APM entities using tag keys and values.

    1.  Select the data source for this map.

    2.  Enter the tag key that you want to use to map the APM data to the service.

        The key can be any tag you use on your APM metadata, for example `service`. The entered key must match the tag you use in the APM metadata and is case-sensitive.

        **Note:** If you use more than one tag to represent a service, you can create an exception. For example, if most tags use `service` except for database metrics, which use `service_name`, you can create an exception for the database metrics.

    3.  Manually enter a tag value or choose one from the drop-down menu.

        **Note:** Values are case-sensitive.

        Values can be strings that are from your APM metadata, like a service name, or they can be a variable used to represent multiple instances, for example `$(service)`. When your key represents a service, a drop-down menu shows fields from the corresponding CI that can be used as a variable. If you choose to use a variable, be sure that the values resolve to values sent in the APM data.

        **Note:** If you selected more than one service to map, the drop-down displays only the fields that are common to all selected services.

    You can now test your mapping or add exceptions.

6.  If some of your entities use different key names or values, create exceptions to the default policy by configuring them in the Exceptions card.

7.  Test the mapping.

    The **Mapping preview** panel shows the test results for the first service mapped. Service Observability sends a request through the connection and returns the entities found using the provided mapping. If you created an exception using a different source, the panel shows the results from each source separately. If the results don't seem correct, try reconfiguring the mapping by changing the tag key or value.

    If you have more than one service mapped, use the **Service** drop-down menu to select and test a different service.

8.  Select **Save mapping**.


## Result

On the **Observability** tab of the Service details page, dashboards and charts appear for the entities found from the mapping.

**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

