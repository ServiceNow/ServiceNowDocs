---
title: Datadog considerations
description: Read this topic to understand how to correctly configure your data mappings for a Datadog integration with Service Observability.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-04-30"
reading_time_minutes: 1
breadcrumb: [Create and manage observability data mappings, Configuring Service Observability, Service Observability, ITOM Health, IT Operations Management]
---

# Datadog considerations

Read this topic to understand how to correctly configure your data mappings for a Datadog integration with Service Observability.

## Service discovery

Services are matched to APM data using the key/value pairs on the APM metadata. For Datadog, the `Software Catalog list entities` API is used. However, that API only returns data for services that include metadata. If you want to map services that don't include metadata, you must create a mapping using `service` as the tag and the name of the service as the value.

For example, say you have a service named `internet-banking-4` that you want to use in a mapping and it doesn't contain metadata. You set up the mapping as shown in this screen shot.

![How to map a service that doesn't contain metadata](../image/so_dd_mapping.png "Datadog mapping when no metadata is present")

## Host discovery

Service Observability uses the Datadog `Hosts list hosts` API to return host data related to the services.

## Database discovery

These specific metrics are used in the queries to map database entities to services:

-   PostgreSQL: `postgresql.connections`
-   MySQL: `mysql.net.max_connections`

If your databases don't emit these metrics, they will not be mapped.

## Default dashboard templates

The Requests, Errors, and Latency charts on the Overview and Observability dashboard templates are created using the Datadog `trace.http.request` trace metric. If a service is not emitting that metric, no data will be found. You can customize the template to use a different trace metric query. See [Customize Service Observability dashboard templates](customize-service-observability-dashboards.md) for more information.

**Parent Topic:**[Create and manage observability data mappings](create-and-manage-observability-data-mappings.md)

