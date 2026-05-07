---
title: Bucket groups for breakdown sources
description: Bucket groups are used to recategorize data so it can be used as a breakdown, for example by grouping a range of values into discrete buckets.You can use a bucket group with a breakdown mapping that does not use a script, to group the values of any mapped field to buckets.When you have a breakdown mapping script that collects a range of values, you can define a bucket group to divide those values into discrete buckets.Specify a group of buckets into which you want to recategorize data.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Breakdown sources, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Bucket groups for breakdown sources

Bucket groups are used to recategorize data so it can be used as a breakdown, for example by grouping a range of values into discrete buckets.

In the data architecture, bucket groups are defined in Bucket Group \[pa\_bucket\_groups\] records and buckets in Bucket \[pa\_buckets\] records. Each Bucket \[pa\_buckets\] record contains a Bucket Group field that is a reference to a Bucket Group \[pa\_bucket\_groups\] record.

To work with a bucket group, create a breakdown source that uses Bucket \[pa\_buckets\] as the facts table and specifies the bucket group in a condition. If a breakdown built on this source uses a breakdown mapping with a script, the breakdown groups the values that the script returns into buckets. If the breakdown mapping specifies a field instead of using a script, the breakdown groups the values of the mapped field into buckets.

**Parent Topic:**[Breakdown sources](breakdown-sources.md)

**Related topics**  


[Create a breakdown mapping on a breakdown record](../task/t_CrtBkdnBreakdownMpngs.md)

## Grouping field values into buckets

You can use a bucket group with a breakdown mapping that does not use a script, to group the values of any mapped field to buckets.

The use case can be as simple as translating the `true` and `false` values of a boolean into two buckets with meaningful labels.

### Sorting boolean values into buckets

A base Performance Analytics installation includes the Active breakdown as part of the Analytics Usage Overview. This breakdown uses a mapping to the job.active boolean field from the Job Log \[pa\_jobs\_logs\] table. The breakdown source uses a bucket group where `true` values for job.active are sorted into the Active bucket, while `false` values are sorted into the Inactive bucket. Note that `false` values are numerically considered to be a value less than one, while `true` values are numerically one and above.

![Bucket group form showing the Inactive and Active buckets and their ranges](../image/bucket-group-scriptless.png)

## Grouping script results into buckets

When you have a breakdown mapping script that collects a range of values, you can define a bucket group to divide those values into discrete buckets.

After you create the bucket group, you create a breakdown source based on the bucket group. Then you create a breakdown that uses that breakdown source. When you create the breakdown mapping for the breakdown, define or select a script for the mapping. The breakdown groups the results that the script returns into the buckets of the bucket group. For an example, see [Example: Script mapping](example-script-mapping.md).

You can write a bucket group for an existing script, or you can first write the bucket group and then write the script. Both must exist before you can create the breakdown.

**Note:** The same script can be used with any number of bucket groups. Also, in principle any scripts that returned the same kind of data could be used with the same bucket group.

## Create a bucket group

Specify a group of buckets into which you want to recategorize data.

### Before you begin

Role required: pa\_data\_collector or higher

### Procedure

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Bucket Groups**.

2.  Select **New**.

3.  Enter a **Name** that clearly identifies the bucket group, like `Age Ranges in Days`.

4.  Double-tap **Insert a new row** to create a bucket.

5.  Enter a **Name** for the first bucket, then press Enter or tap the green check icon.

6.  Double-tap in the **Start** and **End** columns to enter the starting and ending values for the range.

    Records that match the end value are excluded from the bucket. Therefore, set the end value of one bucket and the start value of the next bucket to be the same. Records that exactly match that value are sorted into the bucket that has that value as the start value.

    **Warning:** If the end value of one bucket does not match the start value of the next bucket, you have a 'hole' where records are not sorted into any bucket. For example, if you have a bucket that ends at 20 and the next bucket starts at 21, records for which the script returns a value between 20.0000~ and 20.9999~ do not get sorted into any buckets.

7.  Press **Submit** after all the bucket ranges have been defined.


### Incident Age Ranges bucket group

Consider the case where you want to group incidents by age, as follows:

-   Less than a day
-   1–5 days
-   6–30 days
-   31–90 days
-   More than 90 days

In **Performance Analytics** &gt; **Scripts**, you already have a script named Incident.Age.Days. This script derives the age in days of an incident from its opening date and the latest date on which a score was collected:

```
var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
var days=function(x,y){return diff(x,y)/(24*60*60*1000);};
days(current.opened_at, score_end);
```

You create a bucket group named Incident Age Ranges \(Days\). In this bucket group, you define a set of buckets that start at the desired date and end at the beginning of the next bucket. For example, the 06–30 Days bucket starts at 6 and ends at 31:

![The 06–30 day bucket](../image/bucket.png)

This bucket will contain incidents from the age of precisely 6 days to the age of 30 days, 23 hours, 59 minutes, and 59 seconds.

At the end, you have a bucket group with five buckets corresponding to the age ranges in which you want to divide incidents.

![Bucket groups](../image/BucketGroups.png)

**Note:** The Script Mapping example shows a breakdown that uses this bucket group and script.

### What to do next

Create a breakdown source that uses the Bucket \[pa\_buckets\] facts table, the Sys ID field, and the condition \[Bucket group\]\[Is\]\[&lt;the name of the bucket group you created&gt;\]. Then create a breakdown that uses this breakdown source and uses the relevant script for the breakdown mapping.

**Related topics**  


[Example: Script mapping](example-script-mapping.md)

[Scripting in Performance Analytics](pa-scripts.md#)

