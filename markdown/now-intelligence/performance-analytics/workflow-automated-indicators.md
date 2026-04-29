---
title: Workflow for creating indicators
description: Start with ServiceNow AI Platform tables and work your way up to a completed indicator with score collection that you can share on a dashboard.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Workflow for creating indicators

Start with ServiceNow AI Platform tables and work your way up to a completed indicator with score collection that you can share on a dashboard.

## Before you begin

Design your KPIs before trying to create them. Using KPI Composer, start by deciding on the business goals you want to achieve with Performance Analytics. For each business goal, determine the critical success factors for that goal. Finally, decide what measurements you need to make to see your progress on those critical success factors. These measurements correspond to the KPIs you need to implement. For more information about designing your Performance Analytics Solution, see [Design your Performance Analytics solution with KPI Composer](../concept/designing-pa-solution.md).

Role required: none

## About this task

When you know what KPIs you need, you can begin to create indicators and breakdowns and, if necessary, their data sources. The following workflow applies to automated indicators, which are the implementation of KPIs that collect scores from ServiceNow AI Platform database tables. \(Remember that you can combine and apply operations to automated indicators in formula indicators. You can also have manual indicators and external indicators, which do not refer to the ServiceNow AI Platform database at all.\)

**Important:** Performance Analytics should be implemented by qualified personnel. Several training courses are available, as described in this [ServiceNow Community article](https://community.servicenow.com/community?id=community_article&sys_id=44c3a3ecdbf43f84d82ffb24399619c2). This documentation is not meant to substitute for training.

Whereas designing KPIs for Performance Analytics is a top-down process, the technical implementation of indicators is a bottom-up process:

## Procedure

1.  Identify the table with the data you want to analyze.

    Minimum Role: pa\_data\_collector.

    What tables do your KPIs refer to? For example, if your KPI is about incidents, the information is in Incident \[incident\]. If the KPI is about change requests, the table is Change Request \[change\_request\]. If you use KPI Composer to design your KPIs, you already have this information.

2.  Determine the subsets of records that are relevant to your KPIs.

    Minimum Role: pa\_data\_collector.

    Almost certainly you do not have a KPI that refers to all the records of a table. Instead you have KPIs that refer to subsets of the records, such as Number of Open Incidents, Open Incidents That Have Been Reassigned at Least Once, or Incidents That Were Resolved on the Day They Were Opened. For each table, note the conditions that you can use to define relevant subsets of records, such as ‘open,’ ‘reassigned at least once,’ ‘resolved,’ ‘status &gt; resolved on the day it was opened'.

    Again, if you use KPI Composer to design your KPIs, you already have this information.

3.  Decide which indicator sources you need, based on the conditions that define the subsets of records that are relevant to your KPIs.

    Minimum Role: pa\_data\_collector.

    An indicator source is a data source that refers to a ServiceNow table and one or more conditions that filter the records on that table. You want as few indicator sources as possible. The main reason for this parsimony is efficiency. Data collection involves querying the database for sets of indicators that share an indicator source, not for each indicator. Minimizing the number of indicator sources also helps maintain a single source of truth across indicators. If you need to change a condition, you can change it on the indicator source and propagate this change automatically to all associated indicators.

    Look for common conditions that you can apply to multiple indicators when you are designing indicator sources. Consider the following KPIs:

    -   Number of incidents that are open.

    -   Number of open incidents that have been reassigned at least once.

    -   Incidents that have been open for more than 30 days.

    -   Incidents that are marked ‘resolved’.

    -   Incidents that were resolved the day they were opened.

    You could create two indicator sources that would get scores collected for all these KPIs:

    -   One on the Incidents table, filtering for incidents that are open.

    -   Another one on the Incidents table, filtering for incidents that have been resolved.

4.  Search for existing indicators and indicator sources that match your needs.

    Minimum Role: pa\_data\_collector, pa\_power\_user \(indicators only\).

    Redundant indicators and indicator sources are a common problem. Only when you have verified that no suitable indicators or indicator sources exist, create the indicators and indicator sources.

    If you can find indicator sources that meet your needs, see if there are already indicators on those sources that match your designed KPIs.

    **Note:** KPI Composer incorporates a search for suitable existing Performance Analytics indicators into the design process.

5.  Create any missing indicator sources that you need.

    Minimum role: pa\_data\_collector.

6.  Create any missing automated indicators that match the KPIs you need.

    Minimum role: pa\_power\_user.

    After you have the indicator sources, someone with the pa\_power\_user role, such as a business analyst, can create automated indicators.

    When you create the indicators, add any additional conditions. These conditions apply only to one or two indicators and are not efficient to apply at the level of the indicator source. If you have efficiently divided your conditions between indicator sources and indicators, some indicators on an indicator source will have no additional conditions. These indicators are simply aggregations on a column in the indicator source.

7.  Associate and map any relevant breakdowns with the new indicators.

    Minimum role: pa\_power\_user.

    When you designed your indicators, you also should have designed any breakdowns to apply to the indicators. Breakdown design is included in KPI Composer. You may need to create new breakdowns or breakdown sources, but that is outside the scope of this workflow.

8.  Collect and manage a matrix of breakdowns.

    Minimum role: pa\_power\_user.

    If you want to collect more than one level of breakdown, such as breaking down by both Priority and Category, set up the breakdown matrix. Be sure to exclude unnecessary or nonsensical breakdown combinations.

9.  Edit a job for the indicator.

    Minimum role: pa\_data\_collector.

    Add one scheduled and \(usually\) one unscheduled data collection job to the indicator. Run an unscheduled job to collect historical data for the indicator, if historical data exists. Usually you only run this job when you create an indicator and never again. Activate the scheduled job to collect periodic data moving forward, usually following the frequency of the indicator. Collect only for one period. For example, when you have an indicator with the Daily frequency, set the scheduled job to collect every day for the previous \(last completed\) day.


## Result

At the end of this workflow, you have an automated indicator that is populated with data. This automated indicator corresponds to a measurement, a critical success factor, or a supporting indicator that you designed in KPI Composer.

## What to do next

You can include this indicator in a formula indicator. You can also design widgets to visualize the indicator and create dashboards to share these visualizations with the appropriate stakeholders.

