---
title: Map a bucket group to a Data snapshots source field
description: To be able to filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/map-bucket-group-to-ds-source.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [bucket group, data snapshots, performance analytics]
breadcrumb: [Bucket group mappings and calculated fields, Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Map a bucket group to a Data snapshots source field

To be able to filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.

## Before you begin

Role required: pa\_power\_user or higher

## About this task

There are two types of fields that you can map a bucket group to:

-   A normal numeric table field
-   A [calculated field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) that you created on two date/time fields. You have to map a bucket group to a calculated field to use that field as an indicator filter in KPI Details. For more information, see [Create a calculated field for a Data snapshots source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-a-calculated-field.md).

**Note:** You can also map a bucket group to a Choice field. Doing so replaces the Choices in the field with the values in the Bucket group.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Breakdowns** &gt; **Bucket Group Mappings** and select **New**.

2.  Fill in the fields as follows:

    |Field|Contents|
    |-----|--------|
    |Indicator|The name of the Data snapshots indicator that you want to use a bucket group for|
    |Field type|Select from Calculated fields or Table fields|
    |Field/Calculated field|Name of the field that you are mapping the bucket group to|
    |Bucket group|Name of the bucket group that you are mapping to the field. If none of the existing bucket groups meet your needs, create one as described in [Create a bucket group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_BucketGroups.md).|

3.  Select **Update**.


## Mapping a bucket group to a table field

You want to filter the count of resolved incidents by the length of time it took to resolve them. You have created a Data snapshots source named incident\_dataset, which you use for Data snapshots indicators on the Incident \[incident\] table. You have also created an indicator named Resolved incidents, which is a record count on the Incident table of incidents where the Resolve time &gt; 0. The Resolve time field contains the time taken to resolve each incident, which is the data that you want to filter indicator scores by.

However, Resolve time is a numerical field of time in seconds. The range of values of this field on your instance is from 0 to something over 9 million. Technically, you are not allowed to use a numerical field to filter indicator scores, and practically, you would not want to. Instead, you have to split these values into discreet buckets.

You look through the existing bucket groups but cannot find one that is suitable. So you calculate the number of seconds in a day, and you create a bucket group called Resolution time based on days:

-   Unresolved: 0-1 second
-   &lt; 1 day: 1-86,400 seconds
-   1-5 days: 86,400-432,000 seconds
-   5-30 days: 432,000-2,592,000 seconds
-   30-90 days: 2,592,000-7,776,000 seconds
-   &gt; 90 days: 7,776,000 seconds +

\[Omitted image "resolution-time-bucket-group.png"\] Alt text: Resolution time bucket group.

Now, you create a bucket group mapping of the Resolution time bucket group to the Incident.Resolve time field.

|Record field|Value|
|------------|-----|
|Indicator|Resolved incidents|
|Field type|Table fields|
|Field|Resolve time|
|Bucket group|Resolution time|

On KPI Details, you open the Resolved incidents indicator. In the filter panel, you expand Resolve time and see the Resolution time buckets. You select the buckets that interest you and also select **Display as separate time series**.

\[Omitted image "resolved-incidents-kpid.png"\] Alt text: KPI Details showing resolution times of incidents split into buckets.

You have a separate time series of counts for resolved incidents in each resolution time bucket.

## Mapping a bucket group to a calculated field

You would like to examine how old incidents were when they resolved. There is no field on Incident \[incident\] that tallies incident age. Therefore, you create a calculated field on the Incident table that shows the difference between the Created and Updated time stamps. The last time the incident was updated serves as a proxy for when the incident was resolved. \(For more information, see [Create a calculated field for a Data snapshots source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-a-calculated-field.md).\)

\[Omitted image "calculated-field-form.png"\] Alt text: Completed form for incident age calculated field.

The Age calculated field appears under Eligible calculated fields on the Data snapshots source for the Incident table. It is eligible because both fields in the formula are listed as fields that can be used as filters.

\[Omitted image "eligible-calculated-field.png"\] Alt text: The Age calculated field shown in the Eligible Calculated fields related list of the incident\_dataset data snapshots source record.

However, you still can't use the Age field to filter indicator scores in KPI Details. It is a numeric field. To use the Age field, you have to map a bucket group to the field. Fortunately, there is a suitable bucket group called Incident Age Range that is provided in the base system. You map this bucket group to the Age field on the Resolved Incidents indicator.

|Record field|Value|
|------------|-----|
|Indicator|Resolved incidents|
|Field type|Calculated fields|
|Calculated Field|Age|
|Bucket group|Incident Age Range|

On KPI Details, you open the Resolved incidents indicator. You look for Age under the filters but don't find it. Therefore, you select **Configure** on the Filters panel and select the Age filter.

\[Omitted image "configure-kpid-filters.png"\] Alt text: Opening the Configure panel for filters on KPI Details. \[Omitted image "select-age-filter.png"\] Alt text: Selecting the Age filter on KPI Details.

Now you can filter scores by Age. You choose every age bucket and **Display as separate time series**, to get a separate line for each bucket.

\[Omitted image "resolved-incidents-age-kpid.png"\] Alt text: KPI Details showing age of resolved incidents split into buckets.

**Parent Topic:**[Bucket groups and calculated fields in Data Snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/ds-bucket-groups-calculated-fields.md)

