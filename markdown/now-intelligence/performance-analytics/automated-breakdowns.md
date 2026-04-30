---
title: Automated breakdowns
description: An automated breakdown uses a breakdown source to determine selectable elements.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Automated breakdowns

An automated breakdown uses a breakdown source to determine selectable elements.

Automated breakdowns are based on a breakdown source, which is a set of records from a table. The breakdown maps these records, known as breakdown elements, with fields on tables that indicators collect scores from. Scores collected from mapped tables can then be grouped and filtered based on the values in the mapped fields and the breakdown elements.

For example, the Groups breakdown source that includes records from the Groups \[sys\_user\_groups\] table is available by default. This breakdown source specifies the filter **\[Active\]\[is\]\[true\]** to include only active groups as elements. You can map this breakdown source to fields on other tables that reference the Groups table, such as the Incident **Assignment group** field. Scores collected from the mapped table are grouped based on the value of that field. You can then filter the scores on the Analytics Hub and dashboards by selecting the breakdown and an element, such as to show scores only for incidents assigned to the Hardware group.

1.  [Create an automated breakdown](../task/t_CreatingABreakdownForIndicators.md)  
To create an automated breakdown, select a breakdown source for it to use and apply access restrictions. Then map which field on the indicator source references the breakdown source. Finally, assign indicators to the breakdown.
2.  [Create a breakdown mapping on a breakdown record](../task/t_CrtBkdnBreakdownMpngs.md)  
Specify which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to query the indicator source.
3.  [Assign an indicator to an automated breakdown](../task/t_AssigningAnIndicatorToABreakdown.md)  
Associate automated or formula indicators with a breakdown to enable the collection of broken down scores for those indicators.

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

