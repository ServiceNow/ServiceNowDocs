---
title: Connect an observability data source
description: Connect Service Observability to an external application performance management \(APM\) instance. Service Observability displays metrics in the Service Operations Workspace \(SOW\) from that APM instance.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Service Observability, Service Observability, ITOM Health, IT Operations Management]
---

# Connect an observability data source

Connect Service Observability to an external application performance management \(APM\) instance. Service Observability displays metrics in the Service Operations Workspace \(SOW\) from that APM instance.

## Before you begin

For New Relic, an API key is required.

For Dynatrace connections, the API key that you use must have `Read entities` and `Read metrics` scope permissions.

For Datadog, you need both an API key and an application key. If an application key is restricted to a specific scope, those scopes are required for the following endpoints:

-   https://api.datadoghq.com/api/v2/catalog/entity
-   https://api.datadoghq.com/api/v1/hosts
-   https://api.datadoghq.com/api/v1/query
-   https://api.datadoghq.com/api/v2/query/timeseries

Role required: sn\_sow\_svcobs.admin

## About this task

The first step to ingesting APM data is to create a connection to the APM instance.

Service Observability supports the following APM vendors:

-   Datadog
-   Dynatrace
-   New Relic

## Procedure

1.  Navigate based on your version of Service Observability.

    -   Version 1.5.0: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability Management** &gt; **Manage Observability** &gt; **Data sources**
    -   Version 1.6.x or later: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability****Data sources**.
2.  Select your APM vendor.

3.  On the **Add connection** form, fill in the fields.

    You can use an existing HTTP or HTTPs connection and an existing API key credential or create one.

    **Note:** For New Relic, the User name field should be the New Relic account ID.

    For a description of the field values, see [Add connection form](../reference/add-connection-form.md).

4.  Select **Save**.


## Result

A new connection appears in the list of observability data sources. You use this connection when you create a data mapping.

## What to do next

Map your connection to the services that you want to monitor in Service Observability. See [Create and manage observability data mappings](create-and-manage-observability-data-mappings.md).

**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

