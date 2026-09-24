---
title: Bucket groups and calculated fields in Data Snapshots
description: Bucket groups let you use numeric data as breakdowns. Calculated fields show numeric data derived from date fields. Map bucket groups to either numeric or calculated fields on Data snapshots indicator sources to use those fields as breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/ds-bucket-groups-calculated-fields.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [indicator, breakdown, data snapshots, KPI, performance analytics]
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Bucket groups and calculated fields in Data Snapshots

Bucket groups let you use numeric data as breakdowns. Calculated fields show numeric data derived from date fields. Map bucket groups to either numeric or calculated fields on Data snapshots indicator sources to use those fields as breakdowns.

To filter indicator scores by the values of a field, the field must have a discrete set of possible values. Numeric data is continuous, so numeric fields on their own cannot be used to filter indicators. However, if you can split numeric field values into buckets, you can use the buckets to filter indicators. Do so in two steps:

1.  Define a group of buckets to split the expected range of the numeric field values into meaningful sets. These [bucket groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) are a classic Performance Analytics feature.
2.  Map the numeric field to the bucket group.

Calculated fields are a special type of numeric field. They show the difference between two date/time fields on a Data snapshots source table. For example, a calculated field on the Created and Updated fields shows the time difference between when a record was created and the last update made to it. To use a calculated field as a filter, first find or create a group of buckets that divide the range of values of that field into sets. Then map the field to that bucket group.

Calculated fields are active on all instances. You don't have to activate anything to use them.

## Limitations

-   Calculated fields support only date/time fields.
-   Calculated fields do not support score\_start or score\_end.
-   You can visualize calculated fields only in KPI Details. You cannot show them on data visualizations and thus not on dashboards.

-   **[Create a calculated field for a Data snapshots source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-a-calculated-field.md)**  
Show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.
-   **[Map a bucket group to a Data snapshots source field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/map-bucket-group-to-ds-source.md)**  
To be able to filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

**Related topics**  


[Bucket groups for breakdown sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_BucketGroups.md)

