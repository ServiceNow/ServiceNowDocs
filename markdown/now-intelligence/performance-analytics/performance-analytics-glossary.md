---
title: Performance Analytics terms
description: Performance Analytics uses terms and concepts that can differ from industry norms due to the unique nature of the ServiceNow platform.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics terms

Performance Analytics uses terms and concepts that can differ from industry norms due to the unique nature of the ServiceNow platform.

## automated breakdown

Automated breakdowns are based on a breakdown source, which is a set of records from a table. The breakdown maps these records, known as breakdown elements, with fields on tables that indicators collect scores from. Scores collected from mapped tables can then be grouped and filtered based on the values in the mapped fields and the breakdown elements.

## automated indicator

An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data. The indicator also specifies a data collection job and any breakdowns to apply.

**Related topics**  


[indicator \(KPI\)](performance-analytics-glossary.md#)

[database view](performance-analytics-glossary.md#)

## breakdown

A grouping or a filter of indicator scores that is based on a qualitative attribute such as Priority, Category, or Assignment Group.

**Related topics**  


[breakdown element](performance-analytics-glossary.md#)

[indicator \(KPI\)](performance-analytics-glossary.md#)

## breakdown element

The values for a breakdown. For example, the Priority breakdown may have the elements Critical, High, and Low.

**Related topics**  


[breakdown](performance-analytics-glossary.md#)

## breakdown mapping

A breakdown mapping specifies the relationships between breakdowns and indicator sources. A breakdown mapping references either a field on the indicator source or a script that queries the indicator source.

## breakdown source

A set of records from a table or database view that constitute the unique values, or breakdown elements, of a breakdown source. Can be a bucket group. Multiple breakdowns can use the same breakdown source.

**Related topics**  


[breakdown](performance-analytics-glossary.md#)

[breakdown element](performance-analytics-glossary.md#)

[bucket group](performance-analytics-glossary.md#)

## bucket group

Gathers continuous data into discrete groups when there is no table field that can serve as breakdown elements. For example, a bucket group might take differences between timestamps and divide them up into hourly periods.

## contributing indicator

An indicator that is used in the formula of a formula indicator. A contributing indicator can be an automated or a formula indicator.

## database view

A database view defines table joins for reporting purposes.

For example, a database view can join the Incident table to the Metric Definition table. This view can be used for an indicator source.

## data collector, data collection job

A scheduled job that collects data from one or more indicator sources to produce indicator scores.

## data snapshots

An alternative architecture for indicators. This architecture uses a change data capture \(CDC\) process, which captures data changes from configurable tables that are optimized for generating scores and time series at run-time. Data snapshots avoid the need for breakdown matrices, allowing unlimited breakdowns.

## formula indicator

Produces a computed indicator score from one or more other indicators. Besides indicator scores, the formula can include calculations such as the gap between an indicator score and the indicator target.

## indicator \(KPI\)

A performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time. Businesses track these scores to measure current conditions and to forecast trends.

## indicator score

The value of an indicator for a specific collection period. For automated indicators, this value is calculated in a data collection job. For formula indicators, this value is calculated by performing operations on multiple automated indicators.

## indicator source

Defines sets of records from a ServiceNow table or database view that have a common characteristic, for example, that the Priority field value is critical. Indicators use indicator sources to calculate scores. Indicator scores are KPI values. Indicator sources specify a table, filtering conditions, and the frequency for collecting data.

## KPI

KPI can be a synonym for indicator, or it can refer to a unique combination of an indicator with specific breakdown elements.

## manual breakdown

The process where you manually define the breakdown elements and the indicator scores for each element, rather than using the records from a breakdown source.

## manual indicator

An indicator that is not associated with an indicator source. An indicator's scores are not generated automatically by a data collection job. Instead, a user populates these indicators by adding scores to the score sheet manually.

## snapshot

A list of table records \(sys\_ids\) that are collected at the time that the indicator scores for those records are collected.

## target

The future hoped-for indicator scores that represent goals that your organization wants to achieve. A target can be global or can be personal to one user.

## threshold

The user-defined top or bottom limit of the normal range of scores for an indicator. You can set up an alert to inform you when a threshold is breached and how. For example, you can set up an alert to let you know when a score reaches an all-time high or low.

