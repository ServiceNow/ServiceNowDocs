---
title: Example: Script mapping
description: The Age breakdown uses the Incident.Age.Days script to calculate the age of incidents in days and map the values to the Incident Age Ranges bucket group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/example-script-mapping.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a breakdown mapping on a breakdown record, Automated breakdowns, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Example: Script mapping

The Age breakdown uses the Incident.Age.Days script to calculate the age of incidents in days and map the values to the Incident Age Ranges bucket group.

In the first two images, you see the Age breakdown, which uses the Incident.Age.Days breakdown source and the Incident.Age.Days script for breakdown mapping. You also see that the breakdown source refers to the Incident Age Range \(Days\) bucket group.

\[Omitted image "age-breakdown.png"\] Alt text: The age breakdown with Incident.Age.Days source and mapping highlighted.

\[Omitted image "incident-age-days-bkdown-source.png"\] Alt text: The Incident.Age.Days breakdown source showing the Incident Age Ranges bucket group

The Incident.Age.Days script takes the time stamp when the incident was opened from the incident table and subtracts this from the time stamp at the end of the collection period. The script converts this value from milliseconds to days.

```
var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
var days=function(x,y){return diff(x,y)/(24*60*60*1000);};
days(current.opened_at, score_end);
```

The resulting numbers of days are sorted into the buckets of the bucket group.

\[Omitted image "incident-age-ranges-bucket-group.png"\] Alt text: Incident Age Ranges bucket group buckets

Here is the result of running this script on the Number of open incidents indicator.

\[Omitted image "detailed-scorecard-age-breakdown.png"\] Alt text: Analytics Hub for the Number of open incidents indicator showing the Age breakdown.

**Parent Topic:**[Create a breakdown mapping on a breakdown record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CrtBkdnBreakdownMpngs.md)

**Related topics**  


[Scripting in Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-scripts.md)

