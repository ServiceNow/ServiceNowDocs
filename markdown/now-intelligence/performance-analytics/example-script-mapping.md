---
title: Example: Script mapping
description: The Age breakdown uses the Incident.Age.Days script to calculate the age of incidents in days and map the values to the Incident Age Ranges bucket group.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a breakdown mapping on a breakdown record, Automated breakdowns, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Example: Script mapping

The Age breakdown uses the Incident.Age.Days script to calculate the age of incidents in days and map the values to the Incident Age Ranges bucket group.

In the first two images, you see the Age breakdown, which uses the Incident.Age.Days breakdown source and the Incident.Age.Days script for breakdown mapping. You also see that the breakdown source refers to the Incident Age Range \(Days\) bucket group.

![The age breakdown with Incident.Age.Days source and mapping highlighted.](../image/age-breakdown.png)

![The Incident.Age.Days breakdown source showing the Incident Age Ranges bucket group](../image/incident-age-days-bkdown-source.png)

The Incident.Age.Days script takes the time stamp when the incident was opened from the incident table and subtracts this from the time stamp at the end of the collection period. The script converts this value from milliseconds to days.

```
var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
var days=function(x,y){return diff(x,y)/(24*60*60*1000);};
days(current.opened_at, score_end);
```

The resulting numbers of days are sorted into the buckets of the bucket group.

![Incident Age Ranges bucket group buckets](../image/incident-age-ranges-bucket-group.png)

Here is the result of running this script on the Number of open incidents indicator.

![Analytics Hub for the Number of open incidents indicator showing the Age breakdown.](../image/detailed-scorecard-age-breakdown.png)

**Parent Topic:**[Create a breakdown mapping on a breakdown record](../task/t_CrtBkdnBreakdownMpngs.md)

**Related topics**  


[Scripting in Performance Analytics](pa-scripts.md#)

