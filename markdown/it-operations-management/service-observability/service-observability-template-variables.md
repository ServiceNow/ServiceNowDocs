---
title: Service Observability template variables
description: Understand the template variables that you can use in your queries when editing Service Observability dashboards and charts.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Service Observability template variables

Understand the template variables that you can use in your queries when editing Service Observability dashboards and charts.

You can use the following template variables in your query. Variables enable the query to be used for multiple services, hosts, and database instances, as well as for the time period currently selected for the dashboard.

**Note:** Amazon CloudWatch uses slightly different template variables. See [Advanced query support for AWS and Azure](advanced-query-support.md) for more information.

Aside from the variables listed below, you can also use any tag key used in the chart's data mapping as a template variable.

|Variable|Description|
|--------|-----------|
|`{$ENTITIES_HOST}`|Returns metrics for the selected host|
|`{$ENTITIES_MYSQL}`|Returns metrics for the selected MySQL instance|
|`{$ENTITIES_POSTGRESQL}`|Returns metrics for the selected PostgreSQL instance|
|`{$ENTITIES_SERVICE}`|Returns metrics for the selected service.|
|`{$ENTITIES}`|Returns metrics for the selected entity; either service, host or database.|
|`{$START_TIME}`|Returns metric time series using the selected start time.|
|`{$END_TIME}`|Returns metric time series using the selected end time.|

## Example query

Let's say you're using NewRelic and you create a data mapping that maps the key `service` to the value `checkout-service`.

A simple query built using the query builder might look like this:

```
rate(count(apm.service.transaction.duration), 1 minute
```

It would return the rate of transactions for the `checkout-service` service.

Instead you might use a full vendor query like this:

```
SELECT rate(count(apm.service.transaction.duration), 1 minute) as 'Web throughput' FROM Metric WHERE (entity.guid = 'NDc2NDMyNXxBUE18QVBQTElDQVRJT058MTA3NjIyODQwMw') AND (transactionType = 'Web') LIMIT MAX SINCE 30 minutes ago TIMESERIES UNTIL now
```

It would return the duration for the hard-coded `NDc2NDMyNXxBUE18QVBQTElDQVRJT058MTA3NjIyODQwMw` entity from the last 30 minutes.

To create a query that would return the time series for any selected service at any time period, you can replace the entity and times with template variables:

```
SELECT average(convert(apm.service.transaction.duration, unit, 'ms')) as metricValue, average(convert(apm.service.transaction.duration, unit, 'ms')) - 100 as loop FROM Metric WHERE entity.guid IN (${ENTITIES}) FACET entity.guid, entity.name SINCE ${START} UNTIL ${END} TIMESERIES LIMIT 25
```

**Parent Topic:**[Service Observability reference](service-observability-reference.md)

