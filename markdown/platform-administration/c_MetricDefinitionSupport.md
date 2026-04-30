---
title: Metrics
description: A metric measures and evaluates the effectiveness of IT service management processes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure core features, Administer the ServiceNow AI Platform]
---

# Metrics

A metric measures and evaluates the effectiveness of IT service management processes.

For example, a metric could measure the effectiveness of the incident resolution process by calculating how long it takes to resolve an incident.

A metric can often be easily obtained from the data. To find the number of incidents created today, a report counts the number of incidents in the incident table with a Created date of today. However, metrics must be gathered as data is updated. For example, determining how long an incident was assigned to a certain group requires collecting information about assignment changes and calculating the duration of each assignment.

The Metric plugin provides an easy, declarative way of defining metrics. Once defined, the data for the metric is gathered, and instances of the metric are calculated and stored. For example, the "Assigned to Duration" metric measures the amount of time an incident is assigned to an individual. To define this metric, you create a metric definition of the type "Field value duration" and select the "Assigned to" field from the Incident table. A metric instance is created for each incident assignment showing its duration. Reporting on the duration of incident assignments becomes easy.

You can report on a metric by using a [Working with database views for reporting](c_DatabaseViews.md) that links the metric to the table on which it is defined.

To install the Metric Definition plugin \(com.glide.metrics\), navigate to **System Definition** &gt; **Plugins**, search for Metric Definition, and click **Install**.

