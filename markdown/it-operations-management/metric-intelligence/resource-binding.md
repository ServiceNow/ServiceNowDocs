---
title: Metric binding to resources
description: Bind metrics to resources to simplify metric events binding by enabling binding to resources such as specific disks or web pages, in addition to binding to CIs.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Metric binding, Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric binding to resources

Bind metrics to resources to simplify metric events binding by enabling binding to resources such as specific disks or web pages, in addition to binding to CIs.

Metric Intelligence models metric series in either of the following methods:

-   Binding a metric series to a CI and to the metric being monitored for that CI using a 'CI/Metric' format. For example, 'win\_server\_001/response\_time\_mean'.
-   Binding a metric series to a CI, a resource within that CI, and the metric being monitored for that resource, using a 'CI/Resource/Metric' format. For example, 'win\_server\_001/Disk — C/disk\_usage'. This method is referred to as **resource binding**.

The first method enables modeling, storing, aggregating, and querying data at the CI level. However, resource binding creates resource records for specific monitored entities, such as an individual web page or a disk. Therefore, resource binding is more efficient when there are multiple resources of similar types within a CI, and metrics applicable to a category of these resources are mapped to these resources.

Use cases:

-   Common examples are disks, processors, and network interfaces. In cases in which these entities are being monitored but do not exist in the CMDB, using resources for metric binding is useful.
-   Some monitoring solutions capture metric data within services such as KPIs for individual web pages in an application. In such cases where the entity being monitored is not a configuration item, metric binding to resources can be helpful.

In those situations, using resource binding results in more meaningful aggregations across similar metrics \(such as: avg disk\_usage for a host across all disks\).

## Resource binding process

The MID Server generates metric binding events that are processed by the instance. When processing a metric binding event, there is an attempt to identify the CI to which this metric binding event belongs. If this attempt is successful, then the metric binding event is bound to the identified CI and binding to a resource is attempted. The following steps describe the attempt to bind a metric binding event to a resource:

1.  Identify the CI class of the CI that was bound to the metric binding event.
2.  Locate the resource class which is mapped to that CI class \(using the CI Type To Resource Class \[sa\_ci\_type\_to\_resource\_class\] table\).
3.  Read the **resource\_path** attribute value in the **additional\_information** field in the metric binding event.
4.  Check if a resource record exists in the resource class table, in which **name** is equal to **resource\_path** and **cmdb\_ci** is equal to the CI that was bound to the metric binding event.
5.  If such resource record exists, then the metric binding event is bound to that resource. Otherwise, a new resource record is created with the preceding values and the metric binding event is bound to the newly created resource.

## Configure resource binding

-   Ensure that the [sa.metric.use.resource.binding](../reference/installed-with-metrics.md) system property is set to true \(default\).
-   For series intended to be bound to resources, ensure that the **resource\_path** attribute is populated by doing either step:
    -   Use an event rule to add the **resource\_path** attribute to the **Additional information** field in events. For more information, see [Creating an event rule to map metrics to specific CIs](event-rule-bind-metrics-to-ci.md).
    -   Populate the **resource\_path** attribute as a part of the respective CI identifier when data is sent to the MID Server for processing.
-   Review the default mappings in the CI Type To Resource Class \[sa\_ci\_type\_to\_resource\_class\] table and adjust as needed. It is critical that mappings are set as desired prior to data processing.

    Managing the CI Type To Resource Class table requires the evt\_mgmt\_admin role.


## Resource tables

Resource binding uses an underlying hierarchy structure of resources which is a subset of the \[cmdb\_ci\] hierarchy. Metric Intelligence installs the following resource tables:

-   CI Resource \[ci\_resource\] \(parent table\):
-   Tables that extend CI Resource \[ci\_resource\]:
    -   ci\_resource\_hardware
    -   ci\_resource\_appl
    -   ci\_resource\_service
    -   ci\_resource\_vm\_object
    -   ci\_resource\_database

## Mapping CIs to resources

Mappings of CI classes to resource classes are stored in the CI Type To Resource Class \[sa\_ci\_type\_to\_resource\_class\] table. This table is installed with Metric Intelligence, and is used during metric binding to resources.

|CI class|Resource class|
|--------|--------------|
|cmdb\_ci\_hardware|ci\_resource\_hardware|
|cmdb\_ci\_appl|ci\_resource\_appl|
|cmdb\_ci\_service|ci\_resource\_service|
|cmdb\_ci\_database|ci\_resource\_database|
|cmdb\_ci\_vm\_object|ci\_resource\_vm\_object|

