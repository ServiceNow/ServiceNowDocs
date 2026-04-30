---
title: Automated indicators
description: An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Automated indicators

An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data.

Automated indicators are the most frequently used type of indicator and are perhaps the most fundamental component of Performance Analytics. Use an automated indicator to calculate scores on a set of records from a table that stores information about a business process, such as change requests or HR cases. You have the score calculated automatically in a scheduled [data collection job](performance-analytics-glossary.md#), which follows the same periodicity as the frequency in the indicator source. You also set one or more data collection jobs that you run manually, for example to collect a span of historical data when you first create the indicator.

You can associate the indicator with any number of breakdowns to slice or filter the indicator scores. For example, if you have an indicator for the number of open incidents, you can associate this indicator with the Priority breakdown to see how many Critical priority incidents you have. You can also associate the indicator with the Category breakdown to compare the number of Hardware and Software incidents.

If you have an indicator source to use and want to create a fairly straightforward automated indicator, you can use the wizard. If you need to specify the indicator more fully, use the form that is described in this section. For more information about creating an indicator from a wizard, see [Create an automated indicator with a wizard](../task/t_CrtIndctrIndctrWzrd.md#). Before creating an indicator through either means, plan out your indicator as described in [Planning your indicators](planning-indicators.md). Also see whether an appropriate indicator is already available in one of the baseline Performance Analytics Solution content packs.

You can use automated indicators as inputs to a formula indicator, for example to calculate the percentage of open incidents that are new incidents.

1.  [Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#)  
To analyze the performance of a business process that is recorded in a ServiceNow table, use an automated indicator. If a suitable indicator is not provided in a Platform Analytics Solution, create a new one.
2.  [Assign and map breakdowns](../task/create-breakdown-mapping.md#)  
Select which breakdowns to assign to an indicator. Map which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to associate the indicator and breakdown sources.
3.  [Add a collection job to an indicator](../task/t_EditAJobForTheIndicator.md)  
To collect scores for an automated indicator, add a collection job to that indicator.
4.  [Performance Analytics snapshots](pa-snapshots.md)  
Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. Snapshots enable users to drill down into the records from a Performance Analytics indicator visualization.

**Parent Topic:**[Performance Analytics indicators](c_Indicators.md)

