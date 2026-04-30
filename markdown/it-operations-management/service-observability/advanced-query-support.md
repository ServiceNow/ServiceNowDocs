---
title: Advanced query support for AWS and Azure
description: Understand how to create advanced queries for Service Observability dashboard charts.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Advanced query support for AWS and Azure

Understand how to create advanced queries for Service Observability dashboard charts.

Advanced queries in Service Observability support most vendor-specific query languages. Simply copy a query from the APM chart and paste it into the Advanced query field in Service Observability. However, queries to AWS and Azure must be JSON-formatted and follow the guidelines outlined in this topic.

**Note:** As of version 1.10, you can import charts directly from AWS and Azure. See [Edit APM data charts on Service Observability dashboard templates](../task/edit-service-observability-dashboards.md) for more information.

## AWS advanced queries

Data from AWS is accessed using the `GetMetricData` API. Queries can be either a direct request in JSON format to that API or they can be in the form of a `DashboardBody` metric widget. For example, you can use the widget representation for a chart that exists on an AWS CloudWatch dashboard.

## Direct GetMetricData request

The following example shows a `GetMetricData` JSON query for a chart that displays the average CPU Utilization for an ELB instance.

```
{ 

    "StartTime": 1637061900, // can be replaced with “${START}” 
    "EndTime": 1637074500, // can be replaced with “${END}” 
    "MetricDataQueries": [ 
        { 
            "Expression": "SELECT AVG(CPUUtilization) FROM SCHEMA(\"AWS/EC2\", InstanceId)", 
            "Id": "q1", 
            "Period": 300, 
            "Label": "Cluster CpuUtilization" 
        }, 
        { 
            "Id": "m1", 
            "Label": "Unhealthy Behind Load Balancer", 
            "MetricStat": { 
                "Metric": { 
                    "Namespace": "AWS/ApplicationELB", 
                    "MetricName": "UnHealthyHostCount", 
                    "Dimensions": [ 
                        { 
                            "Name": "LoadBalancer", 
                            "Value": "app/EC2Co-EcsEl-EXAMPLE69Q/fdd2210e799e4376" // can be replaced with “${ENTITIES}” or “${ENTITIES_ELB}” 
                        } 
                    ] 
                }, 
                "Period": 300, 
                "Stat": "Average" 
            } 
        } 
    ] 
} 
```

## Copied source for a single object in an AWS CloudWatch dashboard

This example shows the JSON copied directly from a single object in the widgets list of the Source view for a CloudWatch dashboard.

```
{
  "type": "metric",
  "x": 9,
  "y": 0,
  "width": 15,
  "height": 5,
  "properties": {
    "view": "timeseries",
    "metrics": [
      [ "AWS/ApplicationELB", "RequestCountPerTarget", "TargetGroup", "targetgroup/api-tg/1e3dc9z72fe21ca2", "AvailabilityZone", "us-west-1a" ],
      ["...", "targetgroup/api-tg-cs/82a1db5f950073e1", ".", "." ]
    ],
    "region": "us-west-1"
  }
}
```

Both types of queries can use template variables to represent a set of entities or the start and end time selected in the UI. For example, instead of querying for a single ELB instance, you can replace the `Value` field for the `LoadBalancer` dimension with `${ENTITY_ELB}`. The query is run against each ELB instance associated with the selected service in the Service Observability UI. The chart displays a time series for each one.

**Note:** JSON objects copied from the source of a CloudWatch dashboard don't include explicit time fields. The values from the time picker in the Service Observability UI are used automatically.

<table id="table_tgs_c53_zfc"><thead><tr><th>

AWS field

</th><th>

Template variable

</th></tr></thead><tbody><tr><td>

`Dimensions[n].Value`

</td><td>

-   `ENTITIES`
-   `ENTITIES_HOST`
-   `ENTITIES_LAMBDA`
-   `ENTITIES_API_GATEWAY_HTTP`
-   `ENTITIES_API_GATEWAY_REST`
-   `ENTITIES_ELB`
-   `ENTITIES_RDS`

 The `Dimensions[n].Value` field must be a resource identifier key.

</td></tr><tr><td>

`StartTime`

</td><td>

`START`

</td></tr><tr><td>

`EndTime`

</td><td>

`END`

</td></tr></tbody>
</table>## Azure advanced queries

You run an advanced query for an Azure-based chart by copying the source from the Azure UI and pasting it in the **Advanced query** field.

To copy the source:

1.  In the Azure UI, export and download the dashboard.
2.  Copy the JSON for a single chart. Charts are located at `properties.lenses[i].parts[j].metadata.settings.content.options.chart`.
3.  Paste the JSON into the query field. The JSON must include at least the following:

    ```
    ``` 
    { 
    “metrics”: [ 
      “name”: string, 
      “resourceMetadata”: { 
        “id”: string 
        } 
      ] 
    } 
    ``` 
    ```

    The `id` field must be either an Azure resource ID or a [template variable](service-observability-template-variables.md).


**Parent Topic:**[Service Observability reference](service-observability-reference.md)

