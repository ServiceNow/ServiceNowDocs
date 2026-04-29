---
title: Exploring GRC: Metrics
description: A metric is used to measure and evaluate the effectiveness of your organizational processes. A metric or a combination of metrics can provide an insight into a system, component, or process. The GRC: Metrics application enables other applications to assess, compare, and track the performance of the processes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Exploring GRC: Metrics

A metric is used to measure and evaluate the effectiveness of your organizational processes. A metric or a combination of metrics can provide an insight into a system, component, or process. The GRC: Metrics application enables other applications to assess, compare, and track the performance of the processes.

## Metrics

The GRC: Metrics application is installed automatically with the Operational Sustainability Management application from the ServiceNow® Store. The user role that is responsible to read, create, and update the metric definitions and metrics is the Operational Sustainability Management metrics manager \(sn\_esg.metrics\_manager\).

With the GRC: Metrics application, you can define metrics by using the metrics form. Metrics are a combination of a metric definition and an entity. Applying the metric definition to an entity creates a metric. Once the metrics are defined, data is gathered to track the effectiveness and performance of your processes. For example, consider a metric that measures the effectiveness of an incident resolution process by calculating the time it takes to resolve an incident.

Every organization has a range of data sources for building and structuring their own metric analysis. To establish a useful metric, the metrics manager must first assess and set the goals. Next, the manager sets the targets for the metrics that are integrated with their business decisions.

## Qualitative and quantitative metrics

You can classify your metrics into qualitative and quantitative measurements.

Qualitative metrics in Operational Sustainability Management are derived from the subjective opinion that you form based on other information. Some examples of qualitative metrics in the Operational Sustainability Management sectors are brand credibility, corporate value, and so on.

Quantitative metrics in Operational Sustainability Management are the metrics that you can measure in a specific number through certain formulas. Some examples of quantitative metrics for an organization include reporting total energy use, energy use by region, and so on.

## Examples of metrics

Consider the example of measuring greenhouse gas emissions for business entities in your organization. Greenhouse gas emissions are categorized into three groups called Scopes by the international Greenhouse Gas \(GHG\) Protocol.

You want to measure the metrics for Scope 3 Emissions for the following categories: employee travel and purchased goods. The employee travel policy applies to all the employees in the organization. You can collect the metrics for the employee travel policy manually by providing instructions in the metric definition.

On the other hand, the metrics for the purchased goods are collected automatically based on the specified conditions method, schedule, and core property in the metric definition. The metric collection process is illustrated in the following image.

![Define a metric.](../image/define-a-metric.png "Define a metric")

## Metric data by entity

The metric data by entity table \(sn\_grc\_metric\_data\_by\_entity\) includes metric definition data and metric data for entities and the aggregated data for parent entities defined in the entity hierarchy. For example, if an ESG reporting disclosure manager wants to understand the total emissions for an entire year for a particular location and if the location has sub-locations, you can also aggregate the data and use it for reporting purposes. For example, consider that your organization has a location Japan. Japan, in turn, has two sub locations, Tokyo and Kyoto. Assume that you want to find your total yearly Scope 1 emissions for the year 2022 for Japan. Using the time dimensions feature, you can aggregate your data and get a view of your total emissions for a year. You can also aggregate the data for a quarter, week, or a month depending on your reporting requirements. The data in this table is collected according to the calendar of metric or entity.

