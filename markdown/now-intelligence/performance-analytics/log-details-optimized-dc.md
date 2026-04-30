---
title: Log details for optimized data collector
description: Starting with the Tokyo release, a new, optimized data collector is available. The log details for this data collector differ from the log details of the classic data collector.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Data collection process and logging, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Log details for optimized data collector

Starting with the Tokyo release, a new, optimized data collector is available. The log details for this data collector differ from the log details of the classic data collector.

## Collection overview

The data collection job involves executing an SQL query for each indicator source that uses the data collector. The query repeats for every collection time from the start date to the stop date. Then queries run for the next indicator source. Each step of executing a query is documented in the data collection job log.

![Flow chart showing the relation between the different levels of processes in a data collection job](../image/data-collection-subprocesses.png "High-level view of data collection job")

## Starting and completing collection job

Follow the data collection process as revealed in log messages. The log messages in each subprocess have been separated into their own tables.

**Note:** This log is for the optimized HSQL data collector as described in [Optimizing data collection](../concept/optimized-data-collection.md). If **com.snc.pa.dc.hsql** is "false," you are using the classic data collector. Otherwise, you are using the optimized data collector. For more information about that log, see [Log details for classic data collector](original-data-collection-process.md).

<table id="table_kwh_k4g_qbb"><thead><tr><th>

Collection job step

</th><th>

Example of resulting log entry

</th></tr></thead><tbody><tr><td>

Shows the domain of the collection job Run As user.

</td><td>

User &lt;admin&gt; belongs to domain global

</td></tr><tr><td>

Collection starts. Job start specifies whether scores, text index, or both are being collected. Messages also specify that the optimized HSQL data collector is in use and whether debug logs are enabled. Only Customer Service and Support can enable debug logs.

</td><td>

Starting collection of Both scores and text index. Value of properties in system -Using HSQL data collector: true

 Debug logs enabled: true

 Node Name : vsr007

</td></tr><tr><td>

Shows the domains for which scores are collected. Also shows other relevant details about the domains.

</td><td>

DomainConfig: Testing Domain Config Collection logs - 3d359877b77000106886e664de11a97c, Type: conditions, RollUpType: roll\_up\_children, collectAggregate? Yes, collectChildren?: Yes, AggregateDomain: Name: 3d359877b77000106886e664de11a97c - SysID: d1659c77b77000106886e664de11a91e, Domains: Default,MSP,ACME,Cisco,Initech,Oceanic Airlines

</td></tr><tr><td>

Lists indicator sources that the job collects data for, including their unique IDs.

</td><td>

Indicator Sources to collect: Incidents.New: b54f2c23d7030100b96d45a3ce61032f, Incidents.Open: b5cf2c23d7030100b96d45a3ce6103cc, Incidents.Closed: 2ac8dd31ff2302001e68ffffffffff3d, Incidents.Resolved: 4c207c23d7030100b96d45a3ce610308

</td></tr><tr><td>

