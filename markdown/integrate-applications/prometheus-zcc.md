---
title: Prometheus
description: The Prometheus connector provides read-only access to data and metadata in Prometheus.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Community connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Prometheus

The Prometheus connector provides read-only access to data and metadata in Prometheus.

A connection admin can create a connection to Prometheus and give data stewards access to that connection in Zero Copy Connector Hub. A data steward can select the established connection to create a data fabric table and map data from Prometheus. This allows users to retrieve Prometheus data through the table list view or GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](managing-data-fabric-tables-zcc.md).

Prometheus is a time-series monitoring system. The data it exposes consists of metric samples collected over time, each identified by a metric name and a set of key-value labels. The Prometheus connector surfaces each label as an individual queryable column, making it possible to filter and compare metrics using standard SQL operators.

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

**Related topics**  


[Create a Prometheus connection](../task/create-prometheus-connection.md)

