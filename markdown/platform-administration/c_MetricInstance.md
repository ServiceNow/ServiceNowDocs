---
title: Metric instance
description: A metric instance is a record in the metric\_instance table. A record holds one instance of a metric.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Metrics, Configure core features, Administer the ServiceNow AI Platform]
---

# Metric instance

A metric instance is a record in the metric\_instance table. A record holds one instance of a metric.

Metric instance records get created and updated in one of two ways:

-   If the metric is a duration, the system automatically populates the metric instance table with duration values.
-   If the metric is calculated from a script, the script itself must populate the metric\_instance table.

Some of the notable fields in the metric\_instance table are:

-   Metric definition: the metric definition for which this metric instance was gathered.
-   Value: For a "Field value duration" metric this is the value of the table field for which duration is calculated. For example, for the "Assigned to Duration" metric, the Value is the name of the person assigned to the incident. For other metrics, the value can be any value calculated by the metric.
-   ID: Identifies the specific record for which the metric is gathered. For example, the specific incident.
-   Duration: Time duration for a Field value duration metric.