Lists each indicator associated with the job and the indicator properties that are related to data collection:-   Are records collected in a [snapshot](../concept/performance-analytics-glossary.md#)?
-   Are any breakdowns excluded?
-   Are the collection periods in the indicator source overridden?
-   Is the breakdown matrix collected?
-   If the breakdown matrix is collected, are any breakdown combinations excluded?

</td><td>

JobIndicator: Number of open incidents - de537dc3d7131100b96d45a3ce610305 Job Indicator Properties: collectIndicator?: Yes, BreakdownCollectionType: WITH\_EXCLUDE Excluded Breakdowns: Assignment Group, State Indicator Properties =&gt; CollectingRecords: Yes, Overridden Collection Periods: No, Scripted?: No, Breakdown Combinations?: Yes, Excluded Breakdown Combinations: No combination is excluded.

</td></tr><tr><td>

Iterate steps for each indicator source

</td><td>

See table [Steps iterated for each indicator source](log-details-optimized-dc.md#section_indicator-source).

</td></tr><tr><td>

Show statistics for the data collection job

</td><td>

Statistics: inserts 184, updates 0, deletes 92, errors 0, warnings 0

</td></tr><tr><td>

Complete job

</td><td>

Collection ended

</td></tr></tbody>
</table>## Steps iterated for each indicator source

|Collection job step|Example of resulting log entry|
|-------------------|------------------------------|
|Retrieve indicator source.|Processing indicator source Incidents.Open|
|Repeat that optimized HSQL data collector is in use.| |
|List indicators that have additional conditions, beyond the conditions inherited from the indicator source.|Indicator: Admin Logins - \[sys\_id of indicator\], Additional Conditions: ref\_isc\_login\_event.login\_type=login\_admin, Is Collect Records: true|
|Iterate steps for each collection period.|See table [Steps iterated for each collection period](log-details-optimized-dc.md#section_collection-period)|
|Retrieve next indicator source.|Processing indicator source Incidents.New|

## Steps iterated for each collection period

<table id="table_collection-period"><thead><tr><th>

Collection job step

</th><th>

Example of resulting log entry

</th></tr></thead><tbody><tr><td>

Start date of collection job.

</td><td>

Collecting for 20191103 on Indicator Source Incidents.Open

</td></tr><tr><td>

Fetch the following fields:-   The unique fields of the breakdown sources \(typically sys\_id\)
-   The indicator fields used in breakdown mappings
-   The table fields used in scripted breakdown mappings
-   The indicator source fields used in text analytics, if the text index is collected \(typically includes short\_description\)

</td><td>

Fetching "short\_description,sys\_id, opened\_at, assignment\_group, description, priority, category" from "incident"

</td></tr><tr><td>

Generate SQL based on the conditions that are specified in the indicator source.**Note:** If the indicator source specifies Today in one of the conditions, Today is considered relative to the period for which the data collection job is executed. For example, the Incidents.New indicator source includes the condition **\[Opened\]\[on\]\[Today\]**. With days defined to start at 07:00:00, when data is collected for 2019-10-28, the job produces the SQL script on the right.

</td><td>

SELECT task0.\`sys\_id\` FROM task task0 WHERE task0.\`sys\_class\_name\` = 'incident' AND \(task0.\`opened\_at\` &gt;= '2019-10-28 07:00:00' AND task0.\`opened\_at\` &lt;= '2019-10-29 06:59:59'\)

</td></tr><tr><td>

Display the number of records fetched by the SQL.

</td><td>

Fetched 150 rows from Indicator Source Incidents.Open \(facts table: incident\)

</td></tr><tr><td>

Delete previous results.

</td><td>

Deleted previous results 1 for Indicator: Impersonations

</td></tr><tr><td>

Run the map/reduce function to calculate indicator scores.

</td><td>

See the table [Steps of the map/reduce function](log-details-optimized-dc.md#section_map-reduce)

</td></tr><tr><td rowspan="2">

If text indexing is active and has been configured for the indicator source, the data collector stores the resulting text index.

</td><td>

Storing Text Index for indicator source Incidents.Open

</td></tr><tr><td>

Bytes used by text index: 41,984 for: Incidents.Open

</td></tr><tr><td>

Objects are offloaded to the HSQL database whenever one of the following thresholds is exceeded:-   Number of scores
-   Number of snapshots
-   Total number of Count Distinct values

 Log number of times the offload limit was exceeded for each category of object. Each time the offload limit is exceeded in one category, all objects are moved to HSQL temporary database storage. At the end of the map/reduce function, any remaining records are offloaded. The number of remaining records is usually less than the threshold, and this offloading is also logged.

</td><td>

Number of times offload limit crossed threshold for scores: 275Number of times offload limit crossed threshold for snapshots: 0

 Number of times offload limit crossed threshold for distinct values: 0

 Offload batch of records which didn't cross threshold: 1

</td></tr><tr><td>

Begin storing newly collected results for the indicator source.

</td><td>

Storing collected results for indicator source Incidents.Resolved

</td></tr><tr><td>

Any indicator with a null value is logged.

</td><td>

Stored 'Value when nil': 0.0 as score for indicator: Number of incidents deflected by knowledge

</td></tr><tr><td>

Finish storing results.

</td><td>

Stored collected results

</td></tr><tr><td>

Specify which indicators the data collector does not collect scores for.

</td><td>

Not collecting for Indicator: Summed age of open incidents with excluded Breakdown: Assignment Group

</td></tr><tr><td>

Finish collecting data for that indicator source for that period.

</td><td>

Collection for 20200519 on Indicator Source Incidents.Open finished

</td></tr><tr><td>

Display the average amount of time spent on a record to process additional conditions that were set on indicators.

</td><td>

Average time taken to process additional indicator condition for each record: 138 ms

</td></tr></tbody>
</table>## Steps of the map/reduce function

<table id="table_map-reduce"><thead><tr><th>

Collection job step

</th><th>

Example of resulting log entry

</th></tr></thead><tbody><tr><td>

The map/reduce function runs.

</td><td>

Applying map/reduce function for indicator source Incidents.Open

</td></tr><tr><td>

Warning if text indexing is active for the job but cannot run because of a missing or invalid text index configuration.

</td><td>

Skipping text index collection as there is missing or invalid text index configuration

</td></tr><tr><td rowspan="7">

Process each record on the indicator source to calculate scores. Log messages track running total of processed records. Each time the number of resulting scores or snapshots exceeds a limit, all objects are offloaded to the HSQL database. The offloading is logged after the map/reduce function completes.

 Processing for each record involves:

 -   Execute or evaluate any scripts.
-   Validate indicator conditions.
-   Calculate the indicator score.
-   For each breakdown:
    1.  Calculate the breakdown score or execute the breakdown script.
    2.  Retrieve all breakdown unique values.
    3.  Create or update the array for scores or snapshots. The array is: `Indicator, Breakdown 1, Artifact 1, Breakdown 2, Artifact 2, Domain, Value, Array of [sys_id]`

</td><td>

Processed 15.8% \(3\) records

</td></tr><tr><td>

Processed 31.6% \(6\) records

</td></tr><tr><td>

Processed 47.4% \(9\) records

</td></tr><tr><td>

Processed 63.2% \(12\) records

</td></tr><tr><td>

Processed 78.9% \(15\) records

</td></tr><tr><td>

Processed 94.7% \(18\) records

</td></tr><tr><td>

Processed 100% \(4\) records, Result Object size: 20 MB

</td></tr><tr><td>

The map/reduce function completes.

</td><td>

Applied map/reduce function

</td></tr></tbody>
</table>**Parent Topic:**[Data collection process and logging](../concept/data-collection-process-logging.md)

**Related topics**  


[Optimizing data collection](../concept/optimized-data-collection.md)

[View the data collection job logs](../task/t_ViewingADataCollectionJobLog.md)

